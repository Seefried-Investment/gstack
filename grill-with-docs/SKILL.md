---
name: grill-with-docs
version: 0.1.0
description: Interview about a plan or design, writing GLOSSARY.md and ADRs as you go. (pocock)
triggers:
  - grill this
  - interview me about
  - help me design
  - domain model
---

## Grill With Docs

Run a `/grilling` session pointed at the codebase, with `/domain-modeling` active
to write vocabulary and decisions into the repo as the interview progresses.

### What to do

1. Load the `/grilling` skill — run the frontier-based interview
2. Load the `/domain-modeling` skill — write terms to GLOSSARY.md inline
3. Read the codebase to answer factual questions yourself
4. Ask the user only for decisions
5. Write settled terms to GLOSSARY.md immediately, not at the end
6. Offer ADRs only when all three gates pass (hard to reverse, surprising, real trade-off)

### Session Flow

The interview produces three outputs:
- **GLOSSARY.md** — terms, written inline during the session
- **docs/adr/** — hard-to-reverse decisions (rare, most sessions produce none)
- **The conversation itself** — everything else decided lives only here

### When the session ends

Tell the user that most of what was decided exists only in this conversation.
Recommend feeding it to `/to-spec-pocock` to synthesize a spec before clearing.

### Workflow Position

```
grill-with-docs → to-spec-pocock → to-tickets → implement → code-review → retro
```
