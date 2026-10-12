# Wiro AI Plugin

Independent ChatGPT/Codex integration for the official Wiro MCP server, not affiliated with Wiro. Nine skills cover setup, model discovery, image, video, audio, task management, cost optimization, batch workflows and general model workflows.

## Install in Codex

Install from the private GitHub repository using a GitHub account with repository access:

```powershell
codex plugin marketplace add git@github.com:kiliczsh/wiro-ai-plugin.git
codex plugin add wiro-ai-plugin@wiro-local
```

Alternatively, run from a local clone:

```powershell
codex plugin marketplace add .
codex plugin add wiro-ai-plugin@wiro-local
```

Configure Wiro authentication separately through a supported secure credential form; installation alone does not confirm a working connection.

## Package structure

`plugin.json` and `mcp.json` provide the portable package. `.codex-plugin/plugin.json` and `.mcp.json` provide Codex compatibility. `.agents/plugins/marketplace.json` declares the local marketplace. Include all nine skills, references and icons when packaging.

## Development

Keep both manifests synchronized, validate JSON and referenced paths, and copy generated output URLs exactly. Exclude credentials, caches and task outputs from releases.

## License

No license has been selected. Add an explicit license before granting reuse rights.

## Security
Do not store Wiro credentials in this package. API Key Only uses a single bearer key. Signature-Based uses a single `API_KEY:API_SECRET` bearer credential. Whether ChatGPT exposes the secure Connected accounts API-key form requires live verification. This plugin does not include an OAuth proxy, custom dashboard or hosted backend.

## Validation
After secure connection, call `search_models` as a non-billable smoke test. Only then attempt a user-approved billable `run_model` call.
