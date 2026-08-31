# Construction scraper maintenance patch

- Preserves hourly unseen-job behavior and existing `seen_links.csv`.
- Normalizes ATS posting timestamps to `YYYY-MM-DD` where possible.
- Lever uses its API creation/update timestamp instead of hardcoded `N/A`.
- iCIMS/generic job-detail and SuccessFactors pages attempt JSON-LD/text posting-date extraction.
- Uses `Unknown` only when a source does not expose a reliable posting date.
- Adds GitHub Actions concurrency protection.
- Uses `git pull --rebase` before push to reduce `fetch first` failures.
- Uses `git add -A`, so optional generated files do not cause pathspec failures.

Do not delete `seen_links.csv` when installing this patch.
