# Product Manager Copilot (skills + artefacts)

[![YouTube](https://img.shields.io/badge/YouTube-%40aiforwork__app-FF0000?logo=youtube&logoColor=white)](https://www.youtube.com/@aiforwork_app)
[![Medium](https://img.shields.io/badge/Medium-%40julian.oczkowski-000000?logo=medium&logoColor=white)](https://medium.com/@julian.oczkowski)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Julian%20Oczkowski-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/julianoczkowski/)

https://github.com/user-attachments/assets/621169c2-778c-448c-8d8d-de8597a28fce

A **product-management copilot** built on the **Pragmatic Institute Framework™**
(Foundations · Focus · Build). It guides a product manager from a raw idea all the
way to launch the *market-driven* way — and produces a **client-ready artifact
(Markdown or Word `.docx`) at every stage**.

> Ask it *"I want to build a feature"* and it won't just spit out a PRD. It routes
> you through the right Pragmatic stages — market problems → personas → positioning →
> strategy → business case → requirements → roadmap → release → launch — and hands
> you a finished document each step of the way.

This is an **Agent Skills** bundle packaged as a **Claude Code plugin**. The same
`skills/` folder works in **Claude Code**, **Claude Desktop**, and **Cursor**.

> **Disclaimer:** This is an independent tool that operationalizes the publicly
> described Pragmatic Framework for practitioners. It is **not affiliated with,
> endorsed by, or sponsored by Pragmatic Institute**. "Pragmatic Framework" and
> "Pragmatic Institute" are trademarks of their respective owner.

---

## Contents

- [What's inside](#whats-inside)
- [The skills, explained](#the-skills-explained)
- [Install](#install)
  - [Claude Desktop](#claude-desktop-as-a-personal-plugin)
  - [Claude Code](#claude-code-as-a-plugin)
  - [Cursor and other agents](#cursor-and-other-agents-via-the-skills-cli)
- [Artifacts: Markdown or Word](#artifacts-markdown-or-word-one-folder-per-feature)
- [How the journey works](#how-the-journey-works)
- [Repo layout](#repo-layout)
- [Author](#author)
- [License](#license)

---

## What's inside

**1 router + 17 stage skills + a shared knowledge base.**

| Course | Skills |
|---|---|
| **(Router)** | `pm-copilot` — detects intent and orchestrates the journey |
| **Foundations** | `pm-market-problems` · `pm-win-loss-analysis` · `pm-distinctive-competence` · `pm-competitive-landscape` · `pm-personas` · `pm-positioning` · `pm-gap-analysis` |
| **Focus** | `pm-product-strategy` · `pm-opportunity-scoring` · `pm-product-canvas` · `pm-product-roadmap` |
| **Build** | `pm-requirements` · `pm-use-scenarios` · `pm-prd` · `pm-release-plan` · `pm-stakeholder-communication` |
| **Go-to-market** | `pm-launch-plan` |

Each skill embeds the real Pragmatic method — the urgent/pervasive/willing-to-pay
test, the four market segments, the positioning-statement formula, the
`Priority = Market Evidence × Impact` prioritization, the Strategy Matrix, opportunity
scoring, roadmap-vs-release, the MRD and Release Charter templates, and more — and
ends by writing the corresponding artifact.

The shared knowledge base lives in `skills/pm-copilot/references/`:
- `framework.md` — the 37-box map, definitions, rules, and reusable primitives.
- `journey.md` — stages → skills → artifacts, and the intent-routing table.
- `artifact-output.md` — the shared "ask Markdown or .docx, then write it" procedure.

---

## The skills, explained

Each skill runs one stage of the market-driven journey and ends by writing an artifact
into the feature's folder. You can invoke any of them directly, or let `pm-copilot`
route you.

https://github.com/user-attachments/assets/520bbb41-67b0-42dd-a65c-2d52a6920fca

**Router**
- **`pm-copilot`** — the entry point. Figures out what you're asking for, tells you where
  you are in the framework, and routes you to the right stage — or runs the whole
  "build a feature" sequence end to end. *(Orchestration; no artifact of its own.)*

**Foundations — understand the market**
- **`pm-market-problems`** — Discover and validate real problems that are *urgent, pervasive,
  and worth paying to solve*; who to interview (the four segments), observation vs.
  interview, NIHITO. → *Market Discovery notes + a scored Market Problems Table.*
- **`pm-win-loss-analysis`** — Understand why buyers chose you or a competitor, run by an
  objective interviewer who evaluates the buying process, not the salespeople. → *Win/Loss
  Interview Guide + Findings Report.*
- **`pm-distinctive-competence`** — Pin down what your organization can do that rivals can't —
  attributes that are *valued + different + provable*. → *Distinctive Competencies worksheet.*
- **`pm-competitive-landscape`** — Map competitors and alternatives, decide when to fight and
  when to run, and plot the Solution Matrix. → *Competitive analysis + Solution Matrix.*
- **`pm-personas`** — Build evidence-based **buyer** and **user** personas (usually different
  people). → *Buyer Persona + User Persona.*
- **`pm-positioning`** — Describe the product by the problems it solves, not features; the
  ≤25-word positioning statement + problem-oriented capabilities. → *Positioning Document
  + POC worksheet.*
- **`pm-gap-analysis`** — Score your team across all 37 framework activities to find the
  biggest gaps and where to invest first. → *Gap Analysis table + top-3 action plan.*

**Focus — turn knowledge into strategy**
- **`pm-product-strategy`** — Force the *who-to-win × what-to-build* choice with the Strategy
  Matrix, and compare the team's view against leadership's. → *Strategy Matrix + alignment notes.*
- **`pm-opportunity-scoring`** — Rank competing opportunities objectively on competency fit,
  competition, investment, and buyer impact. → *Opportunity Scorecard.*
- **`pm-product-canvas`** — Build the business case: value prop / creation / capture, market
  sizing, buy-build-partner, and a go/no-go. → *Product Canvas / Business Case.*
- **`pm-product-roadmap`** — Communicate vision and phases as a *plan, not a commitment*
  (roadmap vs. release plan; Desire → Discover → Define → Do). → *Product Roadmap.*

**Build — define and deliver**
- **`pm-requirements`** — Turn validated problems into prioritized market requirements
  ("*[persona] has [problem] with [frequency]*", Priority = Evidence × Impact). → *Market
  Requirements Document (MRD).*
- **`pm-use-scenarios`** — Put each problem in a day-in-the-life story (Problem Card; avoid
  ambiguous terms; the *What* vs. *How* split). → *Use Scenarios document.*
- **`pm-prd`** — Assemble personas + problems + requirements + scenarios into the full spec
  the team builds from. → *Product Requirements Document (PRD).*
- **`pm-release-plan`** — Commit an increment: MVP scope, themes ("100% of something"),
  estimation, market window, and sign-off. → *Release Plan / Charter.*
- **`pm-stakeholder-communication`** — Keep everyone aligned: the Influence × Importance
  matrix, a comms plan, and status updates that expose risk early. → *Stakeholder
  Communication Plan + Status Update.*

**Go-to-market**
- **`pm-launch-plan`** — Plan a launch where *readiness is more than product readiness*:
  messaging, sales enablement, demand programs, a readiness checklist, and metrics. →
  *Launch Plan + Readiness Checklist.*

---

## Install

### Claude Desktop (as a personal plugin)
Add this repo as a plugin marketplace from the app UI.

https://github.com/user-attachments/assets/d01f1a09-3438-4fc6-8dd5-687a1594f077

1. Open **Settings → Customize → Connectors**.
2. Next to **Personal plugins**, click the **+**, then **Add → Add marketplace**.
3. Choose **Add from a repository**.
4. Paste the repo URL — `https://github.com/julianoczkowski/product-manager` (or just
   `julianoczkowski/product-manager`) — and click **Sync**.
5. Open the **Plugins → Personal** directory, find **Product Manager Copilot** under
   the **product-manager** marketplace, open it, and click **Install**.

### Claude Code (as a plugin)
```
/plugin marketplace add julianoczkowski/product-manager
/plugin install product-manager@product-manager-marketplace
```

### Cursor and other agents (via the Skills CLI)
Install straight from this repo with Vercel's open
[Skills CLI](https://github.com/vercel-labs/skills):
```
npx skills add julianoczkowski/product-manager
```

---

## Artifacts: Markdown or Word, one folder per feature

Every stage asks how you want the deliverable — **Markdown (`.md`) or Word (`.docx`)**.

<img width="1093" height="606" alt="artefacts" src="https://github.com/user-attachments/assets/2c7f580c-af0d-477d-8134-db017515e911" />

- **One folder per feature.** The first artifact of a session creates a folder named
  after your feature/product (e.g. `satellite-tracking-system/`) in the working
  directory, and every subsequent artifact is saved there and numbered
  (`01-…`, `02-…`) — so you accumulate a complete, ordered dossier, not scattered files.
- **Every artifact carries the same header:** Company · Feature/Product · Author · Date.
  These are collected once at the start of a session and reused.
- **DOCX is produced natively.** The `.docx` is created using whatever native
  document-creation capability the host environment (Claude Code / Cursor / Cowork)
  provides — there is **no bundled converter script or Python/pandoc dependency** to
  install. Markdown stays the source of truth; if an environment can't write `.docx`,
  the skill delivers polished Markdown and tells you so rather than faking a file.

---

## How the journey works

<img width="1093" height="606" alt="flow" src="https://github.com/user-attachments/assets/1390bea8-d0a5-40fb-b4d5-39796cae249f" />


1. **Orient** — the router reads the framework map and figures out where you are.
2. **Route** — it maps your ask to the right stage (see `journey.md`).
3. **Interview** — the stage skill asks the few questions it needs (evidence first).
4. **Draft** — it produces the artifact, leading with the *market problem*, citing
   evidence, and flagging assumptions instead of inventing data.
5. **Deliver** — Markdown or `.docx`, saved into the feature's folder and numbered so
   your artifacts accumulate into a complete, ordered dossier.
6. **Advance** — it names the next Pragmatic stage and offers to continue.

---

## Author

<img width="236" height="236" alt="avatar2" src="https://github.com/user-attachments/assets/5677ddb5-6b0b-4054-a70b-a143761dd307" />

Built by **Julian Oczkowski** — I build AI tools for knowledge work.

- 🎥 **[YouTube · @aiforwork_app](https://www.youtube.com/@aiforwork_app)** — walkthroughs and AI-for-work tutorials
- ✍️ **[Medium](https://medium.com/@julian.oczkowski)** — deep dives on product and AI workflows
- 💼 **[LinkedIn](https://www.linkedin.com/in/julianoczkowski/)** — connect and follow along

## License
[MIT](./LICENSE) — covers this project's own content (skill authoring, docs, manifests).
The Pragmatic Framework concepts are the intellectual property of Pragmatic Institute;
this project is an independent, unaffiliated practitioner aid. See [NOTICE](./NOTICE.md)
for the full trademark disclaimer and [SECURITY](./SECURITY.md) to report issues.
