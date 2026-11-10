# Component Architecture

- Use shared components for repeated behavior or a meaningful design-system primitive, not merely to eliminate a few lines.
- Define clear component contracts, controlled/uncontrolled behavior, and accessibility expectations.
- Prefer composition, slots, and render props only when they make the API clearer.
- Keep domain-specific components separate from generic primitives.
- Avoid giant components that combine routing, fetching, business rules, and complex presentation.
- Document variants and avoid boolean-prop explosions.
- Test user-visible behavior and keyboard interaction, not implementation details alone.
