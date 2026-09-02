# Model Routing and Governance

## Routing policy

A routing policy maps a workload to an approved model using explicit constraints rather than a universal default.

```text
Request → classify workload and constraints → choose approved route → execute → observe → fall back if needed
```

## Example policy

| Workload | Default route | Escalation or fallback |
| --- | --- | --- |
| Low-risk summary | Cost-efficient approved model | Higher-quality model if confidence is low |
| Grounded knowledge answer | Model optimized for instruction following | Abstain and create a review case if evidence is insufficient |
| Complex synthesis | Highest-quality approved model | Queue or defer when capacity limits are reached |
| Tool use | Model with validated tool-call behavior | Retry once, then route to human review |

## Routing inputs

- Required task quality
- Context length
- P95 latency target
- Budget or cost ceiling
- Regional and data-residency requirements
- Tool-use capability
- Current provider capacity and error rate

## Governance controls

- Approved-model allowlist by tenant and workload
- Role-based access to experiments and production policies
- Prompt, model-version, and decision audit trail
- Data handling, retention, and regional constraints
- Human review for high-impact or low-confidence outputs
- Rollback to a prior model or policy version

## Product stance

Customer choice is valuable when it solves a real capability, cost, or compliance need. The platform should constrain choice when unlimited options would create support burden, unreliable quality, or governance gaps.
