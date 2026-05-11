# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository purpose

A single [Marp](https://marp.app/) presentation deck. The talk is "When AI goes off script — Tales from the docs pipelines" (the README still describes an earlier music-theory-themed version of the talk; the actual slide content has moved on). There is no application code here — the deliverable is a slide deck rendered from Markdown.

## Layout

- `source/slides.md` — the only source file for the deck. Marp front matter at the top sets author/title and an inline `style:` block that imports Font Awesome and tweaks colors. HTML comments (`<!-- ... -->`) are speaker notes.
- `assets/img/` — images referenced from slides as `../assets/img/<name>` (paths are resolved relative to `source/slides.md`, not the repo root).
- `assets/themes/*.css` — a large collection of custom Marp themes (from the third-party "MarpX" project, MIT-licensed). Activate one by adding `theme: <name>` to the front matter and registering the CSS via Marp CLI's `--theme` flag.
- `output/` — destination for built artifacts (HTML/PDF/PPTX). Currently empty; nothing is committed here.
- `.vale.ini` + `vale-styles/` — prose-linting config. Both are listed in `.gitignore` and `vale-styles/` is managed by `vale sync` (the `Packages = Google, proselint, write-good, MDX` line tells Vale what to fetch). Treat them as local-only artifacts.

## Common commands

There is no `package.json`, `Makefile`, or build script. Use Marp CLI directly, run from the repo root so the relative `../assets/img/...` references resolve:

```bash
# HTML preview
marp source/slides.md -o output/slides.html --html

# PDF
marp source/slides.md -o output/slides.pdf --pdf --allow-local-files

# Use a custom theme from assets/themes/
marp source/slides.md -o output/slides.html --theme assets/themes/marpx.css

# Live server for editing
marp -s source/
```

`--allow-local-files` is required when exporting PDF/PPTX because slides pull in local images.

For prose linting (after `vale sync` populates `vale-styles/`):

```bash
vale source/slides.md
```

## Authoring conventions to preserve

- Slides are separated by `---` on its own line. Don't reflow the document — each slide is a discrete unit.
- Background images use Marp's directive syntax inside an image tag, e.g. `![bg right:50%](../assets/img/foo.jpg)` and `![bg contain](../assets/img/bar.png)`. Keep this syntax intact when editing.
- Inline HTML (e.g. `<span>`, `<i class="fa-...">` for Font Awesome icons, `<br />`) is intentional and required for the visual effects — don't "clean it up" to plain Markdown.
- Speaker notes live in `<!-- ... -->` HTML comments under the slide they belong to. Preserve them; they're not dead content.
