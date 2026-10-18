# Versioning

Ship with AI uses semantic versioning for content. A version number is
`MAJOR.MINOR.PATCH`, and each part says what a reader who cites this repository
can rely on.

The following table lists what each kind of change does to the version:

| Change | Version part | Example |
|---|---|---|
| A wording fix, a corrected link, or a clarified sentence | Patch | `1.0.0` to `1.0.1` |
| Adding a guide, a prompt, a skill, or a workflow | Minor | `1.0.0` to `1.1.0` |
| Moving, renaming, or removing a guide, a prompt, a skill, or a workflow | Major | `1.0.0` to `2.0.0` |

## What a major version keeps

A major version keeps a stub at every old path. The stub holds one sentence and a
link to the new path, so a link in an article or a blog post still leads
somewhere. Stubs are removed only at the next major version.

## Headings

A link can point at a heading, so a heading's text is part of what a citation
relies on. A change that renames a heading keeps the old anchor with an explicit
`<a id="old-anchor"></a>` above the new heading.

## How to cite a version

Cite a tag, not `main`. A link such as
`https://github.com/zthewriter/ship-with-ai/blob/v1.0.0/README.md` always shows the text
that was released, while `main` keeps changing.

Each release is recorded in [CHANGELOG.md](CHANGELOG.md).
