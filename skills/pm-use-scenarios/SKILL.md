---
name: pm-use-scenarios
description: >-
  Write Pragmatic Institute use scenarios — short stories that put a market problem
  in context from the persona's point of view (a component of requirements). Use
  when the PM asks for "use scenarios", "a day in the life", "user story context",
  "problem statements", or needs to reframe a feature request as a real problem so
  development understands the WHAT (not the HOW). Produces a Use Scenarios document
  as a Markdown or Word .docx artifact.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Use Scenarios (Pragmatic Framework: Planning → Use Scenarios)

**Rule:** *articulate problems from the persona's point of view.* A use scenario
illustrates a market problem as a "story" that puts it in context (including current
results) — it is one component of requirements. See
`../pm-copilot/references/framework.md`. Personas should exist first (`pm-personas`).

## Anatomy of a Problem Card
Map interrogatives to fields:

| Field | Interrogative |
| :--- | :--- |
| **[Problem Name]** | *What* problem |
| **[Persona]** | *Who* has it |
| **has [use scenario]** | *Why* it occurs |
| **with [frequency]** | *When* it occurs |

Reframing sentence (great for turning a feature request into a problem):
> **[Persona]** struggles with **[problem]** when **[context]** because **[why it matters]**.

## What vs. How — stay on the WHAT
| WHAT = the problem → **PM → DEFINE** | HOW = the solution → **Team → DESIGN/BUILD** |
| :--- | :--- |
| Name, Persona, Use Scenario, Frequency, Market evidence, Impact | Overview, flow chart, use cases, UI, prototypes, error conditions |

A use scenario ≠ a use case. A use scenario tells the problem story; a use case
enumerates every interaction in the functional spec (the team's job).

## Three considerations when articulating a problem
1. **Avoid ambiguous terms** — do not use: *flexible, adaptable, user-friendly, TBD,
   adequate, rapidly/quickly/fast, fault tolerant, scalable, ASAP,
   maximize/minimize/optimize (any "-ize" word), and/or, etc.* Replace each with a
   concrete, observable statement.
2. **Edge cases ("what if?")** — will your persona *actually* do it? Don't design for
   situations that won't happen.
3. **Who is significant?** — the U-curve: the vocal extremes (novices + experts) are
   *where we listen*; the proficient majority is *where we should listen.* Write for
   the majority.

## Interview the user (batch questions)
1. Which persona and which market problem is this scenario for?
2. Walk me through a real situation where this happens — what triggers it, what do they
   do today, and what's the current (bad) result?
3. How often does it occur (frequency)?
4. What evidence shows this is real (counts across inputs) and how bad is it (impact)?

## Artifact template
```markdown
# Use Scenarios — <Product / Release>

**Company:** <company>  ·  **Feature / Product:** <feature / product name>
**Author:** <author>  ·  **Date created:** <date>  ·  **Version:** 1.0

## Scenario 1 — <Problem Name>
**Problem Card**
- **Problem Name:** <what>
- **Persona:** <who>
- **Use Scenario:** <why — the situation that causes the problem>
- **Frequency:** <when / how often>

**Day in the life**
<A short first-person narrative: the persona's context, the trigger, what they do today,
and the frustrating current result. Concrete and specific — no ambiguous terms.>

**Market evidence:** <# of documented occurrences across inputs>
**Impact:** <1–5 on the impact scale (or 99999 if contractual)>

## Scenario 2 — <Problem Name>
…
```

## Deliver the artifact
Follow `../pm-copilot/references/artifact-output.md`: confirm inputs, **ask Markdown
or .docx**, write the `.md`, convert to `.docx` on request via your environment's native document-creation capability. Then offer the next stage: roll these scenarios into prioritized
**`pm-requirements`** or a full **`pm-prd`**.
