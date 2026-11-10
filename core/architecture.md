# Application Architecture

## Principles

- Choose architecture from actual product needs; avoid enterprise complexity for a small app.
- Prefer clear module boundaries and one source of truth for domain rules.
- Keep secrets and privileged operations on the server.
- Make data ownership, authorization, and failure behavior explicit.
- Avoid duplicating business rules across UI and API.

## Stack selection

1. Inspect existing stack first.
2. For greenfield work, compare at least two plausible options only when the trade-off matters.
3. Decide based on team familiarity, ecosystem, hosting, SEO, data needs, integrations, cost, and maintenance.
4. Record why the chosen stack fits and what alternatives were rejected.

## Architecture document

For a non-trivial application, record:
- Client, server, and background responsibilities.
- Routes and module boundaries.
- Data model and ownership.
- API contracts and validation.
- Authentication and authorization model.
- External services and failure modes.
- Logging, monitoring, deployment, and rollback approach.

## Data flow

For every critical action, trace:
user action → client validation → authenticated request → server authorization → domain validation → persistence / integration → response → UI state.

Client validation improves usability but never replaces server-side validation or authorization.

## Evolution

Prefer additive, reversible changes. Use migrations for schema changes. Define rollback and compatibility considerations before high-risk releases.
