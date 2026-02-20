# AI Skills

A collection of [Claude Code](https://claude.ai/code) skills for better AI-assisted writing and development. Each skill is designed to be invoked via the [superpowers plugin](https://github.com/superpowers-sh/superpowers).

## Skills

| Skill | Description |
|-------|-------------|
| [remove-ai-slop](skills/remove-ai-slop/) | Detect and eliminate AI writing patterns from text |

## Installation

### Prerequisites

These skills require the [superpowers Claude Code plugin](https://github.com/superpowers-sh/superpowers). Install it first.

### Adding Skills

1. Clone this repository or copy the skill directories you want
2. Place them in your superpowers skills directory (see superpowers docs for the exact path)
3. Invoke them in Claude Code with the `Skill` tool or via `/skill-name`

## Using a Skill

Once installed, Claude Code will automatically consider invoking skills when relevant. You can also explicitly request a skill:

```
Use the remove-ai-slop skill to clean up this draft.
```

Or via slash command:

```
/remove-ai-slop
```

## Contributing

Contributions welcome. Before submitting a skill:

1. Read [CLAUDE.md](CLAUDE.md) — it explains the format requirements and editing discipline
2. Each skill needs both `SKILL.md` (machine-readable, superpowers-compatible) and `README.md` (human-readable with examples)
3. The `description` field in the YAML frontmatter must start with `"Use when..."` and be ≤ 1024 characters
4. Include before/after examples in the README
5. Open a PR with a brief explanation of what problem the skill solves

## License

MIT
