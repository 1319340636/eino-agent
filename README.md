# Go + React 全栈智能体平台
> 本项目是在[NexusAgent]基础上进行的个人学习与二次开发，重点实践 Go 后端工程、Agent 运行时、RAG 和全栈部署。
面向多场景智能体应用，提供对话、工具调用、知识库检索、Skills 管理和可视化工作流能力。后端采用分层设计，前端提供管理控制台与工作流画布。

## 核心功能

- **全栈应用架构：** 使用 Gin、GORM 和 React 19 构建前后端，包含用户认证、会话管理、模型配置和管理界面。
- **Agent 运行：** 基于 Eino 实现 ReAct 与工具调用，通过 SSE 向前端推送模型输出和工具执行事件。
- **Skills：** 支持 Skill 的管理、Agent 绑定与按需加载，让 Agent 根据任务使用相应的指令和参考资料。
- **RAG 知识库：** 文档经过异步 ETL、解析、分块和向量化后入库；检索结合向量召回、关键词召回、RRF 融合及重排序。
- **智能体与工作流：** 支持 Host/Expert 协作和 A2A 通信；工作流使用 YAML 描述，并提供画布编辑、条件分支、并行执行和人工审批节点。
- **工程化能力：** 集成 PostgreSQL、Redis Streams、Milvus、MinIO，并提供 Docker Compose、Kubernetes 部署配置、链路追踪和指标监控。

## 技术栈

| 模块 | 技术 |
|---|---|
| 后端 | Go、Gin、GORM、PostgreSQL |
| Agent | Eino、ReAct、Function Calling、MCP、A2A |
| 前端 | React 19、TypeScript、Vite |
| RAG 与任务处理 | Milvus、MinIO、Redis Streams |
| 部署与可观测性 | Docker、Kubernete
