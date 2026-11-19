# BizPeel MCP

Remote MCP server for verified startup revenue, traffic sources, SEO keywords, ad creatives, and 700+ competitive growth breakdowns inside Claude, ChatGPT, Claude Code, Codex, and Cursor.

- **Remote Endpoint**: `https://bizpeel.com/mcp`
- **Transport**: Remote `streamable-http` (no local installation required)
- **Connect Guide**: https://bizpeel.com/docs/connect-agent
- **Tool Reference Docs**: https://bizpeel.com/docs/mcp-tools
- **Website**: https://bizpeel.com

## Quick Start

### Claude Code

```bash
claude mcp add --transport http --scope user bizpeel https://bizpeel.com/mcp
```

### MCP JSON Config (Cursor, VS Code, Codex)

```json
{
  "mcpServers": {
    "bizpeel": {
      "url": "https://bizpeel.com/mcp"
    }
  }
}
```

### Claude.ai & ChatGPT

Add `https://bizpeel.com/mcp` as a custom Remote MCP Connector and complete OAuth sign-in.

## Authentication

- **OAuth 2.1** with PKCE (`S256`) and Dynamic Client Registration (`https://bizpeel.com/.well-known/oauth-protected-resource/mcp`, `https://bizpeel.com/.well-known/oauth-authorization-server`), or
- **API Key / Bearer Token**
- A paid BizPeel subscription is required for tool execution.

## Available Tools (12 Core Tools + 48 Live Capabilities)

| Tool | Description |
| :--- | :--- |
| `search_projects` | Search 700+ verified startups by keyword, revenue band, category, or growth channel |
| `list_facets` | List available categories, directions, and filter facets |
| `get_project` | Fetch structured metadata and report versions for a startup |
| `get_report` | Retrieve a complete Markdown competitive teardown report |
| `get_report_chapter` | Read a specific chapter from a teardown report |
| `get_metrics` | Query verified revenue, traffic, and growth metrics |
| `get_trending` | Retrieve daily revenue rankings and steady earners vs. spikes |
| `export_projects` | Export filtered startup lists for comparison and analysis |
| `search_capabilities` | Discover 48 live competitive intelligence capabilities (SEO, ads, traffic, backlinks, social) |
| `get_capability` | Inspect parameter schema and per-call pricing for a live data capability |
| `run_capability` | Execute a live competitive intelligence lookup for any domain |
| `get_account` | Check current subscription quota and research balance |

## Support & Legal

- Documentation: https://bizpeel.com/docs/connect-agent
- Privacy Policy: https://bizpeel.com/privacy
- Terms of Service: https://bizpeel.com/terms
- Support: support@bizpeel.com

## License

MIT
