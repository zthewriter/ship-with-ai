# Contributing

Thank you for helping. This project is better with more people checking it.

## How contributions work

1. **Every change is a pull request.** Nobody pushes to `main` directly, including
   collaborators. `main` is protected.
2. **Every pull request is reviewed and approved by the maintainer,
   [@zthewriter](https://github.com/zthewriter), before it is merged.** The
   [CODEOWNERS](.github/CODEOWNERS) file makes that review required.
3. **The maintainer merges.** Contributors do not merge their own pull requests.
4. **Automated checks must pass** before a pull request can be merged.

To contribute: fork the repository, create a branch, make your change, and open a pull
request against `main`. For anything bigger than a fix, open a Discussion first.

## Ways to contribute

- **Fix something.** A wrong statement, a broken link, or an unclear sentence.
- **Share a workflow or skill.** Add it to `workflows/` or `skills/` with a short
  description. Remove keys and personal URLs first.
- **Improve a diagram.** Diagrams are Mermaid, so they are plain text in the page.
- **Write a page.** Open a Discussion first so we can agree on scope.
- **Ask a question.** If something confused you, it confuses others. Start a
  Discussion in **Q&A**.

## Before you open a pull request

1. Keep one idea per page and one diagram per page.
2. Explain why before how. A reader should know when to use something.
3. Use American English and second person ("you"). Write for someone who has never
   coded: explain every technical term the first time, or link the
   [glossary](glossary.md).
4. Make every claim checkable. Link a source for figures, and explain how a
   number was measured.
5. Never commit secrets. Examples read keys from environment variables.

## Page template

```markdown
# Title in sentence case

One or two sentences: what this is and why it matters.

## How it works

The explanation, with one diagram.

## When to use it

## Common mistakes

## Further reading
```

## Review

A maintainer replies to every pull request and Discussion within two business days.
By contributing, you agree that your contribution is licensed under the
[MIT License](LICENSE) for code and [CC BY 4.0](LICENSE-CONTENT) for writing and
diagrams.

Everyone taking part follows the [Code of Conduct](CODE_OF_CONDUCT.md).
