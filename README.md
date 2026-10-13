# Albright Family Insurance Reporting Site

Static, self-contained GOAL performance reports for Albright Family Insurance (#550), deployed on Vercel. Same layout as the other GOAL client report sites: a report hub at the root, one page per report.

## Structure

- `index.html`: report hub (Campaign Reports, Website & Research)
- `Albright-Campaign-Overview-Since-Launch-10-13-26.html`: all campaigns since launch (Jul 25, 2025 through Oct 13, 2026)
- `Albright-Home-Campaign-Performance-Since-Launch-10-13-26.html`, `Albright-Home-After-Hours-Campaign-Performance-Since-Launch-10-13-26.html`, `Albright-Auto-Campaign-Performance-Since-Launch-10-13-26.html`: one page per campaign
- `Albright-Inbound-Call-Review-10-13-26.html`: inbound call review, Oct 1 to Oct 13, 2026
- `Albright-SEO-Audit-10-13-26.html`: Allstate agent page SEO audit
- `Albright-TX-Hail-Storm-Risk-10-13-26.html`, `Albright-TX-Demographic-Research-10-13-26.html`, `Albright-TX-ZIP-Data-10-13-26.csv`: Texas market research
- `Albright-Performance-Dashboard-10-10-26.html`: earlier interactive dashboard (not linked from the hub)
- `vercel.json`: Vercel config: clean URLs, security headers, `noindex` so the reports stay out of search engines

## Deploying

No build step. In Vercel, import this repo with:

- **Framework Preset:** Other
- **Build Command:** *(leave empty)*
- **Output Directory:** *(leave empty, serves the repo root)*

Or from the CLI: `vercel --prod`

## Adding a report

Add the report as its own `Albright-<Report-Name>-MM-DD-YY.html` page with an "All reports" link back to `index.html`, add a card for it in `index.html`, and push to `main`; Vercel redeploys automatically.
