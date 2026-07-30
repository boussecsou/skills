# AI Agent Skills

**Production-ready, modular skills for AI agents** — Claude, Cursor, Grok, and beyond.

A curated collection of high-quality agent skills focused on process automation, workflow orchestration, and applied AI. Built by [Ali Boussecsou](https://github.com/boussecsou).

---

## What are Agent Skills?

Skills are modular instruction packages that extend an AI agent’s capabilities. Each skill contains:

- A clear description (triggers when the skill should activate)
- Precise instructions the agent loads on demand
- Optional scripts, references, and assets

They follow the [agentskills.io](https://agentskills.io) specification and work across compatible agents.

---

## Repository Structure

```text
skills/
├── skill-name/
│   ├── SKILL.md          # Required — frontmatter + instructions
│   ├── scripts/          # Optional — executable helpers
│   ├── references/       # Optional — docs loaded on demand
│   └── assets/           # Optional — templates, images, etc.
└── ...
```

---

## Skills

| Skill | Description |
|-------|-------------|
| *Coming soon* | Skills will be listed here as they are added. |

---

## Usage

1. Clone or download the skill folder you need.
2. Place it in your agent’s skills directory (e.g. `.claude/skills/`, `.cursor/skills/`, or the equivalent for your agent).
3. The agent will automatically discover the skill via its `description` and load the full instructions when relevant.

---

## Creating a New Skill

Follow the standard skill format:

```yaml
---
name: my-skill
description: What this skill does and when to use it. Include trigger words and scenarios.
---

# Instructions

Write clear, imperative instructions. Keep them concise and focused on knowledge the model does not already have.
```

Guidelines:
- `name` must match the folder name (kebab-case)
- Description is the only thing visible before the skill is loaded — make it count
- Prefer progressive disclosure: keep `SKILL.md` lean and move long content to `references/`

---

## License

This repository is licensed under the [MIT License](LICENSE).

---

## Author

**Ali Boussecsou**  
Process Automation & Applied AI  
[GitHub](https://github.com/boussecsou) · Morocco
