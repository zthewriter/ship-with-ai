# Agent skills

A *skill* is a short instruction file that teaches your AI coding tool how to do a
task the right way, every time, without you having to explain it again. Each folder
here holds one `SKILL.md` file.

| Skill | Teaches your AI tool to |
|---|---|
| [connect-mcp-server](connect-mcp-server/SKILL.md) | Add an MCP server to your AI tool and confirm it works |
| [add-tests](add-tests/SKILL.md) | Add simple tests to your project and prove they catch mistakes |
| [pre-deploy-check](pre-deploy-check/SKILL.md) | Check your project before it goes live |
| [explain-an-error](explain-an-error/SKILL.md) | Read an error, explain it in plain words, then fix the cause |

## How to install a skill

Copy the skill's folder into the skills folder your tool reads:

| Tool | Folder in your project |
|---|---|
| Cursor | `.cursor/skills/` |
| Claude Code | `.claude/skills/` |
| Codex | `.agents/skills/` |

For example, `.cursor/skills/pre-deploy-check/SKILL.md`. Your tool picks it up when a
task matches the skill's description. You can also ask for one by name: "use the
pre-deploy-check skill".

Check your tool's documentation if the folder has moved; these locations change.

## Write your own

A skill is a Markdown file with a short header:

```markdown
---
name: my-skill
description: What it does and when to use it, in one or two sentences.
---

# My skill

Steps your AI tool should follow.
```

The description matters most, because it is how your tool decides to use the skill.
Share good ones with a pull request.
