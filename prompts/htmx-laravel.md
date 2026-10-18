# HTMX and Laravel

Use this when the app is forms and pages, you want little JavaScript, and you
want PHP. Laravel renders the HTML. HTMX swaps in the updated piece. If you want
Laravel's own full UI stack instead of HTMX, use [Laravel](laravel.md).

## Why this combination

- **Laravel** is the batteries-included PHP framework: tables, sessions, mail,
  and a place for background jobs.
- **HTMX** keeps the browser work in HTML, which matches a server that already
  renders pages.
- **PHP** is the language Laravel runs. Hold the tool to current Laravel docs so
  it does not copy unsafe old PHP.

## Prompt

```text
I want to build a web app people can log into, made of pages and forms.

Use Laravel, because I want a PHP framework that includes database migrations,
sessions, and server-rendered pages. Follow the current Laravel docs. Do not
copy PHP snippets that build SQL by concatenating strings.
Use HTMX, because updates should be HTML fragments from Laravel. Do not add
React, Vue, or a Node server.
Use Postgres, because accounts and private records are tables.
Use Laravel's session guard. HttpOnly, Secure, SameSite cookies. No tokens in
localStorage.

The app is for <who it is for>.
The only task in this version: <main task>.

Rules:
- Database URL from the environment. Migrations for every schema change.
- Every private query is scoped to the signed-in user.
- No secrets in Blade views. No writes on GET.
- Semantic HTML, labeled inputs, layout works at 375 pixels wide.
- Do not add MongoDB, GraphQL, or a second language.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me.
```
