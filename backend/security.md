# Application Security

Apply risk-based security review informed by OWASP guidance and the application's threat model.

## Minimum checks

- [ ] Authentication and authorization are enforced server-side.
- [ ] Every resource access checks user/tenant ownership.
- [ ] Inputs are validated and outputs encoded appropriately.
- [ ] SQL/command injection and unsafe deserialization are prevented.
- [ ] CSRF protections are appropriate for the auth and request model.
- [ ] CORS is restricted to required origins.
- [ ] Rate limiting and abuse controls cover sensitive endpoints.
- [ ] Secrets are managed outside source control and client bundles.
- [ ] File uploads are constrained and stored safely.
- [ ] Logs avoid credentials, tokens and unnecessary personal data.
- [ ] Dependencies and deployment configuration are reviewed.
- [ ] Errors do not reveal internals.

Never run destructive security tests against production without explicit authorization and a safe test plan. Record findings with severity, evidence, impact and remediation.
