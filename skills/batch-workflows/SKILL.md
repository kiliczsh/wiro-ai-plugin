---
name: batch-workflows
description: Plan multi-step Wiro workflows with cost approval and robust task chaining.
---

# Multi-step workflows
Plan discovery → schema validation → price estimation → user approval for chargeable batches → run each task once → wait/poll → collect real output URLs → review billed costs. Never fabricate file links or pass an output into a downstream model until the prior task has completed and produced a valid accessible URL. `upload_file` accepts a URL, not arbitrary local file bytes; only upload when required or reused. For large batches, state expected task count and potential cost, and request explicit approval. Do not claim automatic scheduled execution or background persistence without host support. If an individual task fails, report partial successes and do not retry chargeable runs without approval.
