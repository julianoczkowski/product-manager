---
name: pm-product-strategy
description: >-
  Build a Pragmatic Institute Strategy Matrix — a forced-choice 4×4 that decides
  who to win and what to build over a set time frame, and surfaces alignment
  between the product team and leadership. Use when the PM asks about product
  strategy, "where should we invest", "what should we build for whom", focus,
  prioritizing markets, or avoiding a spread-too-thin roadmap. Produces a Strategy
  Matrix as a Markdown or Word .docx artifact.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Product Strategy (Pragmatic Framework: Focus → Market Definition / Product Portfolio)

A good product strategy balances **"Who do we want to pursue?"** with **"How do we
solve the market's problems?"** and must support the company strategy. The **Strategy
Matrix** forces the team to make tough choices early so resources aren't spread thin
("peanut butter"). See `../pm-copilot/references/framework.md`.

Two strategies to compare:
- **Implicit strategy** — what the product team, working from market data, believes the
  focus should be (and what resources are actually being allocated).
- **Explicit strategy** — what leadership clearly states the focus is.
Filling both **independently** and comparing them reveals alignment and gaps.

## The matrix
Top-left cell = the **TIME FRAME** (e.g. 1 / 3 / 5 years).

- **Columns — what to build:**
  - **Improve Existing Products** — enhancements/updates, usually no added price.
  - **Add New Options** — monetized add-on modules that **require** the existing product (can't stand alone).
  - **Offer New Products** — net-new standalone offerings (own SKU / pricing / launch).
  - **Invest in New Technology** — deep technical change: resolve tech debt, re-architect, on-prem → SaaS.
- **Rows — who to win:**
  - **Pursue Existing Customers** — satisfaction, renewal, larger share of wallet.
  - **Convert Competitors' Customers** — displace competition; reduce switching costs.
  - **Win Potentials / New Customers** — net-new customers who have the problem but aren't shopping.
  - **Approach New Segments** — invest in new segments to solve net-new problems.

**Rule: focus on no more than 4 of the 16 cells.**

## Method
1. Set the **time frame**.
2. The product team fills the matrix from **market data** (implicit); leadership fills a
   blank one independently (explicit). Mark cells with an **X**, planned resources, or a
   **% allocation out of 100**.
3. **Compare** — overlaps = alignment; gaps = the conversation to have.
4. Revisit at intervals as the market changes.

## Interview the user for inputs (batch questions)
1. What **time frame** are we planning for?
2. What does **leadership** say the strategy/focus is (the explicit strategy)?
3. Given the market evidence, where do **you** think we should focus (implicit)?
4. Where are resources **actually** going today?
5. Any hard constraints (must-serve customers, contractual commitments, tech debt)?

## Artifact template
```markdown
# Strategy Matrix — <product/BU>  ·  Time frame: <1/3/5 yrs>

**Company:** <company>  ·  **Feature / Product:** <feature / product name>
**Author:** <author>  ·  **Date created:** <date>  ·  **Version:** 1.0

## Implicit strategy (product team, from market data)
| Who to win \ What to build | Improve Existing | Add New Options | Offer New Products | Invest in New Tech |
| :--- | :---: | :---: | :---: | :---: |
| Pursue Existing Customers |  |  |  |  |
| Convert Competitors' Customers |  |  |  |  |
| Win Potentials / New Customers |  |  |  |  |
| Approach New Segments |  |  |  |  |
<!-- Mark ≤4 cells with % of 100 (or X). Note the market evidence behind each. -->

## Explicit strategy (leadership)
<!-- Same grid, filled independently by leadership. -->

## Alignment
- **Agreed focus (overlap):** <cells>
- **Gaps / disagreements to resolve:** <cells + the discussion needed>
- **Chosen focus (≤4 cells) and why:** <rationale tied to market problems + distinctive competence>
```

## Deliver the artifact
Follow `../pm-copilot/references/artifact-output.md`: confirm inputs, **ask Markdown
or .docx**, write the `.md`, convert via your environment's native document-creation capability on request. Next stage:
score the specific opportunities within your chosen cells with **`pm-opportunity-scoring`**,
then make the case with **`pm-product-canvas`**.
