# Component Risk Assessment Dashboard — Publish Bundle

This bundle contains a shareable, publish-ready version of the dashboard and the underlying data files extracted from the current working HTML.

## Files
- `component-risk-assessment-dashboard.html` — working self-contained dashboard.
- `index.html` — duplicate entry file for static hosting.
- `data/component_risk_rows.json` and `.csv` — component-level scorecard data.
- `data/supplier_data.json` and `.csv` — supplier-level records shown in Supplier Data.
- `data/historical_supply_disruptions.json` and `.csv` — disruption event records.

## How to share
Send the ZIP file as-is. Anyone can unzip it and open `component-risk-assessment-dashboard.html` locally.

## How to publish
1. Unzip the folder.
2. Upload the full folder to GitHub Pages, Netlify, Vercel, SharePoint, or any static site host.
3. Use `index.html` as the entry page.

## Notes
- The HTML is self-contained and does not depend on the `data/` folder to run.
- The `data/` files are included for auditability, reuse, and future refactoring to external data loading.
- Nested values in the CSV exports are stored as JSON strings so no detail is lost.
