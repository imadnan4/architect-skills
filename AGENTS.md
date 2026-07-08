# Architect Skill Pack — Agent Instruction

Before implementing, scaffolding, or making any architecture/technology decision, consult the
Architect Skill Pack in this repo:

1. Read `README.md` to discover the available skills.
2. When the task matches a skill's `description` / `when_to_use`, Read that skill's `SKILL.md`
   (e.g. `skills/database-intelligence/SKILL.md`).
3. Apply its Decision Tree, Anti-Patterns, and Architecture Prompts.
4. Before merging code, run `skills/architecture-review/SKILL.md` (review engine + scorecard).

Load only the skill relevant to the current task. Do not load every skill at once — this keeps the
context window small.

If no specific chapter matches, start from `skills/architecture-principles/SKILL.md` (the brain:
requirements-first thinking pipeline and golden rules).

Artifact starters (PRD/ADR/ERD/API) and verification checklists live inline in the relevant skills
(e.g. `architecture-review`); load them on demand rather than keeping separate top-level folders.
