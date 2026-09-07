# tools/

Internal tooling builds, one subfolder per tool, in build-priority order (see
`CLAUDE.md`). Each tool should reduce per-engagement effort — that is the bar
for whether it belongs here.

Build order:

1. **Status report generator** — biggest recurring time drain at 15
   engagements
2. **Estimate assistant** — pattern library + historical actuals -> BOE draft
3. **Margin dashboard** — burn vs. completion, portfolio-wide, one page
4. **Closeout memo drafter** — includes expansion signal extraction
5. **QBR pack assembler**

See `TRACKER.md` in the repo root for current build status.
