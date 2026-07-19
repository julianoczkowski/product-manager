---
name: pm-personas
description: >-
  Create Pragmatic Institute buyer and user personas — archetypes grounded in
  real market evidence, written so the team stays connected to real people. Use
  when the PM asks about personas, "who is the buyer", "who is the user", target
  audience, ICP, or wants to make a persona come alive. Distinguishes the buyer
  (makes/influences the purchase) from the user (uses it daily). Produces a Buyer
  Persona and a User Persona as a Markdown or Word .docx artifact.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Personas (Pragmatic Framework: Planning → Buyer Personas & User Personas)

**Rule:** *Teams that understand personas and their problems build remarkable products.*
A persona is an **archetype built from observed patterns**, not a fictional character
you invented. Ground every trait in market evidence (interviews, win/loss, support,
usage). See `../pm-copilot/references/framework.md` for the market-driven basics.

- **Buyer persona** — the archetypical person who **makes or influences the purchase**
  decision (motivations, barriers, buying process). Guides marketing and sales.
- **User persona** — the archetypical person who **uses** the product day to day.
  Guides the product. In B2B the buyer and user are usually different people — **build
  one of each.** Create a separate persona whenever the problems genuinely differ.

## The Interview Matrix (get a balanced cross-section)
Before writing personas, make sure you've talked to a balanced sample. Map who to
interview across segments and persona types:

| Segments | Buyer Personas (Economic · Technical · Functional) | User Personas (User 1 · User 2 · User 3) |
| :--- | :--- | :--- |
| Segment A | who fills each buyer role | who the day-to-day users are |

Buyer roles: **Economic** (owns the budget/ROI), **Technical** (gatekeeps on fit/risk),
**Functional** (uses the outcome, champions internally). Balance interviews across all
four market segments: customers, competitors' customers, evaluators (win/loss) and
potentials.

## Interview the user for inputs (batch questions)
1. Which **product/feature** and **market segment** is this persona for?
2. Is this a **buyer** or a **user** persona? (Do both if B2B.)
3. What **problems/roadblocks** does this person have (their words, first person)?
4. What are their **goals** — who they want to be, what they want to do, how they want to feel?
5. What **behaviors** shape how they approach those goals?
6. Their **background** — how did they get to their current situation/outlook?
7. What **evidence** backs this (how many interviews/tickets/win-loss notes)?

## Artifact templates

### User Persona
```markdown
# User Persona — <Name>

**Company:** <company>  ·  **Feature / Product:** <feature / product name>
**Author:** <author>  ·  **Date created:** <date>

**Name:** <memorable name + role>  |  **Segment:** <segment>
**Relevant Information:** <age/role/context that matters for the product>
> "<A quote in their own voice that captures their outlook.>"

## Problems
Roadblocks that keep them from achieving their goals (first person):
- "I can't …"
- "It takes too long to …"

## Background Story
<Enough story to explain how they got to their current situation and outlook.>

## Goals
- **Be:** <who the persona wants to be>
- **Do:** <what the persona wants to do>
- **Feel:** <how the persona wants to feel>

## Behaviors
- <Specific behaviors that impact how they approach their goals.>

## Evidence
- <interview count / sources>  · > TODO: <gaps to validate>
```

### Buyer Persona
```markdown
# Buyer Persona — <Name>

**Company:** <company>  ·  **Feature / Product:** <feature / product name>
**Author:** <author>  ·  **Date created:** <date>

**Name / Role:** <name>  |  **Buyer type:** Economic / Technical / Functional
**Segment:** <segment>
> "<quote capturing what they care about in a purchase>"

## Problems & goals (business outcome they're buying)
- <problem in first person>  ·  <the outcome/ROI they need>

## Buying process & barriers
- **How they buy:** <steps, who else is involved, timeline>
- **Selection criteria:** <what must be true to choose a vendor>
- **Barriers / objections:** <risk, budget, switching cost>

## What moves them
- **Triggers:** <what starts the search>  · **Information sources:** <where they look>

## Evidence
- <win/loss, interviews, sources>  · > TODO: <gaps>
```

## Deliver the artifact
Follow `../pm-copilot/references/artifact-output.md`: confirm inputs, **ask Markdown
or .docx**, write the `.md`, convert to `.docx` on request via your environment's native document-creation capability.
Deliver a buyer and a user persona where relevant. Next stage: use these personas to
write **`pm-positioning`** (per persona) or prioritized **`pm-requirements`**.
