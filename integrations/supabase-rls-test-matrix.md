# Supabase RLS Test Matrix

Use this matrix for tables and storage objects accessible from the client-facing Data API.

| Actor | Read own | Read others | Insert own | Insert as others | Update own | Update others | Delete others |
|---|---:|---:|---:|---:|---:|---:|---:|
| Anonymous | Deny unless explicitly public | Deny | Deny unless explicit public workflow | Deny | Deny | Deny | Deny |
| Authenticated user A | Allow per policy | Deny by default | Allow per policy | Deny | Allow per policy | Deny | Deny |
| Authenticated user B | Allow own | Deny A's private rows | Allow own | Deny | Allow own | Deny A's rows | Deny |
| Admin/staff | Explicitly define scope | Explicitly define scope | Explicitly define scope | Explicitly define scope | Explicitly define scope | Explicitly define scope | Explicitly define scope |
| Service role | Trusted server only | Trusted server only | Trusted server only | Trusted server only | Trusted server only | Trusted server only | Trusted server only |

This table is a conservative baseline, not a policy generator. Public catalog reads, shared workspaces, delegated access and admin operations require explicit product rules.

For each table:
1. List the data classification and owner/tenant field.
2. Define read and mutation rules separately.
3. Test both allowed and denied operations.
4. Test identifier tampering and role escalation.
5. Verify policies after migrations in a disposable test environment.
6. Ensure no privileged key is shipped to the browser.
