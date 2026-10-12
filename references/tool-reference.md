# Official Wiro MCP tool reference
Source: https://wiro.ai/docs/wiro-mcp-server
Discovery: search_models, get_model_schema, recommend_model, explore.
Execution: run_model.
Task management: wait_for_task, get_task, list_tasks, get_task_price, cancel_task, kill_task.
Utility: upload_file, search_docs.
The official hosted server advertises 13 tools. Discover exact input/output schemas live before using them; this reference is not a substitute for authenticated tool discovery.
Model slugs use `owner/model`. Completed media may be returned as resource links. Wiro advises `wait_for_task` for long jobs rather than resubmission.
