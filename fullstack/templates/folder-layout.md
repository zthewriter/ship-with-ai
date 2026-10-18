# Folder layout

Hand this shape to your AI when it creates the project. Names vary by framework.
The jobs do not. If a file does not serve one of these jobs, ask why it exists
before you keep it.

## A JavaScript full-stack app (Next.js and its cousins)

```text
your-app/
  app/                 screens. Folders become URLs.
  app/api/             endpoints, if they live in this app
  components/          shared buttons, fields, and layout
  lib/                 server-only helpers: database, auth checks
  prisma/ or drizzle/  schema and migrations
  public/              images and files the browser may fetch
  .env.example         variable names, empty values
  .gitignore           includes .env
  README.md            how to run it locally, no secrets
```

`lib/` code that reads `DATABASE_URL` is imported only from server files. Browser
components import `components/`, not `lib/db`.

## A separate API plus a website

```text
api/
  src/routes/          one folder per resource: orders, accounts
  src/middleware/      auth, error shape, rate limit
  src/db/              connection and migrations
  .env.example
web/
  src/                 screens and components
  .env.example         public site URL only, no database URL
```

Two folders, two deploys, one decisions note. The website does not get a copy of
the API's secrets.

## What good looks like

- A route file is short because the check and the query have names.
- Shared UI lives in one place, so the button style cannot drift.
- Migrations are files, reviewed like code.
- `.env` is ignored. `.env.example` is committed.

## What to tell your AI

"Match this layout. Do not add `services/`, `cache/`, or a second app unless the
decisions note says so. If you need a new top-level folder, say why first."

See the [environment variable template](env-example.md) for the names that go in
`.env.example`.
