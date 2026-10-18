# React Router

Use this for a logged-in website when you want each screen to load its data on
the server and each form to post to the server. React Router's framework mode is
the current home of Remix. If a tutorial says Remix, this is the stack it means
now.

## Why this combination

- **React Router** treats a page as a server load plus a form post. You do less
  client-side fetching, and a failed save has a place to land.
- **TypeScript** names the loader data so the screen cannot invent fields.
- **Postgres** holds the accounts. The server, not the browser, is the only
  thing that talks to it.

Skip this if you want the largest pile of examples. That pile is
[Next.js](nextjs-typescript.md).

## Prompt

```text
I want to build a web app people can log into.

Use React Router in framework mode with React and TypeScript, because I want
the server to load each screen's data and I want forms to post to the server.
This is the current home of Remix. Follow the current React Router framework
docs. Do not switch to Next.js or to the old Remix package names.
Use TypeScript so loader and action data have named shapes.
Use Postgres, because accounts and private rows are tables.
Use a session cookie that is httpOnly, Secure, and SameSite. Hash passwords
with argon2 or bcrypt. No tokens in localStorage.
Use one styling system: <Tailwind or plain CSS>.

The app is for <who it is for>.
The only task in this version: <main task>.

Rules:
- DATABASE_URL from the environment. Migrations for every schema change.
- Every private query includes the signed-in user's id from the session.
- Secrets stay on the server. .env.example lists names with empty values.
- Errors are { "error": "sentence" }. No writes on GET.
- Semantic HTML, labeled inputs, layout works at 375 pixels wide.
- Do not add GraphQL, MongoDB, or a second UI framework.
- Search the MCP server before inventing a name. If my notes disagree with this
  prompt, stop and tell me.
```
