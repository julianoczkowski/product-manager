# Producing the artifact (shared procedure)

Every Product Manager Copilot skill ends by producing a **client-ready artifact**. Follow this
procedure identically across all skills so the experience is consistent.

**Know your host environment.** This plugin runs in hosts with full file tools —
Claude Code CLI, Cursor, VS Code Copilot — where folders work, and in app hosts —
Claude Desktop, the Codex desktop app — where files are delivered individually and
you may not be able to create folders. The steps below say what to do in each case.
Never fail or stall a step because the environment can't do folders; the session's
context carries the dossier either way.

## 1. Collect the standard header inputs (once per feature, then reuse)
Every artifact carries the same header. Ask for these **once** and reuse them for
every subsequent artifact (don't re-ask each time):

- **Company name** — the organization the work is for.
- **Feature / Product name** — the feature or product this work is about.
- **Author** — the person creating the artifact (their name).
- **Date created** — today's date (use the current date; the user can override).

If you're resuming a feature that already has artifacts (§3), read these from the
most recent artifact's header instead of re-asking. If any are unknown, ask for them
before writing the first artifact. If the user says "just use X" or "skip it," record
a clear placeholder (e.g. `<company>`), never invent a real-looking value.

## 2. Put the mandatory header at the top of EVERY artifact
Immediately under the artifact's H1 title, insert this block **verbatim** (filled in).
This **overrides** any header shown in an individual skill's template — always include
these four fields, plus any doc-specific fields the template adds (version, persona, etc.):

```markdown
**Company:** <company>  ·  **Feature / Product:** <feature / product name>
**Author:** <author>  ·  **Date created:** <date>
```

All four fields must always be present, but a label may be adapted when the document
type demands it — e.g. **Scope / Product** in a gap analysis, or
**Author (interviewer)** in a win/loss guide. Adapt labels, never drop fields.

## 3. Find or resume the feature dossier
All artifacts for a feature/product belong together as one **dossier**, so the PM ends
up with a complete, ordered set — not scattered files. Most users arrive through
`pm-copilot` and build the dossier across several sessions, so **always check for an
existing dossier before starting a new one**:

- **Look first.** Check the working directory for a slugified feature folder (e.g.
  `satellite-tracking-system/`) or loose `NN-*.md` artifacts matching this feature —
  and in app hosts, check the conversation context for artifacts produced earlier.
  If found, **resume**: reuse the folder (or naming), the header inputs (§1), the
  stage numbering, and the open caveats (§4). Don't create a second dossier or
  re-interview for what it already answers.
- **Folder-capable hosts** (Claude Code CLI, Cursor, VS Code Copilot): create the
  feature folder in the user's current working directory the first time you produce
  an artifact, and save **every** artifact for that feature into it. Confirm the
  folder name with the user if unsure.
- **File-only hosts** (Claude Desktop, Codex desktop app): don't attempt folders.
  Deliver standalone files named `<feature-slug>-NN-<artifact>.md` (e.g.
  `satellite-tracking-system-06-positioning.md`) so the files still group and sort as
  a dossier wherever the user saves them.

## 4. Reuse prior artifacts and carry their caveats forward
The dossier is the memory of the engagement — downstream artifacts must build on it,
not ignore it or silently look better-evidenced than the artifacts they build on.
Before interviewing the user and before writing:

- **Reuse content.** Pull personas, positioning statements, validated problems,
  priorities, dates, and evidence counts from the dossier's existing artifacts instead
  of re-asking. Confirm briefly that they're still current, then build on them.
- **Carry caveats forward.** Scan the existing artifacts for **open caveats**:
  unvalidated-evidence warnings, `[ASSUMPTION: …]` markers, and items under "Open
  questions / evidence to gather." Restate every caveat that is **load-bearing for the
  current artifact** in its own assumptions / open-questions section. In particular,
  if a prior artifact flags that its evidence is unvalidated, repeat that warning in
  every downstream artifact that relies on it.
- **Retire resolved caveats.** If the user has since supplied the missing evidence or
  validation, don't restate the warning — note it as resolved (and what resolved it)
  so the trail stays honest without becoming permanent boilerplate.

## 5. Confirm you have enough to write a good artifact
Don't stall on perfection, but a market-driven artifact needs evidence. If the user
hasn't given you the inputs the skill asks for, ask focused questions first (batch 2–4).
If the user says "just draft it," fill gaps with clearly-marked `> TODO:` /
`[ASSUMPTION: …]` placeholders rather than inventing evidence, and list those gaps at the
end under **"Open questions / evidence to gather."**

## 6. Ask the format — every time
Before writing the file, ask:

> **How would you like this delivered — Markdown (`.md`) or Word (`.docx`)?**

If the user already stated a preference earlier in the session, honor it without re-asking.

## 7. Write the file

**Naming — `NN` is the journey stage number**, from the table in `journey.md`
(00 = gap analysis … 16 = launch plan). It is **not** the order artifacts happen to be
produced in — a dossier with gaps in its numbers is normal and expected, and the
numbering stays stable across sessions. Examples: `06-positioning.md`,
`11-requirements.md`.

- **Companion artifacts** from the same stage share the stage number with a
  descriptive suffix: `06-positioning-poc-worksheet.md`, `02-win-loss-findings.md`,
  `00-gap-analysis-action-plan.md`.
- **Per-instance artifacts** (one per interview/visit, like Market Discovery
  Documents) add an instance slug: `01-market-discovery-<contact-or-org>.md`.
- In file-only hosts, prefix with the feature slug as described in §3.

**Formats:**
- **Markdown** — write a clean `.md` file with the naming above.
- **Word `.docx`** — you decide how to produce it, using whatever document-creation
  capability the current host provides (built-in Office/document tooling, a DOCX
  library, etc.). Preserve the full structure: the header block, headings, tables,
  and lists.
  - If the current host has no way to produce a real `.docx`, say so plainly, deliver
    the polished Markdown instead, and tell the user they can paste it into Word or
    export it themselves. Never fail silently or fake a `.docx`.

Keep the Markdown as the source of truth even when delivering `.docx`, so the content is
identical across formats.

## 8. Offer the next step
After delivering, name the Pragmatic stage that naturally comes next and offer to
continue (see `journey.md`). Example: after a Positioning Document → "Next in the
framework is turning this into prioritized **Requirements**. Want me to run that?"

## Writing-quality bar for every artifact
- Lead with the **market problem**, not the solution or the feature.
- Use the **persona's first-person voice** when stating problems.
- Cite **evidence** (interview counts, survey %, win/loss, support tickets) for claims;
  flag unproven claims as assumptions.
- Restate **inherited caveats** from earlier artifacts in the dossier (§4) — a downstream
  artifact must never read as better-evidenced than the inputs it builds on.
- Keep positioning statements ≤25 words and product descriptions ≤50 words.
- Prefer tables for anything scored or prioritized.
- Always start with the standard header block (§2), and where the Pragmatic template
  calls for it, add a confidentiality note and a change-tracking table.
