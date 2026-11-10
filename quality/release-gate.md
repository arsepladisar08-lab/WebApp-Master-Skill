# Release Gate

Do not treat a successful build as sufficient evidence that an application is production-ready.

## Required checks (adapt to project)

- [ ] Requirements and acceptance criteria reviewed.
- [ ] Production build passes.
- [ ] Typecheck and lint pass where configured.
- [ ] Relevant unit and integration tests pass.
- [ ] Critical browser journeys pass or have documented manual verification.
- [ ] Authorization and ownership rules tested.
- [ ] Error, empty, loading and success states reviewed.
- [ ] Responsive behavior checked at representative widths.
- [ ] Accessibility scan and keyboard review performed for changed UI.
- [ ] Secrets and environment configuration reviewed.
- [ ] Database migrations and rollback implications reviewed.
- [ ] Performance/SEO checked where relevant.
- [ ] Deployment target, environment variables and rollback path confirmed.

## Evidence report

For each check record:
- Command or method.
- Pass/fail/blocked/not run.
- Concise output or evidence.
- Remaining risk or follow-up.

## Release safety

Production deployment, destructive migrations, data deletion, force-pushes and history rewrites require explicit user authorization. Use preview/staging where possible. Do not claim a deployment occurred unless the platform confirms it.
