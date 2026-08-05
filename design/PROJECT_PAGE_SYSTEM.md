# PROJECT PAGE SYSTEM
Solarisx Portfolio — Version 1.0

Governed by CORE_EXPERIENCE_STATEMENT.md. Extends
UX_ARCHITECTURE_BLUEPRINT.md §1/§3 (Proof of Craft owns the index; this
document owns the depth layer behind it). Case-study narrative structure
comes from OPERATING_MANUAL.md LAW 33 and is not restated here.

> The index proves competence. The project page proves thinking.

---

## 1. Purpose

Proof of Craft is a scan surface — a visitor reads it in seconds and leaves
with an impression. The project page is where that impression is earned in
detail: what the work was, what was decided, and what it became.

- **Primary job:** show the craft itself. Visual storytelling leads —
  the reel, the frames, the motion. Engineering is shown as what made the
  craft possible, never as the headline (per the governing identity in
  UX_ARCHITECTURE_BLUEPRINT.md §3).
- **Not:** a README, a spec sheet, or a tech-stack showcase.
- **Restraint:** a project page is optional depth. A project with nothing
  substantive to add should stay index-only rather than pad a page out.

---

## 2. Route Architecture

| Decision | Value |
|---|---|
| Route pattern | `/projects/:slug` |
| Index route | `/` — the single-page narrative, unchanged |
| Link behaviour from Works | Opens in a **new browser tab** |
| Superseded pattern | `/work/[slug]` — replaced; see §11 |

The single-page narrative remains the product. Project pages are a
side layer reached from it, never a step inside the scroll.

**New-tab rule.** Clicking a project in Works opens `/projects/:slug` in a
new tab. This is a deliberate exception to the usual convention that
internal links stay in the same tab: the scroll narrative is a paced
sequence, and returning to a lost scroll position mid-story breaks the
edit. The visitor's place in the story is preserved by never leaving it.

**Consequence:** because the origin tab is never lost, a project page does
not need a "back to work" control as its primary affordance. It may still
carry a link home for visitors who arrive directly (search, shared link).

**Implementation note — new dependency.** The project currently has no
router. Client-side routing requires adding one (`react-router-dom` is the
conventional choice for this stack). Per TECH_STACK.md's dependency rule
this must be justified before install: it is, because the alternative —
hand-rolled history handling — is more code for less correctness. The
addition is an implementation decision, not a design one, and is recorded
here only so it is not discovered late.

---

## 3. Project Data Model Changes

The existing `projects` array in `src/constants/index.js` stays the source
of truth for the index. Depth content is **additive** — no existing field
changes name, type, or meaning.

**Added to each project:**

| Field | Type | Purpose |
|---|---|---|
| `slug` | string | URL segment. Lowercase, hyphenated, stable — it is a permalink, so it must not change once shared |
| `caseStudy` | object \| `null` | Depth content. `null` (or absent) means index-only: the row renders as it does today and links externally instead |

**Existing fields, unchanged in meaning:** `id`, `name`, `outcome`, `role`,
`year`, `stack`, `liveHref`, `repoHref`, `image`, `bgImage`, `featured`.

**Behavioural change to existing fields:** `liveHref` and `repoHref` stop
being the row's primary destination and become external links presented
*inside* the project page. A row with a `caseStudy` links to
`/projects/:slug`; a row without one keeps its current external behaviour.

**Where content is missing:** use explicit `TODO:` placeholders, the same
convention already used in `constants/index.js`. A page must never invent
a metric, client, outcome, or award to fill a section — an absent section
is omitted, not fabricated.

---

## 4. Project Content Structure

`caseStudy` sections follow LAW 33's narrative, reduced to what a
visual-craft portfolio actually needs. **Every section is optional.** Only
Overview and at least one media block are required for a page to exist.

| Section | Answers | Notes |
|---|---|---|
| Overview | What is it, what was my role, what was the goal | Always present |
| Challenge | What problem or brief started it | |
| Approach | How it was decided — references, direction, iteration | The thinking; the section that separates proof from screenshots |
| Craft | What was actually made — cuts, motion, systems, interfaces | The visual centrepiece |
| Result | What it became, where it ran, what came of it | Omit entirely rather than assert an unmeasured outcome |
| Credits | Collaborators, team, roles | Required whenever the work was not solo |
| Links | Live, repo, external profile | Terminal position — links leave; they do not lead |

Ordering is fixed. A visitor comparing two project pages should recognise
the same sequence, per LAW 3's consistency rule.

---

## 5. Reusable Components

Reuse before building. The page is assembled from what exists.

| Need | Use | Status |
|---|---|---|
| Section heading + intro copy | `AnimatedHeaderSection` | Exists |
| Staggered paragraph reveal | `AnimatedTextLines` | Exists |
| Motion curves and durations | `src/lib/motion.js` (`EASE`, `DURATION`) | Exists |
| Design tokens | `@theme` block in `src/index.css` | Exists |
| Video/still preview switching | Extension-based selection, as implemented in `Works.jsx` | Exists — extract to a shared component when the second consumer appears, not before (LAW 3's exception rule) |
| Project page shell | New — layout, sections, links | To build |
| Media gallery | New | To build |

New components are created only where the table says so. Anything that
appears once stays inline until repetition justifies abstraction.

---

## 6. Media Handling

Media is the substance of these pages, not decoration.

**Video (primary medium)**
- `autoplay`, `muted`, `loop`, `playsInline`, no `controls` — matching the
  behaviour already established in the Works preview.
- Silent by default. A visitor must never be startled by audio. If a piece
  genuinely requires sound, it is an explicit opt-in control, never autoplay.
- `poster` frame required for anything above the fold, so the page has a
  composed first frame rather than a blank rectangle while loading.
- `preload="metadata"` — never `auto`. A project page may hold several
  clips; they must not all fetch in full on load.

**Stills**
- Used where a frame reads better held than moving, and as poster sources.

**Galleries**
- A sequence of stills or clips presented as a set. Layout follows
  COMPOSITION_PRINCIPLES.md; the gallery is a composition, not a grid dump.
- No lightbox, carousel, or zoom UI unless a specific piece needs it —
  those are interaction patterns that must pass
  UX_ARCHITECTURE_BLUEPRINT.md §6's three-purpose test first.

**Weight — a hard constraint.** Source clips currently in the repository
run to 21 MB. Pages carrying several such files are not shippable.
Every clip must be compressed for web delivery before it lands on a page,
and long pieces should link out to a hosted player rather than self-host.
This is a launch blocker, not a nicety.

**Future media.** Stills, clips, and galleries cover current needs. New
media types (audio, embeds, interactive demos) are added here first, with
the same test applied: does it show craft, or does it decorate?

---

## 7. Animation and Transition Rules

TRANSITION_PHILOSOPHY_CANONICAL.md governs motion inside the page. This
section covers only what is specific to project pages.

- **Route change is not a transition.** The page opens in a new tab, so
  there is no outgoing frame to hand off from. Nothing is inherited
  across the tab boundary and no route-transition animation is authored —
  §1's "a transition is an edit" has no edit to make here.
- **Within the page**, section reveals use the existing shared components
  and therefore the existing curves and durations. No new easing curve is
  introduced; the four canonical curves are the whole vocabulary.
- **`ease-revelation` stays out.** A project page is evidence, not a
  Revelation moment (CREATIVE_DIRECTION_BOARD.md §1).
- **Media does not animate on entry.** A clip playing is already motion;
  layering a reveal on top of it is decoration.
- **Reduced motion** is inherited from the global rule in
  `src/lib/motion.js`. Nothing project-page-specific is invented.
  Autoplaying clips are the one open question — see §10.

---

## 8. Responsive Behavior

Per COMPOSITION_PRINCIPLES.md, mobile is a different composition, not a
narrower desktop.

| Breakpoint | Behaviour |
|---|---|
| Mobile | Single column. Media full-bleed to the page gutter. Metadata (role, year, stack) stacks beneath the title rather than sitting opposite it |
| Tablet | Single column, wider gutters, media may inset |
| Desktop | Text blocks respect `--content-max-width` (65ch); media may exceed it and go full-bleed |

Long-form body copy uses `--text-body-lg`, which
DESIGN_SYSTEM_TOKENS.md §2 already designates for case-study reading.

Mobile carries the tightest media budget. Where a page holds several
clips, mobile should favour posters that play on interaction over several
simultaneous autoplaying videos.

---

## 9. SEO and Meta Requirements

Each project page needs its own title, description, and share image —
a shared link should preview the project, not the site index.

| Tag | Value |
|---|---|
| `<title>` | `{project name} — Dagim Demissie` |
| `description` | The project's `outcome` line |
| `og:title` / `twitter:title` | Same as `<title>` |
| `og:description` / `twitter:description` | Same as `description` |
| `og:image` / `twitter:image` | Project poster still, 1200×630 |
| `og:url` | Canonical `/projects/:slug` |
| `og:type` | `article` |

**Known constraint — must be solved before this ships.** The site is a
Vite SPA with one static `index.html`. Tags injected at runtime are not
present in the served HTML, so social scrapers and many crawlers will see
the index metadata for every project page. Per-route metadata therefore
requires one of: pre-rendering the project routes at build time, static
generation per project, or server-side rendering. Choosing between these
is an engineering decision and is deliberately left open here — but
shipping project pages without resolving it means link previews are
silently wrong, so it cannot be skipped.

---

## 10. Adding a Future Project

1. Add the project to `projects` in `src/constants/index.js` with a stable
   `slug`.
2. Add `caseStudy` content following §4's section order. Omit sections
   with nothing true to say; use `TODO:` placeholders for content that is
   coming but not yet written.
3. Place media under `public/assets/projects/`, compressed for web (§6).
   Add a `poster` still for every clip.
4. Confirm the row still reads correctly in the Works index — the index
   entry is not generated from the case study and must be checked
   independently.
5. Confirm the page's meta values resolve (§9).

No route registration step: routes derive from `slug`. Adding a project is
a content change, not a code change.

---

## 11. Supersedes

This document replaces the `/work/[slug]` route pattern previously
recorded in UX_ARCHITECTURE_BLUEPRINT.md §1, §3, §5 and §7. Those
references have been updated to `/projects/:slug`. No other canonical
document referenced the route.

The blueprint's §8 open question — how many projects get full case-study
treatment at launch — remains open and is not resolved here.

---

## 12. What This Document Does Not Cover

- *Why* Proof of Craft holds the weight it does → HIERARCHY_SYSTEM.md
- *Where* elements sit within a frame → COMPOSITION_PRINCIPLES.md
- *How* frames hand off in the single-page narrative → TRANSITION_PHILOSOPHY_CANONICAL.md
- Exact colour / type / spacing / motion values → DESIGN_SYSTEM_TOKENS.md
- Case-study narrative theory → OPERATING_MANUAL.md LAW 33
