# Margin Dashboard

**Priority: 3**

## What it does

Portfolio-wide view of hours burned vs. milestones complete, one page.

## The 70/70 rule

Flag any engagement at 70% hours burned with under 70% of milestones complete.
On fixed-fee, catching drift at 70% rather than 100% is the difference between
a change order and an absorbed loss.

## Inputs
- Hours logged per engagement
- Milestone completion from Lists
- Fee and target margin from the engagement record

## Output
Single-page view plus an alert feed. Feeds automation #3.

## Design notes
- Continuous, not monthly. A monthly margin review is a postmortem.
- Alert must be actionable: which engagement, how far off, what the change
  order conversation would cover.

## Status
Not started.
