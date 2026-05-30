# AGENTS.md

This file guides Codex when working in this repository.

## Web search

Do not use the built-in WebSearch tool. It does not work at Booking.com.
Use the websearch MCP tools (`mcp__websearch__*`) for web searches instead.

## Repository purpose

A single [Marp](https://marp.app/) presentation deck: "Rock the docs 🤘".
The talk applies music theory and band dynamics to technical writing. There is
no application code; the deliverable is a slide deck rendered from Markdown to
HTML, PDF, and PPTX.

## Layout

- `source/slides.md` is the only source file for the deck. Marp front matter at
  the top sets author/title and an inline `style:` block that imports Font
  Awesome and defines helper classes. HTML comments are speaker notes, not dead
  content.
- `.marprc.yml` is the central Marp CLI config. It sets `inputDir: ./source`,
  `output: ./output`, `themeSet: ./assets/themes`, the active `theme: dracula`,
  `template: bespoke`, `allowLocalFiles: true`, and the HTML allowlist.
- `assets/img/` contains images referenced from slides as
  `../assets/img/<name>`. Paths resolve relative to `source/slides.md`.
- `assets/themes/*.css` is the MarpX theme collection. Switch the active theme
  in `.marprc.yml`, not in slide front matter, so all export formats stay aligned.
- `output/` contains built artifacts (`slides.html`, `slides.pdf`,
  `slides.pptx`). Prefer rebuilding them instead of hand-editing them.
- `.vale.ini` and `vale-styles/` configure prose linting. If `vale-styles/` is
  absent, run `vale sync` before using Vale.
- `playground/`, `plans/`, and `.remember/` are local working notes and memory.
  Do not treat them as deck source.

## Common commands

Builds go through npm scripts so `.marprc.yml` is honored:

```bash
npm run marp:serve   # live preview server on PORT=9999, watches all files
npm run marp:html    # build HTML to output/
npm run marp:pdf     # build PDF with local image embedding
npm run marp:pptx    # build PPTX with local image embedding
npm run lint         # markdownlint *.md
npm run format       # markdownlint --fix *.md
npx markdownlint source/slides.md  # lint the slide source
```

For prose linting:

```bash
vale sync            # first run only, if vale-styles/ is missing
vale source/slides.md
```

## Skill and workflow routing

- For substantial deck structure, timing, presenter-flow, or Marp export work,
  use a Marp/presentation skill when one is available (`marp-authoring`,
  `marp-slides`, `create-marp-deck`, or `presentations`). Keep the result as
  Marp Markdown unless the user explicitly asks for a different artifact.
- For copy, clarity, voice, or speaker-note review, use docs/prose skills when
  available (`docs`, `review-style`, `assess-docs`, or Vale tools). This talk has
  a deliberate voice; do not sand off the music metaphor or memoir tone.
- For visual layout, screenshots, export debugging, or checking that images
  render, use browser automation such as Playwright. Validate the rendered deck
  after changes to background directives, themes, images, inline HTML, or CSS.
- For repo-instruction maintenance, use instruction/automation skills when
  available (`claude-md-improver`, `claude-automation-recommender`, or similar)
  and keep recommendations specific to this Marp deck.
- For dependency or tool syntax questions, prefer current docs through
  MCP-backed tools such as context/documentation lookup or the approved
  websearch MCP tools.

## Editing workflows

- Small copy edit: modify `source/slides.md`, preserve slide separators and
  speaker notes, then run `npx markdownlint source/slides.md`. Run Vale when the
  edit affects prose quality rather than only mechanics.
- Structural deck edit: inspect the slide map first with
  `rg --color never -n "^---$|^#{1,3} " source/slides.md`, edit one slide unit
  at a time, then run `npm run marp:html`.
- Visual/theme/asset edit: keep image paths relative to `source/slides.md`, keep
  Marp background directives intact, run `npm run marp:html`, and inspect the
  rendered deck or screenshots.
- Export edit: use `npm run marp:pdf` or `npm run marp:pptx`. These require a
  Chromium-class browser; the scripts already enable local file access.
- Instruction-file edit: keep `AGENTS.md` and `CLAUDE.md` aligned except where
  the agent-specific tool names differ.

## Authoring conventions to preserve

- Slides are separated by `---` on its own line. Do not reflow the whole file;
  each slide is a discrete unit.
- Background images use Marp directive syntax inside an image tag, for example
  `![bg right:50%](../assets/img/foo.jpg)` and
  `![bg contain](../assets/img/bar.png)`.
- Inline HTML (`<span>`, `<i class="fa-...">`, `<br />`, and configured
  `div`/`iframe`/`video` usage) is intentional and required for visual effects.
- Speaker notes live in `<!-- ... -->` comments under the slide they belong to.
  Preserve them.
- Keep the active theme in `.marprc.yml`. Do not add a `theme:` override to
  `source/slides.md`.

## Automation ideas to suggest

- Post-edit hook for root Markdown files: run `npm run lint`.
- Post-edit hook for `source/slides.md`, `.marprc.yml`, `assets/img/**`, and
  `assets/themes/**`: run `npm run marp:html` to catch Marp or asset failures.
- Pre-edit guard for `output/**`: ask whether the user wants a rebuild instead
  of manual changes to generated artifacts.
- Optional deck-review subagent: check narrative flow, slide count, timing,
  speaker-note usefulness, and whether the voice still sounds like the talk.
- Optional visual-review subagent: render the deck and inspect screenshots for
  clipped text, broken backgrounds, unreadable contrast, and theme regressions.
