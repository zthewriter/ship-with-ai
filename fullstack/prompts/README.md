# Prompts to paste

The prompt that names your framework, language, and why lives in
[prompts](../../prompts/README.md). Paste that one first. Use the prompts below
after the [decisions note](../checklists/before-you-prompt.md) exists
and the [MCP server](../12-persistent-context-with-mcp.md) is connected. Paste one
at a time. If the tool starts a second framework or a second database, stop and
point it at the note.

Replace the angle brackets. Do not paste real keys into the chat.

## 1. Agree the stack

```text
Read fullstack/13-choose-your-stack.md and my decisions note.
Search the MCP server before you answer.
Propose the stack in one short paragraph and list what you will not add.
Do not write code until I agree.
```

## 2. Create the project

```text
Create the app from my decisions note.
Use the folder layout in fullstack/templates/folder-layout.md
and the env names in fullstack/templates/env-example.md.
Current docs for <framework> only. Do not add services I did not name.
Show me how to run it locally. Do not invent secret values.
```

## 3. Build the main task

```text
Build only this task: <main task>.
Screens follow fullstack/03-components-layout-and-design.md.
Data goes through endpoints in fullstack/07-apis-and-endpoints.md.
Every private query is scoped to the signed-in user on the server.
Error responses use { "error": "sentence" }.
Search the MCP server if you are unsure of a name we already chose.
```

## 4. Add sign-in

```text
Add sign-in using <auth library> as described in fullstack/09-authentication.md.
HttpOnly Secure SameSite session cookie. Hash passwords with argon2 or bcrypt.
Do not store tokens in localStorage. Do not log passwords, hashes, or session ids.
Sign-out deletes the session on the server.
```

## 5. Review like a backend engineer

```text
Review the API and database against fullstack/07, fullstack/08, and fullstack/10.
List each private route and the line where it checks the signed-in user.
Point out any string-built SQL, any secret in client code, any write on GET,
and any error that leaks a stack trace.
Do not expand the feature. Fix only the issues you listed, after I say yes.
```

## 6. Prepare production

```text
Walk fullstack/checklists/production.md against this repo.
For each unchecked item, say what file you would change.
Do not deploy. Do not print env values.
Remind me to use a separate database for preview and for production.
```

## 7. Keep the next session honest

```text
Search the MCP server for the stack, the endpoint list, and the security rules.
Summarize them in five lines. If the code disagrees with the notes, stop and
tell me which file drifted. Do not silently "clean it up" by picking a new
library.
```
