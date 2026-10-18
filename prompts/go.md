# Go

Use Go when the backend is its own API and you want a small language and one
file you can copy to a server. Go's standard library serves HTTP. You do not
need a large framework. The screens are still HTML, CSS, and JavaScript. Go does
not replace React.

There are two honest pairs. Paste one.

- **Go and Next.js** when the UI is a rich logged-in app and Go owns the rules
  because you want that API to stay small and obvious.
- **Go and HTMX** when the app is forms and pages and you want one language on
  the server returning HTML.

Do not pick Go because a benchmark beat Node. Pick it because you want the
single binary and the small language. If you want the most help from an AI on a
first website, use [Next.js](nextjs-typescript.md) and leave Go out.

## Why Go

- The language stays small, so a later chat has fewer tricks to invent.
- `go build` produces one binary. Deploy is "run this file".
- [`net/http`](https://pkg.go.dev/net/http) is enough for a clear API. The
  [Go docs](https://go.dev/doc/) and the
  [web applications article](https://go.dev/doc/articles/wiki/) belong in your
  MCP server.
- You will write more plumbing than in Rails. That is the trade.

## Prompt: Go API and a Next.js website

```text
I want a web app people can log into. The API is a separate Go service. The
website is Next.js.

Use Go for the API, because I want a small language and a single binary, and
the standard library's net/http is enough. Follow the current Go docs. Do not
add a second Go web framework unless net/http cannot express a route, and if
you think that, stop and tell me first.
Use Next.js with TypeScript for the website only, because the screens need a
rich UI and Next.js is the frontend. The website calls the Go API. It does not
talk to Postgres. Do not move the database into Next.js.
Use Postgres, because accounts and private rows are tables. Use a Go SQL driver
or a small query library with placeholders. No string-built SQL.
Use an httpOnly Secure SameSite session cookie issued by the Go API. Hash
passwords with argon2 or bcrypt. No tokens in localStorage.
Use Tailwind on the website.

The app is for <who it is for>.
The only task in this version: <main task>.

Rules:
- DATABASE_URL only on the Go service. Migrations are SQL files in git.
- Every private query includes the signed-in user's id.
- REST JSON. Errors are { "error": "sentence" }. No writes on GET.
- CORS allows only the website's origin. CORS is not authentication.
- Do not add Rust, Node as a second API, MongoDB, or GraphQL.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me.
```

## Prompt: Go and HTMX

```text
I want a web app people can log into, made of pages and forms.

Use Go and net/http, because I want one small language and HTML rendered by the
server. Follow the current Go docs. Use HTMX so updates are HTML fragments.
Do not add React, Next.js, or a second server.
Use Postgres with placeholders. No string-built SQL.
Use an httpOnly Secure SameSite session cookie. Hash passwords with argon2 or
bcrypt.

The app is for <who it is for>.
The only task in this version: <main task>.

Rules:
- DATABASE_URL from the environment. SQL migrations in git.
- Every private query is scoped to the signed-in user.
- No secrets in templates. No writes on GET.
- Semantic HTML, labeled inputs, layout works at 375 pixels wide.
- Do not add MongoDB or another language.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me.
```
