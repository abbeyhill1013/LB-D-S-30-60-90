# Internal Tools

Build order is payback order. Do not skip ahead.

| # | Tool | Directory | Purpose |
|---|---|---|---|
| 1 | Status generator | `status-generator/` | Jira + RAID -> weekly status drafts |
| 2 | Estimate assistant | `estimate-assistant/` | Pattern + actuals -> BOE draft |
| 3 | Margin dashboard | `margin-dashboard/` | Burn vs. completion, portfolio-wide |
| 4 | Closeout drafter | (later) | Engagement record -> closeout memo |
| 5 | QBR assembler | (later) | Outcomes, utilization, proposal |

## Design rule

Every tool must reduce per-engagement effort or catch a problem earlier. At
9-15 concurrent engagements, a tool that adds per-engagement work is a net loss
regardless of how good its output is.

## Output contract

Tools output to the templates in `templates/`. If a template changes, its tool
needs updating.

## Test data

Synthetic only. See the content boundary in CLAUDE.md.

---

See `TRACKER.md` in the repo root for current build status.
