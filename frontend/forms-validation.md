# Forms and Validation

- Give every field a clear label and explain required formats or constraints.
- Validate on the client for immediate feedback and on the server at the trust boundary.
- Use schema validation where it improves consistency; share schemas only where runtime and security boundaries allow.
- Normalize input carefully without corrupting legitimate user data.
- Preserve user input after recoverable failures.
- Prevent accidental duplicate submissions and handle retry/idempotency for consequential operations.
- Present field-level errors and a useful form-level summary.
- Support keyboard navigation, autofill and mobile input ergonomics.
- Treat uploaded files as untrusted: validate size, type, content, storage policy and access.
