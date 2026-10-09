# Review report

## Structural checks

- `SKILL.md` contains valid frontmatter with `name` and `description`.
- Five reference files are present and every referenced path resolves.
- `evals/evals.json` parses as JSON and contains five test cases.
- The skill body is 100 lines, keeping the core workflow small enough to load.

## Generality checks

- The skill does not require React, Tailwind, a specific router, or a specific component library.
- The reference product is not named in the skill instructions; its ideas are expressed as stack-neutral patterns.
- The workflow explicitly inspects an existing project and preserves its conventions.
- The eval set covers React, Vue/CSS Modules, admin, settings, dashboard, AI chat, and a simple landing page.
- The skill separates reusable design principles from business content, branding, and reference-project code.

## Behavior checks

- State coverage includes loading, skeleton, empty, filtered-empty, error, retry, validation, submitting, success, disabled, permissions, and destructive confirmation.
- Responsive behavior, keyboard access, visible focus, semantic structure, contrast, touch targets, and reduced motion are explicit.
- The output contract asks for changed files, assumptions, state matrix, verification results, and manual QA.

## Follow-up review

Run the five prompts in `evals/evals.json` against a real project and inspect whether the generated implementation follows the host stack. If a future project exposes a repeated pattern, add it to a reference file rather than hard-coding that project's framework into `SKILL.md`.
