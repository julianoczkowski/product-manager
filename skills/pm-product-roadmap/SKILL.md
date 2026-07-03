---
name: pm-product-roadmap
description: >-
  Build a Pragmatic Institute Product Roadmap that communicates vision, direction
  and priorities over time — a plan, not a commitment. Use when the PM asks for a
  "roadmap", "product vision", "what's coming", "phases", "themes over time", or
  wants to align stakeholders on direction (as distinct from a dated release plan).
  Frames outcomes and market problems over time-frames, not features on dates.
  Produces a Product Roadmap as a Markdown or Word .docx artifact.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Product Roadmap (Pragmatic Framework: Focus → Product Roadmap)

**Rule:** *the roadmap is a plan, not a commitment.* It illustrates the vision and key
phases of deliverables. Communicate **outcomes and the market problems you'll solve**,
using **time-frames rather than specific dates**, and reflect innovation's
unpredictability. External guidance: **under-promise so the team can over-deliver.**
See `../pm-copilot/references/framework.md`.

## Roadmap vs. Release Plan (keep them separate)
| Roadmap | Release Plan / Charter |
| :--- | :--- |
| Strategic, long-term stakeholder discussion | Tactical, near-term execution |
| Highlights outcomes & impact, not just features | Communicates specific dates, deadlines, outputs |
| Time-frames, not delivery dates | Defined scope, dates, backlog |
| Addresses real market needs/problems | Tracks actively worked items |

A roadmap ≠ backlog: "roadmap = menu, backlog = recipes." For the dated commitment,
use the `pm-release-plan` skill.

## The four stages of roadmapping
- **Desire** — articulate the need for change, the company mission, and the product vision.
- **Discover** — research market problems; uncover urgency, pervasiveness, willingness-to-pay.
- **Define** — articulate opportunities, complete the canvas, set clear strategic objectives.
- **Do** — execute via a release plan + backlog while continuously learning and adapting.

## Types and formats
- **Types:** strategy roadmap, release roadmap, feature roadmap — pick to match the audience.
- **Formats:** dated, undated, or hybrid (quarters/half-years). Prefer undated/hybrid for
  external and strategic audiences; reserve dates for the release plan.

## Interview the user (batch questions)
1. Product vision and the mission it serves (the "Desire").
2. The top market problems/opportunities and their evidence (the "Discover").
3. Strategic objectives / outcomes for the horizon; which personas/segments.
4. Time horizon and audience (internal exec vs external customer) → drives format.
5. Known themes already committed vs. exploratory.

## Artifact template
```markdown
# Product Roadmap — <Product>

**Company:** <company>  ·  **Feature / Product:** <feature / product name>
**Author:** <author>  ·  **Date created:** <date>  ·  **Version:** 1.0
**Horizon:** <e.g. 18 months>   **Audience:** <internal / external>
> This roadmap is a plan, not a commitment. It communicates direction and the market
> problems we intend to solve, not dated deliverables.

## Vision
<1–2 sentences: the change we want to create and the product vision.>

## Strategic objectives (outcomes)
- <outcome 1 — the market problem it addresses>
- <outcome 2 — …>

## Roadmap
| Theme | THIS YEAR (Q1) | (Q2) | (Q3) | (Q4) | NEXT YEAR (H1) | (H2) | BEYOND |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| <Theme A> | ● | ● | | | | | |
| <Theme B> | | | ● | ● | | | |
| Market / persona goals | <goal> | | | | <goal> | | |
| Target metrics | <metric> | | | | | | |

## Themes
### <Theme A>
- **Market problem / persona:** <who + first-person problem>
- **Desired outcome:** <outcome, not feature>
- **Evidence:** <why now>

## What this is NOT
Dates and committed scope live in the Release Plan, not here.
```

## Deliver the artifact
Follow `../pm-copilot/references/artifact-output.md`: confirm inputs, **ask Markdown
or .docx**, write the `.md`, convert to `.docx` on request via your environment's native document-creation capability. Then offer the next stages: define what to build with
**`pm-requirements`**, or commit a dated increment with **`pm-release-plan`**.
