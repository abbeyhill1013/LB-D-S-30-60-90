# Estimate Assistant

**Priority: 2**

## What it does

Given a pattern, band, and client deltas, drafts a basis of estimate with hours
by WBS element, plus SOW-ready assumptions and exclusions.

## Inputs
- `patterns/` — the selected pattern
- Pattern actuals log — historical variance for calibration
- Client-specific deltas, entered by the estimator

## Output
BOE draft plus SOW assumption and exclusion blocks.

## Design notes
- Three-point on the deltas, not on the base — the base comes from the band.
- Surface the historical variance for that pattern alongside the estimate. If
  a pattern has been running 25% over, the estimator should see that.
- Flag when deltas are large enough that the band selection is wrong.
- Never silently pad. Contingency is explicit and held at portfolio level.

## Status
Not started.
