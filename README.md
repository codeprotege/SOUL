---
id: soul-readme
schema_version: 1.0
title: SOUL README
purpose: Provide an overview of the SOUL system files, roles, and update conventions.
created: 2026-02-10
updated: 2026-02-10
tags:
  - soul
  - readme
  - overview
related_files:
  - AGENTS.md
  - Overarch.md
  - Collab.md
  - Exp.md
  - workflow.md
  - codebase.md
  - subagent/
---

# SOUL README

## Overview
SOUL is a structured agent system with explicit metadata, workflows, and shared memory across sessions. All core rules live in `SOUL/AGENTS.md`.

## Core Files
- `AGENTS.md`: Controller rules and read order.
- `Overarch.md`: Mission, scope, and constraints.
- `Collab.md`: Metadata tags and file relationships.
- `Exp.md`: Shared session memory (newest entries at top).
- `workflow.md`: Workflow logic registry and update log.
- `codebase.md`: Reusable code snippets with per-snippet metadata.

## Subagents
Specialized profiles live in `SOUL/subagent/`. Use them when a task matches their description and tags.

## Update Conventions
- Keep metadata current and authoritative.
- Record new workflows in `workflow.md`.
- Capture reusable snippets in `codebase.md`.
- Update `Collab.md` when new tags or relationships are discovered.
