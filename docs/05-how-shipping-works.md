# How shipping works

When developers say "ship it", they mean a chain of steps that gets your change from
your computer to the people using your app, safely. AI coding tools will do most of
these steps for you, but you need to know what they are so you can tell when
something is wrong.

## The whole picture

```mermaid
flowchart LR
  accTitle: How a change ships
  accDescr: You edit on your computer, commit a snapshot, open a pull request, CI checks it, you try a preview, merge it, and it goes live in a production deploy.
  E[1. Edit on your computer] --> C[2. Save a snapshot: commit]
  C --> B[3. Propose it: pull request]
  B --> T[4. Robots check it: CI]
  T --> P[5. Try it: preview]
  P --> M[6. Accept it: merge]
  M --> D[7. Go live: production deploy]
```

## Each step in plain words

**1. Edit.** You, or your AI tool, change files on your computer. Nothing anyone else
sees has changed yet.

**2. Commit.** A commit is a saved snapshot with a note about what changed. *Git* is
the tool that keeps these snapshots, so you can always go back.

**3. Pull request (PR).** You put your changes on a separate copy, called a *branch*,
and ask to add them to the main version. A PR is a page that shows exactly what
changed. It is where mistakes get caught.

**4. CI (continuous integration).** Robots automatically run checks on your PR: do the
tests pass, does the app build, are there leaked passwords. A red X means stop and
read why.

**5. Preview.** Hosts like Vercel and Netlify build a private copy of your app for
each PR, with its own link. Click around it before anyone else sees the change.

**6. Merge.** You accept the PR into the main version.

**7. Production deploy.** The main version goes live for real users. Many hosts do
this automatically after a merge.

## Why bother with all this?

Because the alternative is editing the live app directly, and the first time your AI
tool deletes something important, there is no undo. Every step above is a chance to
catch a mistake before your users do.

## What to ask your AI coding tool

- "Create a new branch for this change and commit with a clear message."
- "Open a pull request and summarize what changed."
- "The CI check failed. Read the log and explain the error in plain words before
  fixing it."
- "Do not push to main directly."

The [agent skills](../skills/) teach your AI tool to do this without being asked.

## Next

[Rescue guides](06-rescue-guides.md)
