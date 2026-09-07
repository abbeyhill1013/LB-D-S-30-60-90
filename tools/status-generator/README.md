# Status Report Generator

**Priority: 1** — the biggest recurring time drain. At 15 engagements, writing
status by hand is most of a workday every week.

## What it does

Reads engagement state, drafts a status report per engagement in the standard
format, routes to review. Target: 5 minutes of editing per report instead of
30-40 minutes of writing.

## Inputs
- Jira: issue status, completions, blockers for the engagement's project
- Lists: RAID entries, milestone status, hours burned
- Previous week's status (for continuity — "next period" becomes "completed")

## Output
`templates/status-report.md`, populated, one file per engagement.

## Design notes
- Draft, never send. A human reviews every one.
- Green engagements still get a report; the point is async status replacing
  meetings, not skipping communication.
- Internal margin footer is stripped from the client-facing version.
- Narrative section is the hard part — it must read as written, not generated.
  Feed it the previous week for continuity.

## Status
Not started.
