# Decisions to make before you prompt

Fill this in before the AI writes the app. Unanswered blanks become whatever the
model saw last on the internet.

```text
App name:
One-sentence job:
Who it is for:
The main task they repeat:

Framework:
Database: Postgres
Auth:
Styling: Tailwind or plain CSS
API lives: inside the app, or a separate backend
Host:
Error JSON: { "error": "sentence" }

Private data: queries include the signed-in user's id
Not using:
```

## Why each line is there

**One main task.** The first version does that task, plus sign-in if the task has
private data. Extra modules can wait.

**Framework and "not using".** [Choose your stack](../13-choose-your-stack.md)
picks the first. The second stops a later chat from mixing in another one.

**Where the API lives.** One website means inside the app. A second client that
is actually being built means a separate API. "Maybe someday" stays inside the
app.

**Error JSON.** One shape, so the screens can show it.

Put the finished note in the [MCP server](../12-persistent-context-with-mcp.md)
you connect before generating code. Then use the
[prompts](../prompts/README.md).
