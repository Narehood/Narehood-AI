# Project instructions

## Purpose

Describe the project, its users, and the outcome it provides. Keep locked
product decisions here so agents do not rediscover them from chat history.

## Architecture

- List the important directories and components.
- Identify generated files and external interfaces.
- Document the supported toolchain and target environments.

| Layer | Role |
| --- | --- |
| YOUR_FRONTEND | Describe client responsibilities |
| YOUR_API | Describe API or worker responsibilities |
| YOUR_DATA | Describe databases and ownership boundaries |
| YOUR_AUTH_BILLING | Describe identity and entitlement sources of truth |

## Phase boundaries / locked decisions

- Document what is in scope for the current phase.
- Record explicit non-goals and archives (branch names as placeholders only).
- Prefer short, durable bullets over narrative history.

## Pull requests

This section grants standing authorization for task-owned branches and pull
requests in this project's repository. Verify its exact owner and repository
before remote writes; it does not authorize writes to upstream or unrelated
repositories, deployments, or a broader task.

Unless the user explicitly says not to, or the change cannot produce a
reviewable result:

1. Work on a feature branch (not the default branch directly).
2. Keep the branch synced with the base branch and resolve merge conflicts
   before asking for review.
3. Open or update a pull request after pushing meaningful work.
4. If the host reports merge conflicts on the PR, fix them on the branch and
   push again until the PR is mergeable.

## Blocked by keys or auth

If a task is blocked by a missing secret, API key, login, 2FA, or dashboard
permission on the human's side:

1. Stop. Do not invent workarounds that ship a degraded product.
2. Ask clearly for the exact credential or action needed.
3. Wait for the human before continuing expensive work (paid builds, store
   submits, production deploys).

## Working boundaries

- Preserve unrelated changes.
- Do not expose or commit credentials, sessions, private data, or environment
  files.
- Require authorization for destructive operations, migrations, and
  deployments; reuse authorization only for the operations and targets it
  covers. Ask about unresolved product or architecture decisions only when they
  materially affect the result.
- Do not burn expensive paid builds or deploys mid-feature; batch them after
  the feature work is ready.
- In public repositories, never commit personal absolute paths, private deploy
  hosts, app IDs, entitlement product IDs, or secret values.

## Commands

Document the exact setup, formatting, lint, type-check, test, build, and run
commands used by this repository.

```bash
# Example placeholders — replace with real commands
npm install
npm run lint
npm test
npm run build
```

## Validation

- Run focused checks while implementing.
- Run the complete required local gate before reporting done.
- Inspect the final status and diff.
- Verify visible behavior with screenshots or equivalent rendered evidence.
- Report skipped checks and unresolved manual testing explicitly.

## Documentation routing

- Read `SPEC.md` for requirements and acceptance criteria.
- Read `ROADMAP.md` for phase order and exit criteria.
- Read `TASKS.md` for current work and validation status.
- Read `STATUS.md` when present for shipped, blocked, deploy, and
  secrets-location notes (placeholders only in public starters).
- Follow project design or domain skills when this file points to them.
