# WebApp Master Skill

A modular, framework-aware skill system for planning, designing, implementing, testing, securing, and shipping production-minded web applications.

**Default language:** English for agent instructions. Project-facing copy follows the user's requested language.

## What this repository is

WebApp Master Skill is an orchestration layer plus focused engineering playbooks. It is designed to help an AI coding agent work with an existing repository or build a new WebApp without confusing visual completeness with functional completeness.

It does not prescribe one universal stack. The project brief, existing codebase, operational constraints, and user preferences determine the stack.

## Quick start

1. Read [SKILL.md](SKILL.md).
2. For a new application, follow [workflows/new-webapp.md](workflows/new-webapp.md).
3. For an existing codebase, follow [workflows/existing-webapp.md](workflows/existing-webapp.md).
4. Load only the specialist modules needed for the current task. See [core/module-routing.md](core/module-routing.md).
5. Verify work using [quality/release-gate.md](quality/release-gate.md).

## Repository map

```text
.
├── SKILL.md
├── README.md
├── CHANGELOG.md
├── LICENSE
├── core/          # Intake, planning, architecture, routing and execution
├── design/        # Visual direction, design systems, responsive and UX review
├── frontend/      # React, components, state, forms and frontend security
├── backend/       # APIs, data, auth and application security
├── quality/       # Testing, review, accessibility, performance and release gates
├── deployment/    # Vercel, CI/CD and production readiness
├── workflows/     # New app, existing app, feature, redesign and bug-fix flows
└── references/    # Stack selection, evidence and source attribution
```

## Design principles

- Inspect before changing; preserve working behavior and established conventions.
- Plan proportionally: do not turn a small bug fix into a full discovery ceremony.
- Prefer the smallest coherent change that satisfies the acceptance criteria.
- Treat accessibility, responsive behavior, security, and error states as product requirements.
- Use real project dependencies and verify APIs against installed versions and official documentation.
- Never claim a feature works based only on generated code or a successful build.
- Keep secrets out of source control and never fabricate production credentials, data, or test results.
- Avoid default-looking interfaces: design choices must follow the product, audience, content, and brand.

## Portability

The main skill uses Markdown instructions and does not require one specific agent runtime. Some optional workflows may reference tools such as Playwright, GitHub Actions, or Vercel; use the equivalent available tool when the named one is unavailable. Do not pretend a tool was invoked if it was not.

## Sources and attribution

See [references/source-map.md](references/source-map.md) for upstream repositories and the scope of adaptation. This project is an independent, selective synthesis—not a verbatim mirror of upstream skill packs. Refer to upstream licenses before copying any substantial text or code.

## Status

Initial foundation release. Specialist modules are intentionally concise and should be expanded through real project use, tests, and version-specific documentation review.
