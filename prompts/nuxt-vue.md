# Nuxt and Vue

Use this when the app is a website people log into and you want the screens to
look like HTML. Vue templates are HTML with a few extra attributes. Nuxt is the
server and the router. Skip it if you have no preference. Next.js has more
examples. Skip it if you already live in Python, Ruby, or PHP.

## Why this combination

- **Vue** keeps the markup readable if you think in pages rather than in
  JavaScript functions.
- **Nuxt** adds file-based pages and server routes, so you do not assemble a
  server beside Vue yourself.
- **TypeScript** still names the data, even though the templates look like HTML.
- **Postgres** is the same choice as every other logged-in app here.

## Prompt

```text
I want to build a web app people can log into.

Use Nuxt and Vue with TypeScript, because I want HTML-like templates and one
project that includes the server. Follow the current Nuxt docs. Do not rewrite
this as React or Next.js.
Use TypeScript because the shape of each record should fail the build when a
field is invented.
Use Postgres, because sign-in and private records need tables.
Use Nuxt's current recommended auth approach for a session cookie that is
httpOnly, Secure, and SameSite. Do not store tokens in localStorage.
Use one styling system: <Tailwind or plain CSS>.

The app is for <who it is for>.
The only task in this version: <main task>.

Rules:
- DATABASE_URL comes from the environment. Migrations for every schema change.
- Hash passwords with argon2 or bcrypt. Never log secrets or session ids.
- Every private query includes the signed-in user's id from the session.
- REST JSON where the UI calls the server. Errors are { "error": "sentence" }.
  No writes on GET.
- Semantic HTML, labeled inputs, layout works at 375 pixels wide.
- Do not add React, Next.js, MongoDB, or a second backend language.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me.
```
