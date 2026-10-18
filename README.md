# Ship with AI

Plain-language guides for vibe coders. Choose a web stack, tell an AI why you
chose it, and ship a full-stack app. The same repo covers RAG, persistent
context, and what to do when something breaks.

No jargon without an explanation. No assumed computer science degree.

> Writing docs or working in DevRel? See
> [Context for AI](https://github.com/zthewriter/context-for-ai).

## Build a web app

How a browser, an API, and a database fit together, how to choose among React,
Vue, Angular, Next.js, Express, and the rest, and the checks that make an app
safe to put in front of real people.

Start at [Build a full-stack web app](fullstack/README.md). Web only. Phone and
TV apps come later.

### Look up one layer

- [Frontend](frontend/README.md): HTML, CSS, JavaScript, components, and handlers
- [Backend](backend/README.md): server handlers, and languages from TypeScript through Go and Rust
- [API](api/README.md): methods, endpoints, and which style to ask for
- [Database](database/README.md): tables, queries, and connections

When you know the combination, paste a prompt from
[prompts](prompts/README.md). Each one names the framework, the language, and
why, so the next chat does not switch stacks.

## Give an AI a memory

1. [What RAG is, in one page](docs/01-what-is-rag.md)
2. [Why your AI keeps forgetting, and how to fix it](docs/02-why-context-matters.md)
3. [The starter architecture](docs/03-starter-architecture.md): a simple, no-code
   setup that gives your AI assistant a memory of your content
4. [Build your first AI assistant with n8n](docs/04-build-your-first-assistant.md),
   step by step, with a [workflow you can import](workflows/)

## Ship it

1. [How shipping works](docs/05-how-shipping-works.md): git, pull requests, tests, and
   deploys, explained with pictures
2. [Agent skills](skills/): ready-made instructions that teach your AI coding tool to
   test, deploy, and debug the right way
3. [Rescue guides](docs/06-rescue-guides.md): what to do when it breaks

## Words you will see

New term? Check the [glossary](glossary.md).

## For writers

If you write documentation for AI rather than build with it, two sibling repos
are for you: [Context for AI](https://github.com/zthewriter/context-for-ai) has
the templates, and the
[Harness Engineering Cookbook](https://github.com/zthewriter/harness-engineering-cookbook)
shows how to deliver your docs to AI tools.

## Link to a stable version

To link to a page or a heading here, put a release tag such as `v1.0.0` in the
URL instead of `main`. Tagged text never changes, moved files keep a stub, and
renamed headings keep their old anchor, as the
[versioning policy](VERSIONING.md) describes. To cite the repository itself, use
[CITATION.cff](CITATION.cff).

## Contributing

Questions are contributions here. If something confused you, it will confuse the next
person, so ask in [Discussions](https://github.com/zthewriter/ship-with-ai/discussions).
See [CONTRIBUTING.md](CONTRIBUTING.md) for more.

## License

Writing and diagrams are released under [CC BY 4.0](LICENSE-CONTENT). Workflows,
skills, and code are released under the [MIT License](LICENSE).

## Maintained by

[Zair Rogelio](https://github.com/zthewriter), a technical writer. Disclosure: I also
build [MCP Studio](https://appatools.com/mcp-studio?utm_source=github&utm_medium=oss&utm_campaign=ship-with-ai&utm_content=readme)
at Appa Tools, which the starter tutorial offers as one option. Every guide names
alternatives, and nothing here requires it.
