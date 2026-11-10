# Browser Testing with Playwright

Use Playwright or the browser automation tool available in the environment.

## Workflow

1. Discover how the app starts and whether the server is already running.
2. Read the helper/tool documentation before invocation.
3. Open the actual application and wait for client rendering/network activity as appropriate.
4. Inspect the rendered page, accessible names, DOM and console.
5. Exercise a real user flow using semantic locators where possible.
6. Assert observable outcomes, not merely that clicks did not throw.
7. Capture screenshots for important visual states and viewport sizes.
8. Close browser/server resources.

## Critical flows

Prioritize sign-up/login, primary creation or purchase flow, data editing, destructive actions, role restrictions, and error/retry handling.

Never use arbitrary sleeps as the default synchronization strategy; prefer locator and condition-based waits. Do not put real credentials or personal data into committed tests.
