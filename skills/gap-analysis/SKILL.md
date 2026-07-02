---
name: gap-analysis
description: >-
  Run a Pragmatic Institute Gap Analysis — a market-driven self-assessment of how
  well the team performs the 37 activities of the Pragmatic Framework, who owns
  each, and where the biggest gaps are. Use when the PM asks "where do we stand",
  "how are we doing on the framework", a product-org self-assessment, a maturity
  check, or where to focus. Produces a Gap Analysis table plus a top-3-gaps action
  plan as a Markdown or Word .docx artifact.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Gap Analysis (Pragmatic Framework: whole-framework self-assessment)

Best done with a **small cross-functional group** (product management, product
marketing, sales, development, executives). It scores every activity in the framework
so the team can agree where to invest. See the full 37-box list in
`../pm-copilot/references/framework.md`.

## The scale
- **Importance** — how important is this activity to the company? **0 (low) – 5 (high)**.
- **Assessment** — how well are you performing it today? **0 (not doing) – 5 (high)**.
- **Gap = Importance − Assessment.** The largest positive gaps are where you're
  under-performing on things that matter most.
- Also estimate **Target Hrs/Wk** vs **Actual Hrs/Wk** per activity; divide total hours
  by 40 to sanity-check how many people are needed.

**Owner role abbreviations:** PM (Product Manager), PMM (Product Marketing Manager),
MC (Marketing Communications), SE (Sales Engineer), Dev (Development), Exec (Executive),
PgM (Program Manager), PjM (Project Manager), PO (Product Owner), TPM (Technical PM), Other.

## Method
1. For each of the 7 columns' activities, agree the **Current Owner** and discuss the
   **Proposed Owner**.
2. Score **Importance (0–5)** and **Assessment (0–5)**; compute the **Gap**.
3. **Triage:** pick the **top 2–3 gaps** to focus on over the next few quarters. If more
   than three tie, the group chooses the three most important.
4. **Fix the strategic (left) side first.** If **Market Problems** has a large gap,
   fix it first — it improves everything downstream.
5. Build an action plan for the top gaps (barriers, how to close, owner).
6. **Redo the Gap Analysis in 6–9 months** to measure improvement and find the next gaps.

## Interview the user for inputs (batch questions)
1. What's the scope — a **product, portfolio, or business unit**? (Startups: whole org.)
2. Who's in the assessment group (which functions)?
3. Walk column by column: for each activity, **Importance (0–5)** and **Assessment (0–5)**,
   current owner, and rough hours. (Offer to go column-by-column so it's not overwhelming.)

## Artifact templates

### Gap Analysis
```markdown
# Pragmatic Framework Gap Analysis — <scope>

**Company:** <company>  ·  **Scope / Product:** <product, portfolio, or BU>
**Author:** <author>  ·  **Assessed by:** <names/functions>  ·  **Date created:** <date>
**Scale:** Importance 0–5 · Assessment 0–5 (0 = not doing) · Gap = Importance − Assessment

## MARKET
| Activity | Current Owner | Proposed Owner | Importance | Assessment | Gap | Target Hrs/Wk | Actual Hrs/Wk |
| :--- | :--- | :--- | ---: | ---: | ---: | ---: | ---: |
| Market Problems |  |  |  |  |  |  |  |
| Win/Loss Analysis |  |  |  |  |  |  |  |
| Distinctive Competencies |  |  |  |  |  |  |  |
| Competitive Landscape |  |  |  |  |  |  |  |
| Asset Assessment |  |  |  |  |  |  |  |

<!-- Repeat a table for FOCUS, BUSINESS, PLANNING, PROGRAMS, ENABLEMENT, SUPPORT
     using the activity lists in references/framework.md -->

**Total hours/week:** <sum>  →  **People needed (÷40):** <n>
```

### Top-3 Gaps Action Plan
```markdown
# Action Plan — Top Gaps

| Rank | Activity | Gap | Barrier | How we'll close it | Owner | By when |
| ---: | :--- | ---: | :--- | :--- | :--- | :--- |
| 1 |  |  |  |  |  |  |
| 2 |  |  |  |  |  |  |
| 3 |  |  |  |  |  |  |

**Re-assess on:** <date + 6–9 months>
```

## Deliver the artifact
Follow `../pm-copilot/references/artifact-output.md`: confirm inputs, **ask Markdown
or .docx**, write the `.md`, convert via your environment's native document-creation capability on request. Then route to
the worst-scoring box using `../pm-copilot/references/journey.md` (e.g. a Market
Problems gap → run **`market-problems`**).
