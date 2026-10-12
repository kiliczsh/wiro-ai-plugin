---
name: setup
description: Connect and diagnose a secure Wiro MCP account using API Key Only or Signature-Based credentials.
---

# Connection and authentication
Use https://wiro.ai/docs/wiro-mcp-server and https://wiro.ai/docs/introduction as authoritative references.
1. Create/select a Wiro project at https://wiro.ai/panel/project. Project authentication type cannot be changed afterward.
2. Hosted MCP URL: `https://mcp.wiro.ai/v1`, Streamable HTTP. API Key Only requires `Authorization: Bearer API_KEY`; Signature-Based requires `Authorization: Bearer API_KEY:API_SECRET` (literal colon, not base64). The plugin declares host-specific bearer API-key authentication, but the ChatGPT Connected accounts UI is not guaranteed to expose it.
3. Enter credentials only in the host's trusted credential form. Never paste into chat, prompt, skill, manifest, logs or public code. If host lacks secure API-key connection, explain that an authenticated OAuth MCP gateway must be built and hosted separately; do not claim this plugin includes such a gateway.
4. After connecting, use `search_models` as a read-only smoke test; do not generate billable content for connection testing.
5. 401: verify key, secret and project auth mode; 403: permissions/signature; 429: backoff. Do not print credential strings or retry billable actions blindly.
6. To disconnect, use the host's account connection controls; never assert revocation at Wiro without confirmation.
