# Solid

Do not start here. Solid looks a bit like React and updates only the piece of
the page that changed. That perk matters when a screen is actually slow because
too much of it rerenders. It does not matter on a normal form.

If you have not seen that slowness, use [Next.js](nextjs-typescript.md). If you
have, paste this and put the [Solid docs](https://docs.solidjs.com/) in your MCP
server. The AI has fewer correct examples and will import React by accident.

## Why you would use it anyway

- **Solid** keeps React-like components without rerendering the whole component
  to change one value.
- **TypeScript and Postgres** do not change. Solid is only the screen. You still
  need a server. This prompt uses Solid's own app framework so you are not
  assembling one.

## Prompt

```text
I want a web app people can log into. The screen has a measured update problem,
which is why this is Solid and not React.

Use Solid with TypeScript, because updates should touch only the values that
changed. Follow the current Solid docs. Do not import React.
Use SolidStart if the current Solid docs still call the full-stack app that.
If the docs use a different name for the official app framework, use that name
and tell me before you install anything else.
Use Postgres. Session cookie, httpOnly Secure SameSite. Hash passwords with
argon2 or bcrypt. No tokens in localStorage.
Use one styling system: <Tailwind or plain CSS>.

The app is for <who it is for>.
The only task in this version: <main task>.

Rules:
- DATABASE_URL from the environment. Migrations for every schema change.
- Server code only talks to the database. Queries include the session user's id.
- REST JSON. Errors are { "error": "sentence" }. No writes on GET.
- Do not add React, Next.js, or MongoDB.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me.
```
