---
name: win-loss-analysis
description: >-
  Run a Pragmatic Institute Win/Loss analysis — understand why recent evaluators
  did or did not buy and the steps they took in their buying process. Use when a
  PM says "why did we win/lose", "win-loss", "why do deals slip", "churn reasons",
  "why did they pick the competitor", or "interview a lost prospect". Enforces the
  rule that win/loss is run by an objective party not involved in the sale, and
  evaluates the buying PROCESS, not the salespeople. Produces a Win/Loss Interview
  Guide and a Win/Loss Findings Report as a Markdown or Word .docx artifact.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Win/Loss Analysis (Framework: Market → Win/Loss Analysis)

**Rule:** *Win/loss should be done by someone not involved in that sales effort.* You are
evaluating **the buying process, not the salespeople**. Build a champion in sales
leadership to get access, and reassure everyone you're studying how the market buys.
Ideally the product team owns win/loss. See `../pm-copilot/references/framework.md`.

## Ranking scales (use verbatim)
- **Perception / quality (most questions):** rank **1–6**, where **1 = Poor, 6 = Excellent**, NA = Not Applicable. (Site-visit value: 1 = Low, 6 = High.)
- **Price / value:** rank **1–5**, where **1 = Lower, 3 = On Par, 5 = Higher**, plus "No Response."
- **Conclusion perception:** rank **1–6**, 1 = Poor, 6 = Excellent.

## The interview guide — 8 sections (~49 questions)

**1. Customer Information** — Company name, address, and a contacts table (Name / Title / Phone / Email).

**2. Engagement Background** — Did you know of us before initial contact? (Y/N) If so, how? Prior perception of company / products & services / support (1–6). How was initial contact made? (Unsolicited RFI / Unsolicited RFP / Cold Call / Channel Lead / Web). Who made contact, and when?

**3. Marketing** — Which informational tools did you use? (corporate & product brochures, website, white papers, analyst reports, trade magazines, technical papers…). Rate corporate literature / product literature / website (1–6) with comments.

**4. Site Visits** — Did you visit customer/reference sites? (Y/N) How many live-product sites? Which sites, and rate each. Overall value of the site visits (1–6).

**5. RFI/RFP Process** — Was the proposal well written? Presented well visually? Did it reflect understanding of your requirements? Meet functional / implementation / support requirements? What would have made it more compelling? (each 1–6 + comments)

**6. Buying Decision** — What were you using before? Extent of each contact's involvement (made final decision / voted / recommended). Who else was involved (Name / Title / Role)? What were you originally looking for, and what were your selection criteria? Did our sales team understand your needs? How did you build the vendor list? Final ranking of vendors (1st/2nd/3rd)? Did you use an outside consultant? Key factors that compelled the choice. Where were we strongest / weakest? Was there a clear point where we were winning or losing? Most important criteria in choosing the winner. Winner's major strengths over the loser. Expected business benefits. **What would it have taken to change the outcome?**

**7. Price/Value** — Price/value of products vs. other vendors (1–5). Price/value of services (1–5). What feature from another vendor should we add?

**8. Conclusion** — Current perception of company / products / services / support (1–6). Would you consider doing business with us in the future? (Y/N + why). Would you recommend us to others? (Y/N + why). General comments.

## Interview the user (batch questions)
1. Are these wins, losses, or both — and which deals/accounts?
2. Who will conduct the interviews? (must be someone not on that sales effort — confirm objectivity)
3. What do you already know about each deal (competitors, criteria, outcome)?
4. Do you want the full guide, or a short version focused on a few key questions?

## Artifact templates

### Win/Loss Interview Guide
```markdown
# Win/Loss Interview Guide — <company / deal>

**Company:** <company>  ·  **Feature / Product:** <name>
**Author (interviewer — objective, not on the sale):** <author>  ·  **Date created:** <date>
**Scales:** perception 1–6 (1=Poor, 6=Excellent, NA) · price/value 1–5 (1=Lower, 3=On Par, 5=Higher)

## 1. Customer Information
| Contact | Title | Phone | Email |
| :-- | :-- | :-- | :-- |

## 2. Engagement Background
- Did you know of us before initial contact? (Y/N) — how?
- Prior perception: company ___ / products & services ___ / support ___ (1–6)
- How/when was initial contact made? By whom?

## 3. Marketing   ## 4. Site Visits   ## 5. RFI/RFP Process
<questions per section above, each with rating + comments>

## 6. Buying Decision
- Selection criteria; who was involved; vendor ranking; where we were strongest/weakest;
  what would have changed the outcome.

## 7. Price/Value      ## 8. Conclusion
- Price/value ratings; future consideration (Y/N); would recommend (Y/N); general comments.
```

### Win/Loss Findings Report (after interviews)
```markdown
# Win/Loss Findings — <segment / period>

**Company:** <company>  ·  **Feature / Product:** <name>
**Author:** <author>  ·  **Date created:** <date>
**Interviews:** <n wins, n losses>  ·  **Conducted by:** <objective party>

## Why we won / why we lost (patterns)
<themes across interviews, with counts>

## The buying process (steps evaluators took)
<stages, decision-makers, criteria, tools used>

## Competitor strengths & our gaps
| Competitor | Where they beat us | Evidence (# interviews) |
| :-- | :-- | ---: |

## What would have changed the outcome
<the single biggest levers, quoted>

## Recommendations
- Product / positioning / sales-enablement actions, prioritized.
```

## Deliver the artifact
Follow `../pm-copilot/references/artifact-output.md`: **ask Markdown or .docx**, write
the `.md`, convert to `.docx` on request via your environment's native document-creation capability. Then
offer the next stage: feed the patterns into **`market-problems`** validation or sharpen
your **`positioning`**.
