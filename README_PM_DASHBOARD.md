# Summer 2027 PM / APM Tracker

Static GitHub Pages dashboard for Summer 2027 Product, APM, and high-upside adjacent recruiting.

## Files that belong in the GitHub repository root

- `index.html` — dashboard UI
- `data.js` — public role data, rankings, sources, and application descriptions
- `.nojekyll` — tells GitHub Pages to serve the static files directly
- `README.md` — these instructions

**Do not upload `pm_dashboard_progress_2026-08-26.json` to a public repository.** That file contains personal application statuses and notes. It is only for the dashboard's **Import progress** button.

## Recommended repository structure

```text
/
├── index.html
├── data.js
├── .nojekyll
└── README.md
```

Do not put these files inside a nested `pm_rebuild/`, `site/`, or `data/` folder. The dashboard loads `./data.js` from the same directory as `index.html`.

## GitHub website setup

### If you already have a repository for this dashboard

1. Open the repository on GitHub.
2. At the repository root, upload/replace `index.html` and `data.js`.
3. Add `.nojekyll` at the root.
4. Delete or ignore old generated filenames such as `PM_2027_index_v2.html` and `PM_2027_data_v2.js`; GitHub Pages needs the new root `index.html`, and that file expects root `data.js`.
5. Commit the changes.
6. Go to **Settings → Pages**.
7. Under **Build and deployment**, choose **Deploy from a branch**.
8. Select branch **main** and folder **/(root)**, then save.
9. Use the exact site URL GitHub displays in the Pages settings.

For a project repository named `pm-2027-dashboard`, the normal URL pattern is:

```text
https://YOUR-GITHUB-USERNAME.github.io/pm-2027-dashboard/
```

For the special repository named exactly `YOUR-GITHUB-USERNAME.github.io`, the normal URL is:

```text
https://YOUR-GITHUB-USERNAME.github.io/
```

### If you are creating a new repository

1. Create a repository, for example `pm-2027-dashboard`.
2. Upload the four repository files above directly to the root.
3. Commit them to `main`.
4. Enable Pages using **Settings → Pages → Deploy from a branch → main → /(root)**.
5. Open the URL GitHub shows under Pages.

## Restoring your application progress

The website intentionally keeps personal application statuses, dates, and notes in browser `localStorage` rather than publishing them in `data.js`.

- If you keep the same GitHub Pages URL and browser, your existing progress may already remain.
- If the URL changes or the progress does not appear, click **Import progress** and select `pm_dashboard_progress_2026-08-26.json`.
- Use **Export my progress** periodically as a backup, especially before changing the repository name or Pages URL.

## 404 checklist

If the site itself returns 404:

1. Confirm the repository root contains a file named exactly `index.html` (lowercase).
2. Confirm Pages is enabled from `main` and `/(root)`.
3. Confirm the URL uses the exact repository name, including hyphens/capitalization.
4. Confirm the files are not nested one folder deeper.
5. Open **Settings → Pages** and use the URL GitHub itself reports rather than a guessed URL.

If the page loads but role data is missing:

1. Confirm `data.js` is beside `index.html` at the repository root.
2. Confirm it is named exactly `data.js`.
3. Hard-refresh the page.
4. Open `https://YOUR-GITHUB-USERNAME.github.io/YOUR-REPO/data.js` directly. If that 404s, the file path/deployment is wrong.

## Local test

From the folder containing `index.html` and `data.js`:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Tracker logic

- **Strategic Rank**: long-run fit/upside for the broader PM → operator/founder/ownership plan.
- **Action Score**: what deserves attention now based on availability, timing, fit, and asymmetric access.
- **Strategic Track**:
  - Core PM
  - Narrative edge
  - Relationship edge
  - High-upside adjacent
  - Broad PM / optionality
  - Technical / likely ineligible

The dashboard opens to the **Action queue** by default and removes captured live applications from that queue once they are marked Applied/Interviewing/Offer/Passed.
