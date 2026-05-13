# 🔊 Rock the docs 🤘😎

> Applying music theory and band dynamics to technical writing.
> A ~30-minute conference talk by Marco Spinello.

A talk about what a power trio can teach a docs team.
Built as a [Marp](https://marp.app/) deck rendered from a single Markdown file. 
The thesis fits on a t-shirt: **writers are bandmates, not session musicians.**
Everything else is just music theory in the right key.

## What the talk covers

*Rock the docs* walks through the anatomy of a working band — the rhythm section, the voice, the producer's chair, the rig — and maps each role onto a part of a technical writer's job.
Stories from the speaker's own instrumental power trio (including songs from the album *Be-Style*) anchor the metaphor; tactical takeaways turn it into something you can act on right away.

The four sections:

- **Foundation** — the rhythm section.
  Style guides, information architecture, linters: the stuff nobody applauds and everyone needs.
- **Voice** — what the band sounds like.
  Why voice is a band sport, not a writer's solo.
- **Polish** — the producer's chair.
  Mixing, reviewing, and staying in the room until the work is done.
- **Tooling** — the workflow as instrument.
  CI, doc-as-code, and what you automate becomes what you can sound like.

## Repo layout

| Path | What's there |
| --- | --- |
| `source/slides.md` | Single source of the deck — Marp Markdown with speaker notes in HTML comments. |
| `assets/img/` | Slide images (AI-generated, sourced from Pixabay). |
| `assets/themes/` | Marp themes (the MarpX collection by Paulo Cunha). The active theme is `dracula`. |
| `.marprc.yml` | Marp CLI config: active theme, input/output dirs, allowed HTML tags. |
| `output/` | Pre-rendered builds: `slides.html`, `slides.pdf`, `slides.pptx`. |
| `package.json` | npm scripts for build, serve, and lint. |
| `plans/` | Original implementation plan from authoring. |
| `playground/` | Working notes and session recaps from the authoring process. |

## See the slides without building

Pre-rendered builds are committed to `output/`:

- HTML — open `output/slides.html` in a browser
- PDF — open `output/slides.pdf`
- PPTX — open `output/slides.pptx`

## Prerequisites

- **Node.js** 18 or later, with `npm`
- A **Chromium-class browser**
  (Chrome, Edge, Brave, or standalone [Chromium](https://www.chromium.org/)) is required by `marp-cli` for PDF and PPTX export.
  HTML build and live preview work without it.

## Setup

```bash
npm install
```

Installs `@marp-team/marp-cli`, `markdownlint-cli`, the Font Awesome plugin, and a few Marp helpers.

## Build and serve

| Command | What it does |
| --- | --- |
| `npm run marp:serve` | Live preview at `http://localhost:9999`, watches all files for changes. |
| `npm run marp:html` | Build `output/slides.html`. |
| `npm run marp:pdf` | Build `output/slides.pdf` (requires Chromium). |
| `npm run marp:pptx` | Build `output/slides.pptx` (requires Chromium). |

All build commands honor `.marprc.yml` and pass `--allow-local-files` so referenced images embed correctly.

## Linting

| Command | What it does |
| --- | --- |
| `npm run lint` | Run `markdownlint` over repo-root Markdown files. |
| `npm run format` | Run `markdownlint --fix` to auto-correct fixable issues. |
| `vale source/slides.md` | Prose linting via [Vale](https://vale.sh/). The local Vale config (`.vale.ini`) and styles (`vale-styles/`) are gitignored — install Vale separately and run `vale sync` to set up. |

## Author

**Marco Spinello** — Senior technical writer.
Guitar in an instrumental power trio.

- LinkedIn: [in/marco-spinello](https://www.linkedin.com/in/marco-spinello/)
- GitHub: [@marcospinello](https://github.com/marcospinello)
- The band's album: [*Be-Style* on Bandcamp](https://spinello-band.bandcamp.com/album/be-style)

## License

- **Talk content** in this repo (slides, README, plans, recaps) — [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). Use it, share it, adapt it — just give credit.
- **Marp themes** in `assets/themes/` retain their original MIT License (MarpX project by Paulo Cunha; license headers preserved in each `.css` file).
- **AI-generated images** in `assets/img/` are subject to the [Pixabay Content License](https://pixabay.com/service/license-summary/).

See [`LICENSE`](./LICENSE) for the full notices.
