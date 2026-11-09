---
name: to-spec-pocock
version: 0.1.0
description: Synthesize a grilling session into a spec document with agreed seams. (pocock)
triggers:
  - write the spec
  - synthesize spec
  - spec from grilling
---

## To Spec (Pocock Method)

Turn the conversation you just had into a **spec**: a decision record that a fresh
session can pick up without the user explaining again.

### What this skill does

- Synthesizes decisions from the current conversation, codebase, GLOSSARY.md and ADRs
- Does NOT interview — the deciding is already done
- Records what was decided, in the project's own vocabulary
- If the spec states something the user never said, that is a defect

### Seams Before Prose

Before writing anything:
1. Sketch the **seams** where the feature will be tested
2. Prefer existing seams to new ones
3. Pick the highest seam possible
4. Check the seams with the user
5. The ideal number of seams for a change is one

### Spec Format

Write the spec as a markdown file in `docs/specs/` with:
- **Context**: what prompted this work
- **Decisions**: what was settled, citing GLOSSARY.md terms
- **Seams**: where testing happens
- **Non-goals**: what was deliberately excluded
- **Open questions**: anything not yet resolved

### After the spec

Recommend `/to-tickets` to break the spec into implementable work items,
or `/autoplan` (gstack) for a full implementation plan with reviews.
