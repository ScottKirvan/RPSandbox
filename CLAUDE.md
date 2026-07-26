# CLAUDE.md — RPSandbox

## What this repo is
Sandbox for testing [Release Please](https://github.com/googleapis/release-please) and
shared GitHub Actions workflow patterns before rolling them out to production repos in the
BojuStudio ecosystem. It is **not** a real shipping product — the code content is mostly a
leftover skeleton from a Git project template (an Unreal Engine plugin template), kept
around because release-please needs *something* to version. The actual point of interest is
the `.github/workflows/` automation.

## Layout
- `.github/workflows/release.yml` — main pipeline, triggered on push to `main`:
  1. `release-please` job runs `googleapis/release-please-action@v4` (config in
     `.github/release-please/release-please-config.json`, manifest in
     `.github/release-please/.release-please-manifest.json`).
  2. `improve-release-notes` — calls local `local-release-notes.yml`, rewrites the
     release-please changelog into narrative prose + a "What Changed" bullet list using
     `actions/ai-inference@v2` (GitHub Models, default `openai/gpt-4o`).
  3. `update-changelog-prs` — calls the **shared/reusable** workflow
     `ScottKirvan/.github/.github/workflows/reusable-update-changelog-prs.yml@main` to add PR
     links into the changelog.
  4. `discord-notify` — calls local `local-discord-notify.yml`, posts only the "What
     Changed" bullet section (not the full narrative) to a Discord webhook
     (`DISCORD_WEBHOOK_TEST` secret).
- `.github/workflows/local-release-notes.yml` / `local-discord-notify.yml` — sandbox forks of
  shared workflows, edited in place here before changes get promoted to
  `ScottKirvan/.github`.
- `.github/workflows/update-version-header.yml` — updates version strings in
  `Source/ScooterUtils/Public/ScooterUtilsVersion.h` and `ScooterUtils.uplugin` after a
  release. **Known bug/leftover:** its `workflow_run` trigger listens for a workflow named
  `"Release Please Workflow"`, but the actual workflow in this repo is named
  `"Release Workflow"` (`release.yml`) — so this job likely never fires as-is. Inherited
  from the template; flag before relying on it.
- `notes/CHANGELOG.md` — release-please-managed changelog (referenced from README).
- `notes/VERSION.md`, `version.json` — release-please "extra-files" version bumps.
- `notes/TODO.md` — scratch todo list, currently just placeholders.

## Working conventions
- release-please uses `release-type: simple`; version bumps flow from Conventional Commit
  messages (`feat:`, `fix:`, `chore:`, etc.) on `main`.
- Squash-merge PRs land on `main` with a different commit hash than the feature branch tip —
  don't be surprised when `git log origin/main..<branch>` still shows a commit after the PR
  is merged; check `gh pr view <branch>` for merge status rather than relying on commit hash
  equality.
- Feature branches are routinely deleted on GitHub after merge (`gh pr list` + `git branch
  -vv` showing `: gone` is the tell). Safe to prune matching local branches after confirming
  with the user.

## Global rules (from e:\1\CLAUDE.md, apply here too)
- Never commit/push directly to `main`; always branch first.
- No attribution/co-author lines in commits or PR descriptions.
- Follow `.github/ISSUE_TEMPLATE` / `.github/pull_request_template.md` if present (none exist
  in this repo currently).
