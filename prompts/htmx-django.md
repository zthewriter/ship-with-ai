# HTMX and Django

Use this when the app is forms and pages, you want little JavaScript, and you
want Python. Django renders HTML. HTMX swaps in the piece that changed. If you
want Django's admin and ordinary Django templates without HTMX, use
[Django](django.md) instead.

## Why this combination

- **Django** gives you an admin, a database layer, and an auth path in Python.
- **HTMX** avoids a second frontend project for screens that are mostly forms.
- **Python** stays the only programming language, which matters if the rest of
  your work is already Python.

## Prompt

```text
I want to build a web app people can log into, made of pages and forms.

Use Django, because I want a Python framework with an admin, a database layer,
and server-rendered pages. Follow the current Django docs. Do not add a Node.js
frontend.
Use HTMX, because updates should be HTML fragments from Django, not a React or
Vue app.
Use Postgres, because accounts and private records are tables.
Use Django's session auth. HttpOnly, Secure, SameSite cookies. No tokens in
localStorage.

The app is for <who it is for>.
The only task in this version: <main task>.

Rules:
- Database settings from the environment. Migrations for every schema change.
- Every private query is scoped to the signed-in user.
- No secrets in templates. No writes on GET.
- Semantic HTML, labeled inputs, layout works at 375 pixels wide.
- Do not add MongoDB, GraphQL, React, or a second language.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me.
```
