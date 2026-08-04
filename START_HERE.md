# START_HERE.md
Solarisx AI Creative System — Canonical Index

Version: 2.0

---

## WHAT THIS FILE IS

This is the authoritative map of the project's current design bible.

**Only documents referenced in §1 below are canonical.** Everything else
— including historical research documents and anything in `_unknown_docs/`
— has zero implementation authority unless explicitly promoted here.

This file is not a historical snapshot. It evolves as the project
evolves — update it when a document's role changes, not just when a new
one is added.

---

## 1. CANONICAL DOCUMENTS — READING ORDER

### Foundation — who, what, and how this project operates

| # | Document | Answers |
|---|---|---|
| 1 | `MASTER_PROMPT.md` | How the AI creative/technical partner should think and operate |
| 2 | `OPERATING_MANUAL.md` | The quality laws and standards every decision is checked against |
| 3 | `PROFILE.md` | Who the creator is — identity, goals, taste, collaboration preferences |
| 4 | `PROJECT_CONTEXT.md` | The portfolio's mission, audience, and success criteria |

### Experience — what this should make someone feel

| # | Document | Answers |
|---|---|---|
| 5 | `CORE_EXPERIENCE_STATEMENT.md` | The emotional target every other design decision serves. **Outranks every other design document on conflict.** |

### Design System — the conceptual overview and its specialized references

| # | Document | Answers |
|---|---|---|
| 6 | `DESIGN_SYSTEM.md` | High-level design overview — conceptual umbrella, points to the specialized documents below rather than duplicating them |
| 7 | `CREATIVE_DIRECTION_BOARD.md` | Creative principles and governing laws — the Direction A/C relationship, typography, color mood, artistic influences |
| 8 | `UX_ARCHITECTURE_BLUEPRINT.md` | Information architecture — frame sequence, site model, each frame's job |
| 9 | `DESIGN_SYSTEM_TOKENS.md` | Concrete implementation values — color, type scale, spacing, motion timing/easing |
| 10 | `HIERARCHY_SYSTEM.md` | What deserves visual emphasis, and how that's expressed through contrast, not volume |
| 11 | `COMPOSITION_PRINCIPLES.md` | How elements are arranged spatially — eye movement, asymmetry, focal points |
| 12 | `TRANSITION_PHILOSOPHY_CANONICAL.md` | How one frame hands off to the next. *(Filename reflects an unresolved naming collision with a document of unknown provenance — see §3. This is the authoritative version regardless of filename.)* |

### Engineering — how this gets built

| # | Document | Answers |
|---|---|---|
| 13 | `TECH_STACK.md` | Technologies, architecture, coding standards |
| 14 | `BUILD_WORKFLOW.md` | Execution phases, review process, delivery workflow |

---

## 2. PRECEDENCE

```
CORE_EXPERIENCE_STATEMENT.md
        ↓ governs
DESIGN_SYSTEM.md (conceptual umbrella)
        ↓ specialized by
CREATIVE_DIRECTION_BOARD.md · UX_ARCHITECTURE_BLUEPRINT.md ·
DESIGN_SYSTEM_TOKENS.md · HIERARCHY_SYSTEM.md ·
COMPOSITION_PRINCIPLES.md · TRANSITION_PHILOSOPHY_CANONICAL.md
```

If `DESIGN_SYSTEM.md` and a specialized document ever disagree, the
specialized document wins for its specific domain — it exists precisely
to be more detailed and more current than the overview.

---

## 3. NON-CANONICAL — REFERENCE / HISTORICAL

Valuable for understanding *why* a canonical decision was made. Not
authoritative — do not implement from these directly.

| Document | Role |
|---|---|
| `CREATIVE_DIRECTIONS_EXPLORATION.md` | The five candidate directions evaluated before Direction A/C was selected |
| `COMPARATIVE_PORTFOLIO_ARCHITECTURE_STUDY.md` | The research behind the evidence-first frame ordering in UX_ARCHITECTURE_BLUEPRINT.md |
| `DESIGN_CRITIQUE_PHASE1.md` | The implementation critique that HIERARCHY_SYSTEM.md, COMPOSITION_PRINCIPLES.md, and TRANSITION_PHILOSOPHY_CANONICAL.md were written to resolve |

---

## 4. UNKNOWN — ZERO AUTHORITY

Origin undetermined. Do not implement from these. Do not delete. Do not
spend further time investigating unless a dedicated maintenance task is
opened for it.

- `_unknown_docs/DESIGN_TOKENS.md`
- `_unknown_docs/TRANSITION_PHILOSOPHY.md`
- `TRANSITION_PHILOSOPHY_DRAFT.md`
- `TRANSITION_PHILOSOPHY_V2.md`

---

## 5. OPERATING INSTRUCTIONS

Before making a design or implementation decision:

1. Check §4's System Map (inside `DESIGN_SYSTEM.md`) for which document
   governs the question at hand.
2. Follow that document's rules.
3. If no canonical document covers it, that's a genuine gap — flag it
   before deciding unilaterally, per PROFILE.md's collaboration
   preferences.

**Documentation is considered complete as of this version.** New design
documents are not created speculatively — only when implementation
exposes a real, specific gap that no existing canonical document covers.

---

## SYSTEM STATUS

```
Canonical structure: established.
Priority: implementation and refinement of the five built frames.
```
