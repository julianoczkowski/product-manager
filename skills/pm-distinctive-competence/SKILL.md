---
name: pm-distinctive-competence
description: >-
  Articulate your organization's Distinctive Competencies the Pragmatic Institute
  way — the unique abilities to deliver value that are valued, different, and
  provable. Use when a PM says "what makes us different", "our moat", "unique
  strengths", "why us", "competitive advantage", or "distinctive competence".
  Strategy = intersect market problems with what only you can do. Produces a
  Distinctive Competencies worksheet as a Markdown or Word .docx artifact.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Distinctive Competencies (Framework: Market → Distinctive Competencies)

Articulate and leverage the organization's **unique abilities to deliver value to the
market.** These are the strengths you intersect with validated market problems to find
opportunities that are *ideal for you* (see the M5 prioritization logic in
`../pm-copilot/references/framework.md`).

## The test — an attribute is a distinctive competency only if it is all three
- **Valued** — the market actually cares about it (it maps to a real problem they'll pay to solve).
- **Different** — *materially* different from competitors and alternatives, not table stakes.
- **Provable** — you have proof (data, track record, patents, references), not just a claim.

Brainstorm broadly first (how you build, deliver, sell, and support), then filter hard.
Most candidate strengths fail the "different" or "provable" test — that's expected.

## Interview the user (batch questions)
1. Brainstorm: where does your organization deliver value across the whole lifecycle (build, deliver, sell, support, data, brand, relationships, IP)?
2. For each attribute — is it materially *different* from competitors and alternatives?
3. What's your *proof* it's both valued and different? (metrics, wins, patents, references)
4. Which market problems (from `pm-market-problems`) do these strengths let you solve better than anyone?

## Artifact template

```markdown
# Distinctive Competencies — <organization / product>

**Company:** <company>  ·  **Feature / Product:** <feature / product name>
**Author:** <author>  ·  **Date created:** <date>  ·  **Version:** 1.0

Brainstorm attributes where your organization delivers value, then test each:
*valued? · materially different? · provable?*

| Attribute | Valued? (Y/N) | Different? (Y/N) | Proof |
| :--- | :---: | :---: | :--- |
| <attribute> | Y | Y | <evidence> |
| <attribute> | Y | N | <why it fails — table stakes> |

## Articulate your Distinctive Competencies
Based on this assessment, the attributes that are valued **and** different **and**
provable are:

1. **Distinctive Competency:** <statement>
2. **Distinctive Competency:** <statement>
3. **Distinctive Competency:** <statement>

## How these map to market problems
| Distinctive Competency | Market problem it lets us win | Evidence |
| :-- | :-- | :-- |
```

## Deliver the artifact
Follow `../pm-copilot/references/artifact-output.md`: **ask Markdown or .docx**, write
the `.md`, convert to `.docx` on request via your environment's native document-creation capability. Then
offer the next stage: score opportunities against these strengths in
**`pm-opportunity-scoring`**, or set direction in **`pm-product-strategy`**.
