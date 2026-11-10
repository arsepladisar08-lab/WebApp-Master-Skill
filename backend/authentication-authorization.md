# Authentication and Authorization

Authentication establishes identity; authorization decides what that identity can do.

- Inspect the existing provider and session model before changes.
- Enforce authorization on server/API/database boundaries, not merely by hiding UI elements.
- Define roles and permissions from least privilege.
- Check ownership and resource scope on every sensitive operation.
- Handle session expiry, refresh, logout, revoked access and account lifecycle.
- Protect OAuth redirect/callback configuration and validate allowed redirect destinations.
- Use secure cookie attributes when cookies are used.
- Do not store plaintext passwords or expose privileged tokens.
- Test anonymous, ordinary user, elevated user, cross-user access and expired-session cases.

For Supabase, review Auth configuration, redirect allowlists, RLS policies, and the difference between anon/publishable and service-role/secret keys. Do not assume RLS is correct simply because it is enabled.
