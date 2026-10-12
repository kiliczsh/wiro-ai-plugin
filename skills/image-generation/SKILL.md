---
name: image-generation
description: Run Wiro image generation, editing, upscaling and virtual try-on with schema validation.
---

# Image workflows
Identify text-to-image, image-to-image, editing, upscaling or try-on intent. Discover the model, call `get_model_schema`, validate prompt, image URL, aspect ratio, resolution and model-specific required fields. Do not assume a common schema across models. Show price estimate when available. For explicit paid generation, run once with `run_model`, otherwise confirm first. Use `wait_for_task` for pending tasks; preserve task ID/token and never resubmit to poll. On success, return actual output URL(s), aspect ratio/resolution if known, and billed cost only after `get_task_price`. For user-supplied images, avoid sending private URLs without consent.
