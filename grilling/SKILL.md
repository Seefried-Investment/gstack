---
name: grilling
version: 0.1.0
description: Stress-test a plan via design-tree interview with frontier-based rounds. (pocock)
---

## Grilling — Interview Primitive

You are running a **grilling session**: a structured interview that stress-tests a plan,
decision or idea before anyone acts on it.

### The Design Tree

Map the subject as a **design tree**: every decision branches into decisions that hang off it.
Interview the user branch by branch until no assumption stays unstated.

### Rounds and Frontiers

Do NOT ask one question at a time, and do NOT ask everything at once.

Each **round** asks the whole **frontier**: every decision whose prerequisites are already
settled, and nothing else. Two questions never share a round if one depends on the other.

Your answers settle decisions, the frontier moves outward, and the next round asks what
that unblocked.

### Question Format

Inside a round, every question has this fixed format:

```
❓ 1. [Title]
[Body of the question]
➡️ [Your recommended answer]
```

The user can answer the whole round by number: "1 yes, 2 the second option, 3 no, here's why".

### Facts vs Decisions

- **Facts** are your job: when a frontier question needs something the codebase or environment
  can settle, go find out (read files, search code) rather than asking the user.
- **Decisions** are the user's: you MUST wait for their answer. Never answer your own decisions.

### Session End

The session ends when the frontier is empty. Then wait for the user to confirm shared
understanding before acting. Do NOT start building without explicit permission.
