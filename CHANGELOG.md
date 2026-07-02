# Changelog

All notable changes to this project are documented here. The format is based on
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to
[Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

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

[Unreleased]: https://github.com/julianoczkowski/product-manager/compare/v0.1.0...HEAD
[0.1.0]: https://github.com/julianoczkowski/product-manager/releases/tag/v0.1.0
