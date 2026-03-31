<p align="center">
  <img src="./1774879630657.jpg" alt="Pigeon Superstition Superposition" width="100%" />
</p>

# Pigeon Superstition Superposition

**Psychological Profiling Toolkit** — a 16-framework cognitive surrogate construction system, deployed as a Cloudflare Workers MCP server.

Built for Claude. Hosted on [Smithery](https://smithery.ai/server/elbpr/pigeon-superstition-superposition).

## What it does

Provides structured psychological profiling through 16 peer-reviewed frameworks, accessible as MCP tools. Claude loads the relevant framework on demand, constructs a cognitive surrogate of the subject, and uses it to inform analysis, communication strategy, or investigative reasoning.

## Tools

| Tool | Purpose |
|------|---------|
| `list_frameworks` | List all 16 frameworks with descriptions and trigger conditions |
| `get_framework` | Load the full methodology for a specific framework by ID |
| `get_profiling_toolkit` | Load the master orchestration router that maps profile questions to frameworks |
| `assess` | Submit evidence for assessment against the current profile state |

## Stack

- Cloudflare Workers (runtime)
- `@modelcontextprotocol/sdk` (MCP protocol)
- TypeScript
- Wrangler (deployment)

## Development

```bash
npm install
npm run dev      # local dev server
npm run deploy   # deploy to Cloudflare
```
