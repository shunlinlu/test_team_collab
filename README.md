---
title: test-team-collab Team Docs Repository
form: index
updated: 2026-06-22
status: active
tags: [team-docs]
---

# test-team-collab Team Docs Repository

This is the team docs repository for test-team-collab. It is separate from the code repo `docs/` directory. It stores coding-agent memory: project design, requirements, test plans, implementation plans, dev records, research notes, and session handoffs.

## Entry Points

- [OVERVIEW](./OVERVIEW.md): project narrative entrypoint.
- [CURRENT](./CURRENT.md): current state.
- [NEXT](./NEXT.md): next actions and open decisions.
- [RISKS](./RISKS.md): risks and blockers.
- [TODO](./TODO.md): claimable tasks and owners.
- [_handoffs](./_handoffs/): append-only session handoffs.
- [dev-records/lushunlin](./dev-records/lushunlin/): personal dev records.
- [decision-log](./decision-log.md): project decisions.

## Commit Rules

Shared high-level docs go through GitLab MR. Personal `dev-records/lushunlin/...`, personal research notes, and `_handoffs/...` may be direct-push if project policy allows.

Never commit secrets, customer private data, internal URLs, `.obsidian/`, `.trash/`, `.DS_Store`, or local editor state.
