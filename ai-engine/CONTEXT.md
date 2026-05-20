# AI Engine 领域词汇表

## 核心概念

### 智能体 (Agent)
基于 LangGraph 的状态化智能体，是整个系统的"AI 大脑"。
- **单智能体 + 多工具架构**: 一个主智能体调度多个工具
- **状态图编排**: 使用 LangGraph 定义对话流程和状态流转
- **条件分支**: 根据用户意图选择不同处理路径

### 工具 (Tools)
智能体通过 LangChain Tool 调用后端 API 完成业务操作：
- **query_schedule**: 查询课表
- **create_checkin**: 老师发起签到
- **do_checkin**: 学生签到
- **query_seat**: 查询图书馆座位
- **reserve_seat**: 预约座位
- **seat_checkin**: 座位签到
- **query_menu**: 查询食堂菜单
- **query_map**: 查询地图地点
- **query_credit**: 查询信誉分
- **query_weather**: 查询天气

### RAG 知识库
基于 LangChain RAG 链路的检索增强生成系统：
- **校园规章制度知识库**: 学生手册内容
- **校园新闻/公告知识库**: 校园动态信息
- **常见问题 FAQ 知识库**: 高频问答

### 向量存储
- **FAISS**: 开发阶段使用的向量数据库
- **Milvus**: 生产环境可选迁移方案

### 对话记忆
- **LangGraph 状态管理**: 维护对话上下文
- **对话历史持久化**: 存储用户对话记录

### SSE 流式输出
FastAPI SSE 推送对话响应，实现打字机效果。

## 技术栈
- **FastAPI**: Web 框架
- **LangChain**: LLM 应用框架
- **LangGraph**: 状态化 Agent 编排
- **DeepSeek**: 底层 LLM（Function Calling 支持）
- **FAISS**: 向量数据库
- **Python 3.10+**: 运行环境
