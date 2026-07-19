---
name: pm-release-plan
description: >-
  Turn a prioritized set of requirements into a committed Pragmatic release plan —
  themed, sized, and signed. Use when the PM asks to plan a release, define MVP
  scope, commit a date, build a release charter, or "what goes in this release".
  Covers MVP done right, themes, the estimation ladder, the market window, and the
  scope/schedule/resources change levers. Produces a Release Charter as a Markdown
  or Word .docx artifact.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Release Plan / Charter (Pragmatic Framework: Roadmap → Release)

The **roadmap drives the release plan**. A roadmap is a plan, not a commitment; a
**release charter is a signed agreement** of what will be delivered. See
`../pm-copilot/references/framework.md`.

**MVP, done right:** *"the version of a new product that allows a team to collect the
maximum validated learning with the least effort."* An MVP is **not** the smallest
collection of features — it must be a real product that viably solves the customer's
**top problems** from day one. Calling a finished "V1.0" an MVP is a waterfall relapse.

## Core methods

**Group requirements into Themes.** A theme groups prioritized problems that share a
persona, a product goal, a technical decision, a strategy, roadmap alignment, or a
target metric. Themes make a release *remarkable* and coherent.
> Rule: **Deliver 100% of something, not 70% of everything.**

**Shape the release** by three dimensions per theme/requirement: **Size · Difficulty ·
Confidence.** Reduce big items by splitting problems.

**Estimation ladder (confidence grows with detail):**
Release → **T-shirt sizes (S/M/L)** → Iteration → **story points** → Day → **daily updates**.
Product management is available to answer questions at every step. The dev team makes
the final estimate.

**Market Window & schedule direction:** On a **date-driven** release, development works
**TO** a date (iterating toward the window); Marketing, Sales and Operations work
backward **FROM** it. On a **content-driven** release there is no committed date —
define the **exit criteria** that trigger launch instead, and the go-to-market clock
starts when they're met.

**Change levers (iron triangle):** **Scope · Schedule · Resources.** Decide up front
which one drives the plan and how you'll absorb change.

## Interview the user (batch questions)
1. **Product, version, project name.**
2. **Release theme(s)** — the unifying message (persona goals / major capability / set of problems).
3. **Which prioritized requirements** are in scope? (pull from an existing MRD/PRD if present)
4. **Date-driven or content-driven?** Is this release driven by a target date / market
   window, or by content (it ships when the themes are done)? Both are equally valid.
   Only if date-driven: what is the target date or market window? "There is no date"
   is a legitimate answer — that's a content-driven release, not a missing input.
5. **Major milestones** — code complete, beta, final QA, release to production, GA.
6. **Change lever** — will Scope, Schedule, or Resources flex when reality hits?

## Artifact template — Release Charter
```markdown
# Release Charter — <Product> <Version>

**Company:** <company>  ·  **Feature / Product:** <name>
**Author:** <author>  ·  **Date created:** <date>  ·  **Version:** <version>
**Project Name:** <project>   **Release Theme:** <theme>
**Schedule:** <date-driven: <target date / market window> · or content-driven: ships when <exit criteria> are met>

## Themes
- **<Theme 1>** — <what it delivers and why (persona/goal/strategy it serves)>
- **<Theme 2>** — <…>

## Deliverables (what we have agreed to deliver)
Based on requirements document **<MRD/PRD name + version>**.
### <Theme 1 / Group name>
- <requirement / capability>  — size: <S/M/L>, confidence: <low/med/high>
- <requirement / capability>
### <Theme 2 / Group name>
- <requirement / capability>

### Major milestones
| Milestone | Target date |
| :--- | :--- |
| Code complete | |
| Beta release | |
| Final QA | |
| Release to production | |
| General availability (GA) | |

## Change plan
| Driver | What will drive the plan? | How will you deal with change? |
| :--- | :--- | :--- |
| Scope | | |
| Schedule | | |
| Resources | | |

## Signatures
*This document lists what we have agreed to deliver. By signing below, I acknowledge
that this is the current plan and that I will inform product management and project
management if the plan changes.*

| Name | Title | Date | Signature |
| :--- | :--- | :--- | :--- |
| | Product Manager | | |
| | Project Manager | | |
| | Development Manager | | |
| | QA Lead | | |
```

## Deliver the artifact
Follow `../pm-copilot/references/artifact-output.md`: confirm inputs, **ask Markdown
or .docx**, write the `.md`, convert to `.docx` on request via your environment's native document-creation capability. Then offer the next stage: set up
**`pm-stakeholder-communication`** to report status against this charter, and
**`pm-launch-plan`** to prepare go-to-market for the target window.
