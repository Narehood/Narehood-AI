# Narehood AI tasks

## Completed phase: Workflow alignment

- [x] Add project planning documents and reusable planning templates.
- [x] Add a focused pull-request readiness skill.
- [x] Add isolated Linux, macOS, and Windows installer integration tests.
- [x] Add pull-request CI, dependency review, Dependabot, and a PR template.
- [x] Align Claude routing and workflow documentation.
- [x] Replace the third-party local review loop with built-in Codex review.
- [x] Add opt-in, cross-platform installation for selected Codex plugins.
- [x] Trust all Git worktrees beneath the current user's `~/github` directory.
- [x] Run local repository, shell, installer, workflow, and skill validation.
- [x] Confirm Windows installer integration, including plugin installation and
  recursive GitHub trust generation, passes in CI.
- [x] Inspect the final diff and stage only workflow-alignment changes.

## Completed phase: Cursor-first + Narehood rebrand

- [x] Reframe SPEC, ROADMAP, TASKS, README, and root AGENTS for Cursor-primary
  Narehood AI (public-safe).
- [x] Complete Narehood AI / narehood-ai rebrand; strip personal absolute paths
  from sample config and skill examples.
- [x] Expand project-docs AGENTS template; add STATUS.md template; update
  ai-project-manager skill.
- [x] Add CURSOR_LAYOUT.md; update SKILLS and WORKFLOW; soften Codex-only skill
  wording; align global instructions.
- [x] Document Cursor skills consumption; extend validate if needed; run
  validate.sh; public-repo leak-check.

## Completed phase: T3 Code control surface

- [x] Document T3 Code as the control surface (`docs/T3CODE_LAYOUT.md`).
- [x] Retarget README, SPEC, AGENTS, SKILLS, and WORKFLOW for T3 Code while
  keeping the repo public-safe.
- [x] Keep `.agents/skills/` canonical; ignore local `.t3/` userdata.
- [x] Document Codex, Claude Code, and Cursor as first-class T3 Code providers
  (`docs/CODEX_LAYOUT.md`, `docs/CLAUDE_LAYOUT.md`, `docs/CURSOR_LAYOUT.md`).
- [x] Run `./scripts/validate.sh` after the retarget.

## Current phase: Upstream refresh before TStack integration

- [x] Compare incoming upstream commits with deliberate Narehood fork changes.
- [x] Resolve and stage the Titus refresh while retaining Narehood branding,
  T3 Code and provider support, public-safe configuration, skills, templates,
  and installers.
- [ ] Validate the merged tree and complete the built-in Codex review loop.
- [ ] Publish a refresh PR targeting only `Narehood/Narehood-AI`.
- [ ] Import `Narehood/tstack` with original history and Theo's attribution
  after the upstream refresh.
- [ ] Schedule updates from `Narehood/tstack` to open or update a sync PR for
  review; never merge those updates automatically.

Validation evidence: `./scripts/validate.sh` passes with 19 skills; all 15
changed skill entrypoints pass the skill validator. Preservation checks confirm
the frontend skill, provider layout docs, STATUS template, installers, and
ignore rules are unchanged. Windows installer integration was skipped locally
because symlink creation requires Developer Mode or administrator privileges.
The live PhotoCraft MCP test was not run because its external CLI is absent.

Review blocker: two built-in `codex review --uncommitted` attempts could
not inspect the repository because the CLI's execution policy rejected
read-only commands. The user requested publishing the refresh PR with this
review still outstanding. Publication does not establish merge readiness;
complete the required review before merging the refresh or starting the
TStack import.

## Pending phase: Enforced repository governance

- [ ] Configure a default-branch ruleset after CI check names exist remotely.
- [ ] Require pull requests, successful validation, and conversation resolution.
- [ ] Require an independent approval when repository ownership permits it.

## Completion rule

Move current-phase tasks to completed only after their acceptance criteria and
required validation pass. Keep external GitHub settings pending until verified
through the live repository.
