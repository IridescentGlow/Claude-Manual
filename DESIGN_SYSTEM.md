# DESIGN_SYSTEM.md
Solarisx Portfolio — High-Level Design Overview

Version: 2.0 — Conceptual umbrella. Explains the *why*; the specialized
documents listed in §4 define the *what*. If this document and a
specialized document ever conflict, the specialized document is
authoritative for its domain (see START_HERE.md for precedence).

Governed by CORE_EXPERIENCE_STATEMENT.md.

---

## 1. Design Identity

The portfolio represents: **Creative Vision + Technical Precision +
Modern Digital Craftsmanship.** The full articulation of what this means
in practice — "a cinematic control room, not a gallery wall" — lives in
CREATIVE_DIRECTION_BOARD.md §2. This section states the identity; that
document governs its execution.

---

## 2. Core Design Principles

- **Intention over decoration** — every element must justify its
  existence (LAW 4)
- **Story over information** — the site is a directed sequence, not a
  stack of independent sections (governing principle, UX_ARCHITECTURE_BLUEPRINT.md)
- **Quality over quantity** — fewer, stronger decisions over many average ones
- **Hierarchy through contrast, not volume** — the strongest content
  doesn't get louder, everything around it gets quieter (HIERARCHY_SYSTEM.md §1)

These four principles are the test every specialized document's rules
were derived from. If a future decision seems to satisfy a specialized
document's letter but violates one of these, the principle wins.

---

## 3. Brand Feeling

The visitor should feel: **Curiosity → Confidence → Memorability →
Trust.** This is the short version. The definitive, felt articulation of
what the experience should leave someone with is
CORE_EXPERIENCE_STATEMENT.md — that document, not this one, is the
emotional source of truth.

---

## 4. System Map — Where To Find What

| Question | Document |
|---|---|
| What should this experience make someone feel? | CORE_EXPERIENCE_STATEMENT.md |
| What's the creative direction — Direction A/C relationship, typography, color mood, artistic influences? | CREATIVE_DIRECTION_BOARD.md |
| How are frames sequenced, what's the site structure, what's each frame's job? | UX_ARCHITECTURE_BLUEPRINT.md |
| What are the exact color / type / spacing / motion values? | DESIGN_SYSTEM_TOKENS.md |
| What deserves visual emphasis, and how is that expressed without making things louder? | HIERARCHY_SYSTEM.md |
| How are elements arranged spatially within a frame — eye movement, asymmetry, focal points? | COMPOSITION_PRINCIPLES.md |
| How does one frame hand off to the next? | TRANSITION_PHILOSOPHY.md |

This table is the practical reason this document exists: a fast answer
to "which document do I open" before going and reading five files to
find out.

---

## 5. Design Review Standard

Before considering any frame or component finished, it should pass:

- **Purpose** — does every element earn its place, or is something here
  only because it was easy to add?
- **Hierarchy** — is it clear what matters most, using HIERARCHY_SYSTEM.md's
  contrast test, not size/color escalation?
- **Consistency** — does it match the token values in DESIGN_SYSTEM_TOKENS.md,
  or has a one-off value crept in?
- **Restraint** — could anything be removed without losing meaning?
- **Identity** — would a visitor who's seen other sections recognize this
  as belonging to the same experience?

This is a process, not a new set of rules — the standards it checks
against all live in the specialized documents above.

---

## 6. Document Status

This document is canonical, but scoped: conceptual framing and
cross-referencing only. Anything that reads like an implementation
detail (a hex value, a duration, a specific spacing number) belongs in a
specialized document, not here — if you find one in this file, it should
be moved, not trusted as current.
