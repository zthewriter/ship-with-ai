# SvelteKit

Use this for a logged-in website when you want small components and less
boilerplate than React. SvelteKit is the full-stack framework. Pin its docs in
your MCP server. The AI has seen fewer complete Svelte apps than React apps and
will drift toward React patterns if you do not forbid that.

## Why this combination

- **Svelte** puts the markup, the style, and the behavior in one component file
  and compiles it ahead of time.
- **SvelteKit** adds routing and server data loading, so you are not building
  that yourself.
- **TypeScript and Postgres** are the same reasons as the Next.js prompt: named
  data, and tables for accounts.

## Prompt

```text
I want to build a web app people can log into.

Use SvelteKit and Svelte with TypeScript, because I want small components and
the server in the same project. Follow the current SvelteKit docs. Do not
introduce React, JSX, or Next.js.
Use TypeScript so each record has a named shape.
Use Postgres, because accounts and private data are tables.
Use a session cookie that is httpOnly, Secure, and SameSite. Hash passwords
with argon2 or bcrypt. No tokens in localStorage.
Use one styling system: <Tailwind or plain CSS>.

The app is for <who it is for>.
The only task in this version: <main task>.

Rules:
- DATABASE_URL from the environment. Migrations for every schema change.
- Every private query includes the signed-in user's id from the session.
- Secrets stay on the server. .env.example lists names with empty values.
- REST or SvelteKit form actions. Errors are { "error": "sentence" }. No writes
  on GET.
- Semantic HTML, labeled inputs, layout works at 375 pixels wide.
- Do not add a second framework or MongoDB.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me.
```
