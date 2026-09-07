# Delivery Operations — Working Context

This repo holds the methodology, templates, and internal tooling for a delivery
and services department. Read this file before doing anything in this repo.

---

## What this department is

A greenfield delivery and services function covering project management,
customer success, and services delivery. One to three people over the first
twelve months, managing 9-15 concurrent engagements.

**Revenue model:** fixed-fee projects plus product/license resale.
There is no time-and-materials work. This matters more than anything else in
this file — on fixed-fee, unmanaged scope is margin already spent, not a
billing conversation.

**Who delivers:** founders/engineers and dedicated consultants. The department
does not perform technical delivery; it scopes, mobilizes, coordinates,
protects margin, and owns renewal and expansion revenue.

**The governing constraint:** 9-15 concurrent engagements at 1-3 people is
3-5x a normal PM load. It only works if engagements collapse into a small
number of repeatable patterns and if not every engagement receives equal
attention. Anything built here should reduce per-engagement effort or catch
problems earlier. If a proposed tool or process adds per-engagement work,
it is the wrong tool.

---

## Content boundary — important

This repo contains **generic methodology only**. Templates, structures,
estimating logic, tooling.

It must not contain:
- Client names or identifying details
- Actual engagement data, fees, or margins
- CRM or Jira exports
- Employer-specific pricing, rates, or contract language

Populated versions live in the work environment, not here. When generating
examples, use placeholders (`[CLIENT]`, `[PATTERN]`, `<fee>`) or clearly
fictional names.

---

## Repo map

| Path | Contents |
|---|---|
| `docs/` | The department blueprint — org design, processes, rollout plan |
| `TRACKER.md` | Build and rollout tracker. Update it as work completes. |
| `patterns/` | Engagement Pattern Library — one file per delivery pattern |
| `templates/` | SOW guardrails, mobilization packet, status, closeout, QBR |
| `estimating/` | Estimate model and estimating conventions |
| `tools/` | Internal tooling builds |
| `automations/` | Power Automate flow definitions and specs |
| `metrics/` | Metric definitions and reporting logic |

---

## Core concepts (use this vocabulary consistently)

**Engagement Pattern** — a repeatable engagement type with a fixed scope
boundary, hour bands, standard assumptions and exclusions, standard WBS, and a
target margin. Estimating starts by selecting a pattern and a band, never from
a blank page. Patterns live in `patterns/`, one file each, following
`patterns/_PATTERN-TEMPLATE.md`.

**Band** — small / standard / complex within a pattern. Each pattern defines
the single variable that drives the band (endpoint count, data source count,
number of agencies, etc.).

**Mobilization Packet** — the artifact that replaces the sales-to-delivery
handoff conversation. No packet, no provisioning. The friction is intentional.

**Tier (A/B/C)** — engagement service level by fee and risk. Tier A gets full
PM attention and QBRs; Tier C is async and exception-managed. Roughly 3/7/5
across 15 engagements.

**Margin watch** — the 70/70 rule: flag any engagement at 70% hours burned with
under 70% of milestones complete. This is the single most valuable automation
in the system.

**Horizons** — how roles are split. Forward (scoping, commercial, expansion),
Present (weekly cadence, hygiene, reporting), Deep (technical delivery).
Roles are split by horizon, not by PM/CS/Delivery function.

---

## System architecture

- **Microsoft Lists** is the portfolio system of record: engagement register,
  capacity/allocation, RAID, expansion pipeline.
- **Jira** is for technical execution only. It already exists in the
  environment. Do not build portfolio reporting inside Jira.
- **Sync direction is Jira -> Lists**, one way. Never the reverse.
- **Power Automate** handles triggers and provisioning.
- **SharePoint/Teams** hold engagement workspaces, provisioned from templates.
- **No PSA tool.** Not until ~20+ concurrent engagements or 5+ delivery staff.
  Build so a later migration is possible, but do not pre-build for it.

---

## Conventions

**Writing style for all generated artifacts:** plain, direct, professional.
Short sentences. No filler, no consultant-speak, no em-dash asides. Client-facing
documents should read as though a competent person wrote them quickly, not as
though they were generated.

**File format:** markdown for anything that is primarily text. Excel only where
calculation is the point (estimate model, margin tracking).

**PDF generation:** use locally available fonts (Liberation Sans, DejaVu Sans
Mono). Do not import Google Fonts.

**Graphics:** prefer inline SVG over CSS border-radius for shaped elements.

**Placeholders:** square brackets for user-supplied values — `[CLIENT NAME]`,
`[PATTERN]`, `[BAND]`.

---

## Build priority

Tools, in order of payback:

1. Status report generator — biggest recurring time drain at 15 engagements
2. Estimate assistant — pattern library + historical actuals -> BOE draft
3. Margin dashboard — burn vs. completion, portfolio-wide, one page
4. Closeout memo drafter — includes expansion signal extraction
5. QBR pack assembler

Automations, in order of payback:

1. Engagement provisioning (Closed Won -> full workspace setup)
2. Weekly status auto-draft
3. Margin watch (70/70 rule)
4. Capacity refresh
5. Milestone -> invoice trigger
6. Closeout -> expansion touchpoints
7. Renewal risk monitor

Do not build 4-7 before 1-3 are running.

---

## When working in this repo

- Update `TRACKER.md` when a tracked item completes. Do not create parallel
  task lists elsewhere.
- New patterns follow `patterns/_PATTERN-TEMPLATE.md` exactly. Consistency
  across patterns is what makes estimates comparable, which is what makes
  estimate accuracy measurable.
- The pattern library is refreshed quarterly against actuals. A stale library
  is worse than no library, because people stop trusting it and revert to
  bespoke estimating.
- Commit with meaningful messages. The history is a dated record of what was
  built and when.
