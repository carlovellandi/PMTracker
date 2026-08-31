# Summer 2027 PM / APM Recruiting Dashboard

Snapshot: 2026-08-31

## GitHub Pages files

Upload these four files **directly to the repository root**:

```text
/
├── index.html
├── data.js
├── .nojekyll
└── README.md
```

Do not upload the private `pm_dashboard_progress_*.json` backup to a public repository.

## What changed in this refresh

- Expanded from 68 to 96 tracked companies / opportunity groups.
- Added newly surfaced 2027 opportunities including Goldman Sachs AWM Product Management, PIMCO Product Strategy, BNY Product Management, GE Vernova Controls Product Management, Workiva PM, Skydio Hardware PM, OpusClip AI PM, Eudia Product, DTCC, Pentair LDP/PM, IBM PM, Capital One BA/product-adjacent, and a long-tail live scan.
- Google APM is marked **Opening soon** with user-provided recruiting intel of **September 22, 2026**. That exact date is intentionally labeled unverified until Google posts the requisition.
- Microsoft is marked **Verify now** because current PM recruiting trackers show the requisition open while some secondary campus sources previously showed an August 27 close.
- Hard/likely eligibility problems are now explicit for roles such as Amazon MBA PMT, Appian CS/CE PM, Relay's Raleigh/Durham/Chapel Hill school restriction, and technical-major-heavy roles.
- Axon is Strategic Rank #1 conditional on the LDI→LDP / senior-access thesis.

## Progress storage and backup — fixed

Application progress is private and is stored in browser `localStorage`, not in public `data.js`.

The updated dashboard now:

1. flushes any currently edited status/date/notes before export;
2. re-reads persisted browser state before building the JSON;
3. **refuses to silently download an empty backup** and warns you if no progress is present;
4. exports a versioned file named `pm_dashboard_progress_YYYY-MM-DD.json`;
5. includes saved-entry counts in the JSON;
6. imports by **merging** with current browser state rather than wiping it;
7. migrates only the original TikTok application and the exact original six AmEx requisitions, so newly added roles are not falsely marked Applied.

Important: `localStorage` is scoped to the exact browser + site origin. If you switch browsers, devices, repository URL, GitHub Pages domain/path, or open the HTML from a different origin, that browser context cannot magically read progress saved under the old origin. Use the private export/import JSON to move state safely.

## GitHub Pages setup

1. Replace the four files at repository root.
2. Commit to `main`.
3. GitHub → **Settings → Pages**.
4. Deploy from branch `main`, folder `/(root)`.
5. Hard-refresh the site after deployment.

`index.html` loads `./data.js`, so both must remain at root.

## Updating later

- Public companies/roles/rankings live in `data.js`.
- UI, progress storage, import/export and migration logic live in `index.html`.
- Personal application progress should never be committed to a public repository.
