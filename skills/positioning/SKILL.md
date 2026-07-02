---
name: positioning
description: >-
  Create a Pragmatic Institute Positioning Document — describe a product by the
  market problems it solves (not features), for one persona in one segment. Use
  when the PM asks for positioning, messaging, "how do we describe/pitch this",
  an internal positioning doc, or a positioning statement. Produces a Positioning
  Document plus a Problem-Oriented Capabilities (POC) worksheet as a Markdown or
  Word .docx artifact.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Positioning Document (Pragmatic Framework: Planning → Positioning)

**Rule:** *Positioning focuses on the problems you solve, not features.* Create a
**separate positioning document for every persona whose problems differ.** Write
problems in the persona's **first-person voice**. This is an internal document (an
"internal press release") used to gain buy-in, brief design/engineering, and hand
off to marketing to build external messaging. See the primitives in
`../pm-copilot/references/framework.md`.

## Prepare
Ideally a team of 3–6 people with market knowledge, staying objective. Start with
one product and one persona/segment. If personas or market problems aren't defined
yet, run `personas` and `market-problems` first (or gather them inline).

## Interview the user for inputs (batch questions)
1. **Product** and the **one persona + market segment** this doc is for.
2. **The problem** — why does this persona care? What's painful today? (Be empathetic; use their words.)
3. **The ideal solution** from the persona's point of view — clear and specific.
4. **Evidence** the problem is real (interviews, win/loss, support tickets, surveys).
5. **What the product does** — enough to map features to capabilities.

## Build it in three steps (per the Pragmatic method)

**Step 1 — Draft the first four sections of the document:**
- **Problem** — "There is a problem in the industry today…" (persona's first person).
- **Solution** — "The ideal solution to this problem is…" (clear, specific).
- **Positioning Statement** — the "billboard," **≤25 words**, using the formula:
  > For **[persona]**, **[product]** **[verb]** **[problem]** by **[verb]** **[primary benefit]**.
- **Product Description** — overview, **≤50 words**.

**Step 2 — Problem-Oriented Capabilities (POC) worksheet.** List every problem the
product solves for this persona (first person) → group similar problems and condense
to **3–5 problem groups** → name the **problem-oriented capability** for each group →
map product **features** to each capability. Table: `Market Problems | Problem-Oriented Capabilities | Product Features`.

**Step 3 — Finish the document** by listing the 3–5 problem-oriented capabilities.

## Artifact templates

### Positioning Document
```markdown
# Positioning Document — <Product Name>

**Product Name:** <name>
**Persona & Market Segment:** <persona> / <segment>
**Company:** <company>  ·  **Feature / Product:** <name>
**Author:** <author>  ·  **Date created:** <date>  ·  **Version:** 1.0
*Internal document — describes the product by the problems it solves.*

## Problem
There is a problem in the industry today: <persona's first-person description of the pain, with evidence>.

## Solution
The ideal solution to this problem is <clear, specific solution from the persona's point of view>.

## Positioning Statement
> For <persona>, <product> <verb> <problem> by <verb> <primary benefit>.
<!-- ≤25 words -->

## Product Description
<≤50-word overview of the product.>

## Problem-Oriented Capabilities
1. <Capability> — <benefit>
2. <Capability> — <benefit>
3. <Capability> — <benefit>
4. <Capability> — <benefit>
5. <Capability> — <benefit>

## Evidence & open questions
- <evidence sources / interview counts>
- > TODO: <anything unproven, flagged as an assumption>
```

### Problem-Oriented Capabilities worksheet
```markdown
# Problem-Oriented Capabilities — <Product> / <Persona>

| Market Problems (persona's first person) | Problem-Oriented Capability | Product Features |
| :--- | :--- | :--- |
| "I can't …" | <Capability> | <feature>, <feature> |
| "It takes too long to …" | <Capability> | <feature> |
```

## Worked reference (from Pragmatic's example)
> For Robin the product manager, Product Minder reduces the frustration of managing
> ideas and requirements from everywhere by integrating all product information into
> a single system.
Capabilities: Instant Requirements, Idea Store, Auto Feedback, Trace Link, Status View.

## Deliver the artifact
Follow `../pm-copilot/references/artifact-output.md`: confirm inputs, **ask Markdown
or .docx**, write the `.md`, convert to `.docx` on request via your environment's native document-creation capability. Deliver both the Positioning Document and the POC worksheet.
Then offer the next stage: turning these problems into prioritized **`requirements`**.
