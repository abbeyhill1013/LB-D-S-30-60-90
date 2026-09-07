# estimating/

The estimate model and the conventions that keep estimates comparable across
patterns and engagements.

Planned contents:

- `estimate-model.xlsx` — the working estimate model. Excel because
  calculation is the point.
- `conventions.md` — how to estimate: always start from a pattern + band,
  never from a blank page; how to handle deals that don't cleanly fit an
  existing pattern; how contingency is applied
- `pattern-actuals-log.csv` — one row per phase/task on a closed engagement:
  planned hours (from the pattern's band) vs. actual, with variance. This is
  the historical-variance input the estimate assistant surfaces alongside a
  new estimate — if a pattern has been running 25% over, the estimator sees
  that at the point of estimating, not after the fact. CSV, not Excel, so it
  diffs cleanly in git as rows accumulate. Log a row per closed engagement;
  do not overwrite prior rows.

This feeds Tool #2 (estimate assistant) in `tools/` — pattern library +
historical actuals -> BOE draft.

See `TRACKER.md` in the repo root for current build status.
