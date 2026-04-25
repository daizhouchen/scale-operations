---
name: scale-operations
status: in-progress
created: 2026-04-25T12:38:30Z
updated: 2026-04-25T12:43:16Z
progress: 86%
prd: .claude/prds/scale-operations.md
github: will-be-set-on-sync
---

# Epic: scale-operations

## Overview

Build a public GitHub-hosted Codex skill for operations management and scaling. The skill should turn management and operating models into practical judgment: diagnose the operating problem, choose the right intervention, translate the method into actions, and define metrics and cadence for validation.

## Architecture Decisions

- Make the workspace root the GitHub repository.
- Put the skill in `scale-operations/` so it remains a standard Codex skill folder.
- Use `SKILL.md` as the compact orchestration layer.
- Use one-level `references/` files for detailed operating judgment:
  - `diagnosis-loop.md`
  - `operating-system.md`
  - `process-systems.md`
  - `economic-control.md`
  - `org-execution.md`
  - `customer-intelligence.md`
  - `output-patterns.md`
- Avoid scripts because the work is judgment-heavy and no deterministic repeated transformation is needed.

## Technical Approach

### Frontend Components

None.

### Backend Services

None.

### Infrastructure

Use git and `gh` to create a public GitHub repository and push the skill project.

## Implementation Strategy

1. Create CCPM planning artifacts.
2. Initialize the skill scaffold using `init_skill.py`.
3. Replace the scaffold body with concise operating instructions.
4. Add reference files that encode model selection as operating heuristics.
5. Generate `agents/openai.yaml`.
6. Validate with `quick_validate.py`.
7. Run local forward-tests with realistic prompts and revise if outputs become framework-heavy.
8. Initialize git, commit, create a public GitHub repo, and push.

## Task Breakdown Preview

- Task 001: Create CCPM PRD and epic.
- Task 002: Initialize the skill scaffold.
- Task 003: Write `SKILL.md`.
- Task 004: Write internalized reference files.
- Task 005: Generate metadata and validate.
- Task 006: Forward-test and refine.
- Task 007: Publish public GitHub repository.

## Dependencies

- `skill-creator` scripts available locally.
- `gh` authentication for GitHub publishing.

## Success Criteria (Technical)

- The skill folder passes quick validation.
- References are linked directly from `SKILL.md`.
- No placeholder resource files remain.
- Git repo contains a clean commit.
- Public GitHub repo is reachable.

## Estimated Effort

Small. One implementation pass with validation and publishing.
