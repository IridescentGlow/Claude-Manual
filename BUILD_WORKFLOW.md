# BUILD_WORKFLOW.md

# SOLARISX PORTFOLIO BUILD WORKFLOW

Version: 1.0

---

# PURPOSE

This document defines the execution process for building the Solarisx Portfolio.

The goal is to provide Claude with a structured workflow for:

- analyzing existing templates
- planning modifications
- implementing improvements
- maintaining quality
- delivering a professional final product

---

# BUILD PHILOSOPHY

The portfolio should not be created by blindly writing code.

The process should follow:

```
Understand the Vision

↓

Design the Experience

↓

Plan the Architecture

↓

Implement Professionally

↓

Refine Through Iteration

↓

Polish Every Detail
```

---

# CORE PRINCIPLE

The objective is not:

"Build a website quickly."

The objective is:

"Transform an existing foundation into a unique, professional creative experience."

---

# TEMPLATE-FIRST APPROACH

The project may begin from:

- open-source GitHub templates
- portfolio starters
- creative website templates
- professional UI systems

However:

The template is only a foundation.

It should not define the final identity.

---

# TEMPLATE SELECTION RULES

A template should be evaluated based on:

## Design Quality

Does it already demonstrate:

- strong layout
- good typography
- quality interactions
- professional presentation?

---

## Technical Quality

Does it have:

- clean architecture
- modern tools
- maintainable code?

---

## Customization Potential

Can it be transformed into a unique portfolio?

---

## Community Quality

Consider:

- documentation
- maintenance
- popularity
- code quality

---

# AVOID SELECTING TEMPLATES THAT ARE:

- outdated
- poorly maintained
- visually generic
- difficult to customize
- dependent on unnecessary technology

---

# INITIAL PROJECT ANALYSIS

Before making changes, analyze:

## Structure

Understand:

- folders
- components
- dependencies
- architecture

---

## Design

Identify:

- typography
- colors
- layouts
- animations
- UI patterns

---

## Strengths

Determine what should be preserved.

---

## Weaknesses

Determine what should be improved.

---

# PRESERVATION RULE

Do not rewrite everything immediately.

First identify:

```
Keep

↓

Improve

↓

Replace
```

---

# REASONING BEFORE ACTION

Before every major change, Claude should explain:

1. What is changing?
2. Why is it changing?
3. What benefit does it provide?
4. What are the possible risks?

---

# END OF PART 1





# BUILD_WORKFLOW.md

# PART 2 — TEMPLATE ANALYSIS & TRANSFORMATION PROCESS

---

# PHASE 1 — TEMPLATE ACQUISITION

The first step is selecting and obtaining a suitable foundation.

Possible sources:

- GitHub repositories
- open-source portfolio templates
- creative developer starters
- UI component libraries

---

# TEMPLATE EVALUATION PROCESS

Before choosing a template, evaluate:

---

## Design Evaluation

Analyze:

- visual quality
- layout structure
- typography
- animation quality
- responsiveness
- originality

Questions:

- Does this feel professional?
- Does it match the desired creative direction?
- Can it support a cinematic portfolio?

---

## Technical Evaluation

Analyze:

- framework
- dependencies
- folder structure
- code quality
- documentation

Questions:

- Is the architecture clean?
- Is it easy to modify?
- Is it actively maintained?

---

## Customization Evaluation

Determine:

- what can be changed easily
- what requires rebuilding
- what should be removed

---

# PHASE 2 — INITIAL PROJECT AUDIT

After cloning the template:

Do not immediately modify the code.

First perform an audit.

---

# CODE AUDIT

Review:

## Framework

Identify:

- Next.js version
- React version
- TypeScript usage
- build system

---

## Dependencies

Classify:

```
Required

Useful

Unnecessary
```

Remove unnecessary dependencies when safe.

---

## Architecture

Understand:

- routing
- components
- styling system
- asset handling

---

# DESIGN AUDIT

Review:

## Layout

Identify:

- page structure
- section order
- spacing system

---

## Visual System

Identify:

- colors
- fonts
- effects
- animations

---

## User Experience

Evaluate:

- navigation
- flow
- interaction quality

---

# PHASE 3 — CUSTOMIZATION STRATEGY

Before changing the template, create a transformation plan.

The plan should define:

---

# KEEP

Elements worth preserving:

Examples:

- strong components
- good animations
- useful architecture
- effective layouts

---

# MODIFY

Elements that need adaptation:

Examples:

- colors
- typography
- sections
- content
- interactions

---

# REMOVE

Elements that do not fit:

Examples:

- unnecessary pages
- generic sections
- unwanted features

---

# ADD

New elements needed for the creator's identity.

Examples:

- video showcases
- creative process sections
- personal branding
- unique interactions

---

# PHASE 4 — BRAND TRANSFORMATION

The template should be transformed into Solarisx's identity.

Replace:

## Generic Branding

With:

- personal identity
- unique messaging
- creator story

---

## Default Content

With:

- real projects
- real experience
- authentic writing

---

## Template Visuals

With:

- custom media
- personal assets
- original presentation

---

# TRANSFORMATION RULE

The final result should never feel like:

"This is a modified template."

It should feel like:

"This was designed specifically for this creator."

---

# PHASE 5 — ITERATIVE DEVELOPMENT

Work in controlled stages.

Recommended order:

```
Foundation

↓

Structure

↓

Content

↓

Visual Identity

↓

Motion

↓

Polish
```

---

# FOUNDATION STAGE

Verify:

- project runs correctly
- dependencies work
- environment is configured

---

# STRUCTURE STAGE

Modify:

- pages
- sections
- component organization

---

# CONTENT STAGE

Replace:

- text
- images
- projects
- descriptions

---

# VISUAL IDENTITY STAGE

Implement:

- design system
- typography
- colors
- spacing

---

# MOTION STAGE

Add:

- transitions
- interactions
- animations

---

# POLISH STAGE

Improve:

- details
- performance
- accessibility
- consistency

---

# END OF PART 2




# BUILD_WORKFLOW.md

# PART 3 — CLAUDE DEVELOPMENT BEHAVIOR

---

# DEVELOPMENT ROLE

During implementation, Claude should act as:

```
Senior Frontend Engineer

+

Creative Technical Advisor

+

Code Reviewer
```

---

# GENERAL BEHAVIOR

Claude should:

- think before changing code
- explain important decisions
- protect existing functionality
- maintain project quality
- prioritize long-term maintainability

---

# BEFORE MAKING CHANGES

Before modifying files:

Claude should understand:

- current implementation
- project structure
- dependencies
- design intent
- possible side effects

---

# CHANGE EXPLANATION STANDARD

For significant changes, explain:

```
Change

↓

Reason

↓

Expected Result

↓

Potential Risks
```

---

# DECISION MAKING

When multiple approaches exist:

Claude should compare:

```
Option A

Advantages

Disadvantages


Option B

Advantages

Disadvantages


Recommendation
```

Choose based on:

- quality
- simplicity
- maintainability
- project goals

---

# QUESTION POLICY

Claude should ask questions when:

- requirements are unclear
- a decision affects the entire project
- important information is missing

Claude should not ask unnecessary questions when:

- the decision is obvious
- a reasonable assumption can be made
- progress would not be affected

---

# ASSUMPTION RULE

When making assumptions:

Claude should:

1. State the assumption.
2. Explain why it was chosen.
3. Allow correction.

---

# CODE IMPLEMENTATION STYLE

When writing code:

Prefer:

- clean solutions
- readable logic
- reusable components
- consistent patterns

Avoid:

- shortcuts
- hacks
- duplicated code
- unnecessary abstraction

---

# FILE MODIFICATION RULE

Before editing:

Understand:

- why the file exists
- what depends on it
- whether another approach is better

---

# REFACTORING RULE

Do not refactor unnecessarily.

Refactor when:

- code is difficult to maintain
- duplication creates problems
- architecture needs improvement

---

# DEBUGGING PROCESS

When encountering errors:

Follow:

```
Observe Error

↓

Identify Cause

↓

Investigate Context

↓

Apply Solution

↓

Verify Fix
```

---

# DEBUGGING REQUIREMENTS

Do not:

- blindly install packages
- randomly change files
- hide errors

Instead:

Understand the problem first.

---

# ERROR REPORTING

When something fails, provide:

## Problem

What happened?

---

## Cause

Why did it happen?

---

## Solution

How to fix it?

---

## Prevention

How to avoid it again?

---

# CODE REVIEW PROCESS

After completing major features:

Review:

## Functionality

Does it work correctly?

---

## Design

Does it follow the design system?

---

## Performance

Does it remain efficient?

---

## Maintainability

Can it be improved later?

---

# QUALITY CONTROL LOOP

Every major feature should go through:

```
Build

↓

Test

↓

Review

↓

Improve
```

---

# COMPLETION STANDARD

A feature is not complete when:

"the code runs."

A feature is complete when:

- it works
- it looks correct
- it follows standards
- it improves the experience

---

# END OF PART 3





# BUILD_WORKFLOW.md

# PART 4 — PROJECT ROADMAP & DELIVERY PROCESS

---

# PROJECT DEVELOPMENT ROADMAP

The portfolio should be built through clear milestones.

The recommended process:

```
Milestone 1

Foundation Setup

↓

Milestone 2

Structure Development

↓

Milestone 3

Content Integration

↓

Milestone 4

Design Implementation

↓

Milestone 5

Animation & Interaction

↓

Milestone 6

Optimization

↓

Milestone 7

Launch
```

---

# MILESTONE 1 — FOUNDATION SETUP

Goal:

Create a stable development environment.

Tasks:

- obtain template or initialize project
- install dependencies
- verify local development
- understand architecture
- configure tools

Success criteria:

☐ Project runs successfully.

☐ Dependencies are understood.

☐ Development environment works.

---

# MILESTONE 2 — STRUCTURE DEVELOPMENT

Goal:

Create the correct portfolio architecture.

Tasks:

- define pages
- organize sections
- create reusable components
- establish content structure

Success criteria:

☐ Website structure is clear.

☐ Components are organized.

☐ Future expansion is possible.

---

# MILESTONE 3 — CONTENT INTEGRATION

Goal:

Replace template content with authentic creator content.

Tasks:

- add projects
- write descriptions
- add experience
- integrate media

Success criteria:

☐ Portfolio represents the creator.

☐ Content feels authentic.

☐ Projects communicate value.

---

# MILESTONE 4 — DESIGN IMPLEMENTATION

Goal:

Apply the Solarisx Design System.

Tasks:

- implement typography
- apply colors
- refine spacing
- improve layouts
- create visual consistency

Success criteria:

☐ Design system is followed.

☐ Website has a unique identity.

☐ Visual quality is professional.

---

# MILESTONE 5 — ANIMATION & INTERACTION

Goal:

Create a memorable experience.

Tasks:

- add transitions
- improve interactions
- refine motion
- polish user experience

Success criteria:

☐ Animations have purpose.

☐ Motion feels natural.

☐ Performance remains strong.

---

# MILESTONE 6 — OPTIMIZATION

Goal:

Prepare the portfolio for real users.

Tasks:

- optimize images
- improve loading speed
- check accessibility
- test responsiveness
- remove unnecessary code

Success criteria:

☐ Fast loading.

☐ Mobile friendly.

☐ No major issues.

---

# MILESTONE 7 — LAUNCH

Goal:

Deploy a professional final product.

Tasks:

- configure deployment
- verify production build
- test final version
- publish

Success criteria:

☐ Website is publicly accessible.

☐ All features work.

☐ Final quality review completed.

---

# FINAL REVIEW PROCESS

Before launch, perform a complete review.

---

# DESIGN REVIEW

Check:

- visual consistency
- typography
- spacing
- branding
- overall impression

---

# TECHNICAL REVIEW

Check:

- code quality
- performance
- accessibility
- security
- maintainability

---

# USER EXPERIENCE REVIEW

Check:

- navigation
- clarity
- interaction flow
- contact accessibility

---

# POST-LAUNCH IMPROVEMENT

The portfolio should continue evolving.

Future improvements:

- new projects
- better case studies
- improved animations
- new technologies
- performance improvements

---

# MAINTENANCE PHILOSOPHY

The portfolio is a living project.

Do not treat launch as the end.

Treat it as:

```
Version 1.0

↓

Continuous Improvement
```

---

# BUILD WORKFLOW COMPLETE

Version: 1.0

```
This document defines the execution
process for creating the Solarisx Portfolio
from foundation to launch.
```

---
