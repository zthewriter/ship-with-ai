# Express and TypeScript

Use this when a second client is real: a partner, or a phone app someone is
actually building, and the website is only one caller. Express is the separate
API. React is the website. If the website is the only client, stop and use
[Next.js](nextjs-typescript.md) instead. A second server you do not need is a
second thing to secure.

## Why this combination

- **Express** is a small TypeScript (or JavaScript) router. AI tools have seen
  more Express handlers than any other separate Node API, so the shape stays
  familiar.
- **TypeScript** names the body of each route. Express will not do that for you,
  which is why the prompt requires a validator.
- **React** on the website calls the API. It does not receive `DATABASE_URL`.
- **Postgres** stays behind Express. Both clients share those rules.

## Prompt

```text
I want a website and a separate API, because <name the second client> will call
the same rules.

Use Express with TypeScript for the API, because I want a separate Node server
and Express is the router with the most readable examples. Validate every body
on the server. Do not skip validation because Express does not include it.
Use React with TypeScript for the website, because the website is one client of
that API. The website never imports the database and never sees DATABASE_URL.
Use Postgres, because both clients share tables for accounts and private rows.
Use an httpOnly Secure SameSite session cookie for the website. Hash passwords
with argon2 or bcrypt. No tokens in localStorage.
Use Tailwind on the website only.

The app is for <who it is for>.
The only task in this version: <main task>.

Rules:
- Two folders: api and web. Secrets only in the api environment.
- Migrations for every schema change. Preview and production use different
  databases.
- Auth middleware on every private route. The handler scopes queries to the
  session user. Do not trust a user id in the body.
- REST JSON. Errors are { "error": "sentence" }. No writes on GET.
- CORS allows only the website's origin. CORS is not login.
- Do not add NestJS, Go, Rust, MongoDB, or GraphQL.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me.
```
