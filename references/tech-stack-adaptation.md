# Adapting to a project stack

Inspect package manifests and existing imports before choosing a library. Use
the project's router, query/cache layer, form conventions, icon set, styling
approach, and test runner. If the project has no component system, introduce
small local primitives only when they remove repetition.

Do not translate a design reference into a dependency list. A token-based CSS
system can be implemented with CSS variables, Tailwind, CSS Modules, or the
project's existing approach. Motion can be CSS or an existing animation library
and should remain optional for reduced-motion users.

If the requested framework is unclear, ask for it when implementation would
otherwise be ambiguous. If the user only needs a visual prototype, keep data
and network behavior mocked and label the seams clearly.
