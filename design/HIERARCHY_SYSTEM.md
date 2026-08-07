---
title: "Hierarchy System"
type: design
status: canonical
related:
  - "[[CORE_EXPERIENCE_STATEMENT]]"
  - "[[UX_ARCHITECTURE_BLUEPRINT]]"
  - "[[COMPOSITION_PRINCIPLES]]"
  - "[[TRANSITION_PHILOSOPHY_CANONICAL]]"
  - "[[DESIGN_SYSTEM_TOKENS]]"
  - "[[DESIGN_SYSTEM]]"
  - "[[PROJECT_PAGE_SYSTEM]]"
---

# HIERARCHY SYSTEM
Solarisx Portfolio — Version 1.0

Governed by CORE_EXPERIENCE_STATEMENT.md. Extends
UX_ARCHITECTURE_BLUEPRINT.md §2 (Primary/Secondary frame weight already
defined there, not restated here) from a documented label into an
applied system. Written from DESIGN_CRITIQUE_PHASE1.md §0 and §7 — the
project doesn't suffer from inconsistency, it suffers from uniformity.

---

## 1. The Governing Rule

> Hierarchy through contrast, not volume.

The strongest frame does not get bigger. Everything around it gets
quieter so it can land. This rule is not optional texture — it's the
test every hierarchy decision in this document has to pass.

---

## 2. The Test, Before Making Anything Louder

Before increasing size, adding color, or adding an element to signal
importance, ask in this order:

1. Can **pacing** (more/less surrounding pause) do this instead?
2. Can **density** (fewer/more elements) do this instead?
3. Can **restraint** (what's deliberately absent nearby) do this instead?
4. Only if none of the above work — can composition or motion carry it
   (see COMPOSITION_PRINCIPLES.md, TRANSITION_PHILOSOPHY.md)?

Size/color increases are not on this list. If a hierarchy problem can
only be solved by making something bigger or more colorful, that's a
signal the surrounding restraint isn't doing its job yet — fix the
surroundings first.

---

## 3. Frame-Level Hierarchy

Applying the test to the five frames (weights per
UX_ARCHITECTURE_BLUEPRINT.md §2):

| Frame | Weight | Pacing | Density | Restraint signal |
|---|---|---|---|---|
| Opening Frame | Primary | Full viewport, no competing content | Sparsest possible — identity, statement, cue only | Nothing else exists here — the absence *is* the emphasis |
| Proof of Craft | Primary (highest) | Most generous surrounding space of any content frame | Sparse — few, unhurried rows | See §4 — the frame needs *internal* hierarchy, not more external volume |
| Context Layer | Primary | Standard | Sparse — two paragraphs, nothing else | Quiet by design; deepens, doesn't compete |
| Capability Map | Secondary | Tighter, faster-moving | Denser — 3-column grid already achieves this (confirmed working in DESIGN_CRITIQUE_PHASE1.md §4) | Grid density itself signals "supporting evidence," not centerpiece |
| Final Frame | Primary | Most generous trailing space (page's actual end) | Single focus (form) | One action, no competing links-as-CTAs |

Capability Map is the one frame that already partially solved this
(density, via its grid) before this document existed — credit that, and
don't undo it by adding a heading-size change on top of a mechanism
that's already working.

---

## 4. Within-Frame Hierarchy — Proof of Craft

Critique finding: all three project rows are currently identical weight,
in a frame with zero internal hierarchy despite being the site's
highest-priority evidence.

**Rule:** a lead/featured item is distinguished through:
- **Extra surrounding space** (more pause before it, more after) — not a
  larger title
- **The accent color, once** — CREATIVE_DIRECTION_BOARD.md §1 already
  establishes the accent as scarce and moment-justified; a single
  accent-colored rule (replacing the neutral border) under exactly one
  row is a legitimate, already-sanctioned use of that scarcity, not a
  new decoration
- **Position** — first in sequence, which the current implementation
  already provides by default (no change needed there)

**Explicitly not:** larger type size for the lead row. Per §1's test,
size is the last resort, not the first.

---

## 5. Attention Priority — One Focal Point Per Frame

Every frame should have exactly one thing the eye is meant to land on
first. Naming it explicitly, per frame:

| Frame | Focal point |
|---|---|
| Opening Frame | The headline (once the signature object is real, this may shift — re-evaluate then, not now) |
| Proof of Craft | The lead project row (§4) |
| Context Layer | The first paragraph's opening line |
| Capability Map | No single focal point by design — Secondary frames are allowed to present as a set, not a hierarchy of one |
| Final Frame | The form's first field |

If two elements in the same frame currently compete for this role,
that's a hierarchy defect — resolve it using §2's test, not by
guessing which one "feels" more important.

---

## 6. What This Document Does Not Cover

- *How* one frame hands off to the next → TRANSITION_PHILOSOPHY.md
- *Where* elements sit spatially within a frame → COMPOSITION_PRINCIPLES.md
- Exact spacing/color/type token values → DESIGN_SYSTEM_TOKENS.md

---

## Related Documents

- [[CORE_EXPERIENCE_STATEMENT]] — governs this document
- [[UX_ARCHITECTURE_BLUEPRINT]] — this document extends its §2 (frame weight)
- [[COMPOSITION_PRINCIPLES]] — companion document; *where* elements sit,
  vs. this document's *why* they carry weight
- [[TRANSITION_PHILOSOPHY_CANONICAL]] — uses this document's §1/§3 for
  transition tier reasoning
- [[DESIGN_SYSTEM_TOKENS]] — holds the exact values this document's rules
  are expressed through
- [[DESIGN_SYSTEM]] — cites this document for its hierarchy review standard
- [[PROJECT_PAGE_SYSTEM]] — cites this document for why Proof of Craft
  holds its weight
