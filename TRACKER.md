# Build & Rollout Tracker — 30/60/90

This is the single tracker for standing up the delivery operations
department described in `CLAUDE.md`. Update it as work completes. Do not
create parallel task lists elsewhere.

Sequencing follows the department's own rules:

- System of record (Microsoft Lists) and workspace provisioning come first —
  nothing else has anywhere to live without them.
- Tools are built in payback order (status report generator first, QBR pack
  assembler last).
- Automations 4-7 are not started until automations 1-3 are running. Building
  capacity refresh or a renewal risk monitor before provisioning and margin
  watch are live is solving a problem the department doesn't have staff to
  feel yet.

**Status values:** Not started · In progress · Blocked · Done

**Target dates below** are calculated from a start date of 2026-09-07.
Replace with your actual kickoff date if different — Day 30 = start + 30
days, Day 60 = start + 60 days, Day 90 = start + 90 days.

| Horizon | Target date |
|---|---|
| Day 30 | 2026-10-07 |
| Day 60 | 2026-11-06 |
| Day 90 | 2026-12-06 |

---

## Day 0–30 — Foundation

Goal: the portfolio has somewhere to live, and the single highest-payback
tool and automation are running. Nothing here is optional — everything in
Day 31–90 depends on this layer existing.

### System of record

| Item | Status | Owner | Notes |
|---|---|---|---|
| Repo scaffold + `CLAUDE.md` in place | Done | | Initial structure committed. |
| Microsoft Lists: engagement register | Not started | | |
| Microsoft Lists: capacity/allocation | Not started | | |
| Microsoft Lists: RAID | Not started | | |
| Microsoft Lists: expansion pipeline | Not started | | |
| SharePoint/Teams workspace template | Not started | | Provisioned per engagement by Automation #1 below. |

### Org design & tiering

| Item | Status | Owner | Notes |
|---|---|---|---|
| `docs/org-design.md` — horizons + role split | Not started | | Forward / Present / Deep, not PM/CS/Delivery. |
| `docs/tiering.md` — Tier A/B/C definitions | Not started | | Target distribution ~3/7/5 across 15 engagements. |

### Pattern library & templates (v1)

| Item | Status | Owner | Notes |
|---|---|---|---|
| `patterns/_PATTERN-TEMPLATE.md` | Done | | Template built; new patterns must follow it exactly. |
| First engagement pattern(s) drafted | Not started | | Start with the 1-2 most common engagement types. |
| `templates/mobilization-packet.md` | Not started | | No packet, no provisioning — the friction is intentional. |
| `templates/sow-guardrails.md` | Not started | | Keyed to pattern + band. |

### Tool #1 — Status report generator

| Item | Status | Owner | Notes |
|---|---|---|---|
| v1 shipped and in use on at least one engagement | Not started | | Biggest recurring time drain at 15 engagements — build this first. |

### Automation #1 — Engagement provisioning

| Item | Status | Owner | Notes |
|---|---|---|---|
| Closed Won → full workspace setup, live | Not started | | Depends on SharePoint/Teams template + Lists register above. |

**Day 30 exit criteria:** engagement register, capacity list, RAID, and
expansion pipeline exist in Lists; at least one pattern and the mobilization
packet exist; the status report generator is producing real reports;
provisioning is automatic on Closed Won.

---

## Day 31–60 — Core cadence

Goal: estimating and margin visibility are live, and weekly status stops
being manual. This is where the department starts running itself instead of
being run by hand.

### Estimating

| Item | Status | Owner | Notes |
|---|---|---|---|
| `estimating/estimate-model.xlsx` | Not started | | Excel — calculation is the point. |
| `estimating/conventions.md` | Not started | | How to handle deals that don't cleanly fit a pattern. |
| Tool #2 — Estimate assistant shipped | Not started | | Pattern library + historical actuals → BOE draft. |

### Margin visibility

| Item | Status | Owner | Notes |
|---|---|---|---|
| Tool #3 — Margin dashboard shipped | Not started | | Burn vs. completion, portfolio-wide, one page. |
| `docs/margin-watch.md` — 70/70 rule + escalation path | Not started | | Flag: ≥70% hours burned with <70% milestones complete. |
| Automation #3 — Margin watch (70/70 rule) live | Not started | | The single most valuable automation in the system. |

### Status cadence automation

| Item | Status | Owner | Notes |
|---|---|---|---|
| `templates/status-report.md` finalized | Not started | | Finalize against real Tool #1 output. |
| Automation #2 — Weekly status auto-draft live | Not started | | |

### Data flow

| Item | Status | Owner | Notes |
|---|---|---|---|
| Jira → Lists one-way sync live | Not started | | One direction only. Never Lists → Jira. |

**Day 60 exit criteria:** estimate assistant and margin dashboard are in
use; weekly status drafts itself; the 70/70 margin watch is live and has
been tested against at least one real engagement; Jira data flows into
Lists automatically. Automations 1–3 are confirmed running before any work
starts on automations 4–7.

---

## Day 61–90 — Scale

Goal: the remaining tools and automations are live, metrics are defined
once and referenced everywhere, and the department has a repeatable
maintenance cadence (quarterly pattern refresh) rather than a one-time
build.

### Remaining tools

| Item | Status | Owner | Notes |
|---|---|---|---|
| `templates/closeout-memo.md` finalized | Not started | | |
| Tool #4 — Closeout memo drafter shipped | Not started | | Includes expansion signal extraction. |
| `templates/qbr-pack.md` finalized | Not started | | Tier A only. |
| Tool #5 — QBR pack assembler shipped | Not started | | |

### Remaining automations

| Item | Status | Owner | Notes |
|---|---|---|---|
| Automation #4 — Capacity refresh live | Not started | | |
| Automation #5 — Milestone → invoice trigger live | Not started | | |
| Automation #6 — Closeout → expansion touchpoints live | Not started | | |
| Automation #7 — Renewal risk monitor live | Not started | | |

### Metrics & ongoing cadence

| Item | Status | Owner | Notes |
|---|---|---|---|
| `metrics/definitions.md` written | Not started | | Canonical definitions — every report references these, none redefine. |
| `metrics/reporting-logic.md` written | Not started | | How each metric is calculated and how often it refreshes. |
| First quarterly pattern-library refresh scheduled | Not started | | A stale library is worse than no library. |
| Full 9-15 engagement portfolio running end-to-end | Not started | | Provisioning → status → margin watch → closeout, all on the system. |

**Day 90 exit criteria:** all five tools and all seven automations are live;
metrics are defined in one place; the first quarterly pattern refresh is on
the calendar; the portfolio is running on the system built here, not on
ad hoc spreadsheets or memory.

---

## Change log

| Date | Change |
|---|---|
| 2026-09-07 | Tracker created. Repo scaffold, `CLAUDE.md`, and `patterns/_PATTERN-TEMPLATE.md` in place. |
