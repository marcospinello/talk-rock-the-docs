---
marp: true
author: Marco Spinello
title: Rock the docs 🤘
style: |
    .fa-twitter, .fa-x-twitter { color: #8be9fd; }
    .fa-linkedin { color: #8be9fd; }
    .fa-github { color: #f8f8f2; }
    @import 'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/7.0.1/css/all.min.css';
    .big {
      font-size: 2em;
      font-weight: 700;
      line-height: 1.15;
    }
    .huge {
      font-size: 2.6em;
      font-weight: 800;
      line-height: 1.1;
    }
    .quiet {
      color: #6272a4;
      font-style: italic;
    }
    .accent {
      color: #ff79c6;
    }
    .manifesto p {
      font-size: 1.4em;
      font-weight: 600;
      margin: 0.6em 0;
      line-height: 1.25;
    }
---

<!--
========================================================================
Rock the docs 🤘  —  Marco Spinello

A 30-minute conference talk for fellow tech writers.
Thesis: writers are bandmates, not session musicians.
Spine: Foundation → Voice → Polish → Tooling.
Section budget (Option C, unequal weights):
  Open ~2m · About+Map ~2m · Foundation ~5–6m · Voice ~6m
  Polish ~9m · Tooling ~5–6m · Close ~2m

Original talk-announcement copy preserved at the bottom of this file as a
speaker reference. Do NOT delete; it has phrasing we plundered for the
cold open and may seed Q&A.
========================================================================
-->

<!-- _class: lead -->

# Rock the docs 🤘

### Applying music theory and band dynamics to technical writing

*Marco Spinello* — Senior technical writer, Booking.com

<!--
Welcome the room. The 🤘 is on purpose — sets the tone now, not later.
~30 seconds on the title slide. Don't introduce yourself yet — slide 6.
-->

---

<!-- _class: lead -->

## I used to play in an 8-piece disco band.

<!--
Lead with the personal hook. A beat of audience confusion is exactly right.
Don't explain yet. Let it land.
-->

---

<!-- _class: lead -->

## Then it became a power trio.

<span class="quiet">Guitar. Bass. Drums.</span>

<!--
The audience starts doing the math: 8 → 3.
Mime the shrinking with your hands if you want.
-->

---

<!-- _class: lead -->

## Same shape as your last reorg.

<!--
Bridge. Recognition laugh expected.
The band experience and the corporate experience share the same shape:
shrinking, pivoting, deciding who's load-bearing.
-->

---

<!-- _class: lead -->

<div class="huge accent">Writers are bandmates,<br />not session musicians.</div>

<!--
This is the talk. Read it slowly. Stop. Let it sit.

Photographable slide #1 — people will start typing.
-->

---

## About me

- ✍️ **Marco Spinello** — Senior technical writer at Booking.com
- 🎸 Guitar in an instrumental power trio
- 🎚️ Co-mixed and co-mastered our album with the recording engineer
- 🐾 No CS background. Curious as a cat.

<!--
~30 seconds. The detail that matters is the third bullet:
"I co-mixed the record." That's not just a fan with a metaphor —
that's having been in the rooms where the work happens.
-->

---

## Where we're going

1. **Foundation** — the rhythm section
2. **Voice** — what the band sounds like
3. **Polish** — the producer's chair
4. **Tooling** — the workflow as instrument

<span class="quiet">Four bandmates. One thesis. Thirty minutes.</span>

<!--
Quick orientation. Don't dwell.
"Each of these maps to a part of your job. We're going to walk through them as a band."
-->

---

## 1. Foundation

### The rhythm section.

<span class="quiet">Style guides. IA. Linters. The stuff nobody applauds.</span>

<!--
Set up the section. The rhythm section is what the band stands on.
Same for docs: style guides, information architecture, the linter.
Boring on paper. Load-bearing in practice.
-->

---

## Tower of Power

### Rocco Prestia. David Garibaldi. Lock-tight.

<span class="quiet">Three players. One pulse. You can't tell where one ends and the next begins.</span>

<!--
If the venue allows audio, play 5 seconds of "What Is Hip" — the canonical
TOP rhythm-section moment. Otherwise just describe it.

The point: the rhythm section isn't multiple people doing similar jobs.
It's a single system, locked together. That's information architecture.
That's a style guide everyone follows. That's the linter that catches the
same drift every time.
-->

---

## What "session musician" thinking gets wrong

> "Style guides are boring."
> "IA is infrastructure."
> "Linters are nags."

### All three are the foundation everyone plays on.

<!--
Push back gently. The session-musician mindset treats foundation as
someone else's job — the IA team, the linter, the platform.

But the band that ignores its foundation falls apart in the first chorus.
If your foundation is broken, no one hears the song.
-->

---

## Monday-morning move

### If you have no style guide, your style guide is whoever shouts loudest in the PR.

<span class="accent">**Lock the foundation, then play.**</span>

<!--
Concrete: pick one foundation thing your team has been deferring
(style guide, IA review, linter setup) and put it on this week's calendar.
One thing.

Manifesto preview — "Lock the foundation, then play." It lands again at the close.
-->

---

## 2. Voice

### In a trio, there's no singer.

<span class="quiet">The guitar is the voice.</span>

<!--
Bridge. We've covered the rhythm section; now: who is the voice?

In a trio, there's no separate vocalist. The guitar carries the melody,
the personality, the screams. Voice is *played*, not just spoken.

Same in docs: voice isn't owned by one person with "writer" in their title.
-->

---

<!-- _class: lead -->

<div class="huge">Voice is not the singer's job.</div>

### It's a band sport.

<!--
Stop. Let it land.

This is the controversial line of the talk. The room may include writers who
think of voice as their own deliverable — the "tone of voice" doc, the brand
bible, the thing the writer owns.

We're going to challenge that.
-->

---

## Cream

### Three virtuosos. No frontperson.

- Jack Bruce — bass, vocals
- Eric Clapton — guitar, vocals
- Ginger Baker — drums, occasional vocals

<span class="quiet">"Sunshine of Your Love" — the riff is the voice before any singing happens.</span>

<!--
Cream traded voice across all three of them — vocals, instruments, even who took
which song. The most famous Cream moment ("Sunshine of Your Love") is a riff.
Three notes. That's voice without anyone singing.

Voice isn't who holds the microphone. It's what the band agrees on.
-->

---

## What "session musician" thinking gets wrong about voice

- Writers as voice-cops policing PRs
- The "tone of voice" doc nobody reads
- Voice as a deliverable instead of a property

### Voice that the band doesn't believe is karaoke.

<!--
The session-musician model: writer hands voice down from on high; everyone else
complies (or doesn't).
The band model: voice is what the band does on a Tuesday afternoon when nobody's
watching.

If only the writer cares about voice, you don't have a voice — you have a brand bible.
-->

---

## Monday-morning move

### Stop being the voice cop. Start running voice as a band activity.

<span class="accent">**Find the voice with the band, not for it.**</span>

<!--
Concrete: invite engineers/PMs/designers to a 30-minute "voice listening" session.
Read three docs together. What do they sound like? Whose voice is that?
Voice gets fixed when the band hears itself.
-->

---

## 3. Polish

### The producer's chair.

<span class="quiet">Mixing. Mastering. The moment the record becomes itself.</span>

<!--
This is the section that matters most to me personally. Polish — the
producer/engineer chair. This is where I spent the most time in the band.
This is where I learned the thesis is true.

Slow down here. The next ~9 minutes are memoir.
-->

---

## When we recorded the album

We tracked over a few weekends in a friend's studio.

The record we wanted didn't exist yet — it lived between the takes, in the edits, in the mix.

<!--
Set the scene with your actual story. Date, place, mood — fill in the specifics
the audience can picture. Keep it short and concrete; people lean in for stories.
-->

---

## We didn't ship the files and walk away.

I sat next to the engineer for the mix. He's also a friend.

<span class="quiet">Two opinions. One pair of speakers. Hours of small calls.</span>

<!--
The friendship matters: we trusted each other to push back. The work matters:
every fader move was an argument we were having about what the band sounded like.

I wasn't there to "approve." I was there because the mix was the work.
-->

---

## The decision that changed the record

<span class="quiet">[Specific mix moment — to be filled in by speaker]</span>

### Nobody else was going to make that call.

<!--
Pick ONE specific moment from the mix and tell it concrete. ~90 seconds.
Candidates:
  - A take you almost cut that became the album's best moment
  - An EQ / compression call that changed a song's character
  - A part where the engineer pushed back and you were right (or wrong, and learned)
  - A moment where you and the engineer disagreed and the disagreement made the record

The slide stays vague on purpose; your voice does the work here.
-->

---

<!-- _class: lead -->

<div class="huge">I didn't ship the file<br />and walk away.</div>

### I stayed for the mix.

<!--
This is the spine of the talk. Read slowly.

The thesis isn't an aphorism — it's a thing I literally did. And it's the thing
the audience can choose to do, or choose not to.
-->

---

## What "session musician" thinking gets wrong about polish

- Writers handing off drafts and disappearing
- Review as a checkbox
- "I delivered the doc" — and then?

### The disowned doc is the session musician's signature.

<!--
You see this all the time: writer ships draft → someone "reviews" → it lands →
the writer is on the next ticket. The doc has no parent. Nobody iterates.
Nobody listens for what's wrong.

That's session-musician work. It's transactional. The mix never happens.
-->

---

## Monday-morning move

### Don't close the ticket on draft submission.

<span class="quiet">Stay for review. Stay for the metrics. Stay for the rewrite when something breaks.</span>

<span class="accent">**Stay for the mix.**</span>

<!--
Concrete: pick your most-read doc from the last quarter. Re-read it.
Where would you fade something down? What needs more presence?
The mix isn't done when you ship — you can come back.
-->

---

## 4. Tooling

### The workflow is the instrument.

<span class="quiet">Roadies. Venues. The rig. What you automate becomes what you can sound like.</span>

<!--
Last section. Bridge from polish: now we're talking about what makes polish
possible at scale — the tooling, the workflow, the platform that decides what
kinds of moves you can even attempt.
-->

---

## In the studio, we made one workflow call early.

<span class="quiet">[Specific workflow / process decision — to be filled in by speaker]</span>

### Everything we could do later was set by that call.

<!--
Pick ONE process / workflow decision from the recording — process, not gear.
Candidates:
  - "We mixed roughs as we went" → caught problems while songs grew, not after
  - "We named files this specific way" → could find anything six months later
  - "We shared sessions over [tool]" → engineer could work between our sessions
  - "We tracked drums and bass live" → committed to the take instead of fixing it later

~45 seconds. The point: the workflow opens or closes doors before any music happens.
-->

---

## The workflow is the tooling.

What you automate decides what you can sound like.

| You automate | You can sound like |
|---|---|
| Lint-on-commit | A band that never plays out of tune |
| Doc-as-code | A band that ships every time it rehearses |
| CI for content | A band that hears itself before the audience does |
| Templated reviews | A band whose feedback loop is shorter than its release cycle |

<!--
Make the tactic concrete with examples the audience already half-believes.

If your CI doesn't lint your docs, you don't have linted docs. If your CMS
doesn't support review-as-you-write, you don't have review.
-->

---

## Monday-morning move

### Audit your writer workflow this week. What would a bandmate change?

<span class="accent">**Choose your workflow like an instrument.**</span>

<!--
Concrete: spend 60 minutes mapping the writer workflow. Where does work get
stuck? What does your CMS make easy that isn't actually valuable?
What would a different tool unlock?

A bandmate optimizes the rig because the rig shapes the music.
-->

---

<!-- _class: lead -->

## The 8-piece became a trio.

### The trio survived because everyone was a bandmate.

<span class="quiet">Nobody was a session musician. Nobody could afford to be.</span>

<!--
Callback to the cold open. Now everything in between gives this its full weight.

In a trio, there's no hiding. Every player is load-bearing. Every miss is heard.
That's the docs team I want to be on.
-->

---

<!-- _class: lead -->

## <span class="accent">The band rules</span>

<div class="manifesto">

Lock the foundation, then play.

Find the voice with the band, not for it.

Stay for the mix.

Choose your workflow like an instrument.

**Be a bandmate, not a session musician.**

</div>

<!--
The photographable slide. Read it once, slow. Then stop talking.

If only one slide makes it onto Twitter, this is the one.
-->

---

<!-- _class: lead -->

## Thank you 🙏

<span class="quiet">Questions, arguments, band recommendations — all welcome.</span>

**Marco Spinello**

<i class="fa-brands fa-linkedin"></i> [your handle] · <i class="fa-brands fa-github"></i> [your handle]

<!--
Q&A. Stay loose. The talk is the talk; the conversation after is where you find
out what landed.

TODO before talk: replace [your handle] placeholders with real handles.
-->

---

<!--
========================================================================
SPEAKER REFERENCE — original talk announcement (kept for source material)

This is the meetup.com / conference-pitch copy that seeded the deck.
Useful for Q&A prep and as a phrase bank.

#### Talk title
Rock the docs

#### Short summary
What do a power trio and a docs team have in common? "Rock the Docs" draws
parallels between playing music in a band (songwriting, tone, dynamics, and
recording) and the craft of technical writing, from stakeholder management
to tone of voice and shift-left thinking.

#### Long summary
"Rock the Docs" tells the story of a disco band that shrank from eight
members to a power trio. Basically the same as a company reorg with built-in
product pivot. Music and technical writing have more in common than meets
the eye: music theory maps the territory like information architecture, a
metronome enforces discipline like git, and song dynamics prevent the "wall
of text" effect of very long, very dense docs.

Guitar tone becomes tone of voice, equalization adjusts it per content type,
and effects act as admonitions that highlight key sections.

The band recording is their MVP, scoped and time-boxed, just like any good
documentation deliverable.

#### Talk announcement on meetup.com
The discotheque gets disco-technical, as Marco Spinello, technical writer at
Booking.com shows us how music theory can be applied to documentation, using
examples from both his professional and creative life.

This light-hearted look at technical writing will cover:
- Why Git is like a metronome
- Why managing stakeholders is not unlike managing band members
- Why recording an album is not unlike delivering an MVP
========================================================================
-->
