# UX and Accessibility Review

Use semantic HTML first. Interactive behavior must be available to keyboard and assistive technology users.

## Review checklist

- [ ] Landmarks and heading hierarchy communicate page structure.
- [ ] Links navigate; buttons perform actions; controls have accessible names.
- [ ] Inputs have labels, instructions and understandable validation errors.
- [ ] Focus order is logical and focus is visible.
- [ ] Dialogs manage focus, Escape behavior and return focus appropriately.
- [ ] Contrast meets WCAG AA for relevant text and interface components.
- [ ] Color is not the only signal for status or errors.
- [ ] Images have meaningful alternatives or are decorative.
- [ ] Motion respects `prefers-reduced-motion`.
- [ ] Dynamic updates are announced appropriately without excessive live-region noise.
- [ ] Mobile targets and layouts are usable at zoom.
- [ ] Authentication and error messages do not expose sensitive information.

Automated scans are useful but cannot prove accessibility. Combine automated checks with keyboard and manual review.
