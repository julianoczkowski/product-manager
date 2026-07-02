---
name: competitive-landscape
description: >-
  Map the Pragmatic Institute Competitive Landscape — identify competitive AND
  alternative offerings, assess their strengths and weaknesses, and develop a
  strategy for winning (knowing when to fight and when to run). Use when a PM says
  "competitive analysis", "competitors", "battlecard", "how do we win against X",
  "alternatives", or "where do we play". Includes the Solution Matrix (customer
  impact vs. depth of investment). Produces a Competitive Landscape analysis and a
  Solution Matrix as a Markdown or Word .docx artifact.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Competitive Landscape (Framework: Market → Competitive Landscape)

Identify competitive **and alternative** offerings in the market, assess their strengths
and weaknesses, and develop a strategy for winning. Frame the comparison universe
correctly — customers don't just choose between named competitors; "do nothing",
spreadsheets, and in-house builds are alternatives too. Analytical rule of thumb: know
**when to fight and when to run.** See `../pragmatic-pm/references/framework.md`.

## The Solution Matrix

Plot **your** products and **competitors'** products on a 2×2:
- **X-axis — Impact to Customer:** Low → High
- **Y-axis — Depth of Investment:** Low → High

| Quadrant | Investment / Impact | Meaning |
| :-- | :-- | :-- |
| **Utilities** | Low investment / Low impact | Keep the lights on; don't over-invest. |
| **No Brainer** | Low investment / High impact | Do these — best return. |
| **Strategic Vision** | High investment / High impact | Big bets that need a business case. |
| **"Why?"** | High investment / Low impact | Avoid — cost without customer value. |

Use the Solution Matrix to: assess incremental technology investment vs. relative market
value with development; frame how the product improves operations when interviewing the
market; position against the competition; price products; position a product portfolio;
and determine sales-channel strategy.

## Interview the user (batch questions)
1. What problem/segment are we competing in, and which personas decide?
2. Who are the direct competitors — and what are the *alternatives* (do nothing, in-house, adjacent tools)?
3. For each: strengths, weaknesses, pricing power, brand equity, and where they beat us?
4. Where do our offerings and theirs sit on customer impact vs. depth of investment?

## Artifact templates

### Competitive Landscape analysis
```markdown
# Competitive Landscape — <market / segment>

**Company:** <company>  ·  **Feature / Product:** <feature / product name>
**Author:** <author>  ·  **Date created:** <date>  ·  **Version:** 1.0
**The comparison universe:** <named competitors + alternatives incl. "do nothing">

| Competitor / Alternative | Strengths | Weaknesses | Our winning strategy (fight or run) |
| :-- | :-- | :-- | :-- |
| <competitor> | <strengths> | <weaknesses> | <how we win, or why we avoid> |

## Where we win
<the problems and segments where our distinctive competencies beat every alternative>

## Where we should not fight
<segments/problems where a competitor has pricing power or brand equity — run>

## Evidence
<win/loss counts, analyst reports, pricing data; flag assumptions>
```

### Solution Matrix
```markdown
# Solution Matrix — <portfolio / market>

Axes: X = Impact to Customer (Low→High), Y = Depth of Investment (Low→High).

| | Low Impact | High Impact |
| :-- | :-- | :-- |
| **High Investment** | "Why?" — <items> | Strategic Vision — <items> |
| **Low Investment** | Utilities — <items> | No Brainer — <items> |

**Our products:** <plotted>
**Competitors' products:** <plotted>
**Read-out:** <where to invest, where to hold, where competitors are exposed>
```

## Deliver the artifact
Follow `../pragmatic-pm/references/artifact-output.md`: **ask Markdown or .docx**, write
the `.md`, convert to `.docx` on request via your environment's native document-creation capability. Then
offer the next stage: sharpen **`positioning`** against these competitors, or set
investment direction in **`product-strategy`**.
