---
name: connect-mcp-server
description: Adds a remote MCP server to the user's AI tool configuration and confirms it works. Use when the user wants to connect an MCP server, add persistent context, or reports that an MCP server shows no tools.
---

# Connect an MCP server

## Steps

1. Ask the user for the server URL, and whether the server is private. Do not ask
   for a token in chat; a private server's token belongs in an environment variable.
2. Find the configuration file for the tool in use, and show the user the change
   before making it:
   - Cursor: `.cursor/mcp.json` in the project, or `~/.cursor/mcp.json` for all
     projects.
   - Claude Code: run `claude mcp add --transport http <name> <url>`.
   - Codex: `~/.codex/config.toml`, under `[mcp_servers.<name>]`.
3. Add the server with the remote URL. For Cursor:

   ```json
   {
     "mcpServers": {
       "my-docs": { "url": "https://example.com/mcp" }
     }
   }
   ```

4. For a private server, read the token from an environment variable. In Codex,
   `bearer_token_env_var` takes the variable's *name*, never the token itself.
5. Tell the user to restart or reload the tool if it only loads servers on startup.
6. Confirm it works: list the server's tools, then call one search tool with a
   question the user's content answers, and show the result with its source link.

## If it shows no tools

- Compare the URL character by character with the one the user copied.
- Read the tool's MCP log and report the first error, not the last.
- Check that a private server has its token, and that the token is in the right
  setting.

## Never

- Never paste a token into a file that is committed to git.
- Never report success without a working tool call.
