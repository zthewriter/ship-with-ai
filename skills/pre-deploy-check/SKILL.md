---
name: pre-deploy-check
description: Checks a project before it is deployed to production and reports anything that would break or leak. Use before deploying, merging to main, or when the user asks if something is safe to ship.
---

# Pre-deploy check

Run each check and report a short pass or fail list in plain words. Stop and explain
before deploying if anything fails.

## Checks

1. **Changes are on a branch with a pull request**, not pushed straight to main.
2. **Tests pass.** Run the project's test command.
3. **The app builds.** Run the project's build command.
4. **No secrets in the code.** Search the changes for API keys, passwords, and
   tokens. Confirm `.env` is listed in `.gitignore`.
5. **Settings exist online.** List every environment variable the code reads, and
   ask the user to confirm each one is set in the host's settings.
6. **No local addresses.** Search for `localhost` and `127.0.0.1` in code that runs
   online.
7. **Database changes are safe.** If the change touches the database, explain what
   will change and whether any data could be lost. Ask before running anything that
   drops or rebuilds a table.
8. **The preview works.** If the host gives a preview link, ask the user to try the
   main flow there.

## After deploying

Open the live app and try the one thing this change was for. Then check the host's
logs for new errors in the first few minutes.

## Never

- Never deploy with a failing check without the user's explicit go-ahead.
- Never print the value of a secret while checking for it.
