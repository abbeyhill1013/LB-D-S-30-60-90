# Margin Dashboard

Tool #3 — build third, after the estimate assistant is running.

Status: Not started. See `TRACKER.md` (Day 31-60).

## Purpose

One page, portfolio-wide: hours burned vs. milestones complete, for every
active engagement. This is where the 70/70 margin-watch rule becomes
visible instead of theoretical — flag any engagement at 70% hours burned
with under 70% of milestones complete.

## Inputs

- Engagement register (Microsoft Lists)
- Capacity/allocation (Microsoft Lists)
- Jira-synced hours (via the one-way Jira -> Lists sync)

## Output

Portfolio-wide margin view, one page. Feeds Automation #3 (margin watch),
which alerts on the same 70/70 threshold this dashboard displays. Exact
output template TBD — add here once decided.

## Design rule

Must reduce per-engagement effort or catch a problem earlier. This tool's
whole job is the second half of that rule: surfacing a margin problem
before it's unrecoverable on a fixed-fee engagement.

## Test data

Synthetic only. No client names, actual fees, margins, or CRM/Jira exports
— see the content boundary in `CLAUDE.md`.

## Open questions

- Refresh cadence — real-time off the Jira sync, or daily/weekly snapshot?
- Does this live as a Lists view, a Power BI report, or a generated
  one-pager?
