# Albright Family Insurance Reporting Site

Static, self-contained performance dashboard for Albright Family Insurance, deployed on Vercel.

## Structure

- `index.html` — the dashboard (all styles, scripts, and images are inlined)
- `vercel.json` — Vercel config: clean URLs, security headers, `noindex` so the report stays out of search engines

## Deploying

No build step. In Vercel, import this repo with:

- **Framework Preset:** Other
- **Build Command:** *(leave empty)*
- **Output Directory:** *(leave empty — serves the repo root)*

Or from the CLI: `vercel --prod`

## Updating the report

Replace `index.html` with the new export and push to `main`; Vercel redeploys automatically.
