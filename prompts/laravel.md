# Laravel

Use this when you already work in PHP, or you are hosting where PHP is the
obvious choice, and you want one framework for pages and data. Use
[HTMX and Laravel](htmx-laravel.md) if you specifically want HTML fragments and
almost no JavaScript.

## Why this combination

- **PHP** runs on ordinary hosting and Laravel is the framework that keeps a
  PHP app in one style.
- **Laravel** covers migrations, sessions, queues, and mail so the AI does not
  invent a package for each.
- **Postgres** is still the database. Cheap PHP hosting is not a reason to skip
  a real database or to paste old SQL-concatenation examples.

## Prompt

```text
I want to build a web app people can log into.

Use PHP and Laravel, because I want one PHP framework for pages, migrations,
sessions, and background jobs. Follow the current Laravel docs. Do not add
WordPress, and do not build SQL by concatenating user input.
Use Laravel's own views for the screens. Do not add React unless I ask.
Use Postgres. Do not use MongoDB.
Use Laravel's session auth. HttpOnly, Secure, SameSite cookies. No tokens in
localStorage.

The app is for <who it is for>.
The only task in this version: <main task>.

Rules:
- Environment variables for the database and app key. Nothing secret in git.
- Migrations for every schema change.
- Every private query is scoped to the signed-in user.
- No writes on GET. No secrets in views.
- Semantic HTML, labeled inputs, layout works at 375 pixels wide.
- Do not add a Node server or a second language.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me.
```
