---
title: test-team-collab TODO
form: state
topic: [implementation]
updated: 2026-07-01
status: active
owner: lushunlin
tags: [team-docs, todo]
target_lines: 120
---

# test-team-collab TODO

> [!summary]
> Keep TODO concise. Each item is one claimable action. Put complex background in [NEXT](./NEXT.md), design docs, dev records, or archive, then link to it.
> TODO ownership is a public intent signal plus optimistic git conflict detection, not a strict distributed lock. Keep stable task identity such as `id: T-YYYYMMDD-NN` when ambiguity is possible.

## In Progress

- [ ] Colleague onboarding via `init --join` @zhou since 2026-07-01 (id: T-20260701-03)

## Blocked

- None.

## Backlog

- [ ] Complete project overview (id: T-20260622-02)
- [ ] Install gitleaks + protect `main` on both repos (id: T-20260701-04)
- [ ] Extend collector: new source / scheduling (id: T-20260701-05)
- [ ] Make collector Windows-compatible by handling missing `os.getloadavg()` (id: T-20260701-07)
- [ ] Grant coolSrping collaborator write access on both GitHub repos (id: T-20260701-08)

## Recently Completed

- [x] Initialize project docs repo @lushunlin 2026-07-01 (id: T-20260622-01)
- [x] Data-acquisition demo + tests @lushunlin 2026-07-01 (id: T-20260701-06); see [_handoffs/2026-07-01-1829](./_handoffs/2026-07-01-1829-team-collab-setup-collector-demo.md)
