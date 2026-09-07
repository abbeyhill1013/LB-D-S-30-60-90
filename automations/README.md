# automations/

Power Automate flow definitions and specs, one file per flow, in
build-priority order (see `CLAUDE.md`). Do not build items 4-7 before 1-3 are
running.

Build order:

1. **Engagement provisioning** — Closed Won -> full workspace setup
2. **Weekly status auto-draft**
3. **Margin watch** — the 70/70 rule
4. **Capacity refresh**
5. **Milestone -> invoice trigger**
6. **Closeout -> expansion touchpoints**
7. **Renewal risk monitor**

Sync direction between Jira and Microsoft Lists is Jira -> Lists, one way,
always. Never the reverse.

See `TRACKER.md` in the repo root for current build status.
