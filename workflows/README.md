# Workflows

Ready-to-import [n8n](https://n8n.io/) workflows. In n8n, open the workflow menu and
choose **Import from File**.

| Workflow | What it does | Guide |
|---|---|---|
| [docs-chat-assistant.json](docs-chat-assistant.json) | A chat assistant that answers from your content through an MCP server and cites its sources | [Build your first AI assistant](../docs/04-build-your-first-assistant.md) |

After importing, replace the MCP Client **Endpoint** with your own server URL and add
your chat model credential. Workflows never contain keys; you add your own in n8n.

Built a workflow worth sharing? Open a pull request. Remove credentials and personal
URLs first.
