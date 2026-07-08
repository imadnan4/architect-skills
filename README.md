# Architect Skills

[![skills.sh](https://skills.sh/b/imadnan4/architect-skills)](https://skills.sh/imadnan4/architect-skills)

A modular, production-grade **system-design skill pack** that turns any coding agent
(OpenCode, Claude Code, Codex, Cursor, Gemini CLI, Copilot, Windsurf, Cline) into a
**Staff/Principal Software Architect**.

Built on the open **Agent Skills** standard: each capability is its own skill folder with a
`SKILL.md`. An agent reads this `README.md` (cheap), then loads **only** the skill whose
description matches the task — so context is never bloated.

## How an agent uses this pack

1. Read this `README.md` to discover available skills.
2. When a task matches a skill's `description` / `when_to_use`, Read that skill's `SKILL.md`.
3. Apply its Decision Tree, Anti-Patterns, and Architecture Prompts.
4. Before merging, run `skills/architecture-review/SKILL.md`.

Do **not** load every skill at once.

## Skills

| Skill | Path | Use when… |
|---|---|---|
| Architecture Principles (brain) | `skills/architecture-principles/SKILL.md` | thinking before any code; requirements-first pipeline; golden rules |
| Architecture Decision Framework | `skills/architecture-decision-framework/SKILL.md` | choosing architecture/tech from requirements; monolith vs microservices; trade-offs |
| Database Intelligence | `skills/database-intelligence/SKILL.md` | choosing/modeling databases; SQL vs NoSQL; Redis/ClickHouse/vector/object storage |
| API & Domain Architecture | `skills/api-domain-architecture/SKILL.md` | REST/GraphQL/gRPC/WebSocket; commands vs resources; auth; idempotency; versioning |
| Scalability & Distributed Systems | `skills/scalability-distributed-systems/SKILL.md` | scaling; caching; queues; event-driven; CQRS/saga/outbox; circuit breakers |
| AI System Architecture | `skills/ai-system-architecture/SKILL.md` | agents; RAG; memory; tool calling; MCP; model routing; guardrails; evaluation |
| Context Engineering | `skills/context-engineering/SKILL.md` | repo structure for AI agents; AGENTS.md/CLAUDE.md; ADRs; context budgets |
| Security by Design | `skills/security-by-design/SKILL.md` | auth; secrets; encryption; injection; multi-tenancy; prompt-injection; compliance |
| Codebase Architecture | `skills/codebase-architecture/SKILL.md` | organizing code by domain; monorepos; layering; module independence; smells |
| Production Engineering | `skills/production-engineering/SKILL.md` | SLOs; health checks; observability; alerts; feature flags; rollback; incident response |
| Architecture Review Engine | `skills/architecture-review/SKILL.md` | pre-merge review; scorecard; challenging design before approval |

## Structure

- `skills/<name>/SKILL.md` — each capability is a self-contained skill (Agent Skills standard).
- Supporting material (artifact templates, checklists, decision trees, playbooks, reference
  architectures) lives *inside* a skill's `references/` when needed, so it is loaded on demand,
  never eagerly.

## Install into a project

The easiest way to use these skills is with the [skills.sh](https://www.skills.sh) CLI:

```bash
npx skills add imadnan4/architect-skills
```

This installs all 11 skills into your project (under `skills/`), where agents like OpenCode,
Claude Code, Codex, Cursor, Gemini CLI, and Copilot can discover and load them on demand.

Alternatively, copy the `skills/` directory manually into your repo, or add this repo as a skill
source. Then tell your agent (root `AGENTS.md` / `CLAUDE.md` / `GEMINI.md`):

> Before implementing or making architecture decisions, read `README.md` in the architect skill
> pack to find the matching skill, then read that skill's `SKILL.md`.

## Contributing / roadmap

Skills follow this structure: `skills/<name>/SKILL.md` with `name` (lowercase-hyphen, = folder),
a trigger-rich `description`, optional `when_to_use`, and a body under ~5K tokens. Roadmap:
Observability, Infrastructure/Cloud, Frontend, Testing, Code Review Intelligence, Performance,
Reference Architectures — each added as a new `skills/<name>/SKILL.md` and registered in this index.
