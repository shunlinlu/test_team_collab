---
title: test-team-collab Next Actions
form: state
topic: [implementation]
updated: 2026-07-01
status: active
owner: lushunlin
tags: [team-docs, next]
target_lines: 80
---

# test-team-collab Next Actions

> [!summary]
> Keep NEXT concise. Each item should describe one executable action, acceptance criteria, and a needed Markdown link. Move background to design docs, dev records, or archive.

## Next Actions

1. Colleague joins via `team-collab init --join test-team-collab`; acceptance: they can pull both repos and see this state. Details in [TODO](./TODO.md).
2. `brew install gitleaks`; acceptance: docs pre-commit actually scans (see [RISKS](./RISKS.md)).
3. Protect `main` on both GitHub repos; acceptance: direct push blocked, changes via PR. Tracked in [TODO](./TODO.md) (T-20260701-04).

## Open Decisions

- None open.

## Deferred

- None.
