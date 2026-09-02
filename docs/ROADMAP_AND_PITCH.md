# Roadmap and PM Pitch

## Roadmap

### Now: trusted model evaluation

- Launch the model catalog and workload-specific offline evaluation suite.
- Establish approval records, test-set versioning, and release gates.
- Pilot with grounded Q&A and summarization workloads.

### Next: controlled customer experimentation

- Add side-by-side experiments, customer-configurable quality thresholds, and model upgrade recommendations.
- Introduce spend dashboards and workload-level cost forecasts.
- Expand to extraction and tool-calling workflows.

### Later: scaled routing and optimization

- Support policy-based routing, capacity-aware fallbacks, and tenant-level budgets.
- Add online evaluation signals, regression alerts, and automated rollback recommendations.
- Build provider performance and portfolio-planning views.

## Three-minute product demo

1. A product builder creates a grounded-Q&A workload and selects quality, latency, and budget criteria.
2. Model Hub compares approved models and surfaces quantitative results alongside qualitative failures.
3. The builder selects a routing policy and submits it for approval.
4. An administrator reviews the projected cost, capacity risk, data constraints, and rollback plan.
5. The decision record becomes the traceable path to production.

## PM pitch

I approach AI products as operational systems, not isolated model demos. My experience spans AI deployment and adoption across customer environments, data-reconciliation and exception workflows in regulated operations, and AI-product delivery from early concept through shipped features. This project applies that perspective to the platform layer: evaluate models against real customer work, make quality-cost-capacity trade-offs explicit, and provide a governed path from experimentation to scaled adoption.

## Interview discussion prompts

- How would you choose the first workload and evaluation threshold?
- When should customer model choice be constrained?
- How would you forecast demand when a new model is introduced?
- Which signals trigger a rollback, and who owns that decision?
