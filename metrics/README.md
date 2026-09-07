# metrics/

Metric definitions and reporting logic for the portfolio. Definitions live
here once; every dashboard and report references them rather than
redefining thresholds inline.

Planned contents:

- `definitions.md` — canonical metric definitions: hours burned, % milestones
  complete, the 70/70 margin-watch threshold, tier distribution (3/7/5),
  expansion pipeline value, renewal risk score
- `reporting-logic.md` — how each metric is calculated from Microsoft Lists
  and Jira-synced data, and at what cadence it refreshes

See `TRACKER.md` in the repo root for current build status.
