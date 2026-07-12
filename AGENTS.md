# AGENTS.md

Guidance for working on this repo. This is the **Product Manager Copilot** plugin — a
Codex / Codex Desktop plugin that packages product-management Agent Skills built
on the Pragmatic Institute Framework.

## Repo layout

- `.Codex-plugin/plugin.json` — plugin manifest. **No `version` field on purpose** (see
  Releasing below). `displayName` is `Product Manager Copilot`; plugin `name` is
  `product-manager`.
- `.Codex-plugin/marketplace.json` — marketplace manifest (`product-manager-marketplace`).
- `skills/<name>/SKILL.md` — one folder per skill. Skills are auto-discovered from this
  folder; the manifests do **not** enumerate them.
- `skills/pm-copilot/references/` — shared knowledge base (`framework.md`, `journey.md`,
  `artifact-output.md`). The router and stage skills read these.
- `README.md`, `CHANGELOG.md` — keep both current when behavior changes.

## Skill conventions

- **Every skill name is prefixed `pm-`** (`pm-copilot`, `pm-personas`, `pm-positioning`, …)
  so typing `/pm-` surfaces the whole toolkit and avoids collisions with generically named
  skills from other plugins. When adding a skill, prefix it `pm-`.
- **Folder name must equal the `name:` field** in that skill's `SKILL.md` frontmatter.
- Cross-references between skills use backticked names (e.g. `` `pm-personas` ``). The
  router's routing tables live in `references/journey.md` and `references/framework.md` —
  update them when adding, removing, or renaming a skill.
- Auto-activation is driven by the `description:` field, not the name. Keep descriptions
  specific and intent-rich.

## How updates reach installed users (IMPORTANT)

Installed clients do **not** see changes just because they were pushed to `main`. The
Codex Desktop marketplace tracks a **synced commit** and only advances it when the user
acts:

- Each install shows **"Synced commit: <sha>"** with two controls: **"Check for updates"**
  (pulls the latest commit on `main`) and a **"Sync automatically"** toggle (off by default).
- **The fix when a user reports stale skills: have them click "Check for updates"** (or
  enable "Sync automatically"). This — not a new release tag — is what actually advances an
  installed Desktop plugin to the latest commit.
- The Codex CLI equivalent is `/plugin marketplace update product-manager-marketplace`
  then `/reload-plugins`; force-refresh by deleting
  `~/.Codex/plugins/cache/product-manager-marketplace/product-manager/` and reloading.

Because there is no `version` field, Codex falls back to the git **commit SHA**, so
every commit is treated as a new version — no manual version bump needed for updates to be
detectable.

## Releasing (tags + GitHub releases)

Desktop sync works off commits, so a release is **not required** for updates to propagate.
Cut a GitHub release anyway to mark meaningful milestones, give users a changelog, and keep
a clean version history. Do this on request or when shipping a notable change:

1. Make sure `main` is pushed and green.
2. Update `CHANGELOG.md`: move items from `[Unreleased]` into a new `[X.Y.Z] — <date>`
   section (Keep a Changelog format, semver). Commit and push.
3. Cut the release at the current `main` HEAD and mark it latest:
   ```
   gh release create vX.Y.Z --target main --latest \
     --title "vX.Y.Z — <short summary>" \
     --notes "<what changed; note any breaking skill renames>"
   ```
4. Verify: `gh release list` (new tag shows **Latest**) and
   `gh api repos/julianoczkowski/product-manager/releases/latest -q .tag_name`.

Bump the version in the tag name using semver: **patch** for docs/fixes, **minor** for new
skills or additive changes, **major** for breaking changes (e.g. renaming or removing
skills that users invoke by name). Renaming a public skill name is breaking — call it out
in the release notes and CHANGELOG.

## Git conventions

- Branch off `main` for substantial work; small doc/manifest edits may go straight to `main`
  when the user asks to commit and push.
- Commit only when the user asks. Use `git mv` for renames so history is preserved.
- After pushing a change users need, remind them to **"Check for updates"** in the app (or
  that "Sync automatically" must be on) — otherwise they stay on the old synced commit.
