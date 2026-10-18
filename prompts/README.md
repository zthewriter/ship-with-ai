# Prompts

Paste one of these into your AI coding tool when you want it to build. Each
prompt names the framework, the language, and why you picked them. The "why" is
for the tool, not only for you. Without it, the next chat will "improve" the
stack by switching to whatever it saw last.

Replace the angle brackets. Do not paste real passwords, API keys, or database
URLs into the chat.

Connect an [MCP server](../fullstack/12-persistent-context-with-mcp.md) with this
repository and your decisions note before you paste. The prompts tell the tool
to search it.

The workflow prompts in [fullstack/prompts](../fullstack/prompts/README.md) are
for later in the build (review, production). Start here, with the combination.

## Which combination

| You are building | Use | Why this, and not the neighbor |
| --- | --- | --- |
| A website people log into, and you have no language yet | [Next.js and TypeScript](nextjs-typescript.md) | One project for screens and server. The most accurate examples for an AI. |
| The same app, and you want templates that look like HTML | [Nuxt and Vue](nuxt-vue.md) | Vue's templates stay close to HTML. Nuxt adds the server. |
| The same app, and you want small components | [SvelteKit](sveltekit.md) | Less boilerplate. You must pin the SvelteKit docs, because the AI has seen fewer of these than React. |
| The same app, and you want the server to own each screen's data | [React Router](react-router.md) | Forms post to the server. This is the current home of Remix. |
| Mostly articles or a marketing site | [Astro](astro.md) | Sends very little JavaScript. A logged-in product does not belong here. |
| Forms and pages, little JavaScript, and you want Ruby | [HTMX and Rails](htmx-rails.md) | The server returns HTML. Rails already knows accounts and tables. |
| Forms and pages, and you want Python | [HTMX and Django](htmx-django.md) | Same HTML style, in the Python stack. |
| Forms and pages, and you want PHP | [HTMX and Laravel](htmx-laravel.md) | Same HTML style, in the PHP stack. |
| A full app, and you already work in Python | [Django](django.md) | Admin, database, and auth in one opinionated framework. |
| A full app, and you already work in PHP | [Laravel](laravel.md) | One style for pages, data, mail, and jobs. |
| A full app, and you already work in Ruby | [Rails](rails.md) | Conventions do a lot of the choosing for you. |
| A second client will call the same rules, and you want the most examples | [Express and TypeScript](express-typescript.md) | A separate API. React on the website. |
| A separate API, and you want each route to declare its input | [Fastify and TypeScript](fastify-typescript.md) | Like Express, with validation built into the route. |
| A small separate API that may run on more than one kind of host | [Hono and TypeScript](hono.md) | A short router. The UI stays a TypeScript frontend. |
| A large API that several people will own | [NestJS](nestjs.md) | A fixed place for every module. Too much ceremony for five routes. |
| A large team wants one strict style on the screens and the API | [Angular and NestJS](angular-nestjs.md) | Both are opinionated TypeScript. Structure is the perk. |
| A separate API, and you want a small language and one deployable file | [Go](go.md) | Simple servers, a single binary. The UI is still Next.js or HTMX. |
| A separate API, and you chose Rust on purpose | [Rust and Axum](rust-axum.md) | The compiler catches a class of bugs. A first login app is slower here. Read that page before you paste. |
| Fine-grained updates are the actual problem | [Solid](solid.md) | Not a first app. The page says when the prompt is allowed. |
| The first load must not download the whole app | [Qwik](qwik.md) | Not a first app. Same warning. |

Language background: [backend languages](../backend/languages.md), including the
Go and Rust tradeoffs. Screen language: [frontend languages](../frontend/languages.md).

## After you paste

If the tool suggests a different framework, database, or language, reply with:

```text
No. Keep the stack in the prompt. The reason is in the prompt. Do not switch.
```

Then keep going on the main task only.
