---
name: generic-frontend-design
description: >
  Design and implement polished, production-ready frontend interfaces for
  SaaS products, AI applications, dashboards, admin panels, data tools, and
  business web apps. Use this skill whenever the user asks to create or
  improve a frontend page, UI component, interaction flow, dashboard, form,
  table, settings page, responsive layout, loading state, empty state, error
  state, theme system, animation, or visual design system. Adapt to the
  project's existing framework, CSS strategy, component library, routing, and
  state management instead of assuming a fixed stack.
---

# Generic Frontend Design

Create interfaces that are coherent, usable, responsive, and complete across
the states users actually encounter. Treat the existing project as the source
of truth when one exists; use a reference product only to learn patterns, never
to copy its business content or branding.

## Operating workflow

1. Inspect the project before editing. Identify the framework, package manager,
   entry points, routing, design tokens, component library, data layer, testing
   commands, and existing page conventions.
2. Restate the requested user flow and identify the primary action, supporting
   information, permissions, and failure points. If a key product decision is
   missing, ask one focused question; otherwise make a documented assumption.
3. Choose a page pattern from `references/page-patterns.md` and reuse existing
   primitives before introducing new ones.
4. Define or reuse semantic design tokens for color, typography, spacing,
   radius, elevation, and motion. Keep the page visually consistent in light,
   dark, and narrow layouts when those modes exist.
5. Implement the happy path and every relevant loading, empty, error,
   validation, disabled, success, and permission state. Give each state a
   useful next action where possible.
6. Add interaction feedback at the point of action: pending indicators,
   confirmation for destructive operations, inline validation, toast or inline
   result messages, and preservation of user input after recoverable errors.
7. Check keyboard access, focus visibility, labels, semantic headings,
   contrast, reduced-motion behavior, and touch target size.
8. Run the repository's focused checks and inspect the rendered result at wide
   and narrow viewports. Report commands run and any unverified assumption.

## Design rules

- Establish a clear hierarchy: page title and purpose, primary action,
  context or filters, content, then secondary actions.
- Prefer one strong primary action per surface. Use secondary and destructive
  actions with distinct emphasis and confirmation where consequences are hard
  to reverse.
- Use semantic tokens rather than scattered literal colors. Status colors must
  also have text or icon meaning; never communicate status by color alone.
- Keep spacing, control heights, radius, and typography consistent within a
  surface. Increase density for data-heavy views without making controls hard
  to use.
- Build for content variation: long labels, missing values, zero results,
  multiple errors, slow requests, and very small screens.
- Use motion to explain change and hierarchy. Keep transitions short and
  purposeful, avoid animation during frequent data updates, and honor
  `prefers-reduced-motion`.
- Preserve user context after filtering, pagination, validation failure, or a
  recoverable request error. Avoid surprising full-page resets.
- Make responsive behavior intentional: decide what stacks, scrolls, hides,
  or becomes an alternate control rather than letting content overflow.

## Implementation contract

Before writing code, state briefly:

- the files or components to change;
- the selected page pattern;
- the data and state assumptions;
- the complete state matrix;
- the responsive and accessibility decisions.

After writing code, provide:

- a concise change summary;
- verification commands and their results;
- any remaining product or integration assumptions;
- a short manual QA checklist for the main flow and edge states.

## Scope and originality

Extract principles from reference products such as mature admin or AI
interfaces, but do not copy their names, logos, proprietary text, real user
data, API keys, or business workflows. Do not add a new UI framework when the
repository already has a suitable system. Keep implementation choices
compatible with the current project unless the user explicitly requests a
migration.

Read the relevant reference file only when needed:

- `references/design-principles.md` for visual hierarchy and tokens.
- `references/page-patterns.md` for page-level composition.
- `references/interaction-states.md` for state and feedback coverage.
- `references/responsive-and-accessibility.md` for adaptive and inclusive UI.
- `references/tech-stack-adaptation.md` for working with an unfamiliar stack.
