# Security policy

Ship with AI holds documentation, guides, prompts, skills, and workflows. It runs no service, so a security
problem here is one of the following:

- A secret, key, token, password, or real hostname committed in a page, an
  example, or the history.
- An instruction in a page that would lead a reader, or an AI agent following it,
  to expose data or run something unsafe.

## Report a problem

Email z@zwrites.com with the file path, the line, and what is wrong. Do not open a
public issue for a leaked secret, because an issue makes the secret easier to find.

You get a reply within two business days. A leaked secret is removed from the
current files right away, and its owner is asked to rotate it. Removing a secret
from the history does not make it safe again, so rotation is the fix that counts.

## Supported versions

Corrections go to `main` and to the next release. A published tag is never
rewritten, so a page that cites a tag keeps pointing at the same text.
