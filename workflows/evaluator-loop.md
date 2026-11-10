# Workflow: Generator–Evaluator Loop

1. Planner creates a feature contract with acceptance criteria.
2. Generator implements one bounded feature and reports evidence.
3. Evaluator inspects the code diff and runs relevant checks independently.
4. If FAIL, return actionable findings and regression expectations.
5. Generator fixes the findings.
6. Evaluator reruns failed checks and related regression tests.
7. Mark accepted only when P0 criteria pass and no critical blocker remains.
8. Persist status and evidence in the progress record.

For small tasks, use a lightweight review. For high-risk auth, payments, personal data, destructive actions or multi-tenant data access, require explicit security/authorization testing.
