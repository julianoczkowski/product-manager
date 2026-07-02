# Pragmatic PM

A **product-management copilot** built on the **Pragmatic Institute Framework™**
(Foundations · Focus · Build). It guides a product manager from a raw idea all the
way to launch the *market-driven* way — and produces a **client-ready artifact
(Markdown or Word `.docx`) at every stage**.

> Ask it *"I want to build a feature"* and it won't just spit out a PRD. It routes
> you through the right Pragmatic stages — market problems → personas → positioning →
> strategy → business case → requirements → roadmap → release → launch — and hands
> you a finished document each step of the way.

This is an **Agent Skills** bundle packaged as a **Claude Code plugin**. The same
`skills/` folder works in **Claude Code**, **Cursor**, and **Claude Cowork**.

> **Disclaimer:** This is an independent tool that operationalizes the publicly
> described Pragmatic Framework for practitioners. It is **not affiliated with,
> endorsed by, or sponsored by Pragmatic Institute**. "Pragmatic Framework" and
> "Pragmatic Institute" are trademarks of their respective owner.

---

## What's inside

**1 router + 17 stage skills + a shared knowledge base.**

| Course | Skills |
|---|---|
| **(Router)** | `pragmatic-pm` — detects intent and orchestrates the journey |
| **Foundations** | `market-problems` · `win-loss-analysis` · `distinctive-competence` · `competitive-landscape` · `personas` · `positioning` · `gap-analysis` |
| **Focus** | `product-strategy` · `opportunity-scoring` · `product-canvas` · `product-roadmap` |
| **Build** | `requirements` · `use-scenarios` · `prd` · `release-plan` · `stakeholder-communication` |
| **Go-to-market** | `launch-plan` |

Each skill embeds the real Pragmatic method — the urgent/pervasive/willing-to-pay
test, the four market segments, the positioning-statement formula, the
`Priority = Market Evidence × Impact` prioritization, the Strategy Matrix, opportunity
scoring, roadmap-vs-release, the MRD and Release Charter templates, and more — and
ends by writing the corresponding artifact.

The shared knowledge base lives in `skills/pragmatic-pm/references/`:
- `framework.md` — the 37-box map, definitions, rules, and reusable primitives.
- `journey.md` — stages → skills → artifacts, and the intent-routing table.
- `artifact-output.md` — the shared "ask Markdown or .docx, then write it" procedure.

---

## Install

### Claude Code (as a plugin)
```
/plugin marketplace add /Users/Shared/Development_Projects/product-manager
/plugin install pragmatic-pm@pragmatic-pm-marketplace
```
Or, once pushed to GitHub: `/plugin marketplace add <owner>/<repo>` then
`/plugin install pragmatic-pm@pragmatic-pm-marketplace`.

Then just talk to it: *"I want to build a feature that lets users export reports."*
The `pragmatic-pm` skill auto-activates and routes you.

### Cursor / Claude Cowork (as portable skills)
Copy the `skills/` subfolders into the project's skills directory (e.g.
`.claude/skills/`). The skills are plain `SKILL.md` files with **no external
dependencies and no bundled scripts**, so they load and run directly in any of the
three tools.

---

## Artifacts: Markdown or Word, one folder per feature

Every stage asks how you want the deliverable — **Markdown (`.md`) or Word (`.docx`)**.

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

1. **Orient** — the router reads the framework map and figures out where you are.
2. **Route** — it maps your ask to the right stage (see `journey.md`).
3. **Interview** — the stage skill asks the few questions it needs (evidence first).
4. **Draft** — it produces the artifact, leading with the *market problem*, citing
   evidence, and flagging assumptions instead of inventing data.
5. **Deliver** — Markdown or `.docx`, saved into the feature's folder and numbered so
   your artifacts accumulate into a complete, ordered dossier.
6. **Advance** — it names the next Pragmatic stage and offers to continue.

---

## Repo layout
```
product-manager/
├── .claude-plugin/
│   ├── plugin.json
│   └── marketplace.json
├── skills/
│   ├── pragmatic-pm/         # router + references/ (framework, journey, artifact-output)
│   ├── market-problems/ … launch-plan/   # 17 stage skills
├── README.md
└── LICENSE
```

## License
MIT (for the plugin code and skill authoring). The Pragmatic Framework concepts are
the intellectual property of Pragmatic Institute; this project is an independent,
unaffiliated practitioner aid.
