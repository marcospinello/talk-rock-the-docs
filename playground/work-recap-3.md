# Rock the docs — work recap (session 3)

Resumes from `/playground/work-recap-so-far.md` (session 1) and `/playground/work-recap-2.md` (session 2). Read both first for the full chain of brainstorming reasoning. This file captures everything decided and built in session 3.

## Status

**Brainstorming complete. First implementation pass done.** Plan was written and user-approved (`plans/your-recommendation-option-c-fluttering-teacup.md`). Theme switched, `source/slides.md` fully rewritten with 30 slides + speaker notes. Build verified clean. Two speaker-fillable placeholders remain (your specific memoir moments). All work committed to git.

## What was decided this session

### Talk parameters changed
- **Length: 40–45 min → ~30 min.** The locked "4 roles × 7–8 min each" math no longer holds at 30 min; we resolved this with Option C below.

### Decisions locked (in the order we took them)

1. **Texture rotation — Option A** (the queued-but-unsent recommendation from session 2):
   - Foundation = case-study
   - Voice = contrarian
   - Polish = memoir
   - Tooling = tactic

2. **Section budget — Option C (unequal weights):**
   - Foundation: ~5–6 min (lean 3-beat, drop contrarian)
   - Voice: ~6 min (full 4-beat)
   - Polish: ~9 min (memoir breathes)
   - Tooling: ~5–6 min (lean 3-beat, drop contrarian)
   - Cold open + closer eat ~4 min total. Total ~30 min.

3. **Cold open — disco-band-shrinking-to-trio reorg.** Plunders the framing already in the talk announcement comments; "company reorg with built-in product pivot" is the audience hook before the thesis is named.

4. **Foundation case anchor — Tower of Power's rhythm section.** Interlocking precision = IA-as-system. Flag: TOP is instantly recognizable to musicians but a tech-writer audience may need a 5-second audio cue (slide notes recommend "What Is Hip"). Polish-pass decision once venue A/V is known.

5. **Voice case anchor — Cream.** Three virtuosos trading voice across instruments and microphones; "Sunshine of Your Love" riff is the voice before any vocals. Supports the contrarian claim *"voice is not the singer's job; voice is a band sport."*

6. **Tooling case anchor — mini-memoir from your recording setup.** Acknowledged tradeoff: two memoir-flavored sections in a row (Polish then Tooling). Decided this is fine because the closer's emotional weight benefits from already being in personal-story territory.

7. **Tooling angle — process/workflow decision (not gear).** Tactic shape: *"the workflow is the tooling; what you automate decides what you can sound like."* Strong fit for the writer audience (CI, lint-on-commit, doc-as-code, CMS choice).

8. **Manifesto tone — imperative commands.** "Band rules taped to the rehearsal-room wall."

9. **Manifesto draft — Variant A (measured commands), 5 lines:**
   ```
   Lock the foundation, then play.
   Find the voice with the band, not for it.
   Stay for the mix.
   Choose your workflow like an instrument.
   Be a bandmate, not a session musician.
   ```

10. **Theme — switch from `socrates` to `dracula`.** Dark mode, dev-aesthetic contrast, set in `.marprc.yml` so all output formats stay consistent.

## What was implemented

### Files modified
- **`.marprc.yml`** — single-line change: `theme: socrates` → `theme: dracula`.
- **`source/slides.md`** — full rewrite. 30 slides, all with speaker notes in `<!-- ... -->` HTML comments. Front matter retains the existing FA import and adds helper CSS classes (`.big`, `.huge`, `.quiet`, `.accent`, `.manifesto p`). Original talk-announcement copy preserved as a comment at the bottom of the file as a phrase bank for Q&A.
- **`.gitignore`** — fixed a real bug: the prior exception attempt (`!playground/foo.md`) was non-functional because `playground/` excluded the parent dir, and git can't re-include a file whose parent dir is excluded. Changed to `playground/*` so the exceptions actually work. The recap files are now genuinely trackable.
- **`output/slides.html`** — rebuilt on dracula by `npm run marp:html`.

### Files added (now tracked thanks to the gitignore fix)
- `playground/progress-status.md`, `playground/work-recap-so-far.md`, `playground/work-recap-2.md` — the prior session's recaps.

### Plan written
`plans/your-recommendation-option-c-fluttering-teacup.md` — full plan file written during plan mode and approved. Captures the locked decisions, slide-by-slide outline, files-to-modify list, and verification steps. The auto-generated filename is whimsical; consider renaming to `plans/rock-the-docs-design.md` if it bothers you (cosmetic only).

### Slide-by-slide outline (as built in `source/slides.md`)

| # | Section | Title / focus |
|---|---|---|
| 1 | Open | Title slide |
| 2 | Open | "I used to play in an 8-piece disco band." |
| 3 | Open | "Then it became a power trio." |
| 4 | Open | "Same shape as your last reorg." |
| 5 | Open | Thesis reveal — "Writers are bandmates, not session musicians." |
| 6 | About | About me (TW + guitarist + co-mixed the album) |
| 7 | Map | Where we're going (4 sections preview) |
| 8 | Foundation | Foundation: rhythm section intro |
| 9 | Foundation | Tower of Power case |
| 10 | Foundation | What "session musician" thinking gets wrong |
| 11 | Foundation | Monday-morning move ("Lock the foundation, then play") |
| 12 | Voice | Voice: in a trio, no singer — guitar is the voice |
| 13 | Voice | Contrarian — "Voice is not the singer's job. It's a band sport." |
| 14 | Voice | Cream case |
| 15 | Voice | What "session musician" thinking gets wrong about voice |
| 16 | Voice | Monday-morning move ("Find the voice with the band, not for it") |
| 17 | Polish | Polish: the producer's chair intro |
| 18 | Polish | Memoir 1 — set the scene ("When we recorded the album") |
| 19 | Polish | Memoir 2 — co-mixing with the engineer-friend |
| 20 | Polish | **Memoir 3 — the decision that changed the record [PLACEHOLDER]** |
| 21 | Polish | Thesis lived — "I didn't ship the file and walk away. I stayed for the mix." |
| 22 | Polish | What "session musician" thinking gets wrong about polish |
| 23 | Polish | Monday-morning move ("Stay for the mix") |
| 24 | Tooling | Tooling: the workflow as instrument intro |
| 25 | Tooling | **Mini-memoir — workflow call early in the recording [PLACEHOLDER]** |
| 26 | Tooling | The tactic ("the workflow is the tooling") with comparison table |
| 27 | Tooling | Monday-morning move ("Choose your workflow like an instrument") |
| 28 | Close | Closer callback — the trio survived because everyone was a bandmate |
| 29 | Close | Manifesto — the 5 imperatives (Variant A) |
| 30 | Close | Thank you / Q&A |

### Build verification
- `npm run marp:html` — clean. Output is 122K, dracula renders, all 30 slides emit cleanly.
- `npm run lint` — only flags pre-existing line-length issues in `CLAUDE.md` and `README.md`. No issues in slides.

## Speaker-fillable placeholders (intentionally left)

These need your voice; can't be invented:

1. **Slide 20 — "The decision that changed the record."** Pick one specific mix moment from your album:
   - A take you almost cut that became the album's best moment
   - An EQ / compression call that changed a song's character
   - A part where the engineer pushed back and you were right (or wrong, and learned)
   - A disagreement between you and the engineer that produced the record
   Speaker notes under the slide spell this out.

2. **Slide 25 — "In the studio, we made one workflow call early."** Pick one process/workflow decision from the recording (process, not gear):
   - Mixing roughs as you went
   - File-naming convention
   - Shared sessions over a specific tool
   - Live tracking vs. fixing later
   Speaker notes spell this out too.

3. **Slide 30 — your real LinkedIn / GitHub handles** (currently `[your handle]` placeholders).

## Known follow-ups (deliberately deferred)

In rough priority order:

1. **Speaker fills the two memoir placeholders.** Do this before any other polish — it's the thing only you can do.
2. **Image sourcing.** `assets/img/` has only `.DS_Store`. Many slides work as text-on-color on dracula, but candidates for images: 8-piece-band silhouette, trio silhouette, org-chart shrink, Tower of Power photo, Cream lineup photo, mix-room/studio photo. Source from Wikimedia / Unsplash with permissive licenses.
3. **First read-through.** `npm run marp:serve` (port 9999), walk through end to end at presenter pace. Time it. Polish memoir is the budget risk — if it runs long, the deck blows past 30 min.
4. **Dracula style tweaks if needed.** Stock dracula may clash with the `.fa-twitter`/`.fa-linkedin` aqua/blue accents. Patch in the front-matter `style:` block if anything looks wrong.
5. **Tower of Power audio cue.** Decide based on venue A/V whether to embed a 5-second clip or skip. If embedding, Marp's allowlist supports `<video>` (already in `.marprc.yml`).
6. **Vale prose pass.** Once `vale-styles/` is populated locally (`vale sync`): `vale source/slides.md`. Style/grammar pass.
7. **Possible slide cuts** if the talk runs long. First to cut: Memoir 3 (slide 20) if you can fold the moment into Memoir 2, or one of the Tooling intro slides (slide 24).
8. **Cosmetic — rename `plans/your-recommendation-option-c-fluttering-teacup.md`** to something like `plans/rock-the-docs-design.md`. Auto-generated whimsical name; harmless.

## Open creative questions for next session

None blocking, but worth deciding once you've walked the deck:

- **Does the dracula theme actually feel rock?** Or does it feel "code editor" and we should revisit (custom style block on top, or a different theme like marpx/jobs/orwell).
- **Does the manifesto land as 5 lines, or should we trim to 4 (Variant B from the brainstorm)?** Decide after presenting it once.
- **Are 30 slides too many for 30 minutes?** Each slide ~1 min average, but the memoir slides sit longer and the cold-open slides go fast. May need to cut 2–3.
- **Do the Monday-morning moves feel concrete enough, or too abstract?** The audience comes for stories; tactics need to feel like a colleague's nudge, not a checklist.

## Resumption instructions for the next session

1. Read `playground/work-recap-so-far.md` (session 1), `playground/work-recap-2.md` (session 2), then **this file** (session 3) for the full chain.
2. Read `plans/your-recommendation-option-c-fluttering-teacup.md` for the approved design plan.
3. Read `source/slides.md` to see the implemented draft.
4. Reload the `superpowers:brainstorming` skill *only* if reopening creative decisions (e.g., manifesto tone, theme). For polish/refinement work, no skill reload needed.
5. Ask the user what they want to work on:
   - Fill the two memoir placeholders (slides 20 and 25)?
   - Walk the deck and time it?
   - Image sourcing pass?
   - Style / dracula tweaks?
   - Slide cuts / pacing?
6. **Do not re-ask anything in "Decisions locked" above** unless the user explicitly reopens it.
7. Build commands to remember:
   - `npm run marp:serve` — live preview on port 9999 (watches files)
   - `npm run marp:html` / `marp:pdf` / `marp:pptx` — build output
   - `npm run lint` — markdownlint
   - `vale source/slides.md` — prose lint (after `vale sync`)

## Session-3 git state at the time of this recap

User committed everything before lunch break:
- `.marprc.yml` (theme switch)
- `.gitignore` (parent-dir exception fix)
- `source/slides.md` (full rewrite)
- `playground/progress-status.md`, `work-recap-so-far.md`, `work-recap-2.md` (now tracked)
- `plans/your-recommendation-option-c-fluttering-teacup.md` (approved plan)
- `output/slides.html` (rebuilt)

This recap (`work-recap-3.md`) was written *after* that commit, so it'll be a separate addition.
