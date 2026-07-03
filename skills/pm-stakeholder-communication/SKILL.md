---
name: pm-stakeholder-communication
description: >-
  Build a Pragmatic stakeholder communication plan and status updates that expose
  risk early and speak each audience's language. Use when the PM asks to manage
  stakeholders, plan comms, write an exec/status update, a project status report,
  a steering-committee update, or "keep everyone aligned". Covers the
  Identify→Analyze→Communicate steps, the Influence×Importance matrix, and the four
  metric categories. Produces a Stakeholder Communication Plan and a Status Update
  as a Markdown or Word .docx artifact.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Stakeholder Communications (Pragmatic Framework: Planning → Stakeholder Communications)

> **Executives communicate in spreadsheets, not screenshots.** **Track trends, not
> absolute numbers.** Manage proactive communications from strategy through execution.

See `../pm-copilot/references/framework.md` for the primitives.

## Three steps
**Identify → Analyze → Communicate.**
1. **Identify** every stakeholder or group affected by or influencing the work.
2. **Analyze** each on two axes and place them on the matrix.
3. **Communicate** on a plan tuned to each quadrant.

**Influence = informal authority** — the power to facilitate or impede an objective;
the ability to persuade or coerce others toward a course of action.
**Importance = formal authority** — the priority given to satisfying that
stakeholder's needs; their power to drive, change, or cancel the work.

## Stakeholder Management Matrix (2×2)
Y = Influence (informal authority), X = Importance (formal authority):

| | Low Importance | High Importance |
| :--- | :--- | :--- |
| **High Influence** | Keep Satisfied | **Manage Closely** |
| **Low Influence** | Monitor | Keep Informed |

## Communication plan — When / How
- **When?** How often · what stages · what depth.
- **How?** What format · what channel.
- **Common errors to avoid:** surprising stakeholders with bad news (ignore/delay/surprise);
  relying solely on email/electronic comms; delivering **disparate** status to different stakeholders.

## Metric categories (pick what's meaningful per stakeholder)
- **Value** — LTV; LTV:CAC.
- **Quality** — defects; % test coverage; fix-to-feature ratio; return rate.
- **Progress** — lead & cycle time; velocity/burndown; % dependencies.
- **Satisfaction** — NPS; CSAT; renewal rate; time-to-value; customer effort (CES).

## Interview the user (batch questions)
1. **Who are the stakeholders** (people/groups) touched by this work?
2. For each — how much **influence** (informal) and **importance** (formal) do they have?
3. What **outcome/metric** does each one actually care about?
4. What **cadence and channel** fits each (weekly meeting, email digest, dashboard)?
5. What's the **current status** and any risks to surface?

## Artifact templates

### Stakeholder Communication Plan
```markdown
# Stakeholder Communication Plan — <Project/Product>

**Company:** <company>  ·  **Feature / Product:** <feature / product name>
**Author:** <author>  ·  **Date created:** <date>

| Stakeholder | Category | Communicator | Channel | Artifact | Frequency | Metric Category | Specific Metrics |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Angela (SVP Sales) | Manage Closely | Jeff (PM) | Weekly meeting (+ email) | Initiative status template | Weekly, Thursday | Value | LTV |
| <name/role> | Keep Informed | | | | | | |
| <name/role> | Keep Satisfied | | | | | | |
| <name/role> | Monitor | | | | | | |
```

### Status Update (Initiative-based)
```markdown
# Status Update — <Product/Release> — <date>

**Company:** <company>  ·  **Feature / Product:** <feature / product name>
**Author:** <author>  ·  **Date created:** <date>

| Initiative | Description | Delivery | Status | Path to Green | Update | What's Next |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| <name> | <goal of this work> | <date/quarter> | 🟢 On track | — | <latest since last report> | <planned work> |
| <name> | <goal> | <date> | 🟡 Elevated risk | <steps to recover> | <milestones met / risks / scope changes> | <next> |

**Status legend:** 🟢 On track · 🟡 Elevated risk · 🔴 High risk · 🔵 Completed · ⚪ Not started · ⚫ On hold.
```

(For an exec audience, offer a **metric-based** variant: Business Objective | Metric
Category | Metric to Move | Goal State | Current State | Initiative | Outcome
[Measuring / Positive / Negative / Uncertain].)

## Deliver the artifact
Follow `../pm-copilot/references/artifact-output.md`: confirm inputs, **ask Markdown
or .docx**, write the `.md`, convert to `.docx` on request via your environment's native document-creation capability. Deliver the plan and a first status update. Then offer the
next stage: **`pm-launch-plan`** as the release nears its market window.
