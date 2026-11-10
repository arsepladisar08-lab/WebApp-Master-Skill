# Testing Strategy

Choose tests by risk and behavior.

- Unit tests: deterministic domain logic and utilities.
- Integration tests: interactions between modules, APIs, persistence and external boundaries.
- End-to-end tests: critical user journeys in a realistic browser environment.
- Visual regression: selected high-value screens where layout regressions are costly.
- Accessibility checks: automated scans plus manual keyboard review.

## Rules

- Test business rules, permissions, edge cases and failure paths—not only happy paths.
- Add regression tests for fixed defects.
- Keep tests deterministic and isolate external services where appropriate.
- Use realistic integration environments for database policies and provider behavior.
- A passing unit suite does not prove the entire application works.
- Do not claim tests passed unless the command ran and exited successfully.

First discover the repository's scripts and test runner. Do not assume command names.
