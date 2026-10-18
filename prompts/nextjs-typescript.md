# Next.js and TypeScript

Use this for a website people log into, when you do not already have a language.
The screens and the server live in one project. Skip it if a second client must
call the API this month. Use [Express](express-typescript.md) or [Go](go.md) for
that.

## Why this combination

- **Next.js** puts React pages and the API in one deploy, and the current docs
  teach the App Router. AI tools have seen this shape more than any other, so
  less of the code is invented.
- **TypeScript** names the shape of a user and a project, so a made-up field
  fails the build.
- **Postgres** stores accounts and the things they own as tables.
- **Auth.js** gives a normal website an httpOnly session cookie, which page
  scripts cannot read.

## Prompt

```text
I want to build a web app people can log into.

Use Next.js with the App Router, React, and TypeScript, because the screens and
the server belong in one project and the current Next.js docs are the source of
truth. Ignore Pages Router tutorials.
Use TypeScript because a named type for each request and each database row stops
you from inventing fields.
Use Postgres with Prisma or Drizzle, because accounts and private records need
tables and links between them.
Use Auth.js, because this is a website I own and sign-in should be an httpOnly
session cookie, not a token in localStorage.
Use Tailwind, because the styling should sit next to the components and there
is only one styling system.

The app is for <who it is for>.
The only task in this version: <main task>.

Rules:
- DATABASE_URL comes from the environment. Migrations for every schema change.
- Hash passwords with argon2 or bcrypt. Never log a password, a hash, or a session id.
- Every private query includes the signed-in user's id from the session.
- Secrets stay in server files. Names go in .env.example with empty values.
- REST JSON. Errors are { "error": "sentence" }. No writes on GET.
- Semantic HTML, labeled inputs, and the layout works at 375 pixels wide.
- Do not add Vue, Angular, Express, MongoDB, GraphQL, Go, or Rust.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me. Do not write code for a different stack.
```
