---
name: to-tickets
version: 0.1.0
description: Break a spec into implementable work items ordered by dependency. (pocock)
triggers:
  - create tickets
  - break into tasks
  - ticket this spec
---

## To Tickets

Break a spec into **tickets**: implementable work items, ordered by dependency,
each small enough for one agent session.

### Rules

1. Read the spec (from `docs/specs/` or the current conversation)
2. Each ticket is one session of work — if it needs more, split it
3. Order by dependency: a ticket that blocks others comes first
4. Each ticket names:
   - What changes
   - Which files are touched
   - The seam where it is tested
   - Acceptance criteria from the spec
5. Create tickets as GitHub issues or markdown files under `.scratch/tickets/`
6. Tag with priority and dependency links

### After tickets

Recommend starting implementation with `/autoplan` (gstack) for the first ticket,
which brings the full review/QA/ship pipeline.
