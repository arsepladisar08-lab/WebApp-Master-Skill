# CI/CD

A practical baseline pipeline should:
1. Install dependencies using the committed lockfile and the appropriate frozen/immutable mode.
2. Run formatting/lint checks.
3. Run type checking.
4. Run unit and integration tests.
5. Build the production artifact.
6. Optionally run browser tests and security/dependency checks.
7. Deploy previews for review and production only under the repository's approved policy.

Keep workflows least-privileged. Pin third-party actions appropriately, avoid printing secrets, and use environment protection for production. Cache dependencies safely without caching credentials.

Do not add CI that references nonexistent scripts. Inspect package scripts and current workflows first.
