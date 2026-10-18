---
name: add-tests
description: Adds simple automated tests to a project and proves each one catches a real mistake. Use when the user asks for tests, before changing code that handles money, logins, or data deletion, or after fixing a bug.
---

# Add tests

The user may not be a developer. Explain what each test protects in one plain
sentence.

## Steps

1. Use the test tool the project already has. Look in `package.json` scripts for
   `test`. If there is none, suggest [Vitest](https://vitest.dev/) for JavaScript or
   TypeScript projects and [pytest](https://docs.pytest.org/) for Python, and ask
   before installing.
2. Pick what to test first, in this order:
   - Anything that charges money or changes billing.
   - Anything that controls who can see or change data.
   - Anything that deletes data.
   - The bug just fixed, if there is one.
3. Write a small number of tests that check behavior a user would notice, not
   internal details.
4. **Prove each test can fail.** Temporarily break the code it protects, run the
   test, and confirm it fails. Then restore the code and confirm it passes. A test
   that passes against broken code protects nothing.
5. Run the full test command and show the user the result.
6. If the project has CI, make sure the test command runs there too.

## Report

For each test: what it protects in plain words, and confirmation that it failed when
the code was broken.

## Never

- Never weaken or delete a failing test to make the suite pass without telling the
  user why.
- Never let tests call real payment, email, or production database services.
