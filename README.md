# AI Agent Skills

**Production-ready, modular skills for AI agents** — Claude, Cursor, Grok, and beyond.

A curated collection of high-quality agent skills focused on process automation, workflow orchestration, and applied AI. Built by [Ali Boussecsou](https://github.com/boussecsou).

---

## Architecture

```text
skills/
├── automation/          # Workflows, process automation, RPA-style tasks
├── productivity/        # Personal & team productivity
├── data-analysis/       # Data cleaning, analysis, reporting
├── content/             # Writing, editing, content creation
├── development/         # Coding helpers, code review, scaffolding
└── integrations/        # Tool & service integrations (n8n, APIs, etc.)

templates/
└── skill-template/      # Starter template for new skills
```

Each skill lives in its own folder and must contain a `SKILL.md` file:

```text
skills/<category>/<skill-name>/
├── SKILL.md             # Required — frontmatter + instructions
├── scripts/             # Optional — executable helpers
├── references/          # Optional — docs loaded on demand
└── assets/              # Optional — templates, images, etc.
```

This structure is:
- **Easy to navigate** — categories group related skills
- **Scalable** — just add a new folder under the right category
- **Evolutive** — new categories can be added at any time

---

## Categories

| Category | Purpose |
|----------|---------|
| `automation` | Process automation, workflows, scheduled tasks |
| `productivity` | Daily productivity, note-taking, planning |
| `data-analysis` | Data processing, analysis, visualization, reports |
| `content` | Writing, rewriting, content strategy |
| `development` | Coding assistance, scaffolding, reviews |
| `integrations` | Connecting external tools & APIs |

---

## Skills Index

| Skill | Category | Description |
|-------|----------|-------------|
| *None yet* | — | Skills will appear here as they are added. |

---

## How to Add a New Skill

1. Choose (or create) the right category under `skills/`.
2. Copy the template:
   ```bash
   cp -r templates/skill-template skills/<category>/<your-skill-name>
   ```
3. Edit `SKILL.md`:
   - Set `name` (must match the folder name, kebab-case)
   - Write a precise `description` (this is what the agent sees first)
   - Fill the instructions body
4. Update the **Skills Index** table in this README.
5. Commit and push.

### Skill Format (quick reference)

```yaml
---
name: my-skill
description: What it does and when to use it. Include trigger words.
---

# Instructions go here (imperative style)
```

Guidelines:
- `name` must equal the folder name
- Keep the description under ~1024 characters and make it trigger-rich
- Prefer progressive disclosure — put long reference material in `references/`

---

## Usage

1. Clone this repository or download the skill folders you need.
2. Place them in your agent’s skills directory (examples):
   - Claude / Cursor style: `.claude/skills/` or project-level skills folder
   - Other agents: follow their skill discovery path
3. The agent discovers skills via the `description` field and loads full instructions on demand.

---

## License

This repository is licensed under the [MIT License](LICENSE).

---

## Author

**Ali Boussecsou**  
Process Automation & Applied AI  
[GitHub](https://github.com/boussecsou) · Morocco
