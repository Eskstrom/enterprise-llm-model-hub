# MVP Boundaries

## In scope

- A curated catalog of three to four fictional or publicly documented models.
- Offline comparison for grounded Q&A, summarization, extraction, and tool calling.
- Quality, latency, token-use, and cost-per-successful-task reporting.
- A customer-configurable routing policy for approved models.
- A launch decision record with approval, rollback plan, and model version.

## Deliberately deferred

- Live production traffic routing.
- Direct inference-provider billing and contractual workflow management.
- Fine-tuning, training, or custom model hosting.
- Fully automated model approval or model migration.

## MVP acceptance criteria

1. A builder can compare models using a versioned workload evaluation.
2. A platform administrator can view the reason for a chosen default route.
3. A decision record captures the evidence, cost estimate, governance constraints, and rollback plan.
4. A user can identify which model is appropriate for a workload without assuming one global winner.
