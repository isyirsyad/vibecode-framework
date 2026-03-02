# Development Plan

> **Purpose:** Step-by-step implementation plan for building [app name].
> **Last Updated:** [Date] - [Remark on latest update]

---

## Overview

The project development is to build in **[phases] and [stages]** + post-build QA:

| Phase | Description | Stages | Outcome |
|-------|-------------|--------|---------|
| **[Phase name or number]** | [Insert description of the theme or objective of phase] | [Stage count] | [Insert intended outcome] |

---

## Phase [name or number]: [Title of the phase]

### Stage 1: [Title of the stage]

**What to do:**
- [Tasks/issues/items to complete]

**Deliverables:** [Insert completed items/output/deliverables].

---

## [EXAMPLE] Overview

The project was built in **3 phases, 25 stages** + post-build QA:

| Phase | Description | Stages | Outcome |
|-------|-------------|--------|---------|
| **Phase 1** | Reusable component library (only components used in web app) | 1–9 | ~30 components with Storybook stories |
| **Phase 2** | Web app pages assembled from Phase 1 components | 10–20 | All screens as Next.js routes |
| **Phase 3** | Routing, state management, and final polish | 21–25 | Fully navigable prototype |
| **QA** | Visual comparison against Figma + responsive fixes | — | All 15 routes verified at desktop + mobile |

---

## [EXAMPLE] Phase 1: Reusable Components

### Stage 1: Project Scaffolding & Design Tokens

**What to do:**
- Initialize framework project (e.g., Next.js + TypeScript + Tailwind)
- Define design tokens in global CSS or config (colors, fonts, spacing)
- Install and configure fonts
- Add utility helpers: `cn.ts`, `constants.ts`, etc.
- Install and configure Storybook

**Deliverables:** Working dev server, Storybook running, token file committed.
