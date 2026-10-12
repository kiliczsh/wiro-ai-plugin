---
name: cost-optimization
description: Estimate, compare and audit Wiro generation spending without inventing prices.
---

# Cost controls
Use `get_model_schema` and model catalog to obtain current pricing. Explain units and usage-based uncertainty. Before expensive or batch jobs calculate best-case and worst-case only when grounded by source pricing. After generation use `get_task_price` for final billed amount and billing status. Do not equate price estimate with charge. For cost reports retrieve task history and sum only confirmed charges; separate unknown/unbilled. If budget is given, request approval before any run that could exceed it. Never claim plugin enforces account-level spend limits; it does not.
