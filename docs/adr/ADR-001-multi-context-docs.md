# ADR-001: Multi-Context Domain Documentation

## Status

Accepted

## Context

The 校园生活服务智能体 project consists of three distinct subsystems:
- **Backend**: SpringBoot multi-module Java application
- **Frontend**: Vue 3 TypeScript mobile-first web app
- **AI Engine**: Python FastAPI + LangChain agent system

Initially, all domain knowledge was centralized in a single `CONTEXT.md` at the repo root. As the project grew, this file became unwieldy:
- Backend developers had to scroll through frontend and AI terminology
- AI-specific concepts (RAG, vector stores, LangGraph) were irrelevant to frontend work
- Changes to one subsystem's glossary risked affecting others

We needed a way to organize domain documentation that:
1. Keeps each subsystem's vocabulary co-located and focused
2. Maintains a shared understanding of cross-cutting concepts
3. Allows AI engineering skills to locate the right context automatically

## Decision

We will adopt a **multi-context** documentation layout:

1. **`CONTEXT-MAP.md`** at repo root: Maps contexts to their `CONTEXT.md` files
2. **`CONTEXT.md`** at repo root: Global glossary for cross-cutting concepts
3. **`backend/CONTEXT.md`**: SpringBoot/Java-specific terminology
4. **`frontend/CONTEXT.md`**: Vue/TypeScript frontend terminology
5. **`ai-engine/CONTEXT.md`**: FastAPI/LangChain AI terminology
6. **`docs/agents/domain.md`**: Consumer rules for AI skills

## Consequences

### Positive
- Each subsystem's glossary is focused and maintainable
- AI skills can locate the right context via `CONTEXT-MAP.md`
- Changes to one context don't risk affecting others
- New team members can read only the contexts relevant to their work

### Negative
- Cross-cutting concepts may need to be documented in multiple places
- `CONTEXT-MAP.md` requires maintenance when adding new contexts
- Slightly more complex navigation for full-stack changes

### Neutral
- Existing `CONTEXT.md` content was split into appropriate contexts
- ADR directory was added to document architectural decisions
