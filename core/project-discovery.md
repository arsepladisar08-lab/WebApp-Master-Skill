# Project Discovery

## Goal

Build an evidence-based understanding of the application before making changes.

## Checklist

- [ ] Confirm working directory and Git branch/status.
- [ ] Read repository guidance: `AGENTS.md`, `CLAUDE.md`, `README.md`, package scripts and relevant docs.
- [ ] Identify framework, language, runtime, package manager, lockfile and dependency versions.
- [ ] Identify app entry points, routes, components, API handlers, data access and auth boundaries.
- [ ] Identify environment variable names without exposing their values.
- [ ] Identify test, lint, typecheck, build and deployment commands.
- [ ] Trace the requested flow from UI to server/data and back.
- [ ] Note existing conventions and tests that must remain valid.

## Safe inspection

Prefer read-only inspection first. Do not print secret values. Do not run destructive migrations, deployment commands, resets, or broad dependency upgrades as part of discovery.

## Discovery output

For non-trivial tasks, summarize:
- Confirmed stack and versions.
- Relevant files and data flow.
- Existing conventions worth preserving.
- Risks and unknowns.
- Proposed smallest implementation path.
