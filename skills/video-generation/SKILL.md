---
name: video-generation
description: Generate and resume Wiro text-to-video and image-to-video tasks without duplicate charges.
---

# Video workflows
Determine source type, duration, aspect ratio, reference image, motion and desired style. Search model catalog and inspect schema for valid durations, formats, pricing and limits. Video tasks may run for minutes. Submit `run_model` only once per intended generation; use `wait:false` or bounded wait and `wait_for_task` with the exact returned token. Never rerun a model just to wait. Report intermediate state and eventual real video URL. Do not promise an ETA without provider evidence. Confirm costly multi-clip jobs and provide expected spend when available.
