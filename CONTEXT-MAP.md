# Context Map

This repository uses **multi-context** domain documentation. Each major subsystem has its own `CONTEXT.md` file.

## Contexts

### Global (`CONTEXT.md`)
跨前后端共享的核心领域概念。适用于涉及多个子系统的变更。

### Backend (`backend/CONTEXT.md`)
RuoYi SpringBoot 后端领域词汇表。适用于：
- 若依框架模块开发
- 数据库模型变更
- API 接口变更
- 业务规则实现

### Frontend (`frontend/CONTEXT.md`)
Vue 3 前端领域词汇表。适用于：
- 页面组件开发
- 前端状态管理
- 用户交互流程
- 移动端适配

### AI Engine (`ai-engine/CONTEXT.md`)
FastAPI + LangChain AI 引擎领域词汇表。适用于：
- 智能体工具开发
- RAG 知识库维护
- 对话流程编排
- LLM 调用优化

## Usage

当使用工程技能（如 `improve-codebase-architecture`、`diagnose`、`tdd`）时：
1. 根据修改范围定位相关上下文
2. 读取对应的 `CONTEXT.md` 理解领域语言
3. 如涉及多个子系统，依次读取相关上下文
