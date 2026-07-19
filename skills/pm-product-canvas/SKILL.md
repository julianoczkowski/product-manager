---
name: pm-product-canvas
description: >-
  Build a Pragmatic Institute Product Canvas / business case to justify investing
  in an opportunity — the market-driven way. Use when the PM asks to "make the
  business case", "justify this to leadership", "size the market", "should we buy,
  build or partner", "what's the ROI", "build a product canvas", or "get buy-in
  for this idea". Frames the opportunity as Value Proposition, Value Creation and
  Value Capture, sizes the market, runs the Buy/Build/Partner decision, and ends
  in a go/no-go recommendation with quantified risk. Produces a Product Canvas /
  Business Case as a Markdown or Word .docx artifact.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Product Canvas / Business Case (Pragmatic Framework: Business → Business Plan)

**Rule:** the Business Plan is an *objective* analysis of a market opportunity that
provides the basis for investment. Articulate what you learned in the market,
quantify the risk with a financial model, and **end with a go/no-go recommendation.**
Opinion is irrelevant; the case is built on validated market evidence. See
`../pm-copilot/references/framework.md` for the market-problem test and primitives.

Check the feature dossier first (see `../pm-copilot/references/artifact-output.md`)
and reuse the market problem, personas, positioning, competitive picture, and
distinctive competencies already established there. Where they're missing, gather
them (run `pm-market-problems`, `pm-personas`, `pm-positioning`,
`pm-competitive-landscape`, `pm-distinctive-competence`) — the canvas synthesizes them.

## The Product Canvas — three parts

**1. Value Proposition** — *why this, why us, why now*
- **Market opportunity** — the urgent, pervasive, willing-to-pay problem.
- **Buyer / user persona** — who has the problem and who pays.
- **Positioning statement** — the ≤25-word "For [persona], [product] [verb] [problem] by [verb] [benefit]."
- **Strategic alignment** — how it supports company strategy (tie to the Strategy Matrix).

**2. Value Creation** — *can we win, and at what cost*
- **Distinctive competencies** — the valued + different + provable strengths this leverages.
- **Competitive landscape** — alternatives, their strengths/weaknesses, our winning strategy.
- **Impact to buyers/users** — the positive/negative consequences; the ROI to the buyer.
- **Investment level** — resources (people, material, facility) required.

**3. Value Capture** — *what the business gets back*
- **Market size** — see sizing below.
- **Revenue generation** — projected units × price over the horizon.
- **Costs / profits** — see cost models below.
- **Distribution strategy** — the channels aligned to how the market buys.
- **Success metrics** — how you'll know it worked (Value / Quality / Progress / Satisfaction).

## Market sizing & financials
- **Revenue** = projected number of units × unit price (build a simple multi-period model).
- **Cost — pick one model:**
  - **Percentage-of-Revenue model** — estimated revenue × historical contribution margin.
  - **Estimation model** — sum the *loaded* costs of dedicated headcount across Engineering, Services, Support, Sales, Marketing, Data Science, etc.
- Quantify **risk**: state the key assumptions and what would break the model.

## Buy, Build or Partner decision tree
Work top to bottom:
1. Does the solution **leverage our distinctive competencies?** → **Build.**
2. If no — can we **create it at low cost?** → **Build.**
3. If no — do we **have the time** to reach a solution? If **no → Buy.**
4. If yes — are the **required skill sets available internally?** **Yes → Build; No → Partner.**

## Interview the user (batch questions)
1. The opportunity in one line, the persona, and the market problem + evidence.
2. Strategic fit — which company goal / Strategy-Matrix cell does it serve?
3. Distinctive competencies it leverages; main competitors/alternatives.
4. Rough units, price, time horizon; do you have contribution-margin history or headcount estimates?
5. Any gaps in the solution you'd need to fill (feeds Buy/Build/Partner)?
6. Success metrics leadership cares about.

## Artifact template
```markdown
# Product Canvas / Business Case — <Opportunity>

**Company:** <company>  ·  **Feature / Product:** <feature / product name>
**Author:** <author>  ·  **Date created:** <date>  ·  **Version:** 1.0
**Recommendation:** <GO / NO-GO / GO WITH CONDITIONS> — <one-line rationale>

## 1. Value Proposition
- **Market opportunity (problem):** <urgent, pervasive, willing-to-pay problem + evidence>
- **Buyer persona:** <who pays>  •  **User persona:** <who uses>
- **Positioning statement:** For <persona>, <product> <verb> <problem> by <verb> <benefit>.
- **Strategic alignment:** <company goal / Strategy-Matrix cell it serves>

## 2. Value Creation
| Dimension | Assessment |
| :--- | :--- |
| Distinctive competencies leveraged | <valued + different + provable> |
| Competitive landscape | <alternatives, strengths/weaknesses, our winning strategy> |
| Impact to buyers/users | <ROI / consequences> |
| Investment level | <people, material, facility> |

## 3. Value Capture
- **Market size:** <TAM/segment sizing basis>
- **Revenue model:**

| Period | Units | Unit Price | Revenue |
| :--- | ---: | ---: | ---: |
| Y1 | <#> | <$> | <$> |
| Y2 | <#> | <$> | <$> |

- **Cost model:** <Percentage-of-Revenue @ __% margin  |  Estimation: headcount × loaded cost>
- **Projected profit / contribution:** <$>
- **Distribution strategy:** <channels>
- **Success metrics:** <Value / Quality / Progress / Satisfaction metrics>

## 4. Buy, Build or Partner
<Walk the decision tree; state the recommendation and why.>

## 5. Risk & assumptions
- <key assumption> — <what breaks the model if wrong>
- > TODO: <unvalidated inputs to confirm>

## 6. Recommendation
<Go / No-go / conditions, tied to the evidence above.>
```

## Deliver the artifact
Follow `../pm-copilot/references/artifact-output.md`: confirm inputs, **ask Markdown
or .docx**, write the `.md`, and convert to `.docx` on request via your environment's native document-creation capability. Then offer the next stage: turning the approved opportunity
into a **`pm-product-roadmap`**.
