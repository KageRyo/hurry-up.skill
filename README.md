# hurry-up

Move faster. Avoid overengineering.

[![MIT License](https://img.shields.io/github/license/KageRyo/hurry-up.skill)](LICENSE)
[![Last commit](https://img.shields.io/github/last-commit/KageRyo/hurry-up.skill)](https://github.com/KageRyo/hurry-up.skill/commits/main/)

`hurry-up` is a small behavior skill for AI coding agents. It keeps work focused on the smallest correct change, favors existing project patterns, limits exploration and validation to what the task needs, and leaves unrelated issues for a brief note.

## Use it

Copy this repository's root `SKILL.md` into the destination supported by your coding agent:

| Agent | Setup |
| --- | --- |
| [Codex](https://developers.openai.com/codex/skills/) | `.agents/skills/hurry-up/SKILL.md` in your project. Invoke with `$hurry-up` or let Codex select it when relevant. |
| [Claude Code](https://code.claude.com/docs/en/skills) | `.claude/skills/hurry-up/SKILL.md` in your project. Invoke with `/hurry-up` or let Claude Code load it when relevant. |
| [Claude.ai](https://code.claude.com/docs/en/skills) | Upload the skill folder through Claude's Skills settings, or paste the instructions into a [Project](https://support.anthropic.com/en/articles/9517075-what-are-projects). |
| [Grok Build](https://docs.x.ai/build/features/skills-plugins-marketplaces) | `.grok/skills/hurry-up/SKILL.md` in your project. Invoke with `/hurry-up` or let Grok load it when relevant. |
| [Cursor](https://docs.cursor.com/context/rules-for-ai) | Copy the instructions into `.cursor/rules/hurry-up.mdc` or the root `AGENTS.md`. Cursor applies those rule files; it does not discover this repository's root `SKILL.md` as a skill. |
| DeepSeek | DeepSeek is a model provider rather than a shared skill loader. In a coding client, add the instructions to its supported repository rules; with the API, include them in the system prompt. The [Chat Completions API](https://api-docs.deepseek.com/api/create-chat-completion/) supports system messages. |

For example, from your project root, replace the source path with the location of this clone:

```sh
mkdir -p .agents/skills/hurry-up
cp /path/to/hurry-up.skill/SKILL.md .agents/skills/hurry-up/SKILL.md
```

For Cursor, start `.cursor/rules/hurry-up.mdc` with this rule metadata, then paste the instructions from `SKILL.md` below it:

```md
---
description: Keep coding tasks focused and avoid overengineering.
alwaysApply: true
---
```

Other agents can use the same instructions through their native skill directory, repository instruction file, custom rules, or system/developer prompt. These are usage paths for the plain Markdown instructions, not claims of an official integration or automatic discovery in every product. See each agent's documentation for its current loading rules.

## License

MIT. See [LICENSE](LICENSE).
