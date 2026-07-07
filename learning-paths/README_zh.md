# AI 工程师学习路径

基于 895 份招聘需求对技能的需求分析，以及 [AI Engineering Buildcamp](https://maven.com/alexey-grigorev/from-rag-to-agents) 训练营大纲，梳理出 AI 工程师需要学习什么以及推荐的学习顺序。


## 核心技能 (Core Skills)

核心技能遵循“二八定律”——即 20% 的核心知识能应对 80% 的日常工作。这基于 [AI Engineering Buildcamp](https://maven.com/alexey-grigorev/from-rag-to-agents) 的课程设计和 [招聘需求调研](../role/02-skills_zh.md)。

### 1. 大模型基础 (LLM Fundamentals)
- 理解大模型的工作原理，搞清楚它们擅长什么、不擅长什么。
- 掌握 OpenAI / Anthropic 的 API 调用 —— 学习如何请求模型、流式接收与解析响应。
- 结构化输出 (Structured Output) —— 确保大模型返回符合强类型（JSON/Typed）的数据规范。
- 提示词工程 (Prompt Engineering) —— 针对不同任务撰写高稳定性、高准确度的提示词模板。

### 2. RAG 与检索 (RAG and Search)
- RAG（检索增强生成）—— 使用企业私有数据增强大模型的回答能力。
- 文本检索与向量检索 —— 如 Elasticsearch、Qdrant 的基本配置与使用。
- 针对不同格式文档的切片（Chunking）策略。
- 解析和清洗不同的数据源 —— 如 PDF 文档、YouTube 视频转录文本、网页数据。
* **实操练习项目建议**：智能 FAQ 客服助手、个人文档问答系统、知识库检索。

### 3. AI 智能体 (AI Agents)
- 函数调用 (Function Calling) 与工具使用 (Tool Use) —— 让大模型有执行具体动作的能力。
- 智能体工具调用循环 (ReAct 模式) —— 学习 Agent 的推理与行动循环。
- 常用智能体开发框架 —— 如 PydanticAI、OpenAI Agents SDK、LangChain、Google ADK。
- 模型上下文协议 (MCP) —— 为大模型和其它智能体编写标准工具。
- 多智能体协作系统 —— 智能体路由派发、任务流水线设计、各 Agent 的协同治理。
* **实操练习项目建议**：网页深度调研 Agent、自动化数据抓取与提取流水线、多智能体协同办公流。

### 4. 系统测试 (Testing)
- 针对智能体的测试开发 —— 如何验证工具调用是否正确、输出格式与质量是否达标。
- 大模型作为裁判 (LLM-as-judge) —— 编写程序调用高级模型去给待测模型打分。

### 5. 监控与可观测性 (Monitoring and Observability)
- 智能体运行链路追踪 —— 使用 OpenTelemetry、Logfire、Jaeger 打印 Traces 日志。
- 接口调用成本监控与 Token 消耗统计。
- 用户反馈与点赞点踩的追踪归档。
- 搭建可视化监控面板 —— 使用 Grafana。

### 6. 质量评估 (Evaluation)
- 离线评估 —— 构造黄金评测用例集（golden dataset），在上线前批量验证 Agent 指标。
- 数据检索质量（召回率、准确率）评估。
- 利用大模型批量合成（Synthetic）评测用例数据。
- 结合评测结果回溯调优提示词（Prompt Optimization）。

### 7. 生产环境落地 (Production)
- 将实验环境的 Jupyter Notebook 原型重构为生产级工程项目。
- 快速原型上线部署 —— 如使用 Streamlit 展示 Demo。
- 云平台生产化部署 —— 如 AWS、GCP、Azure。
- 智能体护栏限制 (Guardrails) —— 为 Agent 交互设定安全合规边界。
- 针对大规模数据集的并行流水线处理。


## 其他关键工程技能 (Other Skills)

基于 [招聘需求调研](../role/02-skills_zh.md)。这些技能虽然不属于大模型专属的范畴，但在 AI 工程师的日常工作中频繁出现，是招聘时的必备项。

### 1. Python 与软件工程素养
- **Python 是绝对的必修课** —— 在 82.5% 的岗位中被要求。
- 测试驱动、CI/CD 自动化部署、代码质量管理 —— 这是对每一名工程师的基准要求。
- 熟练使用 Git 工作流以及进行代码评审（Code Review）。

### 2. Web 开发技能
- **FastAPI** —— 目前开发 AI 应用最常提及的 Python Web 框架。
- **React, Next.js** —— 用于开发全栈 AI 产品的前端页面。
- 掌握 REST APIs 设计、GraphQL、微服务架构。

### 3. 云平台与基础设施
- 掌握 AWS、Azure、GCP 中至少一种主流云平台。
- **Docker 与 Kubernetes** —— 容器化构建与容器编排管理。
- **Terraform** —— 基础设施即代码 (IaC)。

### 4. 数据库知识
- **PostgreSQL** —— 大多数企业的默认关系型数据库选择。
- **向量数据库** —— Pinecone、Weaviate、Qdrant、pgvector。
- **Redis** —— 用于会话缓存与 Session 状态管理。

### 5. 机器学习基础
- **PyTorch 基础** —— 22.0% 的纯 AI 开发（AI-First）岗位有提及。
- **向量嵌入 (Embeddings)** —— 理解大模型的数据降维表示。
- **模型微调 (Fine-tuning)** —— 懂得当商业 API 大模型无法满足垂直行业要求时的调优方案。
- 传统机器学习算法的评估指标。

### 6. 数据工程能力
- 数据流水线建设 —— Airflow、Spark、Kafka。
- ETL（抽取、转换、加载）处理。
- Databricks, Snowflake 等数据仓库。

### 7. 其他编程语言
- **TypeScript** —— 在 AI 工程师招聘中流行度仅次于 Python 的语言。
- **Java, Go** —— 适合偏后端重型计算和高并发的团队。
- **SQL** —— 用于基本的数据读写与统计分析。


## 定制转型指南 (Role-Specific Guides)

已经积累了相关技术经验？请直接从你所处的当前角色开始平滑过渡：

- [从数据工程师 (Data Engineer) 转型](from-data-engineer_zh.md) —— 最顺畅的转型路线，预计耗时 3-4 个月。
- [从数据科学家 (Data Scientist) 转型](from-data-scientist_zh.md) —— 评测与算法是你的超能力，重点补充工程基本功。
- [从机器学习工程师 (ML Engineer) 转型](from-ml-engineer_zh.md) —— 最简单的转型路线，将本地模型部署替换为 API 服务调用。
- [从后端工程师 (Backend Engineer) 转型](from-backend-engineer_zh.md) —— 预计耗时 2-3 个月，在扎实的工程底子之上堆叠大模型开发技能。
- [从前端工程师 (Frontend Engineer) 转型](from-frontend-engineer_zh.md) —— 先补齐后端逻辑再叠加 AI 接口，拥有独特的全栈综合优势。


## 典型的 AI 工程技术栈

- **应用表现层**：React, Next.js, FastAPI
- **AI 编排与流控**：LangChain, LangGraph, PydanticAI
- **大模型 API**：OpenAI, Anthropic, Groq, 本地开源模型权重
- **向量存储**：Pinecone, Weaviate, Qdrant, pgvector
- **基础设施与 Ops**：Docker, K8s, AWS/GCP/Azure
- **监控可观测性**：Logfire, Grafana, OpenTelemetry
- **评估与回归校验**：LLM Judges（大模型裁判）, Evidently


## 技能优先级清单

### 必备基础 (Must have)
- Python
- 提示词工程 (Prompt engineering)
- RAG 基础模式
- 掌握至少一种云平台（AWS / Azure / GCP）
- Docker 容器化

### 高价值加分项 (High value)
- 熟练使用 LangChain 或 PydanticAI
- TypeScript 语言
- FastAPI Web 开发
- Kubernetes 容器编排
- 自动化 CI/CD
- PyTorch 基础开发

### 差异化核心壁垒 (Differentiators)
- 智能体编排框架 —— LangGraph, CrewAI
- 大模型微调 (Fine-tuning)
- 评测框架开发与质量管理
- 向量数据库深度运维 —— Pinecone, Weaviate, Qdrant
- 多智能体系统协同模式
