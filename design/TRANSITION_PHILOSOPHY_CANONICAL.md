# TRANSITION PHILOSOPHY
Solarisx Portfolio — Version 1.0 (Canonical, pending START_HERE.md reference)

Governed by CORE_EXPERIENCE_STATEMENT.md. Companion to
CREATIVE_DIRECTION_BOARD.md §6 (Animation Philosophy — timing/easing
character already defined there, not restated here) and
HIERARCHY_SYSTEM.md. Written in response to DESIGN_CRITIQUE_PHASE1.md §6:
`--ease-connective` existed as a token with zero implementation.

---

## 1. The Governing Rule

> A transition is an edit, not a reveal.

Every frame currently reveals itself independently, on its own scroll
trigger, unaware of what came before or after. That produces animation.
It does not produce a cut. This document defines what a transition must
achieve — not how it's triggered in code.

---

## 2. What Makes Something a Transition, Not a Reveal

| Reveal (current default) | Transition (target) |
|---|---|
| Triggers in isolation, no awareness of adjacent frames | Triggers in relationship to the previous frame's exit |
| Uses `ease-cinematic` (entrance character) | Uses `ease-connective` (handoff character) — Board §6 |
| No relationship to what came before | Previous frame visibly hands off to the next |

**What must be true, regardless of implementation:** the incoming frame
should begin before the outgoing frame has fully finished — there must be
a genuine overlap, not a gap and not a hard cut. The outgoing frame's
last visible content should settle using `duration-transition`, not
`duration-reveal` — a handoff is quicker and quieter than an entrance.
Exact trigger thresholds are an implementation decision; if a specific
value proves stable and correct over time, it earns a token in
DESIGN_SYSTEM_TOKENS.md. Until then, it stays out of this document.

---

## 3. Transition Tiers

Not every handoff deserves the same weight. Per
UX_ARCHITECTURE_BLUEPRINT.md §2's frame hierarchy and
HIERARCHY_SYSTEM.md §3:

| Tier | Handoff | Character | Reasoning |
|---|---|---|---|
| **1 — Cold open resolves** | Opening Frame → Proof of Craft | Most considered treatment on the page | The site's thesis resolving into evidence — CREATIVE_DIRECTION_BOARD.md §4's "Evidence begins the story" made literal at the one moment it actually happens |
| **2 — Mid-sequence cuts** | Proof of Craft → Context Layer, Context Layer → Capability Map | Standard connective handoff, `ease-connective`, no added ceremony | Development beats, not thesis moments — uniformity here is correct, not a gap |
| **3 — Arrival** | Capability Map → Final Frame | Should feel like arriving, not just another cut | The resolution beat — distinguishable from Tier 2 through pacing, not size (HIERARCHY_SYSTEM.md §1) |

Tier 1 and Tier 3 are the only two transitions that should read as
distinct from the rest. Everything in Tier 2 should feel identical to
each other — that consistency is what makes Tier 1 and Tier 3 register
as different at all.

---

## 4. Restraint Constraint

Per the project's hierarchy-through-contrast principle
(HIERARCHY_SYSTEM.md §1): Tier 1 and Tier 3 are NOT permitted to:

- Introduce new easing curves beyond the four already defined
- Use `ease-revelation`/`duration-revelation` (Revelation-category only,
  per CREATIVE_DIRECTION_BOARD.md §1 — a transition is never a Revelation
  moment)
- Add visual elements (lines, dividers, decorative marks) not already
  established

They are permitted to differ only through **timing** (longer/shorter
overlap), **pacing** (more/less surrounding pause), and **sequencing**
(what settles before what begins). If a proposed transition treatment
can't be expressed through those three levers, it's decoration — reject
it, per LAW 4's decoration hierarchy.

Not every boundary needs authored motion layered on top of space, either.
For a Tier 2 handoff, generous spacing alone — with no added transition
motion — is sometimes the more restrained and correct choice.

---

## 5. Reduced Motion

Transitions collapse to instant state changes, same as every other
motion category in this project. No separate handling to invent.

---

## 6. What This Document Does Not Cover

- *Why* a frame has the weight it has → HIERARCHY_SYSTEM.md
- *Where* elements sit within a frame → COMPOSITION_PRINCIPLES.md
- Exact duration/easing values, and any future trigger-position tokens →
  CREATIVE_DIRECTION_BOARD.md §6 / DESIGN_SYSTEM_TOKENS.md §4
