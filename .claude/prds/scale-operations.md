---
name: scale-operations
description: Create a Codex skill for internalized operations management and scaling guidance.
status: backlog
created: 2026-04-25T12:38:30Z
---

# PRD: scale-operations

## Executive Summary

Create a Codex skill named `scale-operations` for operations management and scaling. The skill should help Codex diagnose business operating problems, identify constraints, design process/cost/team/customer-data interventions, and produce practical operating plans. It must internalize management models as reasoning aids rather than expose them as a list of jargon.

## Problem Statement

Founders and operators often ask for help with process efficiency, cost control, team execution, and customer retention. Generic advice tends to list frameworks such as OKR, RACI, Lean, AARRR, or LTV/CAC without translating them into operating decisions. The new skill should guide Codex to reason like an operations leader: diagnose the company stage, find the bottleneck, choose the right intervention, define ownership, and verify results with metrics.

## User Stories

- As a founder, I want Codex to diagnose why operations are slowing down after team growth, so that I can fix the true execution bottleneck instead of adding meetings.
  Acceptance criteria: The response identifies the likely bottleneck, proposes a responsibility/operating rhythm change, and gives metrics such as cycle time, rework rate, or decision latency.
- As an operations manager, I want Codex to optimize a workflow, so that I can reduce handoffs, rework, and manual work.
  Acceptance criteria: The response maps current-state assumptions, identifies the highest-leverage node, proposes SOP or automation changes, and defines validation metrics.
- As a founder or finance lead, I want Codex to reduce costs without damaging growth, so that cash runway and profitability improve.
  Acceptance criteria: The response separates fixed/variable costs, protects growth-critical spend, prioritizes cuts by operating impact, and includes cash/runway metrics.
- As a customer success or growth lead, I want Codex to diagnose churn or satisfaction decline, so that I can improve customer experience and retention.
  Acceptance criteria: The response segments customers, identifies touchpoint failure hypotheses, proposes experiments, and defines retention/satisfaction metrics.

## Functional Requirements

- Provide a concise `SKILL.md` with triggering guidance and a repeatable diagnosis loop.
- Include reference files that contain internalized operating judgment, not standalone framework summaries.
- Cover four core domains: process optimization and automation, cost and financial control, team building and leadership, customer relationship and data analysis.
- Include a model-use rule: do not list models by default; use them silently to structure diagnosis unless naming them helps execution or alignment.
- Provide output patterns for operating memo, 30/60/90 plan, workflow redesign, cost-control plan, execution-system design, and customer-retention plan.
- Generate `agents/openai.yaml` with human-facing metadata.
- Validate the skill with the system quick validator.
- Forward-test the skill against realistic scenarios and revise if the outputs become framework dumping.
- Upload the final skill project to a public GitHub repository.

## Non-Functional Requirements

- Keep `SKILL.md` compact and rely on references through progressive disclosure.
- Use imperative instructions suitable for another Codex instance.
- Keep all content ASCII unless existing context requires otherwise.
- Avoid extra documentation files outside the skill anatomy and CCPM planning artifacts.
- Use public GitHub visibility as requested.

## Success Criteria

- `quick_validate.py` passes on the skill folder.
- `agents/openai.yaml` exists and matches the skill purpose.
- At least three realistic forward-test prompts show that outputs prioritize diagnosis, tradeoffs, actions, metrics, and cadence over framework lists.
- The repository is initialized, committed, and pushed to a public GitHub repo.
- The final response includes the repo URL, validation result, and remaining risks if any.

## Constraints & Assumptions

- Current workspace starts empty and is not a git repository.
- The skill name is `scale-operations`.
- The GitHub repository should be public.
- The implementation should use `skill-creator`'s `init_skill.py` and `quick_validate.py`.
- GitHub upload depends on local `gh` authentication and network access.

## Out of Scope

- Legal, tax, audit, or investment advice.
- Industry-specific operating playbooks for every vertical.
- Building a separate software product or web UI.
- Bulk importing third-party copyrighted management material.

## Dependencies

- Codex skill-creator scripts.
- Git and GitHub CLI.
- GitHub account authentication on the local machine.
