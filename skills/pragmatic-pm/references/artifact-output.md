# Producing the artifact (shared procedure)

Every Pragmatic PM skill ends by producing a **client-ready artifact**. Follow this
procedure identically across all skills so the experience is consistent.

## 1. Collect the standard header inputs (once per session, then reuse)
Every artifact carries the same header. Ask for these **once** at the start of a
session and reuse them for every subsequent artifact (don't re-ask each time):

- **Company name** — the organization the work is for.
- **Feature / Product name** — the feature or product this work is about.
- **Author** — the person creating the artifact (their name).
- **Date created** — today's date (use the current date; the user can override).

If any are unknown, ask for them before writing the first artifact. If the user says
"just use X" or "skip it," record a clear placeholder (e.g. `<company>`), never invent a
real-looking value.

## 2. Put the mandatory header at the top of EVERY artifact
Immediately under the artifact's H1 title, insert this block **verbatim** (filled in).
This **overrides** any header shown in an individual skill's template — always include
these four fields, plus any doc-specific fields the template adds (version, persona, etc.):

```markdown
**Company:** <company>  ·  **Feature / Product:** <feature / product name>
**Author:** <author>  ·  **Date created:** <date>
```

## 3. Confirm you have enough to write a good artifact
Don't stall on perfection, but a market-driven artifact needs evidence. If the user
hasn't given you the inputs the skill asks for, ask focused questions first (batch 2–4).
If the user says "just draft it," fill gaps with clearly-marked `> TODO:` /
`[ASSUMPTION: …]` placeholders rather than inventing evidence, and list those gaps at the
end under **"Open questions / evidence to gather."**

## 4. Ask the format — every time
Before writing the file, ask:

> **How would you like this delivered — Markdown (`.md`) or Word (`.docx`)?**

If the user already stated a preference earlier in the session, honor it without re-asking.

## 5. Save everything in one folder per feature
All artifacts for a feature/product belong together, so the PM ends up with a complete
dossier — not scattered files.

- The **first time** you produce an artifact in a session, create a folder named after
  the **feature / product**, slugified: e.g. `satellite-tracking-system/`. Create it in
  the user's current working directory. Confirm the folder name with the user if unsure.
- Save **every** artifact for that feature into that folder, and reuse it for the rest of
  the session (don't create a new folder per artifact).
- This is just an ordinary directory — it works the same in Claude Code, Cursor, and
  Claude Cowork. Use the tool available to you to create the folder and write files;
  don't rely on any bundled script.

## 6. Write the file
- **Markdown** — write a clean `.md` file inside the feature folder. Use a clear,
  numbered filename: `NN-<artifact>.md` (e.g. `03-positioning.md`), so the artifacts
  sort in journey order.
- **Word `.docx`** — produce the `.docx` **using your own / the host environment's
  native document-creation capability** — e.g. the environment's built-in document or
  Office-file tooling, or any DOCX-writing tool available to you in Claude Code, Cursor,
  or Claude Cowork. **Do not depend on any bundled script or shell converter** (there is
  none). Preserve the full structure: the header block, headings, tables, and lists.
  - If no native DOCX capability is available in the current environment, say so plainly,
    deliver the polished Markdown instead, and tell the user they can paste it into Word
    or export it to `.docx` themselves. Never fail silently or fake a `.docx`.

Keep the Markdown as the source of truth even when delivering `.docx`, so the content is
identical across formats.

## 7. Offer the next step
After delivering, name the Pragmatic stage that naturally comes next and offer to
continue (see `journey.md`). Example: after a Positioning Document → "Next in the
framework is turning this into prioritized **Requirements**. Want me to run that?"

## Writing-quality bar for every artifact
- Lead with the **market problem**, not the solution or the feature.
- Use the **persona's first-person voice** when stating problems.
- Cite **evidence** (interview counts, survey %, win/loss, support tickets) for claims;
  flag unproven claims as assumptions.
- Keep positioning statements ≤25 words and product descriptions ≤50 words.
- Prefer tables for anything scored or prioritized.
- Always start with the standard header block (§2), and where the Pragmatic template
  calls for it, add a confidentiality note and a change-tracking table.
