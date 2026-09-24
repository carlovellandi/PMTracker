# Summer 2027 PM / APM Recruiting Dashboard

Snapshot: 2026-09-24  
Build: 2026-09-24.1

## Upload these files to the GitHub repository root

```text
/
├── index.html
├── data.js
├── data-2026-09-24-v1.js
├── .nojekyll
└── README.md
```

The versioned data file is intentional. It prevents an older cached `data.js` from making the site look stale.

## Private progress

Do **not** upload your progress JSON to a public GitHub repository.

The site stores application state in browser localStorage and supports:
- company-level status and notes
- application-level status and notes
- applied dates
- next steps
- next-step dates
- export/import backups

Use `pm_dashboard_progress_2026-09-24_UPDATED_PRIVATE.json` only with the site's **Import progress** button.

## Views

- **Action queue** — open roles you have not already submitted, sorted by action score.
- **Applications** — your actual recruiting pipeline, sorted Offer → Interviewing → Applied → Rejected/Withdrawn. Jane Street's Oct. 7 interview appears here as a next step.
- **Open now** — all currently tracked open roles.
- **Opening soon** — roles expected to open shortly.
- **Watchlist** — future/uncertain targets that should not clutter the action queue.
- **All targets** — full tracked universe.
- **Weekly system** — current recruiting priorities and triggered processes.

## Immediate queue as of Sep. 24, 2026

1. Visa APM — application sprint closes Sep. 24/25.
2. Duolingo APM — deadline Oct. 7/8.
3. Intuit Product Manager / RPM — live.
4. Skydio Hardware Product Management — live.
5. Mastercard Product Management — newly live.
6. Coinbase APM — live; only prioritize if you can honestly articulate substantive crypto/onchain interest.
7. Workiva Product Management — closes Sep. 27/28.
8. Goldman Sachs AWM Product Management — open, including Dallas.
9. PwC TIDE Product Management — closes Sep. 26; Dallas available.
10. Dedalus Labs Product Manager — rolling.
11. Capital One Business Analyst — live, including Plano.
12. PGIM Product & Institutional Client — closes Sep. 28.
13. Northern Trust Digital Client/Product — closes Oct. 9.
14. Amgen Digital Product — live and Business is explicitly a preferred field.
15. Pentair Product Management LDP Internship — excellent Economics/leadership-development fit.
16. Cox Automotive Product Management — Austin posting live.
17. DICK'S Sporting Goods Product Management — business-major-friendly.
18. U.S. Bank Product Management — live.
19. Dow Jones Business & Product Strategy — live.
20. Mutual of Omaha Product Owner — closes Sep. 30.

## Current process triggers

- **Jane Street:** Round 1 interview on Oct. 7, 2026. Interview prep outranks generic recruiting prep.
- **Axon:** application submitted; two first-year LDP referrals/connections now support the candidacy. Avoid unnecessary additional outreach and prepare when the process moves.
- **Google:** APM application submitted after the Sep. 22 opening.

## Deployment

GitHub → **Settings → Pages** → Deploy from a branch → `main` → `/(root)`.

After deploying, confirm the site visibly shows **Build 2026-09-24.1**. If you see an older build, append `?build=20260924-1` to the Pages URL once and hard-refresh.
