# Module Routing

Load only the material needed for the current task. This reduces distraction and keeps instructions proportional.

## Routing matrix

| Task | Read first | Add when needed |
|---|---|---|
| New application | project-discovery, product-planning, architecture | design, frontend, backend, security, testing |
| Existing application | project-discovery | only impacted modules |
| UI-only change | frontend-design, design-system | responsive-design, ux-accessibility, browser-testing |
| React performance | react-practices | performance-seo, testing-strategy |
| Forms | forms-validation | authentication-authorization, security, browser-testing |
| API feature | api-design | database-design, security, testing-strategy |
| Login / roles | authentication-authorization | security, database-design, browser-testing |
| Database change | database-design | security, testing-strategy, deployment/ci-cd |
| Supabase + React/Vite + Vercel | integrations/react-vite-supabase-vercel | supabase-rls-test-matrix, security, browser-testing |
| Supabase RLS/policy change | integrations/supabase-rls-test-matrix | database-design, authentication-authorization, testing-strategy |
| Independent feature acceptance | agents/evaluator-protocol | feature contract, browser-testing, code-review |
| Bug fix | project-discovery | code-review + test module for affected layer |
| Release | release-gate | performance-seo, vercel, ci-cd |

## Loading rules

1. Read the root `SKILL.md` once per task context.
2. Read no more than three specialist modules initially unless the task genuinely spans more domains.
3. Follow links to deeper modules only when a concrete need appears.
4. Prefer project-specific documentation and installed dependency versions over generic examples.
5. If two instructions conflict, prioritize: user constraints → repository rules → actual runtime/framework version → security requirements → this generic guidance.
6. Do not load modules merely because they exist.
