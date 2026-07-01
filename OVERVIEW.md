---
title: test-team-collab Project Overview
form: design
topic: [overview]
updated: 2026-07-01
status: active
owner: lushunlin
tags: [team-docs, overview]
target_lines: 500
---

# test-team-collab Project Overview

## Project Goal

A practice project for the team to learn the **team-collab** workflow (shared
state docs + `$checkpoint`/`$handoff` sync). It ships a tiny data-acquisition
(数采) demo so there is real code, tests, and a handoff to exercise the flow.
Not a production system.

## How to work here (read this first)

**Repos (two, GitHub, over SSH):**

- Code: `git@github.com:shunlinlu/test_team_collab_code.git`
- Docs: `git@github.com:shunlinlu/test_team_collab.git` (cloned into `obsidian-docs/` inside the code repo; gitignored by the code repo).

**Join (colleague, one-time):**

```bash
git clone git@github.com:shunlinlu/test_team_collab_code.git test_team_collab
cd test_team_collab
git clone git@github.com:shunlinlu/test_team_collab.git obsidian-docs
team-collab init --join test-team-collab \
  --code "$PWD" --docs "$PWD/obsidian-docs" \
  --user <your-username> --code-platform github
```

**Daily loop:**

1. `git pull` both repos; read `CURRENT.md` → `NEXT.md` → `TODO.md`.
2. Claim a task in [TODO](./TODO.md) by adding `@your-username`; do the work in the code repo.
3. Keep shared state in the quartet (CURRENT/NEXT/RISKS/TODO) — concise, link-driven. Run `team-collab lint-state obsidian-docs` to check.
4. Mid-session snapshot: `$checkpoint` (local only, no git). End of session: `$handoff <topic>` (writes `_handoffs/`, updates state, commits, pushes docs).
5. Code changes go through the code repo (prefer PRs once `main` is protected).

**Conventions:** personal notes → `dev-records/<username>/`; decisions → [decision-log](./decision-log.md); never `git add .` in the docs repo; never `--no-verify`.

## Current Scope

- In: team-collab wiring, `collector/` demo, docs baseline, onboarding.
- Out: real data sources, production deployment.

## Key Design

- Standalone-git docs layout: `obsidian-docs/` is its own repo nested in the code repo.
- Demo: `collector/collect.py` samples host load average → CSV (stdlib only), covered by `tests/test_collect.py`. See handoff [2026-07-01-1829](./_handoffs/2026-07-01-1829-team-collab-setup-collector-demo.md).
- Open setup follow-ups (gitleaks, branch protection) tracked in [NEXT](./NEXT.md) / [RISKS](./RISKS.md).

## Related Links

- Code repo: https://github.com/shunlinlu/test_team_collab_code
- Docs repo: https://github.com/shunlinlu/test_team_collab
- Tasks: [TODO](./TODO.md)
