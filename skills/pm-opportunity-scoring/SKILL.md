---
name: pm-opportunity-scoring
description: >-
  Score and rank product opportunities objectively with the Pragmatic Institute
  Opportunity Scoring model — across distinctive competency fit, competitive
  landscape, investment level, and impact to buyers/users. Use when the PM asks
  which idea to pursue, "score these opportunities", prioritize projects/bets,
  or compare options objectively instead of by opinion. Produces an Opportunity
  Scorecard as a Markdown or Word .docx artifact.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Opportunity Scoring (Pragmatic Framework: Focus / Business)

Evaluate candidate opportunities objectively so a decision rests on evidence, not the
loudest voice. Score each opportunity on four attributes using a **1-to-5 scale where
1 = Least Favorable and 5 = Most Favorable.** See `../pm-copilot/references/framework.md`.

## The four attributes (1 = least favorable, 5 = most favorable)
| Attribute | What it measures | 1 (least) → 5 (most) |
| :--- | :--- | :--- |
| **Distinctive Competencies** | How much it relies on abilities we already have (valued, different, provable) | 1 = requires building a new competency → 5 = directly uses existing strong competencies |
| **Competitive Landscape** | Size/strength of alternatives | 1 = highly competitive (rival has pricing power/brand equity) → 5 = low competition (we can freeze out the market) |
| **Investment Level** | Resources (people, material, facilities) required | 1 = very high (ground-up build) → 5 = very low (re-use existing assets) |
| **Impact to Buyers/Users** | Consequences for current & potential customers | 1 = negative outweighs positive → 5 = significant positive impact / high ROI for buyer |

**Total = sum of the four scores** (4–20). Rank opportunities by total, but read the
per-attribute scores too — a low Investment + high Impact "no brainer" may beat a higher
total that depends on a competency you don't have.

## Method
1. List the candidate opportunities (ideally ones already validated as urgent, pervasive
   and willing-to-pay — see `pm-market-problems`).
2. Score each attribute 1–5 and **write the rationale** (the evidence) for each score.
3. Sum, rank, and discuss — especially where scores are low on Distinctive Competencies
   (can we really win?) or Investment (can we afford it?).

## Interview the user for inputs (batch questions)
1. What are the **opportunities** to compare? (Name each + the market problem it solves.)
2. For each: do we already have the **competencies** to deliver it, or must we build them?
3. How **competitive** is the space (who else, how entrenched)?
4. Rough **investment** — reuse existing assets, or ground-up?
5. Expected **impact/ROI** for buyers and users (and any downside)?

## Artifact template
```markdown
# Opportunity Scorecard — <product/BU>

**Company:** <company>  ·  **Feature / Product:** <feature / product name>
**Author:** <author>  ·  **Date created:** <date>  ·  **Version:** 1.0
**Scale:** 1 = Least Favorable → 5 = Most Favorable

| Opportunity | Distinctive Competencies | Competitive Landscape | Investment Level | Impact to Buyers/Users | Total | Rank |
| :--- | ---: | ---: | ---: | ---: | ---: | ---: |
| <Opportunity A> | 4 | 3 | 2 | 5 | 14 | 2 |
| <Opportunity B> | 5 | 4 | 4 | 4 | 17 | 1 |

## Rationale (evidence behind each score)
### <Opportunity A>
- **Distinctive Competencies (4):** <why>
- **Competitive Landscape (3):** <why>
- **Investment Level (2):** <why>
- **Impact to Buyers/Users (5):** <why>

## Recommendation
<Which opportunity(ies) to pursue and why — reference the scores and the market evidence.>
```

## Deliver the artifact
Follow `../pm-copilot/references/artifact-output.md`: confirm inputs, **ask Markdown
or .docx**, write the `.md`, convert via your environment's native document-creation capability on request. Next stage:
build the full business case for the winner with **`pm-product-canvas`**.
