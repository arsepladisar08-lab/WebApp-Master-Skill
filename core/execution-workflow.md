# Execution Workflow

## Work in vertical slices

A vertical slice implements one user-visible behavior through the relevant layers: UI, domain logic, API, persistence, and tests.

For each slice:

1. State the expected behavior and acceptance criteria.
2. Identify impacted files, data contracts, and risks.
3. Add or update the most valuable test first when practical.
4. Implement the smallest coherent change.
5. Run focused checks, then broader checks appropriate to the change.
6. Inspect UI/browser behavior for user-facing work.
7. Review the diff for unrelated changes, secrets, debug code, and incomplete states.
8. Update docs and report evidence.

## Parallel work

Parallelize only independent tasks with clear file ownership and stable interfaces. Do not let multiple agents edit the same shared files concurrently. Integrate and verify sequentially.

## Dependency changes

Before adding a dependency:
- Check whether an existing dependency already solves the problem.
- Verify package identity, maintenance status, compatibility and license.
- Add only what is needed and update the lockfile.
- Run the relevant build and tests.

## Change safety

Do not reset, force-push, delete user data, rewrite history, deploy to production, or run destructive migrations without explicit authorization. Preserve unrelated local changes.
