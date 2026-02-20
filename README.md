# AI Skills

A collection of [Claude Code](https://claude.ai/code) skills for better AI-assisted writing and development. Each skill follows the [Agent Skills](https://agentskills.io) open standard, supported natively by Claude Code and Codex CLI.

## Skills

| Skill | Description |
|-------|-------------|
| [remove-ai-slop](skills/remove-ai-slop/) | Detect and eliminate AI writing patterns from text |

## Installation

### Claude Code

```bash
# Personal (all projects)
mkdir -p ~/.claude/skills/remove-ai-slop
cp -r skills/remove-ai-slop/. ~/.claude/skills/remove-ai-slop/

# Project-level (this project only)
mkdir -p .claude/skills/remove-ai-slop
cp -r skills/remove-ai-slop/. .claude/skills/remove-ai-slop/
```

See the [Claude Code skills docs](https://code.claude.com/docs/en/skills) for more detail.

### Codex CLI

```bash
# Personal (all repositories)
mkdir -p ~/.agents/skills/remove-ai-slop
cp -r skills/remove-ai-slop/. ~/.agents/skills/remove-ai-slop/

# Repository-level
mkdir -p .agents/skills/remove-ai-slop
cp -r skills/remove-ai-slop/. .agents/skills/remove-ai-slop/
```

See the [Codex Agent Skills docs](https://developers.openai.com/codex/skills/) for more detail.

## Using a Skill

Once installed, Claude Code will automatically consider invoking skills when relevant. You can also explicitly request a skill:

```
Use the remove-ai-slop skill to clean up this draft.
```

Or via slash command:

```
/remove-ai-slop
```

This follows the [Agent Skills open standard](https://agentskills.io).

## Contributing

Contributions welcome. Before submitting a skill:

1. Read [CLAUDE.md](CLAUDE.md) — it explains the format requirements and editing discipline
2. Each skill needs both `SKILL.md` (machine-readable, Agent Skills-compatible) and `README.md` (human-readable with examples)
3. The `description` field in the YAML frontmatter must start with `"Use when..."` and be ≤ 1024 characters
4. Include before/after examples in the README
5. Open a PR with a brief explanation of what problem the skill solves

## License

MIT
