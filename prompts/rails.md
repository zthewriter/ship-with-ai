# Rails

Use this when you already want Ruby and you want Rails to choose the folder
layout, the ORM, and the session approach. Use [HTMX and Rails](htmx-rails.md)
when you also want interactions to be HTML fragments. Follow the Rails guides.
An AI that ignores the conventions will make a worse Rails app than a boring
Next.js app.

## Why this combination

- **Ruby** is the language Rails is designed around.
- **Rails** ships a database-backed app quickly when the conventions are
  respected: models, migrations, controllers, and server-rendered views.
- **Postgres** matches that model. Do not let the tool swap in a document
  database to avoid a migration.

## Prompt

```text
I want to build a web app people can log into.

Use Ruby on Rails, because I want Rails conventions for models, migrations,
controllers, and server-rendered views. Follow the current Rails guides. Do not
add a Node.js frontend.
Use Postgres. Do not use MongoDB.
Use Rails sessions. HttpOnly, Secure, SameSite. No tokens stored for page
scripts to read.

The app is for <who it is for>.
The only task in this version: <main task>.

Rules:
- Secrets and the database URL stay out of git.
- Migrations for every schema change.
- Every private query is scoped to the signed-in user, in the controller or the
  model scope, not only by hiding a link.
- No writes on GET.
- Semantic HTML, labeled inputs, layout works at 375 pixels wide.
- Do not add React, GraphQL, or a second language.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me.
```
