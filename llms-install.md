# Installing BizPeel MCP in Cline

This guide is designed for AI coding assistants (including Cline) to configure the remote BizPeel MCP server cleanly.

## Prerequisites

- A BizPeel account with an active plan (https://bizpeel.com)
- No local Node.js/Python server installation is required; BizPeel MCP runs over remote Streamable HTTP (`https://bizpeel.com/mcp`).

## Step 1: Add BizPeel to Cline's MCP Settings

Add the following remote Streamable HTTP entry under `mcpServers` in Cline's `cline_mcp_settings.json`:

```json
{
  "mcpServers": {
    "bizpeel": {
      "url": "https://bizpeel.com/mcp",
      "type": "streamableHttp",
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

If using an API key instead of browser OAuth, ask the user for their BizPeel API key from https://bizpeel.com/docs/connect-agent and include an `Authorization` header:

```json
{
  "mcpServers": {
    "bizpeel": {
      "url": "https://bizpeel.com/mcp",
      "type": "streamableHttp",
      "headers": {
        "Authorization": "Bearer YOUR_BIZPEEL_API_KEY"
      },
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

## Step 2: Authenticate & Verify

1. With OAuth: Cline discovers `https://bizpeel.com/.well-known/oauth-protected-resource/mcp` and prompts the user to sign in via browser OAuth 2.1 (PKCE).
2. With API key: verify immediately once the header is saved.
3. Call `list_facets` or `get_account` (both free, unmetered) to verify that all 12 tools are connected.
