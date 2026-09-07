# Estimate Assistant

Tool #2 — build second, after the status generator is running.

Status: Not started. See `TRACKER.md` (Day 31-60).

## Purpose

Combine a selected engagement pattern and band with historical actuals to
produce a basis-of-estimate (BOE) draft. Estimating always starts from a
pattern and a band, never from a blank page — this tool is what makes that
practical instead of aspirational.

## Inputs

- Pattern library (`patterns/`, one file per pattern, following
  `patterns/_PATTERN-TEMPLATE.md`)
- Historical actuals (hours by phase/task from closed engagements)
- `estimating/estimate-model.xlsx` and `estimating/conventions.md`

## Output

BOE draft. Feeds into the estimating model and, downstream, the SOW
guardrails in `templates/sow-guardrails.md`. Exact output template TBD —
add here once decided.

## Design rule

Must reduce per-engagement effort, not add to it. If using this tool takes
longer than pulling the pattern file and eyeballing the band, it has failed.

## Test data

Synthetic only. No client names, actual fees, margins, or CRM/Jira exports
— see the content boundary in `CLAUDE.md`.

## Open questions

- Where do historical actuals live — Lists, the estimate model, or a
  separate actuals log this tool reads from?
- How does contingency get applied — inside this tool, or left to the
  estimator after the draft?
