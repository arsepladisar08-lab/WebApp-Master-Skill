# Database Design

- Model entities and relationships from confirmed business rules.
- Define primary keys, foreign keys, uniqueness, nullability, indexes and deletion behavior.
- Enforce critical invariants in the database where possible, not only in application code.
- Use transactions for multi-step writes that must succeed or fail together.
- Design migrations to preserve existing data; review destructive operations carefully.
- Scope queries by tenant/user ownership where applicable.
- Index real query patterns and validate with query plans when performance matters.
- Store timestamps consistently and handle timezone conversion explicitly.
- Avoid logging secrets and unnecessary personal data.

For Supabase projects, distinguish public client access from trusted server/service-role operations. Never expose a service-role key to browser code. Enable and test Row Level Security for exposed tables and verify policies using representative user roles.
