# NestJS

Use this when the API is large and more than one person needs a fixed place for
each module. NestJS is a structured TypeScript backend. It is a lot of ceremony
for a five-route app. For a large team that also wants a strict UI, use
[Angular and NestJS](angular-nestjs.md) instead of bolting React on later.

## Why this combination

- **NestJS** gives you modules, a standard layout, and dependency injection, so
  people do not invent a new folder scheme per feature.
- **TypeScript** is required by that structure. It is not optional here.
- **Postgres** remains the database. Nest does not replace it.
- **React** is the website in this prompt because the scenario is "the API is
  the structured part". If you want both sides strict, switch files.

## Prompt

```text
I want a large API that several people will work on, plus a website that calls it.

Use NestJS with TypeScript for the API, because I want a fixed module layout and
I do not want each feature to invent its own structure. Follow the current Nest
docs. Do not collapse this into a single Express file.
Use React with TypeScript for the website. The website never sees DATABASE_URL.
Use Postgres.
Use an httpOnly Secure SameSite session cookie for the website, checked by Nest
guards on private routes. Hash passwords with argon2 or bcrypt. No tokens in
localStorage.
Use Tailwind on the website only.

The app is for <who it is for>.
The only task in this version: <main task>. Build the module for that task only.
Do not scaffold empty modules for ideas I did not name.

Rules:
- Migrations for every schema change. Secrets only on the API.
- Guards on every private route. Queries include the session user's id.
- Validate input with Nest's validation pipe. REST JSON.
- Errors are { "error": "sentence" }. No writes on GET.
- CORS allows only the website's origin.
- Do not add GraphQL, MongoDB, or a second backend framework.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me.
```
