---
name: task-management
description: Inspect, resume, cancel and summarize Wiro generations across sessions.
---

# Task management
Use `list_tasks` for authenticated history and `get_task` for details. Report ID, status, model, created time if available, output and actual billing when available. Resume an existing run with `wait_for_task` and its original token; never submit a duplicate run. Use `cancel_task` only for queued tasks and `kill_task` only for running tasks after clear user authorization. Treat cancellation as requested until the provider confirms it. Task states may be submitted/running/completed/failed/cancelled; success requires confirmed completion and `pexit` of `"0"` when present. Do not expose access tokens in summaries.
