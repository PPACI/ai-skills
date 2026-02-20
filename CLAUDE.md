# CLAUDE.md — AI Skills Repository Rules

## RULE: Read Before You Edit

Before editing any skill's `SKILL.md` or `README.md`, you **MUST** first read that skill's `README.md` completely.

This is not optional. Do not skip it.

## Why This Matters

Skills are precision behavioral tools. They encode specific patterns, vocabulary lists, and checklists that must work together coherently. An edit made without reading the full README risks:

- Removing items that are referenced elsewhere in the skill
- Contradicting the skill's underlying logic
- Introducing the very patterns the skill is designed to eliminate
- Breaking compatibility with the superpowers plugin format

Skills fail silently. There is no test suite that catches a skill that's become vague or self-contradictory. The README is your specification — read it.

## Superpowers Format Requirements

Every `SKILL.md` must have YAML frontmatter with exactly two fields:

```yaml
---
name: skill-name
description: Use when [specific triggering condition] to [what it does].
---
```

**Rules:**
- `name`: kebab-case, matches the directory name
- `description`: must start with `"Use when..."` — this is how the superpowers plugin decides when to invoke the skill
- `description` must be ≤ 1024 characters total
- Do **not** summarise the workflow in the description — that belongs in the skill body
- No other frontmatter fields are allowed

## Adding a New Skill

1. Create a new directory under `skills/` named after the skill (kebab-case)
2. Create both `SKILL.md` and `README.md` in that directory
3. Read the existing skills' READMEs for style reference before writing
4. Ensure the `SKILL.md` frontmatter is valid before committing
