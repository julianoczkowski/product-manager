# Changelog

All notable changes to this project are documented here. The format is based on
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to
[Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

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

### Added
- `CLAUDE.md` documenting skill conventions and the release/sync workflow.

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

[Unreleased]: https://github.com/julianoczkowski/product-manager/compare/v0.2.0...HEAD
[0.2.0]: https://github.com/julianoczkowski/product-manager/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/julianoczkowski/product-manager/releases/tag/v0.1.0
