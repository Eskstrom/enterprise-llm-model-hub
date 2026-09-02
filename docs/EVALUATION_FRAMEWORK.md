# Evaluation Framework

## Principle

Evaluate a model against the work it must perform, not against a single abstract benchmark score.

## Workload suite

| Workload | Primary quality measure | Additional checks |
| --- | --- | --- |
| Grounded Q&A | Citation-supported answer rate | Unsupported-claim rate, abstention quality |
| Summarization | Human rubric score | Coverage, factual consistency, length control |
| Structured extraction | Field-level accuracy | Schema adherence, missing-value handling |
| Tool calling | End-to-end task success | Valid arguments, recovery from tool error |

## Evaluation inputs

- A versioned, representative test set.
- Expected outputs or a human scoring rubric.
- Prompt and model versions captured with each run.
- A labeled failure taxonomy: retrieval issue, reasoning issue, formatting issue, tool error, or policy refusal.

## Decision metrics

- Task success rate
- Groundedness or citation accuracy
- P50 and P95 latency
- Input and output tokens per task
- Cost per successful task
- Human correction and override rate

## Release gates

A model may graduate from experiment to production only when it meets the workload quality threshold, stays inside the defined P95 latency and unit-cost bounds, passes governance checks, and has a rollback path.

## Why offline and online evaluation both matter

Offline evaluation catches known regressions before release. Online monitoring reveals whether real customer behavior, data distributions, and usage patterns change the result after launch.
