# DESIGN SYSTEM TOKENS
Solarisx Portfolio — Version 1.0

Translates CREATIVE_DIRECTION_BOARD.md into implementation-ready values.
Tailwind v4 (CSS-first `@theme`) target format. Cross-references only
where a rule is defined elsewhere — values below are net-new decisions.

---

## 1. Color Tokens

| Token | Value | Use |
|---|---|---|
| `--color-bg-base` | `#0B0A09` | Page background |
| `--color-surface-1` | `#141210` | Cards, panels, project rows |
| `--color-surface-2` | `#1D1A17` | Elevated panels, nav overlay |
| `--color-surface-3` | `#262220` | Hover/active elevated state |
| `--color-border` | `#332E29` | Dividers, input borders |
| `--color-text-primary` | `#FFFFFF` | Headlines only (per Board §8) |
| `--color-text-secondary` | `rgba(255,255,255,0.72)` | Body copy |
| `--color-text-tertiary` | `rgba(255,255,255,0.48)` | Metadata, captions |
| `--color-accent` | `#CFA355` | Single accent — sparing use only |
| `--color-accent-dim` | `#B8914B` | Accent hover/active state |
| `--color-accent-subtle` | `rgba(207,163,85,0.12)` | Accent-tinted backgrounds/borders |
| `--color-state-error` | `#C15B4A` | Form validation only |

Text hierarchy uses opacity on white, not separate hex grays — matches
Board §8's explicit rule. No success color: success feedback reuses
`--color-accent` to preserve the one-accent constraint.

```css
@theme {
  --color-bg-base: #0B0A09;
  --color-surface-1: #141210;
  --color-surface-2: #1D1A17;
  --color-surface-3: #262220;
  --color-border: #332E29;
  --color-text-primary: #FFFFFF;
  --color-text-secondary: rgba(255,255,255,0.72);
  --color-text-tertiary: rgba(255,255,255,0.48);
  --color-accent: #CFA355;
  --color-accent-dim: #B8914B;
  --color-accent-subtle: rgba(207,163,85,0.12);
  --color-state-error: #C15B4A;
}
```

---

## 2. Typography Scale

Amiamie only (Board §7). Weight mapping:

| Family variant | `font-weight` | File |
|---|---|---|
| Amiamie Light | 300 | Amiamie-Light |
| Amiamie Regular | 400 | Amiamie-Regular |
| Amiamie Black | 900 | Amiamie-Black |
| Round / Italic variants | — | Reserved, not in default scale (Board §7) |

Action item: convert `.otf`/`.ttf` source files to `.woff2` before
implementation — required for load performance, not currently in the
template's asset set.

| Token | Size | Weight | Line-height | Tracking | Use |
|---|---|---|---|---|---|
| `--text-display` | `clamp(3.5rem, 8vw, 8rem)` | 900 | 0.95 | -0.02em | Opening Frame headline |
| `--text-h1` | `clamp(2.25rem, 5vw, 4rem)` | 900 | 1.05 | -0.01em | Frame titles |
| `--text-h2` | `clamp(1.75rem, 3vw, 2.5rem)` | 400 | 1.1 | 0 | Sub-headings |
| `--text-h3` | `clamp(1.25rem, 2vw, 1.5rem)` | 400 | 1.2 | 0 | Project titles |
| `--text-body-lg` | `1.125rem` | 300 | 1.6 | 0 | Case-study long-form |
| `--text-body` | `1rem` | 300 | 1.6 | 0 | Default body |
| `--text-body-sm` | `0.875rem` | 300 | 1.5 | 0 | Secondary copy |
| `--text-label` | `0.75rem` | 300 | 1.4 | 0.12em, uppercase | Nav, metadata, tags |
| `--text-caption` | `0.6875rem` | 300 | 1.4 | 0.08em, uppercase | Timestamps, fine print |

`--content-max-width: 65ch` — body-copy reading width (Context Layer,
case studies). Frames themselves stay full-bleed; text blocks within them
don't.

---

## 3. Spacing Scale

Base unit 4px. Semantic aliases map to raw scale — use aliases in
components, not raw values.

| Raw token | Value | Semantic alias | Use |
|---|---|---|---|
| `--space-1` | `0.25rem` | `--space-micro` | Icon-to-text, tight grouping |
| `--space-2` | `0.5rem` | | |
| `--space-3` | `0.75rem` | | |
| `--space-4` | `1rem` | `--space-component-sm` | Button padding, small gaps |
| `--space-6` | `1.5rem` | `--space-component` | Card padding, form field gaps |
| `--space-8` | `2rem` | | |
| `--space-12` | `3rem` | `--space-component-lg` | Sub-section grouping |
| `--space-16` | `4rem` | | |
| `--space-24` | `6rem` | `--space-section-sm` | Related content blocks |
| `--space-32` | `8rem` | | |
| `--space-48` | `12rem` | `--space-section` | Between-frame spacing (desktop) |
| `--space-64` | `16rem` | `--space-section-lg` | Major frame breaks (desktop) |

Mobile: halve `--space-section` and `--space-section-lg` at the
`sm` breakpoint — generous pacing degrades to comfortable, not identical.

---

## 4. Motion Timing & Easing

Durations per Board §6. Easing curves are a new decision: **two distinct
curve families, one default, one exception-only** — this is the literal
implementation of the Board §1 governing-relationship rule.

| Token | Value | Character | Use |
|---|---|---|---|
| `--ease-precise` | `cubic-bezier(0.4, 0, 0.2, 1)` | Snappy, instrument-like | Micro-interactions (default) |
| `--ease-cinematic` | `cubic-bezier(0.16, 1, 0.3, 1)` | Weighted deceleration | Reveals, establishing shots (default) |
| `--ease-connective` | `cubic-bezier(0.65, 0, 0.35, 1)` | Smooth in-out | Frame-to-frame transitions (default) |
| `--ease-revelation` | `cubic-bezier(0.34, 1.56, 0.64, 1)` | Slight overshoot/spring | **Direction C exception moments only** — never used outside UX_ARCHITECTURE_BLUEPRINT.md §6 "Revelation" category |

| Token | Value | Use |
|---|---|---|
| `--duration-micro` | `150ms` | Hover, focus, button states |
| `--duration-transition` | `350ms` | Frame-to-frame, component transitions |
| `--duration-reveal` | `800ms` | Section/scroll reveals |
| `--duration-revelation` | `1200ms` | Revelation-category moments only |

`--ease-revelation` and `--duration-revelation` existing as *separate,
named tokens* is intentional: it makes the "scarce exception" rule
enforceable at the code level, not just a documentation convention — using
either token outside a Revelation-category interaction is a code-review
flag, not a style choice.

---

## 5. Surface & Elevation

| Token | Value | Use |
|---|---|---|
| `--shadow-sm` | `0 1px 2px rgba(0,0,0,0.4)` | Resting cards |
| `--shadow-md` | `0 4px 16px rgba(0,0,0,0.5)` | Hover-elevated cards, nav overlay |
| `--shadow-lg` | `0 16px 48px rgba(0,0,0,0.6)` | Modals, floating preview image (Proof of Craft hover) |
| `--radius-sm` | `4px` | Inputs, tags, focus ring |
| `--radius-md` | `8px` | Buttons, cards |
| `--radius-lg` | `16px` | Large panels, project preview images |

No `--radius-full` defined — pill shapes not used anywhere in the current
frame requirements; add only if a specific component needs it.

---

## 6. Component Token Implications

| Component | Token Usage | Rule |
|---|---|---|
| **Button — primary** | `surface-1` bg, 1px `border`, `text-primary`; hover → `accent-subtle` bg, `border-accent`, `duration-micro` / `ease-precise` | Filled solid `accent` reserved for the single highest-priority action per frame (e.g., Final Frame submit) — keeps accent "sparing," per Board §8 |
| **Button — secondary/ghost** | `text-secondary`, underline-on-hover only, no border, no bg | No competing visual weight with primary |
| **Nav — links** | `text-secondary` default, `text-primary` active/current, `accent` underline on active | Matches Blueprint §5's active-state requirement |
| **Project list-row** | `border-b: border` token; hover reveals floating preview image as primary feedback — text stays `text-primary`, no color shift | Avoids double-signaling hover (image *is* the feedback) |
| **Card / Panel** (Context Layer, Capability Map) | `surface-1` bg, `radius-md`, `shadow-sm`; hover (if interactive) → `surface-2`, `shadow-md` | |
| **Form input** (Final Frame) | `surface-1` bg, `border` default, `border-accent` on focus, `state-error` border+text on validation fail | Never remove focus outline without this replacement — LAW 21 requirement |
| **Focus ring** (all interactive elements) | `2px solid accent`, `2px` offset, `radius-sm` | Mandatory, not optional — accessibility gap flagged in original template audit |
| **Signature 3D element** | Uses `--ease-revelation` / `--duration-revelation` for hover response | The one component where these tokens are expected to appear by default |

---

## 7. Open Before Implementation

- Exact accent value (`#CFA355`) still template-inherited, not
  independently validated against the new dark-token background for
  contrast — verify AA contrast ratio once applied to real text use, not
  just decorative use.
- `--text-display` clamp values are a first pass — needs testing against
  actual positioning-statement copy length once Phase 3 content exists.
