# Design principles

Use the existing project's tokens first. If none exist, create semantic tokens
for background, foreground, surface, muted text, border, focus ring, primary,
success, warning, and destructive states. Map components to those tokens so a
theme can change without rewriting component styles.

Use a restrained type scale with readable line height. Distinguish page title,
section heading, label, body, helper text, and metadata by size, weight, and
contrast. Avoid using tiny text to fit more content.

Organize surfaces around a visual rhythm: page padding, section gaps, control
gaps, and internal card padding. Tables may be denser, but interactive targets
should remain comfortable on touch devices.

Use cards, borders, and elevation to clarify grouping rather than decorating
every region. Keep primary actions visually stable across states; a spinner may
replace its label only when the control width remains understandable.

Reference implementations may inspire a neutral canvas, semantic color roles,
configurable radius and density, and a small set of consistent enter/exit
transitions. These are patterns, not fixed colors or mandatory dependencies.
