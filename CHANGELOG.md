# Changelog

All notable changes to this project are documented here. The format is based on
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to
[Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.4.0] — 2026-07-19

### Added
- Shared artifact procedure (`pm-copilot/references/artifact-output.md`) now has an
  explicit "carry forward open caveats" step: before writing, skills scan prior
  artifacts in the feature dossier for unvalidated-evidence warnings, assumptions, and
  open questions, and restate the load-bearing ones (or mark them resolved) so
  downstream artifacts never read as better-evidenced than their inputs.
- New "find or resume the feature dossier" step in the shared artifact procedure:
  skills look for an existing feature folder / numbered artifacts (or artifacts
  earlier in the conversation) before creating anything, reuse the header inputs and
  prior content instead of re-interviewing, and continue the same numbering across
  sessions. Host-aware output: folder-capable hosts (Claude Code, Cursor, VS Code
  Copilot) get one folder per feature; file-only hosts (Claude Desktop, Codex
  desktop app) get feature-slug-prefixed standalone files.
- Filename numbering is now defined: `NN` is the journey **stage** number from
  `journey.md` (stable across sessions, gaps expected), with suffixes for companion
  artifacts (`06-positioning-poc-worksheet.md`) and per-instance artifacts
  (`01-market-discovery-<contact>.md`).
- `pm-gap-analysis` now says what to do when the top gap lands on a framework box
  with no dedicated skill (Pricing, Asset Assessment, Market Definition, Distribution
  Strategy, Buyer Experience): advise from `framework.md` directly and say so.

### Fixed
- Removed the last reference to a "bundled converter" from `pm-copilot` — `.docx`
  output is produced by whatever document capability the host provides, as
  `artifact-output.md` already specified.
- Removed `pm-prd`'s stale `pragmatic/*.md` artifact-lookup glob (it pointed at a
  folder no skill creates); it now resumes the feature dossier like every other skill.
- Fixed a dangling "M5 prioritization logic" reference in `pm-distinctive-competence`
  (now points at the market-problem test and opportunity-scoring attributes).
- `pm-market-problems` templates now match the mandatory-header rule: the Market
  Discovery Document header moved from the bottom to the top, and the Market Problems
  Table gained a header.
- `pm-personas`' interview-balance guidance now includes all four market segments
  (competitors' customers was missing).
- `pm-launch-plan` supports content-driven releases: the launch anchor can be exit
  criteria instead of a date, matching the release charter.
- `pm-requirements`' MRD template no longer duplicates author info (contact table
  merged into the standard header).
- The mandatory-header rule now explicitly permits doc-type label adaptations
  (e.g. "Scope / Product" in the gap analysis) while requiring all four fields.

### Changed
- `pm-release-plan` now treats content-driven releases as a first-class option: the
  interview asks date-driven vs. content-driven before asking for a date ("there is
  no date" is a legitimate answer), the Market Window guidance covers exit-criteria
  launches, and the Release Charter template's `Target Launch Date` field is now a
  `Schedule` field that accepts either form.

## [0.3.0] — 2026-07-12

### Added
- `CLAUDE.md` and `AGENTS.md` repository guidance documenting skill conventions and
  the release/sync workflow for Claude and Codex contributors.
- Codex personal-plugin packaging in `.codex-plugin/plugin.json`, with all existing
  `pm-*` skills exposed from `skills/` and personal marketplace support for the
  ChatGPT desktop app.

### Changed
- Cursor install now uses Vercel's open [Skills CLI](https://github.com/vercel-labs/skills)
  (`npx skills add julianoczkowski/product-manager`), which auto-detects and installs to
  any supported agent (Cursor, Claude Code, Codex, Cline, GitHub Copilot, and ~70 more).
  The manual copy step remains as a fallback.
- `.gitignore` now excludes `*.mp4` (demo videos are uploaded to GitHub's asset CDN, not
  committed).
- README installation instructions now cover both the ChatGPT desktop UI and Codex
  CLI, including marketplace updates and starting a new task after installation.

## [0.2.0] — 2026-07-03

### Changed
- **Breaking:** renamed all 17 stage skills with a `pm-` prefix (`pm-personas`,
  `pm-positioning`, `pm-market-problems`, …) so `/pm-` surfaces the whole toolkit and
  names don't collide with other plugins. Invoke skills by their new prefixed names;
  `pm-copilot` is unchanged.
- Product name is now **Product Manager Copilot** across the README, marketplace
  description, and the router skill.
- README: added a video demo, a Contents index, and split Install instructions into
  separate **Claude Code**, **Claude Desktop**, and **Cursor** sections.

### Removed
- The `version` field in `plugin.json`, so clients detect updates by git commit SHA
  (no manual version bump needed per change).

## [0.1.0] — 2026-07-02

### Added
- Initial release of the **Product Manager Copilot** plugin — a market-driven PM
  assistant based on the Pragmatic Framework (Foundations · Focus · Build).
- `pm-copilot` router skill that detects intent and routes to the right stage, plus
  17 stage skills covering market problems, win/loss, distinctive competence,
  competitive landscape, personas, positioning, gap analysis, product strategy,
  opportunity scoring, product canvas, roadmap, requirements, use scenarios, PRD,
  release plan, stakeholder communication, and launch plan.
- Shared knowledge base (`framework.md`, `journey.md`, `artifact-output.md`).
- Every artifact carries a standard header (Company · Feature/Product · Author · Date)
  and is saved into a per-feature folder.
- Markdown or Word `.docx` output on request, produced via the host environment's
  native document-creation capability (no bundled converter or dependencies).
- Plugin + marketplace manifests, README with an annotated skills list, MIT license,
  and security policy.

[Unreleased]: https://github.com/julianoczkowski/product-manager/compare/v0.3.0...HEAD
[0.3.0]: https://github.com/julianoczkowski/product-manager/compare/v0.2.0...v0.3.0
[0.2.0]: https://github.com/julianoczkowski/product-manager/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/julianoczkowski/product-manager/releases/tag/v0.1.0
