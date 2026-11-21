# Albright Family Insurance Reporting Site

Static, self-contained GOAL performance reports for Albright Family Insurance (#550), deployed on Vercel. Same layout as the other GOAL client report sites: a report hub at the root, one page per report.

## Structure

- `index.html`: report hub (Campaign Reports, Website & Research)
- `Albright-Campaign-Overview-Since-Launch-11-21-26.html`: all campaigns since launch (Jul 25, 2025 through Nov 21, 2026), with the Home (LM) lead marketplace section
- `Albright-Home-Campaign-Performance-Since-Launch-11-21-26.html`, `Albright-Home-After-Hours-Campaign-Performance-Since-Launch-11-21-26.html`, `Albright-Auto-Campaign-Performance-Since-Launch-11-21-26.html`: one page per campaign
- `Albright-Monthly-Sales-by-Source-11-21-26.html`: monthly sales by source and ad channel (Aid), with the ad channels that have the fewest quotes and binds
- `Albright-Source-ZIP-Sales-11-21-26.html`, `Albright-ZIP-Sales-11-21-26.csv`: sales by source, ad channel (Aid) and traffic tier, county and ZIP
- `Albright-Producer-Pipeline-11-21-26.html`: open quotes and sales by producer, from the Producer column of the Nov 19, 2026 quoted and sold list
- `Albright-Inbound-Call-Review-11-21-26.html`: inbound call review, Oct 23 to Nov 21, 2026
- `Albright-Most-Valuable-Prospect-11-21-26.html`: Most Valuable Prospect, the attribute values that hold the most Auto and Home binds in GOAL Analytics, with the lowest CPA marked
- `Albright-SEO-Audit-10-13-26.html`: agency web page SEO audit
- `Albright-TX-Hail-Storm-Risk-10-13-26.html`, `Albright-TX-Demographic-Research-10-13-26.html`, `Albright-TX-ZIP-Data-10-13-26.csv`: Texas market research
- `Albright-Performance-Dashboard-10-10-26.html`: earlier interactive dashboard (not linked from the hub)
- `vercel.json`: Vercel config: clean URLs, redirects from the 11-04-26 and 11-21-26 report URLs to the 11-21-26 pages, security headers, `noindex` so the reports stay out of search engines

## Deploying

No build step. In Vercel, import this repo with:

- **Framework Preset:** Other
- **Build Command:** *(leave empty)*
- **Output Directory:** *(leave empty, serves the repo root)*

Or from the CLI: `vercel --prod`

## Adding a report

Add the report as its own `Albright-<Report-Name>-MM-DD-YY.html` page with an "All reports" link back to `index.html`, add a card for it in `index.html`, and push to `main`; Vercel redeploys automatically.
