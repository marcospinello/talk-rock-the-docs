# Rock the docs — brainstorming recap (session 2)

Resumes from `/playground/work-recap-1.md`. Read that first for the prior chain of reasoning, then this file for everything decided since.

## Status

Brainstorming the deck's structure with the `superpowers:brainstorming` skill (one question at a time). Spine and shape are locked. Paused mid-question on per-section texture rotation.

## Locked decisions

### Talk parameters

- **Title:** "Rock the docs 🤘 / Applying music theory and band dynamics to technical writing"
- **Venue / length:** Conference talk, ~40–45 min
- **Audience:** Mostly fellow tech writers
- **Lens:** Band dynamics as the dominant metaphor (not just music theory in the abstract)
- **Thesis:** *Writers are bandmates, not session musicians.*
- **Raw material in scope:** Real-band case studies; user's own musician experience; tactical playbook material.
- **Raw material out of scope:** Booking.com war stories.

### Personal trio context (new in this session)

- The user's band is an **instrumental power trio** (guitar, bass, drums).
- User plays **guitar**.
- The record was **co-mixed and mastered by the user and the recording engineer**, who is a personal friend.
- Implication 1: in a trio there's no singer — **the guitar is the voice**. The "Voice" section carries what a frontperson section would carry in a fuller band.
- Implication 2: the Polish/producer section has first-person authority no case study can match — the user *was* the bandmate who stayed for the mix, which literally is the thesis.
- Implication 3: power trio framing sharpens the thesis (no one to hide behind; every player is load-bearing) — worth surfacing in the opening hook.

### Narrative shape

- **Spine A — Anatomy of a band (role-driven).** Each band role maps to a docs role.
- **Depth/breadth:** 4 roles, ~7–8 min each (balance — 6 felt list-y, 3 too narrow).
- **Lineup (in order):** Foundation → Voice → Polish → Tooling
  - **Foundation** = rhythm section (IA, style guides, linters — invisible until missing)
  - **Voice** = lead voice / guitar in a trio (narrative identity, the examples that get screenshotted)
  - **Polish** = producer/engineer (review, editing, mixing)
  - **Tooling** = roadies & venue (tooling, platforms, CI)
  - User picked Tooling over Frontperson — closer to writers' daily reality, less DevRel-flavoured.
- **Per-section structural spine (same shape for all four):** role → real-band case study → what session-musician thinking gets wrong → Monday-morning move.
- **Texture varies across sections** to avoid the "list-y" risk: same four beats every time, but rotate which beat carries the most weight per section.
- **Trio shows up as a recurring through-line** in every section, with Polish going memoir-deep. Avoids the deck feeling "biographical for 8 minutes, then not."
- **Cold open:** 60–90 sec personal story from user's trio — a moment that *was* the thesis (a session-musician collaborator who didn't fit, a take that worked because the three of them read each other, or a mix decision that made the record). Thesis revealed on the *next* slide. Lives the metaphor before naming it.
- **Closer:** Callback to the cold-open story (now reframed by everything the audience has heard), then a one-slide manifesto with 4–6 short lines — one per section — that the audience can photograph.

## Open question (paused here)

**Which texture rotation across the four sections?**

Polish is locked as memoir. Need to assign case-study, contrarian, and tactic textures to Foundation, Voice, and Tooling.

- **Option A (my recommendation):** Foundation = case-study, Voice = contrarian, Polish = memoir, Tooling = tactic.
  - Foundation gets the most iconic real-band material (Watts, Bonham, Peart, Tower of Power — instantly recognisable).
  - Voice carries the deck's sharpest opinion (e.g. "voice without a rhythm section is karaoke") — wakes the room mid-talk.
  - Polish = user's mix story.
  - Tooling closes the role arc on concrete tactics, which feeds straight into the manifesto closer without a tonal jump.
- **Option B:** Foundation = case-study, Voice = tactic, Polish = memoir, Tooling = contrarian.
  - Voice gets practical "how writers develop a voice" content; Tooling carries the contrarian punch.
  - Risk: tactic buried in section 2; ends role arc on opinion, making the manifesto feel redundant.
- **Different mix** — user defines.

> **Note for the next session:** the prior version of this file contained a queued answer at the bottom — "Your recommendation: Foundation = case-study, Voice = contrarian, Polish = memoir, Tooling = tactic" — but it was not actually sent in chat before the pause. Treat the texture rotation as **still open**, and confirm the answer with the user before locking it in.

## What still needs deciding (after texture rotation)

In rough order:

1. Real-band case studies per section (Foundation needs the iconic rhythm-section pick; Voice's contrarian/case anchor; Tooling's roadie story if any).
2. The 4–6 manifesto lines (one per section).
3. The specific cold-open trio story (which moment from the user's band).
4. Visual/theme: `.marprc.yml` currently uses `socrates`. Keep it, switch to something rockier (`marpx`, `dracula`), or design a deck-specific style block?
5. Slide-by-slide outline.
6. Implementation in `source/slides.md`.
7. Serve and review via `npm run marp:serve` (port 9999).

## Resumption instructions for the next session

1. Read `/playground/work-recap-1.md` then this file.
2. Re-invoke the `superpowers:brainstorming` skill (the prior session had it loaded — start each new session by reloading it).
3. Re-ask the user the **texture rotation** question (Option A vs B vs custom). Surface the queued-but-unsent answer so they can confirm or change.
4. Do not re-ask anything in "Locked decisions."
5. After texture rotation is answered, continue with the "still needs deciding" list above, one question at a time per the brainstorming skill.
6. Build target: Marp deck in `source/slides.md`, served via `npm run marp:serve` on port 9999. `.marprc.yml` is the config hub; current theme is `socrates`.
