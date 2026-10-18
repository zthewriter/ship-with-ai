# Qwik

Do not start here. Qwik is built so a page can become interactive without
downloading the whole app first. Use it when that first load is the problem you
have. A normal logged-in app should use [Next.js](nextjs-typescript.md). Qwik is
newer, so an AI will guess outdated APIs unless the current docs are in your
MCP server.

## Why you would use it anyway

- **Qwik** resumes a page instead of booting a large JavaScript bundle. That is
  the whole perk.
- **TypeScript** is still the language. **Postgres** is still the database. Qwik
  does not replace either one.

## Prompt

```text
I want a web app people can log into, and the reason it is Qwik is that the
first load must not download the whole application.

Use Qwik with TypeScript. Follow the current Qwik docs. Do not rewrite this in
React or Next.js.
Use Postgres. Session cookie, httpOnly Secure SameSite. Hash passwords with
argon2 or bcrypt. No tokens in localStorage.
Use one styling system: <Tailwind or plain CSS>.

The app is for <who it is for>.
The only task in this version: <main task>.

Rules:
- DATABASE_URL from the environment. Migrations for every schema change.
- Server-only code talks to the database. Queries include the session user's id.
- REST JSON. Errors are { "error": "sentence" }. No writes on GET.
- Semantic HTML, labeled inputs, layout works at 375 pixels wide.
- Do not add a second framework or MongoDB.
- Search the MCP server before inventing a name. If the docs and this prompt
  disagree on a Qwik API name, stop and tell me. Do not guess.
```
