# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository purpose

A single [Marp](https://marp.app/) presentation deck — "Rock the docs 🤘", a talk applying music theory and band dynamics to technical writing. There is no application code; the deliverable is a slide deck rendered from Markdown to HTML/PDF/PPTX.

## Layout

- `source/slides.md` — the only source file for the deck. Marp front matter at the top sets author/title and an inline `style:` block that imports Font Awesome and tweaks colors. HTML comments (`<!-- ... -->`) are speaker notes, not dead content.
- `.marprc.yml` — central Marp CLI config. Sets `inputDir: ./source`, `output: ./output`, `themeSet: ./assets/themes`, the active `theme: socrates`, `template: bespoke`, and an HTML allowlist (`div`, `iframe`, `video`). The npm scripts pass `--config-file .marprc.yml`, so flags here apply to every build.
- `assets/img/` — images referenced from slides as `../assets/img/<name>` (paths resolve relative to `source/slides.md`, not the repo root).
- `assets/themes/*.css` — large collection of custom Marp themes (third-party "MarpX" project, MIT). Switch decks by changing `theme:` in `.marprc.yml`; `themeSet` already registers the whole directory.
- `output/` — built artifacts (`slides.html`, `slides.pdf`, `slides.pptx`).
- `.vale.ini` + `vale-styles/` — prose-linting config, both gitignored. `vale-styles/` is populated by `vale sync` per the `Packages = Google, proselint, write-good, MDX` line. Treat as local-only artifacts.
- `playground/`, `plans/`, `.remember/` — local-only scratch (gitignored or used for in-progress notes); not part of the deck.

## Common commands

Builds go through the npm scripts so `.marprc.yml` is always honored:

```bash
npm run marp:serve   # live preview server on PORT=9999, watches all files
npm run marp:html    # build HTML to output/
npm run marp:pdf     # build PDF (uses --allow-local-files for image embedding)
npm run marp:pptx    # build PPTX
npm run lint         # markdownlint *.md
npm run format       # markdownlint --fix *.md
```

`--allow-local-files` is required for PDF/PPTX so the slides can pull in `../assets/img/...`. The npm scripts already pass it; if invoking `marp` directly, add it yourself.

For prose linting (after `vale sync` populates `vale-styles/`):

```bash
vale source/slides.md
```

## Authoring conventions to preserve

- Slides are separated by `---` on its own line. Don't reflow the document — each slide is a discrete unit.
- Background images use Marp's directive syntax inside an image tag, e.g. `![bg right:50%](../assets/img/foo.jpg)` and `![bg contain](../assets/img/bar.png)`. Keep this syntax intact when editing.
- Inline HTML (`<span>`, `<i class="fa-...">` for Font Awesome icons, `<br />`, and `div`/`iframe`/`video` allowed by `.marprc.yml`) is intentional and required for visual effects — don't simplify it to plain Markdown.
- Speaker notes live in `<!-- ... -->` HTML comments under the slide they belong to. Preserve them.
- The active theme is set in `.marprc.yml`, not in the slide front matter. Change it there so all output formats stay consistent.
