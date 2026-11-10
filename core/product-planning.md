# Product Planning

Use this module for new products and non-trivial features.

## Minimum product brief

- Problem and desired outcome.
- Primary users and their context.
- Core user journeys.
- Must-have capabilities and explicit exclusions.
- Business rules and edge cases.
- Data collected, stored, displayed, and deleted.
- Integrations and operational constraints.
- Success measures.

## Requirements quality

Write requirements as observable behavior. Give each important requirement an identifier and acceptance criteria.

Example:

**REQ-ORDER-01 — Create an order**
- Given a valid cart and customer details,
- when the customer confirms the order,
- then the system persists one order and shows a confirmation.
- Edge cases: duplicate submission, invalid stock, network interruption, unauthenticated request.

## Prioritization

- P0: required for the core journey or safety/security.
- P1: meaningful improvement but not a launch blocker.
- P2: later enhancement.

Separate confirmed requirements from assumptions. Never silently turn an assumption into a business rule. For low-risk ambiguity, make a reversible assumption and disclose it. Ask a concise question when the answer materially changes scope, cost, security, or data design.

## Outputs

For a substantial new app, create `docs/PRD.md` with:
1. Summary and problem statement.
2. Users and roles.
3. Goals / non-goals.
4. User journeys.
5. Functional requirements.
6. Business rules and edge cases.
7. Non-functional requirements.
8. Acceptance criteria and open questions.
