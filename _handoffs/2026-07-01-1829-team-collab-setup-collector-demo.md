---
title: handoff 2026-07-01 team-collab-setup-collector-demo
form: trace
date: 2026-07-01
updated: 2026-07-01
status: done
project: test-team-collab
author: shunlinlu
agent: claude-opus-4-8 via Claude Code
host_class: mac
topic: team-collab-setup-collector-demo
tags: [handoff]
---

# Handoff 2026-07-01 · team-collab-setup-collector-demo

## Summary

Stood up the `test-team-collab` project end to end: leader-initialized the docs
baseline and code agent entry, wired both GitHub remotes over SSH, and pushed.
Added a minimal data-acquisition (数采) demo to the code repo so the team can
practice the full workflow. Repo is ready for a colleague to `init --join`.

## Changed files

| Code repo (test_team_collab_code) | Docs repo (test_team_collab) |
|---|---|
| `AGENTS.md`, `CLAUDE.md`, `.gitignore` (init) | `CURRENT/NEXT/RISKS/TODO.md`, `OVERVIEW/README/decision-log` (baseline) |
| `collector/collect.py`, `collector/__init__.py` | `_handoffs/2026-07-01-1829-…` (this file) |
| `tests/test_collect.py`, `README.md` | state quartet updates (this session) |

## Decisions made

- **Two-repo GitHub layout over SSH.** code = `test_team_collab_code`,
  docs = `test_team_collab` (nested `obsidian-docs/`, gitignored in code repo).
  Why: matches team-collab standalone-git docs layout; SSH chosen after the old
  passphrase-protected `id_rsa` was unrecoverable — generated a new
  passphrase-less `id_ed25519_github` scoped to github.com in `~/.ssh/config`.
- **Global git identity set** (shunlinlu / shunlinlu0803@gmail.com); machine had none.
- **Demo scope kept minimal** (stdlib-only load sampler). Purpose is workflow
  practice, not a real product.

## Tests run

- `python3 -m unittest discover -s tests` → 2 passed.
- Smoke run `python3 collector/collect.py --count 2` → wrote `data/samples.csv` OK.

## Risks

- gitleaks not installed, so the docs repo pre-commit hook only reminds and does
  not actually scan for secrets. Tracked in [RISKS](../RISKS.md).

## Suggested next steps

1. Colleague runs `team-collab init --join test-team-collab` (clone both repos).
2. `brew install gitleaks` to activate real secret scanning.
3. Protect `main` on both GitHub repos (changes via PR).
4. Extend the collector (new source, scheduling) as the next practice task.
