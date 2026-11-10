# Code Review

Review changed code against requirements and actual project behavior.

## Review order

1. Correctness and acceptance criteria.
2. Security, data access and authorization.
3. Data integrity and concurrency.
4. Error handling and user feedback.
5. Accessibility and responsive behavior.
6. Performance and maintainability.
7. Documentation and tests.

Look for:
- UI-only stubs that do not persist or call real logic.
- Missing server-side checks.
- Race conditions and duplicate submissions.
- Unhandled null/empty/error states.
- Unsafe type casts, dead code and unnecessary dependencies.
- Secrets, debug statements and unrelated modifications.
- Tests that assert implementation details but miss user behavior.

Report concrete findings with file/line references, severity, impact and remediation. Distinguish confirmed defects from risks or suggestions.
