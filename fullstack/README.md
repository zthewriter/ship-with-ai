# Build a full-stack web app

This track is how you build a website that can go live: pages people use, a server
that enforces the rules, a database that keeps their data, and sign-in. An AI coding
tool can write almost all of the code. These pages are the part you still need, so
you can pick a stack, notice a dangerous mistake, and put the app in production.

This track is web apps. Phone apps and TV apps come later.

## How to use it

1. Read [the shape of a web app](01-the-shape-of-a-web-app.md) so the words mean
   something.
2. Skim the language and framework pages, then use
   [choose your stack](13-choose-your-stack.md).
3. Write that choice down. Connect an
   [MCP server](12-persistent-context-with-mcp.md) that holds the choice, your
   product notes, and the docs for the tools you picked. That memory is what keeps
   later sessions from inventing a second stack.
4. Paste the matching stack prompt from [prompts](../prompts/README.md). It names
   the framework, the language, and why. The shorter workflow prompts in
   [this folder](prompts/README.md) are for review and production later.
5. Before you share the link, walk the
   [production checklist](checklists/production.md).

You direct. The AI types. You decide what "done" means, because a confident wrong
answer still compiles.

## The pages

1. [The shape of a web app](01-the-shape-of-a-web-app.md): browser, server, database,
   and how a click becomes a saved row
2. [HTML, CSS, and JavaScript](02-html-css-and-javascript.md): the three languages
   in the browser
3. [Components, layout, and design](03-components-layout-and-design.md): how screens
   are built and how they should behave
4. [Frontend frameworks](04-frontend-frameworks.md): React, Vue, Angular, Svelte,
   Solid, Qwik, HTMX, Alpine, and Astro
5. [Full-stack frameworks](05-fullstack-frameworks.md): Next.js, Nuxt, SvelteKit,
   React Router, Rails, Laravel, and Django
6. [Backends, including Express](06-backends-and-express.md): when the server is its
   own project
7. [APIs and endpoints](07-apis-and-endpoints.md): URLs, HTTP methods, status codes,
   and JSON
8. [Databases](08-databases.md): Postgres, SQLite, MongoDB, connections, and migrations
9. [Authentication](09-authentication.md): who someone is, and what they may do
10. [Security](10-security.md): the checks that keep a public app from leaking data
11. [From your laptop to production](11-from-laptop-to-production.md): how the pieces
    run for real people
12. [Persistent context with an MCP server](12-persistent-context-with-mcp.md): memory
    for the AI while you build, and for the product if it answers from your content
13. [Choose your stack](13-choose-your-stack.md): a decision page you can hand to
    your AI tool

## Templates and checks

- [Folder layout](templates/folder-layout.md)
- [Environment variable template](templates/env-example.md)
- [Decisions to make before you prompt](checklists/before-you-prompt.md)
- [Production checklist](checklists/production.md)
- [Prompts to paste](prompts/README.md), and the
  [stack prompts](../prompts/README.md) that say which combination and why

One layer at a time: [frontend](../frontend/README.md),
[backend](../backend/README.md), [API](../api/README.md),
[database](../database/README.md).

New word? See the [glossary](../glossary.md).

Git, pull requests, and previews already have a page:
[How shipping works](../docs/05-how-shipping-works.md).
