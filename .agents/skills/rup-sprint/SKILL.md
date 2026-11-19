---
name: rup-sprint
description: Create, activate, close, inspect, or change a RUP sprint in PLAN.md. Use before any PLAN.md or sprint-status change; do not use to define or promote backlog items.
---

# RUP Sprint Adapter

Use this skill for every mutation of `PLAN.md` or a sprint's lifecycle status.

## Mandatory procedure

1. Read `RUP_patch.md`, then `RUPStrikesBack.patch/RUP_patch.md`.
2. Read `RUPStrikesBack/.claude/commands/sprint.md` and
   `RUPStrikesBack/rules/generic/sprint_definition.md`.
3. Read `PLAN.md` and `BACKLOG.md`, and read `PROGRESS_BOARD.md` if it exists,
   before deciding the affected sprint and its assigned PBIs. Under P0.1,
   an absent board is expected before the first explicitly requested sprint
   execution, even when bootstrap preselects `Sprint.0` as `Progress`.
   For inspection, report that execution tracking has not been initialized;
   for planning, leave the board absent. Neither operation starts execution.
   If existing sprint evidence shows execution has already begun, treat a
   missing board as an inconsistency and stop for a Product Owner decision
   rather than reconstructing statuses from assumptions.
4. Validate stable sprint identifiers and numbering within each phase under
   P0.phase (`Sprint.0`, `I.x`, `E.x`, `C.x`, `T.x`), required fields, valid
   transitions, and that
   every assigned PBI exists in `BACKLOG.md` and is not in another active
   sprint.
5. On the first explicitly requested sprint execution, initialize the board
   through `rup-progress` and the canonical starting-phase procedure. Apply
   P0.1 instead of creating a board during pre-execution planning. When a
   board update is required, use `rup-progress` and create or update only
   rows whose PBI is assigned to the named Sprint in `PLAN.md`.

Do not add, promote, or reprioritize a PBI here. Route those decisions to
`rup-backlog`; stop for a Product Owner decision when the intended assignment
or transition is ambiguous.
