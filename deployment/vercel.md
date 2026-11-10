# Vercel Deployment

Use this module only when Vercel is the confirmed deployment target.

- Inspect project framework, root directory, build command, output directory, install command and Node version.
- Confirm production and preview environment variable names and scopes without printing secret values.
- Verify build locally or in CI before production deployment.
- Check framework-specific routing, serverless/edge runtime constraints and region requirements.
- Use preview deployments to review significant changes.
- Confirm domain, redirects, headers, caching and server function behavior.
- Inspect deployment logs and runtime logs after release.
- Define rollback or revert approach.

Do not assume a repository is linked to the intended Vercel project. Do not alter project settings, promote deployments, or deploy to production without authorization.
