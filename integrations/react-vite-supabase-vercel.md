# Integration Profile: React + Vite + Supabase + Vercel

This is an opinionated profile for projects that have selected this stack. It is not a default mandate. Inspect current repository configuration and provider documentation before implementation.

## 1. Stack responsibilities

| Layer | Responsibility | Boundary |
|---|---|---|
| React + Vite | Browser UI, routing, client state and interactions | Never hold privileged secrets |
| Supabase Auth | Identity and sessions | Validate user identity for protected operations |
| Supabase PostgreSQL | Durable relational data | RLS and constraints enforce data boundaries |
| Supabase Storage | File storage | Policies and signed access govern private objects |
| Supabase Edge Functions / trusted server | Privileged logic and integrations | Secrets remain server-side |
| Vercel | Frontend deployment and supported server functions | Configure build/runtime/env per project |

A Vite single-page app on Vercel is not automatically a secure backend. Do not put privileged operations in browser code.

## 2. Repository discovery

Before changing a project, inspect:
- `package.json`, lockfile, `vite.config.*`, `tsconfig*.json`.
- React, Vite, TypeScript, router, Supabase JS and test versions.
- Existing Supabase client initialization and auth/session handling.
- SQL migrations, generated database types, RLS policies and storage policies.
- Vercel configuration, rewrites, environment configuration and build logs.
- Existing scripts for lint, typecheck, tests and build.

Keep existing conventions unless there is a concrete reason to change them.

## 3. Environment configuration

Typical browser-exposed Vite variables use the `VITE_` prefix. Values with this prefix are bundled into client-side code and must never contain secrets.

Example names only:
- `VITE_SUPABASE_URL`
- `VITE_SUPABASE_ANON_KEY` or the current publishable-key variable recommended by the installed Supabase tooling

Server-only examples:
- `SUPABASE_SERVICE_ROLE_KEY` or the current secret key name recommended by Supabase
- Payment, email, webhook and third-party credentials

Rules:
- Commit only a redacted `.env.example`.
- Never put a service-role/secret key in a `VITE_` variable.
- Never print secret values in logs, diagnostics or final reports.
- Validate required environment variable names at startup with actionable, non-secret errors.
- Keep Preview and Production credentials separated where supported.

## 4. Supabase data security

- Enable RLS on tables exposed through the Data API.
- Write policies for each operation: SELECT, INSERT, UPDATE and DELETE.
- Use ownership or tenant predicates based on authenticated identity and explicit membership rules.
- Do not rely on hidden UI controls as authorization.
- Test policies using anonymous, ordinary, privileged and cross-user identities.
- Add database constraints for uniqueness, relationships and core invariants.
- Use migrations for schema and policy changes; review destructive SQL before execution.
- Keep privileged service-role operations in trusted server contexts only.
- Storage bucket visibility and object policies must match the sensitivity of uploaded files.

## 5. Authentication and roles

Define roles and permissions from actual business rules. A client-side role flag is presentation state, not proof of authorization.

- Verify sessions using the supported Supabase Auth APIs for the installed version.
- Enforce access at RLS, Edge Function, API or other trusted server boundaries.
- Do not trust arbitrary user-editable metadata as an authorization source.
- Validate redirect URLs against an explicit allowlist.
- Handle expired sessions, revoked users, OAuth callback errors and logout.
- Avoid leaking account existence or sensitive profile data in errors.

## 6. Vercel delivery

- Confirm Vite build command and output directory from the actual project, commonly but not universally `npm run build` and `dist`.
- Ensure SPA routes have an appropriate rewrite only when required by the selected router and hosting configuration.
- Verify preview and production environment variables separately.
- Do not assume Vercel functions and Supabase Edge Functions are interchangeable.
- Confirm where each server-side operation runs, what secrets it can access and its runtime limits.
- Use preview deployments for review before production promotion.

## 7. Critical tests

- Anonymous visitor cannot read or mutate protected records.
- Authenticated user can access only allowed rows and objects.
- User A cannot read or update User B's records by changing an identifier.
- Role escalation through client state or user metadata is rejected.
- Expired and invalid sessions fail safely.
- Duplicate form submission does not create duplicate consequential records.
- A successful UI mutation is reflected in durable database state.
- Failed network/database requests show useful feedback and preserve recoverable input.
- Preview and production builds use the correct environment configuration.

## 8. Source-of-truth rule

Supabase, Vite, React and Vercel APIs evolve. Use the current official docs and installed package types for version-specific implementation. This file is a security and architecture checklist, not a replacement for provider documentation.
