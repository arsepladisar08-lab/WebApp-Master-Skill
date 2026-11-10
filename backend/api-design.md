# API Design

- Follow the repository's existing API style unless there is a clear reason to change it.
- Define request and response contracts, status codes, auth requirements and failure modes.
- Validate request parameters, body, headers and uploaded files at the server boundary.
- Use consistent error shapes without leaking internal stack traces or secrets.
- Paginate potentially large collections and define filtering/sorting limits.
- Use idempotency or deduplication for retry-prone operations such as payments and order creation.
- Apply rate limits and abuse controls to sensitive or expensive endpoints.
- Keep business rules on trusted server-side code.
- Version public contracts deliberately and document breaking changes.
