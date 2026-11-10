# React Practices

Use this module when the repository uses React. Verify the installed React and framework versions before applying version-specific APIs.

## Component design

- Keep components focused on a coherent responsibility.
- Separate domain logic and data access from presentation where this improves clarity.
- Prefer composition and explicit props over deeply nested conditionals.
- Do not define component types inside another component unless there is a deliberate reason.
- Use stable, meaningful keys for mapped collections.
- Avoid premature memoization; profile or identify a concrete cost first.

## State

- Keep state as close as practical to the components that own it.
- Derive values during render instead of storing redundant derived state.
- Use reducers or a state library when transitions and shared ownership justify it.
- Avoid effects for values that can be derived or for event-driven mutations.
- Clean up subscriptions, listeners, and async work when appropriate.

## Data fetching

- Use the project's established server/client data-fetching approach.
- Avoid serial waterfalls for independent requests.
- Handle loading, error, empty, stale, and retry states.
- Prevent stale responses from overwriting newer user intent.
- Do not expose server secrets in client bundles.

## Performance

- Inspect bundle size and rendering hotspots before optimizing.
- Lazy-load genuinely expensive or infrequently used features.
- Avoid unnecessary client-side JavaScript.
- Keep images and fonts optimized.
- Follow the framework's current guidance for server rendering, caching, and streaming.

See also [Vercel React Best Practices](https://github.com/vercel-labs/agent-skills/tree/main/skills/react-best-practices).
