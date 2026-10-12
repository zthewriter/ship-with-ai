---
name: explain-an-error
description: Reads an error message or log, explains it in plain words, and fixes the underlying cause rather than the symptom. Use when the user pastes an error, a CI check fails, a deploy fails, or something "just stopped working".
---

# Explain an error

## Steps

1. **Find the first error.** Logs often show many errors that are caused by the
   first one. Quote the first real error line.
2. **Explain it in one or two plain sentences**: what went wrong and why, without
   jargon. If a technical term is unavoidable, define it.
3. **Find the cause, not the symptom.** Ask why the error happened until you reach
   something that changed: new code, a missing setting, a different environment.
4. **Say what you will change before changing it**, and why that fixes the cause.
5. **Fix it and prove it.** Re-run whatever produced the error and show it now
   passes.
6. **Prevent it.** If a test or check would have caught this, suggest adding one.

## Report format

- What happened: one sentence.
- Why: one sentence.
- What I changed: a short list.
- How I confirmed it: the command and its result.

## Never

- Never silence an error by deleting the check, catching and ignoring it, or
  skipping a test.
- Never guess at a fix without reading the error first.
- Never paste secrets from a log into your reply.
