# Production checklist

Walk this on a preview deploy before you point a domain at the app. A green build
does not mean a stranger can use it safely.

## Product

- [ ] The decisions note matches the code: framework, database, auth, error shape
- [ ] The main task works on a phone-width window and on a laptop
- [ ] Empty states and errors use sentences, not raw codes
- [ ] Forms have labels, and you can complete one with the keyboard

## Access

- [ ] Sign up, sign in, and sign out work
- [ ] Passwords are hashed. You never see a plaintext password in the database or
      the logs
- [ ] A signed-out request to a private endpoint gets `401`
- [ ] User A cannot read or edit user B's row by changing an id
- [ ] Admin-only actions check the role on the server

## Data

- [ ] `DATABASE_URL` is an environment variable, different in preview and production
- [ ] Schema changes are migrations, and they run on release
- [ ] Production backups are on, and you know where the restore button is
- [ ] The database is not open to the whole internet

## Secrets and exposure

- [ ] `.env` is gitignored. `.env.example` has names only
- [ ] No secret uses a "public" or "expose to browser" prefix
- [ ] The live site is HTTPS
- [ ] A thrown error does not show a stack trace to the visitor
- [ ] Sign-in is rate-limited

## Release

- [ ] The pull request was clicked through on a preview URL
- [ ] You know how to redeploy the previous version
- [ ] The [MCP server](../12-persistent-context-with-mcp.md) still has the current
      decisions, and private notes are not in a server customers can query

## After it is live

- [ ] You did the main task once on production, with a real account you can delete
- [ ] Logs show that request without a token or password in them

Details live in [security](../10-security.md),
[authentication](../09-authentication.md), and
[from your laptop to production](../11-from-laptop-to-production.md).
