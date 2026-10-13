# Albright Family Insurance Reporting Site

Static, self-contained GOAL performance reports for Albright Family Insurance (#550), deployed on Vercel. Same layout as the other GOAL client report sites: a report hub at the root, one page per report.

## Structure

- `index.html`: report hub (cards linking to each report)
- `Albright-Performance-Dashboard-10-10-26.html`: performance dashboard, all time, snapshot Oct 10, 2026
- `Albright-Inbound-Call-Review-10-13-26.html`: inbound call review, Oct 1 to Oct 13, 2026
- `vercel.json`: Vercel config: clean URLs, security headers, `noindex` so the reports stay out of search engines

## Deploying

No build step. In Vercel, import this repo with:

- **Framework Preset:** Other
- **Build Command:** *(leave empty)*
- **Output Directory:** *(leave empty, serves the repo root)*

Or from the CLI: `vercel --prod`

## Adding a report

Add the report as its own `Albright-<Report-Name>-MM-DD-YY.html` page with an "All reports" link back to `index.html`, add a card for it in `index.html`, and push to `main`; Vercel redeploys automatically.
