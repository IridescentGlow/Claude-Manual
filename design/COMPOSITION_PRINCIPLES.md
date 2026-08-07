---
title: "Composition Principles"
type: design
status: canonical
related:
  - "[[CORE_EXPERIENCE_STATEMENT]]"
  - "[[CREATIVE_DIRECTION_BOARD]]"
  - "[[HIERARCHY_SYSTEM]]"
  - "[[TRANSITION_PHILOSOPHY_CANONICAL]]"
  - "[[DESIGN_SYSTEM_TOKENS]]"
  - "[[DESIGN_SYSTEM]]"
  - "[[PROJECT_PAGE_SYSTEM]]"
---

# COMPOSITION PRINCIPLES
Solarisx Portfolio — Version 1.0

Governed by CORE_EXPERIENCE_STATEMENT.md. Extends
CREATIVE_DIRECTION_BOARD.md §9 (Composition Style — general principles
defined there, not restated here) into per-frame application. Written
from DESIGN_CRITIQUE_PHASE1.md §7's most repeated finding: "where does
the eye travel? Center, every frame, every time."

---

## 1. The Governing Rule

> Every frame needs one clear focal point (HIERARCHY_SYSTEM.md §5).
> How that focal point sits in space should vary deliberately across
> the page — not repeat the same layout by default.

Centered-and-stacked is not wrong. It's currently the *only* composition
on the page, applied to every frame regardless of that frame's actual
role. That's the defect — not the pattern itself.

---

## 2. Page-Level Rhythm

A five-frame page with no compositional variation reads as five
independent screens. A deliberate rhythm reads as one directed sequence.
Rule, borrowed from three-act structure: **symmetry at the edges,
asymmetry in the development.**

| Frame | Composition | Reasoning |
|---|---|---|
| Opening Frame | Symmetrical, centered | Confidence and stability at the open — per LAW 8, symmetry itself communicates this; correct as-is |
| Proof of Craft | Asymmetric — left-aligned title, right-aligned metadata | Already implemented this way in code (title/category two-column split) — confirmed correct, keep |
| Context Layer | Asymmetric — offset, not centered-container | See §3 — currently reads as "accidentally not centered" rather than deliberately placed; needs a real decision |
| Capability Map | Symmetric grid (3-column) | Deliberate break in density (HIERARCHY_SYSTEM.md §3) — grid symmetry here signals "a set," not "a sequence" |
| Final Frame | Symmetrical, centered | Resolution mirrors the open — bookend structure, matching Opening Frame's confidence |

This produces: **symmetric → asymmetric → asymmetric → symmetric(grid)
→ symmetric.** Not alternating for its own sake — each choice traces to
that frame's actual job (open, evidence, deepen, translate, resolve).

---

## 3. Context Layer — The One Real Change This Document Recommends

Current implementation: a centered container (`mx-auto max-w-5xl`)
wrapping left-aligned text (`max-w-[65ch]`). The critique flagged this as
reading like an unexamined default, not a decision. Per §2's rhythm,
this frame should be genuinely asymmetric: text block positioned toward
one side of the frame, with real negative space on the other — not a
centered box that happens to left-align its contents.

This is the only frame in the current five where the composition
recommendation changes anything already built. Every other row in §2's
table confirms what's already there.

---

## 4. Negative Space as Composition, Not Just Spacing

DESIGN_SYSTEM_TOKENS.md §3 defines the spacing *values*. This section
defines what the space is *for*: in an asymmetric frame (Proof of Craft,
Context Layer), the empty side of the composition isn't unused space —
it's what makes the occupied side read as placed rather than centered by
default. Removing it would collapse the asymmetry the frame depends on.

---

## 5. Focal Relationships — Opening Frame Specifically

Flagged in DESIGN_CRITIQUE_PHASE1.md §1: text and the (currently
placeholder) signature object are both independently centered, which is
coincidence, not composition. Once the real asset exists:

- The object and the headline should have an authored spatial
  relationship (behind/around/anchoring the text), not two independently
  centered elements that happen to overlap
- This decision is explicitly deferred, not solved here — the current
  placeholder cannot meaningfully inform it (DESIGN_CRITIQUE_PHASE1.md §1)
- When the real asset arrives, revisit this section specifically before
  finalizing Opening Frame's layout

---

## 6. What This Document Does Not Cover

- *Why* a frame gets more or less visual weight → HIERARCHY_SYSTEM.md
- *How* frames hand off to each other → TRANSITION_PHILOSOPHY.md
- Exact spacing scale values → DESIGN_SYSTEM_TOKENS.md

---

## Related Documents

- [[CORE_EXPERIENCE_STATEMENT]] — governs this document
- [[CREATIVE_DIRECTION_BOARD]] — this document extends its §9 (Composition Style)
- [[HIERARCHY_SYSTEM]] — companion document; this document's focal points
  come from that document's §5
- [[TRANSITION_PHILOSOPHY_CANONICAL]] — companion document covering
  frame-to-frame handoff, not within-frame placement
- [[DESIGN_SYSTEM_TOKENS]] — holds the exact spacing values this document
  applies compositionally
- [[DESIGN_SYSTEM]] — cites this document for spatial arrangement
- [[PROJECT_PAGE_SYSTEM]] — cites this document for gallery layout rules
