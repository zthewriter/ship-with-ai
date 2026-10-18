# Fastify and TypeScript

Use this for the same situation as Express: a real second client, and a
separate API. Pick Fastify when you want each route to declare the shape of its
input up front. Pick Express when you want the largest set of examples. Do not
run both.

## Why this combination

- **Fastify** is a Node server in the same family as Express, and a schema on
  the route rejects bad input before your code runs.
- **TypeScript** matches those schemas to the values inside the handler.
- **React** stays the website, for the same reason as the Express prompt: the
  UI is a client, not the place the rules live.

## Prompt

```text
I want a website and a separate API, because <name the second client> will call
the same rules.

Use Fastify with TypeScript for the API, because I want a schema on every route
so bad input fails before the handler. Follow the current Fastify docs. Do not
switch to Express.
Use React with TypeScript for the website. The website calls the API and does
not receive DATABASE_URL.
Use Postgres for accounts and private rows.
Use an httpOnly Secure SameSite session cookie for the website. Hash passwords
with argon2 or bcrypt. No tokens in localStorage.
Use Tailwind on the website only.

The app is for <who it is for>.
The only task in this version: <main task>.

Rules:
- Two folders: api and web. Secrets only in the api environment.
- A JSON schema or equivalent on every route that accepts a body.
- Migrations for every schema change.
- Auth on every private route. Queries include the session user's id.
- REST JSON. Errors are { "error": "sentence" }. No writes on GET.
- CORS allows only the website's origin.
- Do not add Express, NestJS, MongoDB, or a second language.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me.
```
