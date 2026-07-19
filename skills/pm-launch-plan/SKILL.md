---
name: pm-launch-plan
description: >-
  Build a Pragmatic go-to-market launch plan and readiness checklist. Use when the
  PM asks to plan a launch, GTM, go-to-market, launch readiness, launch checklist,
  release announcement, or "get sales and marketing ready". Coordinates the Programs
  and Enablement columns of the framework around a market window. Produces a Launch
  Plan as a Markdown or Word .docx artifact.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Launch Plan (Pragmatic Framework: Programs → Launch, + Enablement)

> **Launch readiness is more than just product readiness.** A launch is
> cross-functional: the product can be done while the market, the channel, and
> support are not. Plan, execute, and measure the launch as its own deliverable.

Reuse the positioning statement, personas, and launch trigger from earlier artifacts
in the feature dossier if they exist (positioning doc, personas, release charter —
see `../pm-copilot/references/artifact-output.md` for how to find the dossier). See
`../pm-copilot/references/framework.md` for the Programs and Enablement boxes.

## What a launch pulls together
- **Programs:** Awareness (raise profile in strategic segments), Nurturing (move
  prospects through the funnel), Advocacy (testimonials, case studies, references),
  Measurement.
- **Enablement / Readiness:** Sales Alignment (align selling to how the market buys),
  Content (per persona, per buying step), Sales Tools (per selling step), Channel
  Training (how to *sell* the product, not use it).
- **Market Window:** Marketing, Sales, and Operations work **backward from** the launch
  date while Development works **to** it. If the release is **content-driven** (no
  committed date — see the release charter), anchor the backward plan to the release's
  **exit criteria** instead, and re-forecast the launch date as they near completion.

## Interview the user (batch questions)
1. **What's launching**, at what **scale/tier** (major vs minor), and the **target
   date/market window** — or, for a content-driven release, the **exit criteria** that
   will trigger the launch?
2. **Launch goals & success metrics** — awareness, pipeline, adoption, revenue?
3. **Target personas & positioning** — who are we reaching, and what's the core message? (link the positioning doc)
4. **Channels & programs** — how will we create awareness and nurture demand?
5. **Sales readiness** — what content, tools, and training does the channel need?
6. **Cross-functional readiness** — product, marketing, sales, support, ops, legal — who owns what, and what's the go/no-go bar?

## Artifact template — Launch Plan
```markdown
# Launch Plan — <Product> <Version>

**Launch trigger:** <date / market window — or content-driven: launches when <exit criteria> are met>   **Tier:** <major | minor>
**Company:** <company>  ·  **Feature / Product:** <feature / product name>
**Author:** <author>  ·  **Date created:** <date>  ·  **Version:** 1.0

## 1. Launch goals & success metrics
| Goal | Metric | Target |
| :--- | :--- | :--- |
| Awareness | <impressions / reach> | |
| Demand | <MQLs / pipeline> | |
| Adoption | <activations / usage> | |
| Revenue | <bookings / expansion> | |

## 2. Target personas & positioning
- **Buyer persona:** <name> — cares about <…>
- **User persona:** <name> — cares about <…>
- **Positioning statement:** For <persona>, <product> <verb> <problem> by <verb> <benefit>.
- **Key messages:** <problem-oriented message 1>, <message 2>, <message 3>.

## 3. Marketing programs (Programs column)
| Program | Objective | Owner | Timing (from market window) |
| :--- | :--- | :--- | :--- |
| Awareness | | | |
| Nurturing | | | |
| Advocacy | | | |

## 4. Sales enablement (Enablement column)
| Item | Purpose (buying step) | Owner | Status |
| :--- | :--- | :--- | :--- |
| Sales alignment / play | | | |
| Content (per persona/step) | | | |
| Sales tools | | | |
| Channel training | | | |

## 5. Launch readiness checklist
| Area | Owner | Status | Notes |
| :--- | :--- | :--- | :--- |
| Product / QA | | 🟢/🟡/🔴 | |
| Marketing / content | | | |
| Sales / enablement | | | |
| Support / docs | | | |
| Operations / billing | | | |
| Legal / compliance | | | |

**Status legend:** 🟢 Ready · 🟡 At risk · 🔴 Not ready.

## 6. Measurement plan
How and when each success metric is measured post-launch; report against corporate goals.

## 7. Risks & go/no-go criteria
- <risk> — <mitigation>
- **Go/no-go bar:** <the conditions that must be green to launch>
```

## Deliver the artifact
Follow `../pm-copilot/references/artifact-output.md`: confirm inputs, **ask Markdown
or .docx**, write the `.md`, convert to `.docx` on request via your environment's native document-creation capability. Then offer the next stage: keep the launch on track with
**`pm-stakeholder-communication`** status updates, and after launch loop back to
**`pm-market-problems`** and **`pm-win-loss-analysis`** to feed the next release.
