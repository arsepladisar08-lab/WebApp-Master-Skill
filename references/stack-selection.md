# Stack Selection Reference

This is a decision aid, not a mandate. Existing projects should normally keep their established stack.

## Questions

- Is the product mostly content/public pages, an interactive authenticated application, or both?
- Is SEO/server rendering critical?
- Does the team already know a framework?
- Are there existing APIs, databases, identity providers or hosting constraints?
- What are the traffic, real-time, file storage, compliance and cost needs?
- Who will maintain the application?

## Common options

| Need | Options to evaluate |
|---|---|
| React app with straightforward client routing | Vite + React |
| React with integrated server rendering/routing | Next.js or another suitable React meta-framework |
| Lightweight content-first site | Astro |
| Backend API | Existing platform, Node.js framework, Python framework, Laravel, or managed backend |
| Managed auth/data | Supabase, Firebase, or an established provider |
| Relational data and transactions | PostgreSQL or another suitable relational database |
| Deployment | Existing platform first; otherwise Vercel, Cloudflare, Netlify, or container hosting |

## Decision rule

Choose the simplest stack that satisfies the product's requirements, hosting constraints, security model and maintenance capacity. Record limitations and migration cost. Verify current versions and provider capabilities before implementation.
