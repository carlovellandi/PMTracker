# Summer 2027 Product / APM Recruiting Dashboard

Snapshot: **2026-09-06**

Static GitHub Pages dashboard for Summer 2027 product management, APM, product strategy, and high-upside adjacent recruiting.

## GitHub Pages files

Upload these four files **directly to the repository root**:

```text
/
├── index.html
├── data.js
├── .nojekyll
└── README.md
```

`index.html` loads `./data.js`, so keep them beside each other at the repository root.

## What changed in the Sep. 6 refresh

- Expanded to **114 tracked target companies / opportunity groups**.
- Normalized public role status into six clean buckets: **Open now, Opens soon, Watch, Future, Closed, Ineligible**.
- Normalized strategy into seven categories:
  - General Management / Leadership
  - Core PM / APM
  - Product + Strategy
  - Fintech / Investing
  - Consumer / Marketplace
  - Travel / Hospitality
  - Technical Stretch / Ineligible
- Added a dedicated **Applied** tab that shows each submitted requisition separately, including stage, applied date, role status, category, location, notes, and posting.
- Action queue now contains only **Open now / Opens soon** opportunities that are not already fully handled.
- Added separate **Open now**, **Opening soon**, **Watchlist**, and **All targets** views.
- Added smart sorting by view plus optional strategic-rank, action-score, company, and status sorts.
- Progress statuses are now: Not started, Researching, Networking, Ready to apply, Applied, Interviewing, Offer, Rejected, Skipped.
- Legacy `Passed / skipped` progress automatically migrates to `Skipped`.
- Old Axon Boston/Scottsdale application keys automatically consolidate into the new single replacement-application record.
- Microsoft Summer 2027 PM is marked **Closed**; stale third-party listings do not override the manually checked application status.
- Google APM is marked **Opens soon** with Sep. 22 retained as recruiting intel, explicitly labeled as not independently verified.
- New/currently surfaced opportunities include Roblox, Xpansiv, West Monroe, HP, Vanguard, Northern Trust, The Home Depot, PGIM, PwC, Medline, US Foods, Chamberlain, Tencent, TELUS Digital, Allied Solutions, Oshkosh, RLI, and HARMAN watch status, alongside refreshed existing targets.

## Tabs

- **Action queue** — the highest-urgency Open now / Opens soon roles that still need action.
- **Applied** — every individual requisition you have submitted, sorted by stage, then known applied date, then strategic rank.
- **Open now** — all currently tracked open opportunities.
- **Opening soon** — announced / strongly expected upcoming roles.
- **Watchlist** — companies worth monitoring where no clean current undergraduate Summer 2027 role is confirmed.
- **All targets** — strategy-first universe, sorted by Strategic Rank by default.
- **Weekly system** — recruiting operating rules and prep priorities.

## Personal progress

Application progress is stored in browser `localStorage` and is **not** embedded in public `data.js`.

The dashboard keeps the existing storage keys so upgrading the GitHub files should preserve progress when you use the same Pages URL and browser.

Use **Export my progress** periodically. Export now:

- flushes any open edits before saving,
- re-reads the persisted browser state,
- records company/application counts,
- and refuses to silently download an empty backup.

**Do not commit a private progress JSON to a public GitHub repository.**

If progress is missing after a redeploy or browser change, use **Import progress**. Import merges with existing browser progress instead of wiping newer state.

## GitHub Pages setup

1. Repository → **Settings → Pages**.
2. Build and deployment → **Deploy from a branch**.
3. Branch: `main`; folder: `/(root)`.
4. Save and use the exact Pages URL GitHub reports.
5. Hard-refresh after replacing `data.js` or `index.html`.

## Status methodology

`Open now` is intentionally conservative. A role is put there when a current employer page, a currently verified internship feed, or a successfully submitted application supports present availability. Third-party discovery feeds can lag or misclassify openings, so conflicting cases are pushed to Watch / Human Check rather than treated as unquestionably live.

`Action Score` is **current urgency**, not prestige. `Strategic Rank` is long-run fit/upside for the broader operator/founder/ownership path.

## Updating later

For a data-only refresh, replace `data.js`.

If tabs, sorting, progress logic, or the application UI changes, replace both `index.html` and `data.js`.
