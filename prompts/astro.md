# Astro

Use this for a site people mostly read: marketing pages, docs, a blog. Astro
sends as little JavaScript as it can. An island of React or Vue is allowed for
one widget. A product that is almost all logged-in interaction belongs in
[Next.js](nextjs-typescript.md), [Nuxt](nuxt-vue.md), or
[SvelteKit](sveltekit.md) instead.

## Why this combination

- **Astro** is built for content. The default page is HTML and CSS, which is
  what a reading site needs.
- **TypeScript** is for the islands and the few server endpoints, not a reason
  to turn every page into an app.
- **Postgres** only if the site actually saves something, such as a newsletter
  signup you store yourself. Do not add it for a purely static site.

## Prompt

```text
I want to build a content website, not a logged-in product.

Use Astro with TypeScript, because most of this site is reading and Astro sends
little JavaScript by default. Follow the current Astro docs.
Pages are HTML and CSS. Add an interactive island only for <widget, or "none">.
If you add an island, use <React or Vue or "no framework"> and do not use a
second one.
Use one styling system: <Tailwind or plain CSS>.
Do not convert this project to Next.js, Nuxt, or SvelteKit.

The site is for <who it is for>.
The only job in this version: <main task, such as "publish these pages and a contact form">.

Rules:
- Semantic HTML, one h1 per page, works at 375 pixels wide.
- A form posts to an Astro server endpoint. No secrets in the pages.
- If you store submissions, use Postgres and DATABASE_URL from the environment.
  If you do not store them, do not add a database.
- Do not add auth, a dashboard, GraphQL, or MongoDB unless I asked.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me.
```
