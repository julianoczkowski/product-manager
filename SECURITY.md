# Security Policy

## Scope & attack surface

This project ships **only Markdown skill definitions (`SKILL.md`), Markdown reference
docs, and JSON manifests** (`plugin.json`, `marketplace.json`). It contains:

- **No executable code** — there are no scripts, binaries, or build steps.
- **No runtime dependencies** — nothing to install; no package manifest.
- **No network calls, telemetry, or data collection** — the skills never phone home.

The skills are natural-language instructions that an AI agent (Claude Code, Cursor, or
Claude Cowork) reads and acts on. As with any AI instructions, review a skill before use
in a sensitive environment, and remember that any artifacts you generate contain only the
information *you* provide during a session.

## Supported versions

The latest `main` (and the most recent tagged release) is supported. Older versions are
not maintained.

| Version | Supported |
| --- | --- |
| latest `main` / newest release | ✅ |
| older | ❌ |

## Reporting a vulnerability

Please report suspected security issues **privately** — do not open a public issue.

- Preferred: GitHub → the repository's **Security** tab → **Report a vulnerability**
  (private security advisory).
- Or email: **julianreddot@gmail.com**

Please include a description, reproduction steps, and the affected file(s). You can
expect an acknowledgement within a few business days. Since the project ships no
executable code, the most relevant reports involve **prompt-injection or misleading
instructions** in a skill that could cause an agent to take an unintended action — those
are in scope and welcome.
