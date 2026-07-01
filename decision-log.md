---
title: test-team-collab Decision Log
form: decision
topic: [architecture]
updated: 2026-06-22
status: active
owner: lushunlin
tags: [team-docs, decisions]
target_lines: 800
---

# test-team-collab Decision Log

## ADR-001 - Initialize Docs Repository

Date: 2026-06-22

### Context

The project needs an Obsidian docs workspace as shared team memory. New projects should prefer a standalone GitLab docs repo; existing projects may keep a project directory already used inside an owner's Obsidian vault.

### Decision

Use an Obsidian docs workspace plus a code repo `obsidian-docs` link or mount.

### Rationale

This keeps code history clean while giving humans and agents a shared context surface.

### Consequences

Shared high-level docs go through MR. Personal dev records go under `dev-records/lushunlin/`.

### Revisit Trigger

If docs maintenance cost exceeds value, revisit the docs/code boundary and sync strategy.
