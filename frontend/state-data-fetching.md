# State Management and Data Fetching

Choose the simplest state model that meets the app's needs.

- Local ephemeral UI state: component state.
- Complex local transitions: reducer.
- Shared client state: the existing context or state library, if justified.
- Remote server state: the project's query/cache solution; do not duplicate it in a global store without reason.
- URL state: filters, pagination, search and shareable navigation state when appropriate.

Define cache keys, invalidation, optimistic update rollback, retry behavior and stale-data handling. Do not assume a library API; inspect its installed version and official docs.

Avoid storing credentials or sensitive personal information in localStorage. Prefer secure, appropriately configured cookies or provider-managed session mechanisms for authentication.
