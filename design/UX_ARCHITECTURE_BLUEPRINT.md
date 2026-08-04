# UX ARCHITECTURE BLUEPRINT
Solarisx Portfolio — Version 3.0 (retrofit)

Governed by CORE_EXPERIENCE_STATEMENT.md. Structural companion to
CREATIVE_DIRECTION_BOARD.md.

> Evidence begins the story. Context deepens the story. Conversion
> completes the story.

This is an information hierarchy based on visitor psychology, not a fixed
layout. Source evidence: COMPARATIVE_PORTFOLIO_ARCHITECTURE_STUDY.md.

---

## 1. Site Model

```
/ (single-page narrative)
├── Opening Frame      (Hero)
├── Proof of Craft      (Work index)
│     └── /work/[project-slug]   ← expandable depth layer
├── Context Layer       (About)
├── Capability Map      (Capabilities)
└── Final Frame         (Contact)
```

Single-page scroll = narrative. Case studies = optional depth layer — not
forced into the scroll, not split into a conventional multi-page site.

---

## 2. Frame Sequence

| # | Frame | Component | Emotional Job | Weight |
|---|---|---|---|---|
| 1 | Opening Frame | Hero | Curiosity + tone | Primary |
| 2 | Proof of Craft | Work | Confidence — competence experienced before explained | Primary (highest) |
| 3 | Context Layer | About | Trust, grounded in evidence already seen | Primary |
| 4 | Capability Map | Capabilities | Professional legibility | Secondary |
| 5 | Final Frame | Contact | Clarity — conclusion, not persuasion | Primary |

Changed from v1 (Hero→About→Capabilities→Work→Contact) —
reasoning in COMPARATIVE_PORTFOLIO_ARCHITECTURE_STUDY.md, not repeated here.

---

## 3. Frame Requirements

**01 — Opening Frame**
- Contains: identity, one-line positioning statement, visual atmosphere,
  immediate craftsmanship signal.
- Avoid: biography, resume-style intro, skill lists.

**02 — Proof of Craft**
- Contains: featured reel/showcase (highest visual priority), strongest
  projects, dual-view project data — scan view + `/work/[slug]` depth view
  (Challenge → Process → Execution → Result, LAW 33).
- Rule: evidence before claims.

**03 — Context Layer**
- Contains: creative background, philosophy, influences, working style.
- Framing: "behind the work," not a mandatory intro gate.
- Avoid: traditional bio-page structure.

**04 — Capability Map**
- Contains: 4 outcome-oriented capability areas (final, resolved Phase 3):
  Visual Storytelling · Motion Design & Visual Effects · Creative Technology ·
  Systems & Technical Exploration. Tools appear as supporting detail only.
- Order is meaningful: Visual Storytelling leads — it is the primary
  discipline (PROFILE.md §Current Development Direction). Systems &
  Technical Exploration sits last as supporting technical depth, not a
  co-equal professional identity. The governing identity is a visual
  storyteller / creative technologist who uses technology as a creative
  medium — not an engineer who also edits.
- Avoid: tool-rating lists (e.g., star ratings on software names).

**05 — Final Frame**
- Contains: contact method, social/professional links, working form (gap
  vs. original template, which had none).
- Framing: "continue the conversation," not "hire me now."

---

## 4. User Journey

```
OPENING FRAME → PROOF OF CRAFT → CONTEXT LAYER → CAPABILITY MAP → FINAL FRAME
```

Client / Employer / Collaborator (PROJECT_CONTEXT.md) travel this same
sequence, extracting different signal at each stage. No audience-specific
branching UI.

---

## 5. Navigation

- Menu order mirrors frame order: Home / Work / About / Capabilities /
  Contact.
- 5 destinations only.
- Minimal/hidden until requested — never competes with Opening Frame.
- Fully keyboard-operable, screen-reader coherent (gap in original
  template — unresolved).
- `/work/[slug]` pages: clear path back to Proof of Craft.
- Scroll-progress indication: recommended; visual treatment = Design
  System decision.

---

## 6. Interaction Philosophy

Every interaction serves exactly one purpose. None of the three →
decoration, cut it.

1. **Orientation** — nav transitions, section reveals, spatial relationships
2. **Storytelling** — project progression, timeline interactions, visual
   metaphors
3. **Revelation** — signature 3D experience, controlled interactive
   moments (Direction C lives here — CREATIVE_DIRECTION_BOARD.md §1)

---

## 7. Content Flow (placeholder structure only)

```
Opening Frame:    [identity] [positioning statement] [scroll cue]
Proof of Craft:   [intro] [featured reel] [project list: scan + /work/slug]
Context Layer:    [intro: "behind the work"] [narrative] [personal texture]
Capability Map:   [intro] [3–4 outcome areas, tools secondary]
Final Frame:      [intro] [contact method] [links] [form]
```

---

## 8. Open Questions

| # | Question | Status |
|---|---|---|
| 1 | Capability Map category names | Resolved (Phase 3) — final names recorded in §3 |
| 2 | Case study depth — how many projects get full treatment at launch | Open |
| 3 | Fate of template's ServiceSummary/ContactSummary sections | Open — test against §6 once real content exists |
