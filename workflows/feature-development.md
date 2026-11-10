# Workflow: Feature Development

1. Translate the request into observable acceptance criteria.
2. Trace existing UI, domain rules, API and persistence.
3. Identify permission, data migration, integration and concurrency implications.
4. Define interface/data contracts before cross-module work.
5. Add tests for core and failure behavior.
6. Implement a vertical slice.
7. Verify all relevant roles and states.
8. Update documentation and report evidence.

A feature is not complete when only its visual controls exist. Confirm the action reaches the correct business logic and durable state when persistence is required.
