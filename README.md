# skills

Agent skills by [samuhvarta](https://github.com/samuhvarta). Each skill is a folder under [`skills/`](./skills) with a `SKILL.md` file, and follows the [Agent Skills specification](https://agentskills.io/).

## Install

Install with the [`skills`](https://github.com/vercel-labs/skills) CLI:

```sh
# Pick skills and agents interactively
npx skills@latest add samuhvarta/skills

# List the skills in this repo
npx skills@latest add samuhvarta/skills --list

# Install one skill globally
npx skills@latest add samuhvarta/skills --skill tech-writer -g
```

## Skills

| Skill | Description |
|---|---|
| [tech-writer](./skills/tech-writer/SKILL.md) | Writes explanations and documents in ASD-STE100 Simplified Technical English, with Mermaid diagrams. Output is Markdown by default, or interactive HTML on request. |

## Add a skill

1. Create `skills/<name>/SKILL.md`. The `name` field in the frontmatter must match the folder name.
2. Add a row to the [Skills](#skills) table.
