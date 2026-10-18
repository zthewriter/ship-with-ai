# Django

Use this when you already work in Python and you want the whole app in Django,
including its admin. Pages are Django templates. Pick [HTMX and Django](htmx-django.md)
instead if the interactions should be small HTML swaps. Do not also start a
Next.js frontend unless a second client is real.

## Why this combination

- **Python** is readable, and it matches data and machine-learning work if that
  is the world around this app.
- **Django** includes an admin site, an ORM, and a session login path, so you
  are not assembling those from packages the AI chose.
- **Postgres** is the database Django should use for a real deploy. SQLite is
  only for a prototype that stays on one machine.

## Prompt

```text
I want to build a web app people can log into.

Use Python and Django, because I already want Python and Django includes the
admin, the ORM, and session auth. Follow the current Django docs. Do not add
Flask, FastAPI, or a JavaScript frontend framework.
Use Django templates for the screens.
Use Postgres, because this will be used by real people and the tables need
links between users and their records. Do not use MongoDB.
Use Django sessions. HttpOnly, Secure, SameSite. No tokens in the browser.

The app is for <who it is for>.
The only task in this version: <main task>.

Rules:
- Settings and the database URL come from the environment.
- Migrations for every model change.
- Every private query is scoped to the signed-in user.
- No secrets in templates. No writes on GET.
- Semantic HTML, labeled inputs, layout works at 375 pixels wide.
- Do not add Node, React, or a second database.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me.
```
