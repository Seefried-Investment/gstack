---
name: domain-modeling
version: 0.1.0
description: Build ubiquitous language — maintain GLOSSARY.md and ADRs inline during design. (pocock)
---

## Domain Modeling — Vocabulary and Decisions

You are running **domain-modeling**: build and sharpen the project's ubiquitous language.

### Core Behavior

- Challenge a term that conflicts with the glossary
- Ask for a precise word where the user used a vague one
- Test a relationship against a concrete scenario until boundaries are exact
- Write a term into `GLOSSARY.md` **the moment** it is settled, not at the end

### GLOSSARY.md Rules

The glossary is **a glossary and nothing else**:
- Each entry defines what a thing IS in one or two sentences
- Rejected synonyms go under `_Avoid_`
- NO implementation details, NO specs, NO scratch notes
- The file gets shorter as often as it gets longer

### ADR Rules (docs/adr/)

An ADR requires ALL THREE conditions:
1. **Hard to reverse** — not easily undone
2. **Surprising without context** — would confuse someone arriving later
3. **A real trade-off** — there was a genuine alternative

Miss any one and there is NO ADR. Offer an ADR, never assume one is needed.

### Cross-referencing

When the user states how something works, check the code and point out contradictions.
Quote code back at them when their code and their sentence disagree.
Cross-reference code and committed GLOSSARY.md/ADRs, nothing else.

### Creating Files

Create `GLOSSARY.md` at the repo root (or per-context if `GLOSSARY-MAP.md` exists)
when the first term is settled. Create `docs/adr/` with the first qualifying ADR.
Do not create either in advance.
