# Rust and Axum

Use this only when you chose Rust on purpose. Rust's compiler refuses a class of
memory bugs, and there is no garbage collector. That is the benefit. The cost is
that generated code often does not compile, and a first login app moves slower
here than in Go or TypeScript.

If you wanted "a fast API" and you have not measured a problem, use
[Go](go.md) or [Express](express-typescript.md). If you are ready to read
compiler errors and you want the API in Rust, paste the prompt below. Put the
[Rust book](https://rust-lang.org/learn) and the
[Axum docs](https://docs.rs/axum/latest/axum/) in your MCP server first.

## Why this combination

- **Rust** makes ownership and errors explicit. The compiler is part of the
  workflow, not an obstacle to delete with `allow` attributes everywhere.
- **Axum** is the HTTP library to ask for. Do not let the tool switch between
  Axum and Actix in the same project.
- **Next.js** stays the website. Rust does not render your React screens. The
  browser still runs JavaScript.
- **Postgres** with placeholders. Rust's type system does not automatically
  prevent SQL injection if you concatenate strings.

## Prompt

```text
I want a separate API in Rust and a website people can log into.

Use Rust and Axum for the API, because I want the compiler to check memory
safety and I will read compiler errors instead of silencing them. Follow the
current Axum docs. Do not switch to Actix, and do not rewrite the API in Go or
Node.
Use Next.js with TypeScript for the website only. The website calls the Axum
API and never sees DATABASE_URL.
Use Postgres with parameterized queries. No string-built SQL.
Use an httpOnly Secure SameSite session cookie issued by the API. Hash
passwords with argon2. No tokens in localStorage.
Use Tailwind on the website.

The app is for <who it is for>.
The only task in this version: <main task>.

Rules:
- DATABASE_URL only on the API. SQL migrations in git.
- Every private query includes the signed-in user's id.
- REST JSON. Errors are { "error": "sentence" }. No writes on GET.
- CORS allows only the website's origin.
- Do not sprinkle unwrap on library errors to make the build pass. Return a
  proper error response and tell me what failed.
- Do not add a second backend language or MongoDB.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me.
```
