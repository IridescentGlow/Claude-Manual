# Solarisx Knowledge Base

Main navigation page for the Solarisx documentation vault. This is a
navigation aid, not a canonical document — authority and precedence are
defined by [[START_HERE]], not by this file's structure.

---

## Vision

- [[CORE_EXPERIENCE_STATEMENT]] — the emotional target every other design
  decision is checked against. Outranks every other canonical document on
  conflict.
- [[CREATIVE_DIRECTION_BOARD]] — the Direction A/C relationship,
  typography, color mood, artistic influences.
- [[PROFILE]] — who the creator (Dagim Demissie / Solarisx) is: identity,
  taste, collaboration preferences.

## Design System

- [[DESIGN_SYSTEM]] — high-level conceptual umbrella; points to the
  specialized documents below rather than duplicating them.
- [[DESIGN_SYSTEM_TOKENS]] — concrete color, type, spacing, and
  motion-timing values.
- [[HIERARCHY_SYSTEM]] — what deserves visual emphasis, expressed through
  contrast, not volume.
- [[COMPOSITION_PRINCIPLES]] — how elements are arranged spatially: eye
  movement, asymmetry, focal points.

## Engineering

- [[TECH_STACK]] — technical architecture and engineering standards.
  *Describes a Next.js/TypeScript stack — cross-check against the
  project's actual verified stack (React 19 + Vite 6, no TypeScript)
  before treating any specific tool choice here as current.*
- [[BUILD_WORKFLOW]] — the template-to-product transformation process and
  milestone roadmap.
- [[OPERATING_MANUAL]] — "The AI Studio Manual": the quality laws
  (ownership, transformation, systems thinking, design, engineering)
  every decision is checked against.

## Project Architecture

- [[PROJECT_PAGE_SYSTEM]] — the `/projects/:slug` depth layer: route
  architecture, case-study structure, media handling, per-page SEO.
- [[UX_ARCHITECTURE_BLUEPRINT]] — information architecture: frame
  sequence, site model, each frame's emotional job.

## Case Studies

- [[MEDIHELP_CASE_STUDY]] — content source for the `/projects/medihelp`
  page: verified project history, role, and outcome.

## Reading Order

See [[START_HERE]] for the authoritative reading order and precedence
graph — it, not this page, decides what's canonical.

## Visual Map

Two canvases exist, covering the vault from different angles — both
current, neither supersedes the other:

- [[SOLARISX_ARCHITECTURE.canvas|Architecture canvas]] — groups by
  Vision / Design / Engineering / Project System / Case Studies (includes
  [[UX_ARCHITECTURE_BLUEPRINT]] and [[COMPOSITION_PRINCIPLES]] under
  Project System)
- [[Solarisx_Project_Map.canvas|Project map canvas]] — groups by
  Vision / Design System / Engineering / Case Studies / Implementation
  Status (folds [[PROJECT_PAGE_SYSTEM]] into Design System; adds an
  Implementation Status branch tracking `PROJECT_STATUS.md` — not
  wikilinked, since that file lives at the portfolio repo root, outside
  this vault)

---

## Not Yet Linked Here

Three documents START_HERE.md lists as canonical aren't in the structure
above (following the requested MOC skeleton exactly rather than expanding
it unilaterally):

- `MASTER_PROMPT.md`
- `docs/vision/PROJECT_CONTEXT.md`
- `design/TRANSITION_PHILOSOPHY_CANONICAL.md`

Flagging rather than silently omitting — add them above if the MOC should
cover the full canonical set.
