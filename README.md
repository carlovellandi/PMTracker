# Summer 2027 PM / APM Recruiting Dashboard

Snapshot: 2026-08-26

## GitHub Pages files

Upload these files **directly to the repository root**:

```
/
├── index.html
├── data.js
├── .nojekyll
└── README.md
```

Do not rename `index.html` or `data.js`. The page loads `./data.js`.

## GitHub Pages setup

1. GitHub repo → **Settings** → **Pages**.
2. Under Build and deployment choose **Deploy from a branch**.
3. Branch: **main**; folder: **/(root)**.
4. Save.
5. Open the Pages URL GitHub shows.

If the old site returns 404, confirm the repository still exists and Pages is enabled on `main` / `(root)`.

## Personal progress

Application progress is stored in browser localStorage and is **not** embedded in public `data.js`. Use **Import progress** inside the dashboard to restore the separate progress JSON. Do not commit the progress JSON to a public repo.

## Compensation methodology

The dashboard now shows **Year 1 FT TC** and **Year 3 FT TC**. These mean annualized total compensation, not base salary.

- **Year 1:** plausible new-grad/APM-equivalent package after a hypothetical internship conversion.
- **Year 3:** directional package after about two years of progression. It is not a promised promotion.
- A reported company PM level is treated as a verified Year-1 benchmark only if it genuinely maps to APM/new-grad/roughly 0–2 years experience.
- If Levels.fyi's first populated PM level is an experienced level (e.g. DoorDash E4 or Stripe L2), the dashboard uses a clearly marked estimate instead of pretending that experienced level is new-grad compensation.
- Private-company equity and travel/hospitality product compensation are intentionally broad/low-confidence.

## Updating

Public role data lives in `data.js`. Browser progress can be exported/imported from the site. For future refreshes, replace `data.js` while leaving `index.html` unchanged unless the UI itself is being updated.
