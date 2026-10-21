---
name: eedo-workflow
version: 0.1.0
description: Combined gstack + Pocock workflow for EEDO product development. (custom)
triggers:
  - eedo workflow
  - start workflow
  - full pipeline
---

## EEDO Development Workflow

Combined pipeline from gstack (Garry Tan) and Pocock skills (Matt Pocock)
for building the EEDO application — Better Elements' Odoo replacement.

### Phase 1: Understand (Pocock)
**When the plan is fuzzy and words aren't settled.**

1. `/grill-with-docs` — Interview to build shared understanding
   - Writes GLOSSARY.md (domain vocabulary) inline
   - Writes ADRs for hard-to-reverse decisions
   - Uses `/grilling` (frontier-based interview) + `/domain-modeling`

2. `/to-spec-pocock` — Synthesize into a decision record
   - Agree on test seams first
   - Spec records what was decided, nothing more

3. `/to-tickets` — Break spec into implementable work items

### Phase 2: Plan (gstack)
**When the work is defined and ready to implement.**

4. `/office-hours` — Product interrogation (CEO perspective)
5. `/autoplan` — Full implementation plan with all review gates
6. `/plan-ceo-review` — Strategic challenge on the plan

### Phase 3: Build (gstack)
**When the plan is approved and ready to code.**

7. Implement per ticket/plan step
8. `/review` — Code review with adversarial checks
9. `/test-audit` — Test coverage analysis
10. `/cso` — Security audit (OWASP + STRIDE)

### Phase 4: Ship (gstack)
**When implementation is reviewed and tested.**

11. `/ship` — PR creation with full checks
12. `/qa` — Browser-based QA on staging
13. `/land-and-deploy` — Merge and deploy

### Phase 5: Reflect
14. `/retro` — What worked, what didn't, what to change

### Evidence-Driven Development

This project uses REA (Reverse Engineer Anything) evidence from the Odoo 19 instance
as the ground truth for feature requirements. Evidence files in `evidence/` contain
AST-analyzed module structures, API endpoints, and storage patterns.

Always cite evidence IDs when referencing Odoo behavior.
