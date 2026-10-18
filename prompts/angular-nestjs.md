# Angular and NestJS

Use this when a large team wants one strict TypeScript style on the screens and
on the API. Angular is the frontend. NestJS is the backend. Both are
opinionated, which is the point. A solo first app should use
[Next.js](nextjs-typescript.md) instead. The ceremony here pays off when several
people would otherwise invent two different structures.

## Why this combination

- **Angular** includes routing, forms, and HTTP, and it expects TypeScript. A
  large UI has one official way to do those things.
- **NestJS** was shaped by similar ideas on the server, so the words match:
  modules, injection, a place for each feature.
- **Postgres** holds the data. Neither framework is a database.
- **TypeScript on both sides** means a renamed field can fail a build instead of
  failing in production. Share types on purpose. Do not copy them by hand into
  a third language.

## Prompt

```text
I want a web app people can log into, built so a team can extend it without
inventing a new structure each time.

Use Angular with TypeScript for the website, because I want the official Angular
way to do routing, forms, and HTTP. Follow the current Angular docs. Do not add
React or Vue.
Use NestJS with TypeScript for the API, because I want the same kind of
structure on the server: modules and a fixed layout. Follow the current Nest
docs.
Use Postgres. Do not use MongoDB.
Use an httpOnly Secure SameSite session cookie. Nest guards protect private
routes. Hash passwords with argon2 or bcrypt. No tokens in localStorage.
The Angular app calls the API. It never receives DATABASE_URL.

The app is for <who it is for>.
The only task in this version: <main task>. One Angular feature and one Nest
module for that task. Do not generate empty modules for a roadmap.

Rules:
- Migrations for every schema change. Secrets only on the API.
- Queries include the session user's id. Validate input on the API.
- REST JSON. Errors are { "error": "sentence" }. No writes on GET.
- CORS allows only the Angular app's origin.
- Semantic HTML and labeled inputs. Layout works at 375 pixels wide.
- Do not add GraphQL or a third framework.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me.
```
