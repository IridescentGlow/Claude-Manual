# CREATIVE DIRECTION BOARD
Solarisx Portfolio — Version 3.0 (retrofit)

Governed by CORE_EXPERIENCE_STATEMENT.md. Feeds Design System token
implementation.

---

## 1. Governing Relationship

> Direction A is the governing law of the portfolio. Direction C is a
> deliberately scarce exception that requires justification each time it
> is used.

- Default state (Direction A): restrained, premium, cinematic, deliberate,
  confident.
- Direction C permitted only at:
  - Opening Frame introduction
  - Signature typography moments
  - Major project/case-study transitions
  - 1–2 controlled interactive sequences (signature 3D element lives here)
- Test for any proposed exception: UX_ARCHITECTURE_BLUEPRINT.md §6
  (Orientation / Storytelling / Revelation). Fits none → decoration, cut it.
- Per Core Experience Statement: exceptions read as revealed depth, never
  as a break in composure.

---

## 2. Visual Identity

**"A cinematic control room, not a gallery wall."**

- Motion carries meaning like a cut carries meaning.
- Interface behaves as a directed sequence, not independent sections.
- One focal moment at a time.
- Not: dev portfolio with animations added on top. Not: showreel site +
  generic dev-boilerplate. Not: maximalist/experimental for its own sake.

---

## 3. Artistic Influences

| Category | What We Take |
|---|---|
| Film title sequences & trailers | Typography that moves with intention; reveals timed like cuts |
| Color grading workflow logic | Controlled palette; mood from restraint, not variety |
| High-end cinematic studio sites (Awwwards category) | Scroll-as-narrative, pinned staging, confident whitespace |
| Editing-timeline UI (Premiere/Resolve/AE) | Precise alignment, functional typography |
| Modern product-launch sites | One idea per screen; pacing discipline |

---

## 4. Storytelling Approach

> Evidence begins the story. Context deepens the story. Conversion
> completes the story.

- Full frame sequence + reasoning: UX_ARCHITECTURE_BLUEPRINT.md §2.
- Source evidence: COMPARATIVE_PORTFOLIO_ARCHITECTURE_STUDY.md.

---

## 5. Interaction Philosophy

- Full rule: UX_ARCHITECTURE_BLUEPRINT.md §6 (three-purpose test).
- Micro-interactions: fast, precise, instrument-like — never bouncy/
  playful by default.

---

## 6. Animation Philosophy

- Pacing over speed — cuts land when the eye is ready, not on a fixed clock.
- Lead/trail transitions — next frame enters slightly before previous
  exits (J-cut/L-cut logic).
- Establishing shot before detail — wide/context before narrow, every frame.
- Motion has a grade, not just a duration — easing chosen for emotional
  character, not defaulted.

| Moment type | Timing |
|---|---|
| Opening Frame / major reveals / Revelation moments | 600ms+ |
| Frame-to-frame transitions | 250–500ms |
| Micro-interactions | 100–200ms |

---

## 7. Typography

- Primary typeface: **Amiamie**. License verified — OIFL/SIL OFL 1.1,
  commercial use clear. No swap needed.
- Why: geometric Helvetica-lineage; Light→Black + italics + Round variant
  covers full hierarchy without a second family; humanist warmth avoids
  reading as purely technical.
- Display/Opening Frame: Black or Regular, tight tracking, large scale.
- Body: Light weight.
- Labels/metadata: Light weight, wide tracking, uppercase.
- Italic/Round variants: reserved for justified moments only.

---

## 8. Color Mood

- Primary environment: **Dark Premium Theme** — "grading suite, not
  gallery wall."
- Background: deep, layered near-black — never flat `#000000`.
- Surface elevation: subtle lightness steps for depth.
- One accent color only — warm gold (`#cfa355`-adjacent, template's
  existing value) is the leading candidate.
- Text hierarchy: true white reserved for primary headlines; secondary/
  body text drops in brightness, not a separate gray.
- Avoid: neon/cyberpunk accents, multiple competing accents, gradients as
  personality.

---

## 9. Composition Style

- Full-bleed, cinematic framing — frames, not cards.
- Asymmetry only with a reason (attention-directing, not decorative).
- Generous whitespace as a pacing tool — a beat of silence between cuts.
- Project list-row format (not card grids) — preserved from template.

---

## 10. References

**Inspires:** cinematic agency/studio scroll-narrative sites · professional
creative-tool interfaces (grading panels, timeline editors) · motion-
graphics/title-sequence design · minimal typography-forward product sites.

**Avoid:** generic 3D-hero + glassmorphism + gradient-blob template
aesthetic · crypto/Web3 neon dark themes · SaaS marketing-site patterns
(feature grids, testimonial carousels) · corporate-agency "artificial
professionalism."

---

## 11. Feeds Design System

Design System translates, does not reinterpret:

| Board section | Becomes |
|---|---|
| §8 Color Mood | Token values |
| §7 Typography | Type scale |
| §6 Animation timing | Duration/easing tokens |
| §9 Composition | Spacing scale + grid |

Any proposed token must trace back to a rule above.
