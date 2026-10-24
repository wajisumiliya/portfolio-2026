# Cloudflare Pages deployment

This portfolio is a React + Vite frontend built with Node.js tooling, suitable for Cloudflare Pages.

## Deploy using GitHub

1. Open https://dash.cloudflare.com/ and navigate to Workers & Pages.
2. Create an application > Pages > Connect to Git.
3. Authorize GitHub, then select `wajisumiliya/portfolio-2026`.
4. Use:
   - Project name: `portfolio-2026` (or another available name)
   - Production branch: `main`
   - Framework preset: React (Vite)
   - Build command: `npm run build`
   - Build output directory: `dist`
   - Root directory: `/`
5. Save and deploy. Cloudflare assigns a `*.pages.dev` URL.
6. Confirm that the homepage loads, navigation and theme toggle work, project links open correctly, and `/api/health` responds.
7. New GitHub pushes to `main` trigger new production deployments.

The React site is statically hosted; Node.js powers local development and the Vite build. A Pages Function supplies `/api/health` on Cloudflare. The Express server in `server.js` is an optional alternative for Node hosting, not used by Cloudflare Pages.

Do not place credentials in GitHub source files. Restrict any future APIs and do not publicly expose business/employee data.
