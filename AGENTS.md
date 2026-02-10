---
priority: highest
schema_version: 1.0
role: controller
read_order:
  - Overarch.md
  - Collab.md
  - Exp.md
  - workflow.md
  - codebase.md
metadata_rules:
  - Front-matter YAML is authoritative for all SOUL files.
  - If conflicts arise, prioritize: AGENTS.md > Overarch.md > Collab.md > Exp.md.
  - Always load and follow metadata fields before body text.
required_files:
  - Overarch.md
  - Collab.md
  - Exp.md
  - workflow.md
  - codebase.md
---

# SOUL Agent Instructions

## Core Rule
Always read and apply the SOUL files in this order: `Overarch.md`, `Collab.md`, `Exp.md`, `workflow.md`, `codebase.md`.

## File Roles
- **Overarch.md**: Defines the purpose and main task for this agent system.
- **Collab.md**: Collective repo knowledge. Stores metadata, tags, and relationship mappings between files.
- **Exp.md**: Shared session memory across sessions. Stores what the agent learns across sessions; newest entries go at the top.
- **workflow.md**: Workflow logic registry. Updated when new workflows are created or changed.
- **codebase.md**: Reusable code snippet registry with per-snippet metadata.

## Session Protocol
1. Load front-matter metadata for each SOUL file first.
2. Then read the body sections.
3. At session start, locate the repo root, scan metadata tags across the repo, and record tags aligned with `Overarch.md` in `Collab.md`.
3. Update `Exp.md` at the **top** when new knowledge is learned.
4. Update `Collab.md` when new relationships or metadata tags are discovered.
5. Update `Overarch.md` only when the system purpose changes.

## Subagent Usage
- Use the specialized profiles in `SOUL/subagent/` when a task matches a subagent's description.
- Prefer delegating to the most specific subagent over a generic response.
- Check subagent front-matter tags and descriptions before invoking.
