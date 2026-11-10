# Workflow: Bug Fixing

1. Reproduce the issue or identify the narrowest reliable failing condition.
2. Capture exact error text, steps, browser/runtime, expected result and actual result.
3. Trace the root cause through UI, API, auth, data and external services as relevant.
4. Add a focused regression test when practical.
5. Fix the root cause with the smallest safe change.
6. Re-run the regression test and relevant neighboring checks.
7. Verify the user-visible behavior and inspect logs/console when available.
8. Explain root cause, fix, evidence and any remaining uncertainty.

Do not repeatedly change unrelated code based on guesses. After failed attempts, update the diagnosis with new evidence.
