# Hono and TypeScript

Use this for a small separate API when you want short route code and you may
deploy it somewhere that is not a long-running Node process. The website is
still a TypeScript frontend. If you are not sure, use [Express](express-typescript.md).
Hono's perk is size and portability, not a bigger feature list.

## Why this combination

- **Hono** looks like Express and stays small. One style of route can run on
  Node and on several other hosts.
- **TypeScript** is the language Hono is most at home in.
- **React** (or Next.js used only as the UI, calling this API) keeps the screens
  in the ecosystem with the most UI examples. This prompt uses React so the API
  stays the only backend.

## Prompt

```text
I want a small separate API and a website, because <name the second client, or
"the API must deploy on its own">.

Use Hono with TypeScript for the API, because I want short routes and a server
I can move between hosts. Follow the current Hono docs. Do not add Express as
well.
Use React with TypeScript for the website. The website never sees DATABASE_URL.
Use Postgres.
Use an httpOnly Secure SameSite session cookie for the website. Hash passwords
with argon2 or bcrypt. No tokens in localStorage.
Use Tailwind on the website only.

The app is for <who it is for>.
The only task in this version: <main task>.

Rules:
- Secrets only on the API. Migrations for every schema change.
- Validate input in the API. Auth on every private route.
- Queries include the session user's id. Do not trust a user id in the body.
- REST JSON. Errors are { "error": "sentence" }. No writes on GET.
- CORS allows only the website's origin.
- Do not add a second backend framework, MongoDB, or GraphQL.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me.
```
