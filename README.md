# Construction Entry-Level Job Scraper — FINAL

Automated US construction/civil job scraper focused on full-time entry-level through 2 years of required experience.

## Outputs
- `current_jobs.csv` — all matching jobs found in the latest run.
- `new_jobs.csv` — only jobs not already in `seen_links.csv`.
- `seen_links.csv` — deduplication history; keep this file.
- `source_health.csv` — latest per-company source status and match counts.
- `DD-Month-Construction-Jobs.md` — cumulative human-readable history.

## Important filters
- US jobs only.
- Explicit required minimum experience above 2 years is rejected.
- Internships/co-ops are excluded.
- Technology/semiconductor sources use stricter construction/facilities/capital-project title rules to prevent generic engineering false positives.
- Ordinary marketing/service pages are never treated as jobs.
