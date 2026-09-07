# Status Generator

Tool #1 — build first. Biggest recurring time drain at 15 engagements.

Status: Not started. See `TRACKER.md` (Day 0-30).

## Purpose

Turn Jira issue activity and the RAID log into a weekly status draft for
each engagement, so a PM covering 9-15 engagements isn't assembling status
by hand every week.

## Inputs

- Jira (technical execution data, synced one-way into Microsoft Lists per
  the architecture in `CLAUDE.md` — never read/write Jira directly for
  portfolio reporting)
- RAID list (Microsoft Lists)
- Engagement register (Microsoft Lists) — for tier, pattern, and band context

## Output

Drafts into `templates/status-report.md`. If that template changes, this
tool needs updating — the output contract runs template -> tool, not the
other way around.

## Design rule

Must reduce per-engagement effort, not add to it. A generator that requires
as much manual cleanup as writing status from scratch is a net loss at this
volume.

## Test data

Synthetic only. No client names, engagement data, fees, or Jira/CRM exports
— see the content boundary in `CLAUDE.md`.

## Open questions

- Draft quality bar: fully client-ready, or PM-reviewed-then-sent?
- Per-tier behavior: does Tier C get a lighter draft than Tier A?
