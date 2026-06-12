# Melissa's Skills Collection

This repo contains Melissa's custom agent skills for Claude Code.

## Structure

Each skill lives in its own folder with a `SKILL.md` file that defines:
- **Frontmatter** — `name`, `description` (YAML) — used by Claude Code to decide when to invoke the skill
- **Body** — instructions the agent follows when the skill is triggered

## Creating a new skill

1. Create a folder named after the skill (e.g., `my-skill/`)
2. Add a `SKILL.md` with YAML frontmatter (`name`, `description`) and the skill instructions
3. The `description` field is critical — it controls when Claude Code auto-triggers the skill, so make it specific about the user intents it should match

## Conventions

- Skill names use kebab-case
- Keep skills focused — one clear purpose per skill
- The `description` should list concrete trigger phrases/patterns so Claude Code activates the skill at the right time
- Skills can reference CLI tools (e.g., `npx skills`) — include install/usage instructions in the skill body

## Useful commands

- `npx skills find [query]` — search the skills ecosystem
- `npx skills add <package>` — install a community skill
- `npx skills init <name>` — scaffold a new skill
- Browse community skills at https://skills.sh/
