# Rock the docs — work recap (session 3, full day)

Resumes from `/playground/work-recap-so-far.md` (session 1) and `/playground/work-recap-2.md` (session 2). Read both first for the full chain of brainstorming reasoning. **This file supersedes the earlier morning-only version of `work-recap-3.md` (committed in `9d16f90`); the old version remains in git history.**

This is the comprehensive session-3 recap covering both morning (brainstorming → v0.1 implementation) and afternoon (memoir fills → v0.2 → image plan approved).

## Status (right now)

- **Latest git commit:** `8313689 Slide deck v.0.2`
- **Working tree:** clean
- **Deck:** complete first draft. **Both memoir placeholders filled.** No text placeholders remain. 32 content slides total.
- **Build:** clean. `npm run marp:html` passes; `npm run lint` only flags pre-existing line-length issues in `CLAUDE.md` and `README.md` (not slides).
- **Images:** `assets/img/` is still empty. Image plan was reviewed and approved before pause but **directives have NOT been added to `slides.md` yet** — that's the next implementation step on resume.
- **Pause reason:** speaker out for ~2 hours; we resume from this exact state.

## What was locked across all three sessions

Carrying forward all decisions from sessions 1 and 2, plus the new ones from session 3.

### Talk parameters (all locked, not to be re-asked)
- **Title:** "Rock the docs 🤘 / Applying music theory and band dynamics to technical writing"
- **Length:** ~30 minutes (changed in session 3 from the original 40–45 min)
- **Audience:** Mostly fellow tech writers
- **Lens:** Band dynamics as the dominant metaphor
- **Thesis:** *Writers are bandmates, not session musicians.*
- **Personal context:** Speaker plays guitar in an instrumental power trio; co-mixed and co-mastered the band's record with a friend who is the recording engineer.

### Narrative spine — Spine A (anatomy of a band, role-driven)
- 4 roles: **Foundation → Voice → Polish → Tooling**
- Per-section structural beats: role → real-band case → what session-musician thinking gets wrong → Monday-morning move

### Section budget — Option C (unequal weights)
- Foundation: ~5–6 min (lean 3-beat, drop contrarian)
- Voice: ~6 min (full 4-beat)
- Polish: ~9 min (memoir breathes — now 9 slides after session-3 expansion)
- Tooling: ~5–6 min (lean 3-beat, drop contrarian)

### Texture rotation — Option A
- Foundation = case-study
- Voice = contrarian
- Polish = memoir
- Tooling = tactic (now powered by mini-memoir + workflow story)

### Per-section case anchors
- **Foundation:** Tower of Power's rhythm section (interlocking precision = IA-as-system)
- **Voice:** Cream (three virtuosos trading voice — voice as band property, not singer's job)
- **Polish:** Speaker's own story — recording the album with the engineer-friend, *Okefenokee* break + solo
- **Tooling:** Mini-memoir of the band's recording workflow (live tracking with click, reversibility, rough mixes as we tracked, two raw mixes → review comments → final, "like a git PR review")

### Cold open + closer
- **Cold open:** disco-band-shrinking-to-trio reorg (3 slides ladder: 8-piece → trio → "same shape as your last reorg" → thesis reveal)
- **Closer:** callback to disco-to-trio cold open, then manifesto, then thank-you

### Manifesto — Variant A (imperative, measured), 5 lines
```
Lock the foundation, then play.
Find the voice with the band, not for it.
Stay for the mix.
Choose your workflow like an instrument.
Be a bandmate, not a session musician.
```

### Theme
`socrates` → **`dracula`** (locked in session 3, set in `.marprc.yml`)

## What was implemented this session

### Morning — brainstorm to v0.1 (committed)
Commits: `1ef75e6` (gitignore fix), `750046b` (slide deck v0.1), `9d16f90` (initial work recap).

- **`.gitignore`** — fixed a real bug. The session-2 attempt at `!playground/foo.md` exceptions was non-functional because git can't re-include files inside an excluded parent dir. Changed `playground/` → `playground/*` so exceptions actually work. The recap files are now genuinely tracked.
- **`.marprc.yml`** — `theme: socrates` → `theme: dracula`.
- **`source/slides.md`** — full v0.1 rewrite. 30 slides, all with speaker notes. Front matter retains FA import + helper CSS classes (`.big`, `.huge`, `.quiet`, `.accent`, `.manifesto p`). Original talk-announcement copy preserved as a phrase-bank comment at the bottom.
- **`plans/your-recommendation-option-c-fluttering-teacup.md`** — full plan written during plan mode and approved. Captures locked decisions, slide-by-slide outline, file-changes list, verification steps. *(Auto-generated whimsical filename — cosmetic only; consider renaming on a future commit.)*
- **`output/slides.html`** — rebuilt on dracula.

### Afternoon — memoir fills to v0.2 (committed)
Commit: `8313689` (slide deck v0.2).

Two memoir placeholders from v0.1 were filled in concrete detail. The Polish section grew from 7 slides to 9 (added shift-left slide + split memoir-3 into two Okefenokee slides). Total deck: 30 → 32 slides.

#### Polish section, current shape (slides 17–25)

| # | Slide | Status |
|---|---|---|
| 17 | Polish: the producer's chair | unchanged from v0.1 |
| **18** | **Get the sound right at the amp / shift-left for bands** | **NEW in v0.2** |
| 19 | When we recorded the album | unchanged |
| 20 | We didn't ship the files and walk away | unchanged |
| **21** | **Okefenokee — 3:24 (the break breathes, drums go Bonham)** | **NEW in v0.2** |
| **22** | **The solo: a wave breaking on the rocks** | **NEW in v0.2** |
| 23 | "I stayed for the mix" — thesis lived | unchanged |
| 24 | What "session musician" thinking gets wrong about polish | unchanged |
| 25 | Monday-morning move — "Stay for the mix" | unchanged |

#### Tooling section, slide 27 filled
| # | Slide | Status |
|---|---|---|
| 27 | **How we shipped the record / "like a git PR review"** | **filled in v0.2** (was placeholder) |

#### Slide-22 closing line — important honesty correction
Speaker pushed back on a draft line that overstated the mix's role: *"The only reason it made the record is I stayed for the mix."* Replaced with the honest version: *"I carried that wave from the songwriting room. Every take, every mix decision, was aimed at it."* The labor (many takes, one whole take with no edits possible, deliberate refinement in the mix room with the engineer-friend) lives in speaker notes — Option A from the brainstorm — to keep the slide photographable and let the speaker tell the labor story aloud.

### Image plan — approved, NOT YET implemented in slides.md

This is the next implementation step on resume.

#### Format constraint (locked)
- Each image-bearing slide = half-and-half vertical split
- Image as background via Marp directive: `![bg left:50%]` or `![bg right:50%]`
- L/R alternates across the deck (image-bearing slides only; lead slides skipped don't reset the alternation)
- Starting side: **L** (slide 1 = left)

#### Source constraint (locked)
- Pixabay AI-generated only
- URL pattern: `https://pixabay.com/images/search/<term>/?content_type=ai`

#### Skip-list (locked) — 6 slides stay text-only
- Slide 5 — thesis reveal ("Writers are bandmates, not session musicians")
- Slide 7 — map of the talk (4 roles)
- Slide 13 — Voice contrarian ("Voice is not the singer's job. It's a band sport.")
- Slide 23 — "I stayed for the mix" thesis lived
- Slide 28 — tactic table ("The workflow is the tooling")
- Slide 31 — manifesto

#### Filename convention (locked)
- Short, hyphenated, no slide numbers (so renumbering doesn't break names)
- All `.jpg`
- Saved to `assets/img/`

#### Approved 26-slide table

Image-bearing slides, in deck order, with proposed search terms, filenames, and L/R side. Speaker explicitly noted *"we'll probably do a few iterations to get the images right"* — these terms are starting points, not final.

| # | Slide | Pixabay search term | Filename | Side |
|---|---|---|---|---|
| 1 | Title — Rock the docs | `guitar+amp+stage` | `title-stage.jpg` | L |
| 2 | 8-piece disco band | `disco+band+performing` | `disco-band.jpg` | R |
| 3 | Power trio | `rock+trio+silhouette` | `power-trio.jpg` | L |
| 4 | Same shape as your reorg | `org+chart+broken` | `reorg.jpg` | R |
| 6 | About me | `guitarist+electric+guitar` | `about-me.jpg` | L |
| 8 | Foundation: rhythm section | `drums+bass+guitar` | `rhythm-section.jpg` | R |
| 9 | Tower of Power | `funk+horn+section` | `tower-of-power.jpg` | L |
| 10 | Foundation contrarian | `broken+metronome` | `foundation-broken.jpg` | R |
| 11 | Foundation Monday-morning | `sheet+music+neon` | `foundation-monday.jpg` | L |
| 12 | Voice intro (guitar is voice) | `spotlight+microphone+empty` | `voice-intro.jpg` | R |
| 14 | Cream | `vintage+rock+trio` | `cream-band.jpg` | L |
| 15 | Voice contrarian list | `police+abstract+rules` | `voice-cop.jpg` | R |
| 16 | Voice Monday-morning | `band+rehearsal+collaboration` | `voice-collab.jpg` | L |
| 17 | Polish: producer's chair | `mixing+console+studio` | `mixing-board.jpg` | R |
| 18 | Shift-left for bands | `vintage+guitar+amplifier+glow` | `amp-glow.jpg` | L |
| 19 | When we recorded | `recording+studio+interior` | `studio-interior.jpg` | R |
| 20 | We didn't ship and walk away | `two+people+mixing+audio` | `studio-collab.jpg` | L |
| 21 | Okefenokee — 3:24 | `okefenokee+swamp+cinematic` | `okefenokee-swamp.jpg` | R |
| 22 | The solo (wave) | `ocean+wave+rocks+dramatic` | `wave-rocks.jpg` | L |
| 24 | Polish session-musician | `abandoned+notebook+writer` | `polish-disowned.jpg` | R |
| 25 | Polish Monday-morning | `studio+headphones+mixing` | `polish-monday.jpg` | L |
| 26 | Tooling: workflow as instrument | `guitar+pedalboard+rig` | `pedalboard.jpg` | R |
| 27 | How we shipped the record | `recording+studio+workflow+screen` | `workflow.jpg` | L |
| 29 | Tooling Monday-morning | `musician+with+rig` | `tooling-monday.jpg` | R |
| 30 | Closer callback (trio) | `trio+performing+stage` | `trio-stage.jpg` | L |
| 32 | Thank you | `concert+crowd+stage+end` | `thank-you.jpg` | R |

#### Search terms flagged as creative leaps (likely first to revise on iteration)
- Slide 4 (`org+chart+broken`) — metaphorical
- Slide 15 (`police+abstract+rules`) — metaphorical
- Slide 24 (`abandoned+notebook+writer`) — metaphorical

#### Approved workflow on resume
1. Edit `slides.md` to add the 26 `![bg left:50%]` / `![bg right:50%]` directives with proposed filenames. Build stays clean — Marp tolerates missing image files (slides render text-only until files appear).
2. Speaker clicks Pixabay links at their pace, picks AI images, saves them to `assets/img/<filename>.jpg` per the table.
3. As files appear, slides progressively show images. No round-trip needed per-image.
4. Iteration pass: revise any search terms that don't yield good results; re-edit filenames if needed.

## What's NOT done (deliberately, in priority order)

1. **Image directives in `slides.md`** — approved, not yet edited. First task on resume.
2. **Image sourcing itself** — speaker does this manually via Pixabay links.
3. **Timed walkthrough** — `npm run marp:serve`, walk end-to-end at presenter pace. Polish memoir is the budget risk now that it's 9 slides instead of 7.
4. **Real LinkedIn / GitHub handles on slide 32** (currently `[your handle]` placeholders).
5. **Dracula style tweaks if needed** after seeing slides with images. The half-and-half layout may need padding/typography adjustment depending on image vibe.
6. **Tower of Power audio cue** (slide 9) — venue-A/V dependent.
7. **Vale prose pass** — `vale source/slides.md` once `vale-styles/` is populated locally.
8. **Cosmetic — rename `plans/your-recommendation-option-c-fluttering-teacup.md`** to something like `plans/rock-the-docs-design.md`.
9. **Possible slide cuts** if the talk runs long during walkthrough. First to cut: merge old Memoir 1 + 2 (slides 19+20), or one of the Tooling intro slides.

## Known open creative questions (for future reflection)

Not blocking. Worth deciding once speaker has walked the deck once:

- Does the dracula theme actually feel rock once images are in? Or feel "code editor" / mismatched with the band imagery?
- Does the manifesto land as 5 lines, or trim to 4 (Variant B from the brainstorm)?
- Are 32 slides too many for 30 minutes? Average is now < 1 min/slide; memoir slides need to breathe. May need to cut 2–3.
- Do the Monday-morning moves feel concrete enough, or too abstract?

## Resumption instructions for the next session

1. Read `playground/work-recap-so-far.md` (session 1), `playground/work-recap-2.md` (session 2), then **this file** for the full chain.
2. Read `plans/your-recommendation-option-c-fluttering-teacup.md` for the approved design plan.
3. Read `source/slides.md` to see the v0.2 implemented draft.
4. **Skill reload:** only reload `superpowers:brainstorming` if reopening creative decisions (manifesto tone, theme, etc.). For polish/refinement work, no skill reload needed.
5. Ask the speaker what to do first:
   - **Most likely next:** add the 26 image directives to `slides.md` per the approved table above. ~5 min mechanical edit; greenlight already given.
   - **After that:** speaker sources images via Pixabay AI links; we iterate on terms as needed.
   - **Then:** timed walkthrough.
6. **Do not re-ask any locked decision** unless the speaker explicitly reopens it.

## Build commands (cheat sheet)

```bash
npm run marp:serve   # live preview, port 9999, watches files
npm run marp:html    # build HTML to output/
npm run marp:pdf     # build PDF (--allow-local-files already in script)
npm run marp:pptx    # build PPTX
npm run lint         # markdownlint *.md (only checks repo-root *.md, not source/)
vale source/slides.md  # prose lint, after `vale sync` populates vale-styles/
```

## Git state at the time of this recap

```
8313689 Slide deck v.0.2          ← current HEAD
9d16f90 Add work recap            ← initial pre-lunch session-3 recap (now superseded by this file)
750046b Complete slide deck v0.1
1ef75e6 Update gitignore to keep playground files
5cbaf4f Update CLAUDE.md
e592aea add marp config
f1f6ad8 Add CLAUDE.md and talk notes
0eb272d update .gitignore
de6d9ac exclude vale styles
3b71fc4 add themes
ff12128 add gitignore and initial slide draft
```

This recap (rewriting `work-recap-3.md`) is itself an uncommitted change. Speaker can `git add playground/work-recap-3.md && git commit` whenever convenient.
