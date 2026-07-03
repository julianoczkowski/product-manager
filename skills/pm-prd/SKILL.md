---
name: pm-prd
description: >-
  Assemble a full, market-driven Product Requirements Document (PRD) the
  Pragmatic way — problem-before-solution, evidence-based, persona-first. Use
  when the PM asks for a PRD, product spec, feature doc, "write the requirements
  doc", or "put it all together for the team". Pulls in existing personas,
  positioning, market problems, requirements and use scenarios if present, and
  gathers anything missing inline. Produces a Product Requirements Document as a
  Markdown or Word .docx artifact.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Product Requirements Document (Pragmatic Framework: Planning)

A PRD here is a **market requirements document** — it specifies the **WHAT** (the
market problems, personas, and prioritized requirements). The **HOW** (design,
flows, UI, prototypes, error conditions) belongs to the team. Lead with the
problem, cite evidence, and write problems in the persona's **first-person voice**.
See `../pm-copilot/references/framework.md` for the primitives used below.

**Requirement form:** *[persona] has [problem, described in a use scenario] with [frequency].*
**Priority = Market Evidence × Impact** (advanced: × (B + U + C + V) — Buying, Using, Vision, Competitive).

## Reuse what already exists
Before gathering inputs, look for prior artifacts in the working directory and offer
to pull them in (don't duplicate work):

```bash
ls *.md pragmatic/*.md 2>/dev/null | grep -Ei 'persona|positioning|market-problem|requirement|use-scenario|roadmap'
```

If found, read them and reuse their personas, problems, positioning statement, and
prioritized requirements. If not, gather inline (or offer to run `pm-personas`,
`pm-market-problems`, `pm-requirements`, `pm-use-scenarios` first).

## Interview the user (batch questions)
1. **Product & release** — name, version, and the goal of *this* release.
2. **Market forces** — what's driving this now? Is it **content-driven** (ship when
   the problems are solved) or **target-date-driven** (a fixed market window)?
3. **Personas** — who is the buyer, who is the user? (summarize or link)
4. **Top market problems** — in the persona's first person, each with **evidence**
   (interview count, % of customers, win/loss, support tickets, usage data).
5. **Success metrics** — how will you know it worked? (Value / Quality / Progress / Satisfaction)
6. **Out of scope, dependencies, risks.**

## Artifact template
```markdown
# Product Requirements Document — <Product> <Version>

*Confidential and subject to change. For internal use only. No external commitments
can be made based on this document since it is in early planning stages. Content and
timing are very likely to change.*

**Company:** <company>  ·  **Feature / Product:** <feature / product name>
**Author:** <author>  ·  **Contact:** <email>  ·  **Date created:** <date>  ·  **Version:** 1.0

## 1. Overview of the target release
Goal of this release: <one paragraph>.
Market forces driving it: <evidence-backed forces>.
Driven primarily by: <content | target date>. Target window: <date/quarter>.
Related artifacts: <positioning doc, roadmap, canvas, links>.

## 2. Personas
### Buyer persona — <name>
<motivations, buying process, barriers>
### User persona — <name>
<goals, behaviors, problems>

## 3. Market problems (persona's first person, with evidence)
- "<I can't …>" — evidence: <n interviews / % customers / win-loss>
- "<It takes too long to …>" — evidence: <…>

## 4. Requirements (grouped, prioritized)
### GROUP 1 — <group name>
1. **<Requirement>** — <Persona> has <problem, in a use scenario> with <frequency>.
   Priority: <evidence> (inputs) × <impact> (impact) = **<priority>**.
2. **<Requirement>** — … Priority: … = **<priority>**.
### GROUP 2 — <group name>
1. …

## 5. Use scenarios (day-in-the-life)
**<Scenario name>** — <Persona> is trying to <goal>. Today, <what happens, the pain,
the current workaround>. This happens <frequency>. <Why it matters.>

## 6. Requirements summary
| Requirement | Persona | Market Evidence | Impact | Priority | Group | Group Order |
| :--- | :--- | ---: | ---: | ---: | :--- | ---: |
| <name> | <persona> | 25 | 4 | 100 | <group> | 1 |

## 7. Out of scope / non-goals
- <explicitly not doing …>

## 8. Success metrics
| Metric category | Metric | Current | Goal |
| :--- | :--- | :--- | :--- |
| Value | <LTV / revenue> | | |
| Quality | <defects / coverage> | | |
| Progress | <cycle time> | | |
| Satisfaction | <NPS / CSAT / renewal> | | |

## 9. Dependencies & risks
- <dependency / risk> — <mitigation>

## 10. Approvals
| Name | Title | Date | Signature |
| :--- | :--- | :--- | :--- |
| | Product Manager | | |
| | Systems Architect | | |
| | Development Manager | | |
| | Interaction Designer | | |
| | QA Lead | | |

## 11. Change tracking
| Version | Date | Changes | Reason |
| :--- | :--- | :--- | :--- |
| 1.0 | <date> | Initial draft | |

## Open questions / evidence to gather
- > TODO: <unproven claim or missing evidence>
```

## Deliver the artifact
Follow `../pm-copilot/references/artifact-output.md`: confirm inputs (fill gaps with
clearly-marked assumptions rather than inventing evidence), **ask Markdown or .docx**,
write the `.md`, convert to `.docx` on request via your environment's native document-creation capability.
Then offer the next stage: turn the prioritized requirements into a committed
**`pm-release-plan`**, and set up **`pm-stakeholder-communication`** to keep everyone aligned.
