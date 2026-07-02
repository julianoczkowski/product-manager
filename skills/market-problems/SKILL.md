---
name: market-problems
description: >-
  Run Pragmatic Institute market discovery and validate real market problems
  before anything gets built. Use when a PM says "I want to build a feature",
  "do market research", "talk to customers", "discovery", "validate this idea",
  "is this problem real", "NIHITO", or "who should I interview". Enforces the
  outside-in rule: build only for problems that are urgent, pervasive, and that
  the market will pay to solve. Produces a Market Discovery Document and a Market
  Problems Table as a Markdown or Word .docx artifact.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Market Problems — discovery & validation (Framework: Market → Market Problems)

**Rule:** *The answers to most of your questions are not in the building.* Discover,
collect, analyze and communicate problems found in the market, then validate they are
**urgent, pervasive, and that the market is willing to pay** to solve them. See
`../pragmatic-pm/references/framework.md` for the full map.

## Who to listen to

**The Noisy 20% vs. the Quiet 80%.** The noisy 20% (your most excited/unhappy customers
plus loud internal voices — an exec's advisory board, a big-client sales rep, support)
give a limited, skewed view. The **quiet 80%** won't come to you; you must go find them
(industry conferences — leave your booth; professional associations; LinkedIn; end-user
training). *Noisy customers don't represent the whole market.*

**The four market segments** — each is "a person with a problem." Balance interviews
across all four:

| Segment | Lens they speak through | The question to ask |
| :--- | :--- | :--- |
| **Customers** (bought yours) | your product | "What other problems should we be solving for you that we aren't solving today?" |
| **Competitors' Customers** | the competitor's product | "What other problems should we solve that your current product isn't solving?" |
| **Evaluators** (shopping now) | win/loss — don't disrupt the sale | "Why did we win (or lose) your business?" |
| **Potentials** (not shopping) | *no lens — best for innovation* | "What problems are you facing, and why are you not looking for a solution?" |

**NIHITO — Nothing Interesting Happens In The Office.** Recommend ~**10 market visits
per product manager per quarter**. It feels like cold calling, but you aren't selling —
state what's in it for them and expect many "no"s.

## Discovery techniques

**Observation** — take thorough notes, look for patterns, minimize interruptions; if
something catches your eye, ask. Answer: What do customers do / how / why? What's done
manually that could be automated? What's multi-step that could be streamlined? How do
they interact with your product? When do they use other systems, search for info, or
need help?

**Interview** — prepare beforehand; use high-gain, open-ended questions; spend most of
the time *listening*, not educating. Ask: What obstacles keep you from your goals? How
are your goals measured? What do you think about our product/company? What else have you
considered? How bad is the problem? How bad do things have to get before they're fixed?
Where does this fall on your priorities?

## Validate the problem — the three-part test

An **opportunity** is the intersection of all three (fail any one → don't build):
- **Urgency** — When is it urgent? Where is the urgency coming from? What's the level?
- **Pervasiveness** — Is it big enough to build a business on? (look for the quiet 80%)
- **Willingness to pay** — Is it painful enough to pay to solve? Who will pay — and will they pay *you*?

Validate quantitatively with **surveys** (close-ended questions on the three criteria —
avoid leading questions) and **experimentation** (inexpensive, low-fidelity tests of
your hypothesis).

## Interview the user (batch questions)
1. What product/feature area, and who do you think has the problem (persona/segment)?
2. What evidence do you already have (interviews, tickets, win/loss, usage, surveys)?
3. Which of the four segments have you actually talked to? Which are you missing?
4. For each candidate problem: how urgent, how pervasive, would they pay — and what's the proof?

## Artifact templates

### Market Discovery Document (one per visit/interview)
```markdown
# Market Discovery Document

## Contact Info
- **Name:**  |  **Title:**  |  **Organization:**
- **Work phone:**  |  **Email:**  |  **Website:**

## Product Info
- **Product name:**

## Purpose of Call
<why you're talking to them>

## Call Notes
<what they said — verbatim where possible>

## Key Observations and Problems
<problems in the persona's first-person voice; note urgency / pervasiveness / willingness-to-pay signals; which segment>

---
**Company:** <company>  ·  **Feature / Product:** <feature / product name>
**Author:** <author>  ·  **Date created:** <date>  ·  **Version:** 1.0
```

### Market Problems Table (roll-up across discovery)
```markdown
# Market Problems Table — <product / market>

| Persona | Problem Name (first person) | Market Evidence | Impact (1–5, 99999=contractual) | Priority (Evidence × Impact) | Group |
| :--- | :--- | ---: | ---: | ---: | :--- |
| <persona> | "I can't …" | <count of inputs> | <1–5> | <=E×I> | <theme> |

**Market Evidence** = tally of documented occurrences across inputs (interviews, surveys,
sales calls, support tickets, win/loss, analyst reports, reviews, usage data).
Sort by Priority descending. Problems that clear urgent + pervasive + willing-to-pay
become candidate requirements.
```

## Deliver the artifact
Follow `../pragmatic-pm/references/artifact-output.md`: confirm inputs (flag thin
evidence and recommend specific NIHITO visits to fill it), **ask Markdown or .docx**,
write the `.md`, and convert to `.docx` on request via your environment's native document-creation capability.
Then offer the next stage: define **`personas`** for the people who have these problems,
or write **`positioning`** around the validated problems.
