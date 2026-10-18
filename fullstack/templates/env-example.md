# Environment variable template

Copy the names into `.env.example` and commit that file. Put real values only in
`.env` on your machine and in the host's environment settings. `.env` stays in
`.gitignore`.

Empty means empty. Do not invent a realistic password "just as a sample". People
commit those.

```bash
# Server only. Never prefix these so they ship to the browser.
DATABASE_URL=
SESSION_SECRET=

# Auth provider, if you use one. Server only.
AUTH_SECRET=
AUTH_GOOGLE_ID=
AUTH_GOOGLE_SECRET=

# This one is public. It is the site's own address, not a key.
NEXT_PUBLIC_APP_URL=
```

Rename `NEXT_PUBLIC_APP_URL` to whatever your framework calls a browser-visible
value. If the framework has no such prefix, do not create a second copy of
`DATABASE_URL` for the client. The client does not get one.

## Rules

- A new service adds a new name here in the same pull request as the code that
  reads it.
- Preview and production each have their own values. Preview's `DATABASE_URL` is
  not production's.
- If a value has been pasted into a chat, a screenshot, or git, rotate it. Treat
  it as public.

## What to tell your AI

"Read secrets from environment variables. Add every new name to `.env.example`
with an empty value. Refuse to print secret values in logs, errors, or the pull
request description."
