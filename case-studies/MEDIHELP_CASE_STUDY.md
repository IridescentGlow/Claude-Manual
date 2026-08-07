---
title: "MediHelp Case Study"
type: case-study
status: content-only
related:
  - "[[PROJECT_PAGE_SYSTEM]]"
  - "[[DESIGN_SYSTEM]]"
  - "[[TECH_STACK]]"
---

# MEDIHELP_CASE_STUDY.md
Solarisx Portfolio — Content Source, Version 1.2

Governed by `docs/design/PROJECT_PAGE_SYSTEM.md` §4 (section structure and
ordering) and §1's restraint principle (a section with nothing verified to
say is marked as missing, not padded). This document is the single source
of truth for the `/projects/medihelp` page's case-study content —
`ProjectPage.jsx` should draw from here once implementation resumes, not
the reverse.

**Status: content only. No UI implementation has been performed from this
document.** Sections marked `NEEDS USER INPUT` are genuine gaps, not
oversights — do not fill them without new verified information.

---

# MediHelp Case Study

## 1. Project Overview

MediHelp is a full-stack healthcare assistant combining AI-powered symptom
checking, first aid guidance, and educational content, aimed at
communities that are medically underserved.

It was built for a full-stack engineering university hackathon by a team
of full-stack developers.

*Source: [github.com/ellay21/Medihelp-Frontend](https://github.com/ellay21/Medihelp-Frontend)
(product description); `src/constants/index.js` (audience framing, already
verified in the current codebase).*

---

## 2. The Problem

MediHelp was created during a full-stack engineering hackathon, driven by
a shared goal to build a meaningful healthcare solution.

The motivating problem: many communities in Ethiopia face difficulty
accessing timely healthcare guidance. MediHelp's AI-powered symptom
checking, first aid guidance, and educational content were built to give
people a faster, more accessible starting point for basic health
questions.

**Target users:** people in Ethiopia with limited access to healthcare
services, or anyone needing quick health-related guidance.

*Source: verified information provided directly by the project's creator.*

---

## 3. Research / Discovery

MediHelp was built during a 2-day hackathon, which shaped the scope of
research that was possible.

No formal user surveys or interviews were conducted. Discovery was
informal and time-boxed to the hackathon window:

- The team researched the healthcare problem space directly.
- The team discussed ideas and direction with hackathon mentors.

*Source: verified information provided directly by the project's creator.*

---

## 4. Design Process

**Design goal:** create a simple, accessible healthcare experience —
prioritizing clarity and ease of use for people who may be unfamiliar
with a digital health tool.

The team deliberately avoided unnecessary complexity in the interface,
since the intended users needed the product to be immediately usable.

**Confirmed contributions to the visual direction:**
- Chose the visual style
- Created animations
- Created illustrations
- Created graphics

No formal wireframing or Figma-based design process was used — design
decisions were made directly during a fast, hackathon-paced build.

*Source: verified information provided directly by the project's creator.*

---

## 5. Development

**Confirmed contribution:** front-end development, as one of five
front-end developers on the team.

**Frontend work built:**
- Hero section, including the hero video experience
- Additional website sections
- Site-wide animations
- Contact section
- Blog listings
- Team section

**Technical involvement:**
- AI integration
- Authentication
- API communication

**Team structure:** 5 front-end developers, 5 back-end developers.

**Workflow:** the team collaborated in person, used Git for version
control, and coordinated over Telegram.

**Confirmed technologies** (from `src/constants/index.js`, already
verified in the current codebase, not sourced fresh for this document):

- Backend: Django 5.2, Django REST Framework 3.16, PostgreSQL, JWT
- Frontend: React, Tailwind CSS, Sentry, Web Vitals
- AI: Google Gemini API
- Docs: OpenAPI 3 via drf-spectacular

**Architecture** (deployment topology, data flow, and how the frontend's
AI/authentication/API involvement was implemented under the hood) is not
documented beyond what's confirmed above.

**NEEDS USER INPUT** — architecture details beyond the confirmed
technology list and confirmed areas of technical involvement; specific
technical decisions or trade-offs made.

*Source: verified information provided directly by the project's creator;
technology list from `src/constants/index.js`.*

---

## 6. My Role

**Role:** Front-End Developer + Motion Designer

**Engineering:**
- One of five front-end developers on the team
- Built the Hero section, including the hero video experience
- Built the Contact section
- Built the Blog listings
- Built the Team section
- Contributed animations across the site

**Creative:**
- Head of video editing
- Created graphics design independently
- Created project videos and visual assets

*Source: verified information provided directly by the project's creator.*

---

## 7. Challenges

**Technical challenges:**
- Integrating AI into the product within the hackathon timeframe
- Implementing authentication
- Working within a strict hackathon deadline

**Creative challenge:** communicating the importance of healthcare
accessibility in a way that felt approachable rather than clinical.

*Source: verified information provided directly by the project's creator.*

---

## 8. Award Section

MediHelp won **first place** at the hackathon it was built for.

- Certificates were awarded
- A cash prize was received
- MediHelp was named the best solution of the hackathon

This confirms the "Award Winning Solution" title already used in
`src/constants/index.js` is accurate, not marketing language.

---

## 9. Final Outcome

**Confirmed delivered:**
- A complete, working full-stack healthcare platform.
- An AI-powered healthcare assistant, combining symptom checking, first
  aid guidance, and educational content.
- First place at the hackathon, with certificates and a cash prize
  awarded (see §8).

**Not available:** usage figures, adoption numbers, or any real-world
impact metric beyond the hackathon result itself. No metric is invented
to fill this gap.

*Source: verified information provided directly by the project's creator.*

---

## 10. Gallery / Media

## Media Assets

All assets below live in `public/assets/projects/medihelp/` (renamed
this milestone from `medihelp-project/` to match the route slug). Every
raster image has been converted to WebP alongside its kept original —
see `PROJECT_STATUS.md`'s changelog for size figures. **None of these
assets are wired into `ProjectPage.jsx` yet** — this is an inventory for
future implementation, not a record of what's live.

### Hero Video (existing, already wired — unchanged this milestone)
Status: Exists and in use. `public/assets/projects/medi-help.mp4` +
`public/assets/projects/medi-help-poster.jpg` — separate from the
`medihelp/` folder below, already wired into `ProjectPage.jsx`'s Media
section. MediHelp's logo reveal animation, not product/UI footage —
confirmed by direct inspection during the original media-handling pass.

### `hero/`
- `hero.png` / `hero.webp` (1920×1080, 1.3MB → 65KB) — the MediHelp+
  marketing site's hero section: dark-blue "Empower Your Health with AI"
  headline over a medical/AI-themed background, "Get Started for Free"
  CTA. Reserved for future implementation. Not the same asset as the
  already-wired hero video above — this is a still image of a different
  page.

### `screenshots/`
Seven screenshots of the live MediHelp+ web app, all 1920×1080. Reserved
for future implementation — none wired yet. Most show a colorful desktop
wallpaper bleeding in around the browser window edges (capture wasn't
cropped to content); worth re-cropping before use.

- `features.webp` — feature-cards section (Adaptive Symptom Checker,
  Voice-Guided First Aid, Personalized Health Education, Conversational
  Health AI) with an "AI Doctor" graphic. Note: the copy above the cards
  ("Turn Your Vision into Reality: Expert Product Development for
  Startups & Businesses...") is unedited template placeholder text, not
  MediHelp-specific copy.
- `who-we-are.webp` — "Who We Are?" section. Note: contains unedited
  template placeholder text ("Pomegranate Studio... based in Helsinki,
  Finland... Telegram Mini Apps, the TON Blockchain, and the Play2Win
  gaming model") unrelated to MediHelp, plus a "designed by Freepik"
  stock-illustration credit. The "How MediHelp+ Works" 3-step section
  below it (Tell Us How You Feel / Let AI Analyze / Receive Guidance) is
  accurate, on-topic content.
- `find-doctor.webp` — teleconsultation doctor-listing page (Dr. Mesud
  Ebrahim, Dr. Dagim Demissie Kassa, Dr. Tinsae Alemayehu, Dr. Wuhib
  Zenebe). Shows a Windows-activation watermark from the capture
  environment.
- `symptom-checker.webp` — the Symptom Checker feature, a searchable
  symptom checklist. Left edge is slightly cropped (first column's item
  labels partially cut off). Windows-activation watermark visible.
- `login.webp` — filename doesn't match content: this is the Sign-Up
  form ("Sign Up for MediHelp+" — email, name, phone, date of birth,
  password fields), not a login screen.
- `what-users-say.webp` — testimonials (two quotes), a "Join Thousands
  of Users" CTA band, and the site footer. Footer reads "© 2023
  MediHelp+" — inconsistent with the certificate's 2025 hackathon date;
  noted as observed, not resolved.
- `ai.webp` — the "General Assistant" conversational AI feature, shown
  mid-conversation ("Stop Conversation" / "Restart Conversation"
  controls visible). Companion to `videos/ai.mp4` below — same feature,
  static vs. motion.

### `mobile/`
Status: NEEDS USER INPUT — folder exists (empty), no mobile-specific
assets currently exist. Not fabricated.

### `branding/`
- `logo.png` (500×462) — MediHelp's cross/plus mark: solid blue bars
  forming a plus shape, woven through by two gradient ribbon swooshes
  (blue → purple → green → yellow-green). Not converted to SVG — see
  the Logo Vectorization note below for why.
- `favicon.svg` — a genuinely separate vector graphic, not a vector
  version of `logo.png`: an abstract curved leaf/swoosh mark in
  blue-green tones. Already vector (real paths, not an embedded bitmap);
  no conversion needed.

### `award/`
- `certificate.jpg` / `certificate.webp` (1280×869, 136KB → 91KB) — the
  printed award certificate. Reads: "AASTU TECH FEST 2025 HACKATHON —
  FIRST PLACE WINNER'S PRIZE", awarded "TO: MediHelp Plus(+)", "AMOUNT:
  Fifteen thousand [15,000]", dated "07/05/2025". Sponsor logos include
  Google Developer Groups (On Campus AASTU), HubBits, Safaricom, EYEA,
  Visionary Solutions, Cloudet, Minab, MMCY Tech, Kifiya, Helper, Kacha.
  This corroborates §8's award claim with primary-source detail — the
  exact hackathon name, amount, and date weren't previously recorded
  anywhere in this document.
- `award-ceremony.HEIC` / `award-ceremony.webp` (4032×3024, 2.1MB →
  1.2MB; 180° EXIF rotation corrected during conversion) — seven-person
  team photo in front of an "AASTU TECH" step-and-repeat banner, one
  member holding the certificate above.

### `graphics/`
Status: NEEDS USER INPUT — folder exists (empty), no additional graphics
assets currently exist beyond what's already covered under `branding/`
and embedded within the screenshots. Not fabricated.

### `videos/`
- `ai.mp4` (1920×1080, H.264 + AAC, 22.3s, 1.9MB) — screen recording of
  the same "General Assistant" AI conversation feature shown in
  `screenshots/ai.webp`, captured live in motion ("You can speak to
  interrupt the conversation").

### Logo Vectorization
Attempted per this milestone's instructions. No automated vectorization
tool is available in this environment (`potrace`, `autotrace`, and
`vtracer` were all checked and are not installed) — and even with one,
`logo.png`'s two ribbon shapes use a smooth, multi-stop, diagonally
angled gradient (blue → purple → green → yellow-green) following a
curved, twisting path. That's the case automated bitmap tracers handle
worst: they're built for flat-color or limited-palette regions, not
smooth gradient meshes on organic curves — the result would either
posterize the gradient into visible bands or fail outright. Faithfully
reproducing it would require hand-authoring the bezier paths and
gradient stops directly, which risks a subtly-wrong recreation presented
as if it were exact. Per this milestone's explicit instruction not to
fake an SVG by embedding a bitmap, `logo.png` stays a PNG.

---

## 11. Links

Pulled directly from `src/constants/index.js` — no new URLs sourced for
this document.

- **Live:** [medihelp-frontend.vercel.app](https://medihelp-frontend.vercel.app/)
- **Repository:** [github.com/ellay21/Medihelp-Frontend](https://github.com/ellay21/Medihelp-Frontend)

---

## Summary of Gaps

For quick reference — everything still marked `NEEDS USER INPUT`:

1. §5 — architecture detail beyond the confirmed technology list and
   confirmed areas of technical involvement (AI integration,
   authentication, API communication)
2. §10 `mobile/` and `graphics/` — no mobile-specific or additional
   graphics assets exist beyond what's inventoried under `branding/`
   and within the screenshots. Website screenshots, the hero image,
   graphics (logo + favicon), and hackathon materials (certificate +
   ceremony photo) are now inventoried and resolved as of this milestone.

Everything else in this document (Overview, Problem, Research, Design
Process, Development, My Role, Challenges, Award, Final Outcome, Media,
and Links) is sourced and ready to use.

---

## Related Documents

- [[PROJECT_PAGE_SYSTEM]] — this document states directly that it is
  "Governed by `docs/design/PROJECT_PAGE_SYSTEM.md` §4"
- [[DESIGN_SYSTEM]] — the visual system that will govern this project's
  page once implemented; not a textual citation in this document, added
  per this pass's requested example
- [[TECH_STACK]] — this document's confirmed technology list (Django,
  PostgreSQL, React, Tailwind, Gemini API) is the real instance of what
  that document describes in the abstract; not a textual citation, added
  per this pass's requested example
