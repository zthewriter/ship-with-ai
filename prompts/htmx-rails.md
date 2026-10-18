# HTMX and Rails

Use this when the app is forms and pages, you want very little JavaScript, and
you want Ruby. The server renders the new piece of HTML. HTMX swaps it in. Rails
already has a place for accounts, tables, and sessions.

Skip it for a live board or a complex editor. Those fight this model. Use
[Next.js](nextjs-typescript.md) or [Rails](rails.md) with its own frontend tools
only if you have already chosen that path on purpose.

## Why this combination

- **HTMX** keeps behavior in HTML attributes. You can see the request on the
  element.
- **Rails** is convention-heavy, which is a perk when an AI is told to follow
  the official guides and a problem when it does not.
- **Ruby** is the language Rails expects. Do not add a Node server beside it.

## Prompt

```text
I want to build a web app people can log into, made of pages and forms.

Use Ruby on Rails, because I want one Ruby framework with conventions for
database tables, sessions, and server-rendered HTML. Follow the current Rails
guides. Do not add a Node.js server.
Use HTMX, because interactions should return a snippet of HTML from the server
instead of a separate JavaScript frontend. Do not add React, Vue, or Angular.
Use Postgres, because accounts and private records are tables.
Use Rails' session cookie. HttpOnly, Secure, SameSite. Hash passwords the way
current Rails does. No tokens in localStorage or in JavaScript.

The app is for <who it is for>.
The only task in this version: <main task>.

Rules:
- DATABASE_URL or Rails credentials from the environment, never committed.
- Migrations for every schema change.
- Every private query is scoped to the signed-in user.
- No secrets in HTML. No writes on GET.
- Semantic HTML, labeled inputs, layout works at 375 pixels wide.
- Do not add MongoDB, GraphQL, or a second language.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me.
```
