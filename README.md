# Scale Operations

`scale-operations` is a Codex skill for operations management and scaling. It helps Codex reason like a pragmatic COO/operator: diagnose the real operating constraint, choose a focused intervention, translate management methods into execution, and define the metrics and cadence needed to verify progress.

The skill is designed for founders, COOs, operators, and functional leaders working on workflow efficiency, cost control, team execution, customer retention, and data-driven operating systems.

## What It Does

- Diagnoses operational bottlenecks by business stage, model, constraint, and time horizon.
- Optimizes internal workflows, handoffs, SOPs, automation candidates, and quality controls.
- Supports cost control, budgeting, cash discipline, unit economics, and resource allocation.
- Improves team structure, role clarity, hiring plans, leadership cadence, and execution accountability.
- Uses customer data to improve churn, retention, satisfaction, support quality, and CRM actions.
- Produces operating memos, 30/60/90 plans, workflow redesigns, cost-control plans, team execution plans, and retention plans.

## Design Principle

This skill does not dump framework names.

Management models are used as internal reasoning scaffolds. The expected output is practical operating judgment:

- What is the likely constraint?
- What should be fixed first?
- Who owns the change?
- What cadence keeps it moving?
- Which metrics prove it worked?
- What failure signals should trigger revision?

Frameworks are named only when doing so helps a team align around a known format.

## Skill Structure

```text
scale-operations/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── diagnosis-loop.md
    ├── operating-system.md
    ├── process-systems.md
    ├── economic-control.md
    ├── org-execution.md
    ├── customer-intelligence.md
    └── output-patterns.md
```

## Reference Areas

- `diagnosis-loop.md`: stage fit, constraint classification, root-cause reasoning, and anti-jargon rules.
- `operating-system.md`: goals, metrics, management cadence, decision loops, and business reviews.
- `process-systems.md`: workflow design, SOPs, handoffs, bottlenecks, automation, and quality metrics.
- `economic-control.md`: budgets, cost control, cash flow, margin, unit economics, and countermetrics.
- `org-execution.md`: team design, hiring, ownership, leadership cadence, performance, and accountability.
- `customer-intelligence.md`: segmentation, churn, retention, satisfaction, support data, and customer health.
- `output-patterns.md`: reusable structures for operating memos and execution plans.

## Example Prompts

```text
Use $scale-operations to diagnose why our team doubled but execution got slower.
```

```text
Use $scale-operations to build a cost-control plan that improves runway without hurting growth.
```

```text
Use $scale-operations to analyze rising churn and create a 30-day retention operating plan.
```

```text
Use $scale-operations to redesign our order-to-delivery process and identify automation opportunities.
```

## Installation

Copy or symlink the `scale-operations/` folder into your Codex skills directory:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R scale-operations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

Then invoke it explicitly with `$scale-operations`, or let Codex trigger it for operations management and scaling tasks.

## Validation

The skill has been validated with the system skill validator:

```bash
python3 /home/zcdai/.codex/skills/.system/skill-creator/scripts/quick_validate.py scale-operations
```

Expected result:

```text
Skill is valid!
```

It was also forward-tested against cost pressure, customer churn, and team-execution slowdown scenarios to check that it produces decisions, actions, metrics, and cadence rather than framework lists.

## Scope

This skill provides operating guidance and management decision support. It does not provide legal, tax, audit, or investment advice. For regulated decisions, use it to prepare an operating checklist and then involve the appropriate qualified professional.
