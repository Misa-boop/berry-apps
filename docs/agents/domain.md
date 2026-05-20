# Domain Docs

## Layout

Multi-context: `CONTEXT-MAP.md` at the repo root pointing to per-context `CONTEXT.md` files.

| Context | Path | Description |
|---------|------|-------------|
| Global | `CONTEXT.md` | 全局领域词汇表，跨前后端共享的核心概念 |
| Backend | `backend/CONTEXT.md` | RuoYi SpringBoot 后端领域词汇表 |
| Frontend | `frontend/CONTEXT.md` | Vue 3 前端领域词汇表 |
| AI Engine | `ai-engine/CONTEXT.md` | FastAPI + LangChain AI 引擎领域词汇表 |

## CONTEXT.md

`CONTEXT.md` is a **glossary and nothing else**. It defines the domain language of this project — canonical terms, their meanings, and relationships. It does not contain implementation details, specs, or scratch notes.

Skills that read `CONTEXT.md`:
- `improve-codebase-architecture` — uses glossary to identify deepening opportunities
- `diagnose` — uses glossary to understand error context
- `tdd` — uses glossary to name test fixtures correctly
- `grill-with-docs` — challenges plans against the glossary, updates it inline

## docs/adr/

Architecture Decision Records. Each file follows the ADR format:
- Title, status, context, decision, consequences
- Only created when: hard to reverse, surprising without context, result of a real trade-off

## Consumer rules

1. Read `CONTEXT-MAP.md` first to locate the relevant context
2. Read the specific `CONTEXT.md` for the area you're working on
3. If a term in code conflicts with `CONTEXT.md`, flag it
4. When new terms are resolved during a session, update the relevant `CONTEXT.md` inline
5. Only create ADRs when all three criteria are met (hard to reverse, surprising, real trade-off)
