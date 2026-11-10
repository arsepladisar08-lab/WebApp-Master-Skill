# Design System

## Single source of truth

Define reusable tokens before styling multiple pages. Use the project's existing token mechanism where available (CSS variables, Tailwind theme, design tokens, or component theme).

Token groups:
- Color: background, surface, text, muted, border, primary, secondary, accent, success, warning, danger.
- Typography: family, size, line-height, weight, letter spacing.
- Spacing: consistent scale.
- Shape: radius, border widths.
- Elevation: shadows and layering.
- Motion: duration, easing, reduced-motion behavior.
- Breakpoints: content-driven responsive thresholds.

## Rules

- Prefer semantic tokens over raw values repeated across components.
- Check text and interactive-state contrast.
- Do not encode meaning using color alone.
- Avoid token proliferation; add variants only when they represent a real design distinction.
- Document exceptions and migrate consistently rather than mixing several systems.
