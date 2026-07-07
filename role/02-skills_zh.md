# AI 工程师岗位分析

基于从 builtin.com 提取的 895 份招聘需求分析生成。

我在 2026 年 2 月初针对洛杉矶、纽约、伦敦、阿姆斯特丹和柏林等地区，检索了过去 4 周内包含“AI Engineer”关键字的岗位。因此，该数据集主要反映了 2026 年 1 月发布的职位。

这里的全部数据均来自 [分析笔记本 (analysis notebook)](../job-market/analysis.ipynb) 中的定量分析。

## 核心摘要

- **70%** 的岗位直接开发 AI 系统（如 RAG、智能体/Agents）。
- **93%** 的岗位需要生成式 AI 之外的技能——这本质上是一个全栈岗位。
- **35.9%** 的岗位提到了 RAG——这是所有岗位中最常见的技术模式。
- **64.3%** 的 AI 工程师岗位要求具备一定的机器学习（ML）基础知识。
- 云服务商需求热度：**AWS（359 个岗位） > Azure（214 个岗位） > GCP（205 个岗位）**。


## “AI 工程”岗位类型

我们分析的岗位可以归纳为以下三大类：

- 纯 AI 开发 (AI-first)
- AI 支撑 (AI-support)
- 传统机器学习 (ML)

### 纯 AI 开发 (AI-First)：621 个岗位 (69.4%)

直接开发 AI/ML 系统。

**他们构建的内容**：

- RAG（检索增强生成）系统
- AI 智能体 (AI Agents) 和智能体工作流 (Agentic workflows)
- 针对特定领域微调的大语言模型 (LLMs)
- 模型服务 (Model serving) 与推理流水线
- 提示词工程 (Prompt engineering) 与优化

**典型工作职责**：

- “构建用于知识检索的 RAG 系统”
- “实现用于自动化的智能体工作流”
- “针对特定领域任务微调 Llama 3”
- “将 AI 模型部署到生产环境”
- “优化提示词和模型性能”

**常见职位名称**：

- AI Engineer (AI 工程师)
- Senior AI Engineer (高级 AI 工程师)
- Applied AI Engineer (应用 AI 工程师)
- Lead AI Engineer (首席 AI 工程师)
- Staff AI Engineer (资深 AI 工程师)
- Principal AI Engineer (杰出 AI 工程师)
- AI/ML Engineer (AI/ML 工程师)


### AI 支撑 (AI-Support)：255 个岗位 (28.5%)

在 AI 领域工作，但不直接进行 AI 算法或系统研发。

这些角色通过构建 AI-First 工程师所使用的平台、基础设施和工具来赋能 AI 工作。

**他们构建的内容**：

- AI 平台和内部工具链
- GPU 集群和推理基础设施
- 用于训练/微调的数据流水线
- AI 产品的客户端/前端界面
- 部署与监控系统

**典型工作职责**：

- “为 RAG 系统构建底层平台”
- “为模型微调准备数据流水线”
- “构建部署基础设施”
- “构建提示词管理 UI”
- “为 AI 实验创建内部工具”

**常见职位名称**：

- AI Sales Engineer (AI 销售工程师/解决方案工程师)
- AI Data Engineer (AI 数据工程师)
- AI Infrastructure Engineer (AI 基础设施工程师)
- AI Platform Engineer (AI 平台工程师)
- Backend Engineer - AI Systems (后端工程师 - AI 系统方向)
- Full-Stack Engineer (AI/LLM Platform) (全栈工程师 - AI/LLM 平台方向)


### 传统机器学习 (Machine Learning)：16 个岗位 (1.8%)

传统的 ML/DL 工作，不涉及大语言模型 (LLMs) 或智能体。

**他们构建的内容**：

- 经典机器学习模型（scikit-learn, XGBoost）
- 深度学习模型（PyTorch, TensorFlow）
- 计算机视觉系统
- 推荐系统
- 模型训练流水线

**常见职位名称**：

- Computer Vision AI Engineer (计算机视觉 AI 工程师)
- AI Research Engineer - AI Safety (AI 研究工程师 - AI 安全方向)
- AI Research Engineer - Reinforcement Learning (AI 研究工程师 - 强化学习方向)
- AI Research Engineer - Robotics, Control, RL (AI 研究工程师 - 机器人、控制与强化学习)

*注：这些所谓的“AI 工程师”岗位实际上是冠以 AI 头衔的传统机器学习角色。他们进行传统的机器学习工作（PyTorch、TensorFlow、计算机视觉），不包含任何生成式 AI (GenAI) 元素。*


### 如何区分这三类角色？

核心问题在于：该角色是直接开发 AI 系统（ON AI），还是为 AI 开发者提供支持（NEAR AI）？

**纯 AI 开发 (AI-First)**：
- 构建 RAG 系统
- 微调模型
- 实现智能体工作流
- 优化提示词
- 部署 AI 功能

**AI 支撑 (AI-Support)**：
- 为他人构建开发平台
- 管理 GPU 基础设施
- 构建数据流水线
- 创建部署工具
- 为 AI 产品构建 UI 界面

**传统机器学习 (ML)**：
- 训练传统的机器学习模型
- 处理结构化数据
- 构建计算机视觉系统
- **不**涉及大语言模型或智能体


## 数据集统计信息

去重公司数量：590 家

**招聘岗位数量前 20 名的公司**：

- Capital One - 28 个岗位
- G2i - 15 个岗位
- Scale AI - 10 个岗位
- GEICO - 10 个岗位
- Thomson Reuters - 10 个岗位
- Mistral AI - 7 个岗位
- OpenAI - 7 个岗位
- Traversal - 7 个岗位
- Anthropic - 7 个岗位
- EvolutionIQ - 7 个岗位
- Speechify - 6 个岗位
- SentinelOne - 6 个岗位
- NVIDIA - 6 个岗位
- Helsing - 5 个岗位
- Samsara - 5 个岗位
- PwC - 5 个岗位
- New York Life Insurance - 5 个岗位
- Wolters Kluwer - 5 个岗位
- Coinbase - 5 个岗位
- Cloudflare - 4 个岗位

**公司所处阶段分布**：

| 阶段 | 岗位数量 | 占比 |
|-------|-----:|--:|
| 上市公司 (Public) | 293 | 32.7% |
| B 轮融资 (Series B) | 126 | 14.1% |
| A 轮融资 (Series A) | 59 | 6.6% |
| 种子轮 (Seed) | 36 | 4.0% |

**角色细分**：
- 客户对接角色 (Customer-facing)：231 个岗位 (25.8%)
- 管理层角色 (Management)：155 个岗位 (17.3%)

**最常见的职位名称**：
- AI Engineer - 53 个岗位
- Senior AI Engineer - 31 个岗位
- Applied AI Engineer - 20 个岗位
- Lead AI Engineer - 10 个岗位
- Staff AI Engineer - 8 个岗位
- AI/ML Engineer - 7 个岗位
- Principal AI Engineer - 6 个岗位
- Senior AI/ML Engineer - 5 个岗位
- AI Research Engineer - 5 个岗位
- AI Product Engineer - 5 个岗位


## 技能需求分析

**热门生成式 AI (GenAI) 技能**：

- **RAG** - 321 个岗位 (35.9%)
- **提示词工程 (prompt engineering)** - 260 个岗位 (29.1%)
- **LLMs** - 227 个岗位 (25.4%)
- **LangChain** - 168 个岗位 (18.8%)
- **智能体 (agents)** - 129 个岗位 (14.4%)
- **OpenAI API** - 78 个岗位 (8.7%)
- **LangGraph** - 72 个岗位 (8.0%)
- **LlamaIndex** - 52 个岗位 (5.8%)
- **Anthropic API** - 49 个岗位 (5.5%)

**热门机器学习 (ML) 技能**：

- **PyTorch** - 197 个岗位
- **TensorFlow** - 115 个岗位
- **微调 (fine-tuning)** - 76 个岗位
- **模型训练 (model training)** - 57 个岗位
- **模型评估 (model evaluation)** - 40 个岗位
- **scikit-learn** - 33 个岗位
- **向量嵌入 (embeddings)** - 33 个岗位

**热门 Web 开发技能**：

- **React** - 132 个岗位
- **FastAPI** - 96 个岗位
- **APIs** - 58 个岗位
- **REST APIs** - 58 个岗位
- **REST** - 54 个岗位
- **API 设计 (API design)** - 42 个岗位

**热门数据库技能**：

- **向量数据库 (vector databases)** - 97 个岗位
- **PostgreSQL** - 83 个岗位
- **Pinecone** - 53 个岗位
- **Redis** - 43 个岗位
- **Postgres** - 42 个岗位
- **Weaviate** - 41 个岗位

**热门云平台技能**：

- **AWS** - 359 个岗位
- **Azure** - 214 个岗位
- **GCP** - 205 个岗位

**热门工程运维 (Ops) 技能**：

- **Docker** - 277 个岗位
- **CI/CD** - 262 个岗位
- **Kubernetes** - 260 个岗位
- **MLOps** - 107 个岗位
- **Terraform** - 104 个岗位

**热门编程语言**：

- **Python** - 738 个岗位 (82.5%)
- **TypeScript** - 209 个岗位 (23.4%)
- **Java** - 133 个岗位 (14.9%)
- **Go** - 101 个岗位 (11.3%)
- **SQL** - 88 个岗位 (9.8%)


## 生成式 AI 框架生态系统

**主流框架热度**：

- **LangChain** - 168 个岗位 (18.8%)
- **LangGraph** - 72 个岗位 (8.0%)
- **LlamaIndex** - 52 个岗位 (5.8%)
- **CrewAI** - 28 个岗位 (3.1%)
- **AutoGen** - 17 个岗位 (1.9%)


## 支撑性角色：AI-Support 工程师在做什么？

在 255 个分类为 AI-Support 的岗位中：

| 类别 | 岗位数 | 描述 |
|----------|------:|-------------|
| 平台/基础设施 | 168 | 构建 AI 平台、GPU 集群、MLOps 工具链 |
| 销售/解决方案 | 21 | 售前支持、客户演示、AI 解决方案咨询 |
| 前端/UI | 20 | 为 AI 产品、聊天机器人、AI 仪表盘构建前端界面 |
| 后端/通用开发 | 20 | 开发 API、微服务以及 AI 团队所需的内部工具 |
| 数据/流水线 | 11 | 开发数据清洗和抽取流水线、ETL、ML 训练集准备 |

**AI-Support 岗位是否需要 AI 知识？**

- **57.3%** 的 AI-Support 岗位要求具备一定程度的生成式 AI 知识。
- **42.7%** 则完全不需要生成式 AI 技能。

**AI-Support 岗位中常见的生成式 AI 技能需求**：

- LLMs（通用概念） - 15.3%
- RAG - 13.3%
- 提示词工程 (Prompt engineering) - 7.5%
- LangChain - 6.7%
- OpenAI API - 5.5%


### 技能对比 (AI-First vs AI-Support)

| 技能 | AI-First | AI-Support |
|:-------|---------:|------------:|
| RAG | 50.2% | 17.3% |
| 提示词工程 | 42.4% | 9.0% |
| 智能体 | 33.3% | 8.2% |
| LangChain | 24.3% | 6.7% |
| Docker | 31.2% | 30.6% |
| Kubernetes | 26.4% | 36.1% |
| AWS | 43.3% | 40.8% |
| React | 14.2% | 20.8% |


## 研究型 vs 应用型角色

| 角色类型 | 岗位数 | 百分比 |
|----------|-----:|------------:|
| 研究型 (Research) | 39 | 4.4% |
| 应用/生产型 (Applied/Production) | 856 | 95.6% |

**研究型角色工作内容**：

- 新颖算法和技术研发
- 模型架构设计
- 训练方法优化
- 安全性与对齐（Safety and alignment）研究
- 发表论文，推动业界最先进水平 (SOTA)
- 产出结果具有不确定性的实验性工作

*关键词：研究 (research)、科学家 (scientist)、发表论文 (publication)、新颖 (novel)、算法 (algorithm)、架构 (architecture)、最前沿 (SOTA)、实验性 (experimental)*

*典型研究型职位名称*：
- AI Research Engineer (AI 研究工程师)
- Applied Scientist / Research Engineer (应用科学家/研究工程师)
- AI Research Engineer - Reinforcement Learning (AI 研究工程师 - 强化学习)
- AI Research Engineer - Robotics, Control, RL (AI 研究工程师 - 机器人与控制)
- Research Engineer - Decentralized AI Systems (研究工程师 - 去中心化 AI 系统)

**应用型/生产型角色工作内容**：

- 在生产环境中落地现有模型
- 使用 AI API 开发上层应用
- 部署和监控 AI 系统
- 交付面向客户的 AI 解决方案
- 构建 AI 所需的基础设施和平台
- 针对特定业务场景微调模型

*关键词：生产环境 (production)、部署 (deploy)、客户 (customer)、企业 (enterprise)、产品 (product)、API 集成 (API integration)、交付 (shipping)、落地 (implementation)*


### 职责示例对比

| 研究型 | 应用型 |
|----------|---------|
| “在大规模 GPU 集群上运行预训练、后训练，并部署最前沿的模型。” (Mistral Research) | “部署在各行各业具有可衡量业务成效的生产级 AI 解决方案。” (Mistral FDE) |
| “开发新颖的强化学习算法。” | “实现结合了向量存储的 RAG 模式。” |
| “在顶级学术会议上发表论文。” | “为客户交付 AI 功能产品。” |


## AI 工程师还有哪些其他头衔？

**强 AI-First 职位头衔（75% 以上被归类为 AI-First）**：

- AI Engineer - 118 个岗位 (97% AI-First)
- Applied AI Engineer - 25 个岗位 (88% AI-First)
- AI/ML Engineer - 19 个岗位 (95% AI-First)
- Software Engineer, AI - 11 个岗位 (91% AI-First)
- AI Product Engineer - 8 个岗位 (100% AI-First)
- AI Solutions Engineer - 6 个岗位 (83% AI-First)
- AI Research Engineer - 5 个岗位 (100% AI-First)
- Machine Learning Engineer, Gen AI - 5 个岗位 (100% AI-First)
- Forward Deployed AI Engineer - 3 个岗位 (100% AI-First)

**强 AI-Support 职位头衔（75% 以上被归类为 AI-Support）**：

- AI Platform Engineer - 5 个岗位 (80% AI-Support)
- AI Data Engineer - 4 个岗位 (75% AI-Support)
- AI Infrastructure Engineer - 3 个岗位 (100% AI-Support)
- AI Sales Engineer - 3 个岗位 (100% AI-Support)

*核心洞察：“AI Engineer” 是最常见的头衔（其中 97% 是 AI-First）。但仅凭职位名称并不 100% 可靠，关键还是要查看具体工作职责。*


## AI 工程师需要懂多少机器学习？

**64.3%** 的 AI-First 岗位要求具备一定的机器学习 (ML) 知识。

**AI 工程师岗位中最常见的机器学习技能需求**：

- PyTorch - 165 个岗位 (26.6%)
- 微调 (Fine-tuning) - 159 个岗位 (25.6%)
- TensorFlow - 93 个岗位 (15.0%)
- 向量嵌入 (Embeddings) - 81 个岗位 (13.0%)
- 模型训练 - 80 个岗位 (12.9%)
- 模型评估 - 69 个岗位 (11.1%)

**核心结论**：

1. **大多数 AI 工程师需要基础 ML 知识** —— 64% 的职位提及了相关需求。
2. **微调是最常见的 ML 任务** —— 比从零训练模型更加常见。
3. **PyTorch 占据绝对主导地位** —— 在生成式 AI 岗位中，其出现频率是 TensorFlow 的 **2.6 倍**。

*一句话总结：AI 工程师需要掌握实用的 ML 知识（PyTorch 基础、向量嵌入、微调），但除非你专门从事模型开发，否则不需要极深的数学/理论背景。*


## 出了生成式 AI，AI 工程师还需要懂什么？

**93.1%** 的 AI-First 岗位要求具备生成式 AI **以外**的工程技能。

**AI 工程师角色中的技能组合占比**：

- 生成式 AI + 工程运维 (Docker, K8s, CI/CD) - 72.0%
- 生成式 AI + 机器学习技能 - 57.5%
- 生成式 AI + Web 技术 - 49.1%
- 生成式 AI + 任意其他技术 - 93.1%
- **纯粹只懂生成式 AI（不带其他技能）- 仅占 1.4%**

### 期望具备的非 GenAI 技能

| 类别 | 具体技能及占比 | 备注 |
|----------|--------|--:|
| 云平台 | AWS (41.7%), Azure (24.8%), GCP (22.2%) | - |
| 工程运维 | Docker (31.4%), CI/CD (27.7%), Kubernetes (26.6%) | - |
| Web 开发 | React (12.9%), FastAPI (12.9%) | 约 50% 需要做 Web 相关的开发 |
| 编程语言 | Python (88.6%), TypeScript (23.3%), Java (15.1%) | Python 是绝对的必修课 |

**全栈岗位倾向度**：

- 提及前端技能 - 195/621 (31.4%)
- 提及后端技能 - 308/621 (49.6%)
- 提及全栈技能（前后端均有） - 134/621 (21.6%)

在 50.2% 的 AI-First 岗位中出现了生产部署与工程运维（Ops）技能。其中，“部署 (deploy)”在 5,694 条职责描述中出现了 565 次，“监控 (monitor)”出现了 258 次。

*一句话总结：AI 工程师首先是一名专门深耕 AI 领域的全栈工程师。仅有 1.4% 的职位仅招纯粹只做 GenAI 工作的候选人。大多数人需要具备云端部署（AWS/Azure/GCP）、容器化（Docker、K8s）、CI/CD 以及 Web 开发能力（React、FastAPI）。*


## 模型微调 (Fine-Tuning) 的要求

**30.8%** 的 AI-First 岗位提及了微调。

### 微调技术要求的深度分布

| 级别 | 岗位数 | 百分比 | 描述 |
|-------|------:|--:|-------------|
| 主要微调职责 | 25 | 4.0% | 微调是核心重点（如模型架构、LoRA、PEFT 等） |
| 次要/偶发性微调 | 94 | 15.1% | 提到了微调，但非核心工作 |
| 未提及微调 | 502 | 80.8% | 不需要微调技能 |

### 微调的应用场景

- **指令遵循 (Instruction following)**：训练能够听懂复杂指令并执行任务的 Agent。
- **行业领域知识 (Domain knowledge)**：医疗、法律、金融等垂直领域的定制化应用。
- **风格与语气控制 (Style/Tone)**：品牌话术、个性化设定、格式排版规范。
- **公司私有数据 (Company data)**：结合企业内部文档和专有数据。
- **性能优化 (Performance)**：训练更小、更快的模型以降低延迟。
- **语言扩展 (Language)**：支持多语言或非英语场景。
- **隐私保护 (Privacy)**：私有化部署、离线运行、高安全要求的环境。

**核心结论**：

1. **大多数 AI 工程师不需要做微调** —— 只有约 20% 的岗位有此要求。
2. **以微调为主的核心岗位非常罕见** —— 仅占 4%。
3. **最常见的微调场景** —— 垂直领域知识注入以及提升 Agent 的指令遵循能力。
4. **微调是一项进阶专项技能** —— 并非初期的核心必备能力。

*一句话总结：对于大多数 AI 工程师来说，微调是一项加分/可选技能。建议先扎实掌握 RAG 和智能体 (Agents) 的开发。如果你的目标是垂直行业（医疗、金融）、模型优化或专业模型研发，再去深入学习微调。*


## 评估能力 (Evaluation Skills)

**39.6%** 的 AI-First 岗位显式地要求了评估相关的技能（如模型评估、监控、可观测性、测试、质量把控等）。虽然在显式列出 ML 技能的岗位中它只占 69 个（11.1%），但实际职责描述中对它的需求要广泛得多。

**这是决定人才分水岭的差异化技能**。RAG 和 Agents 正在成为行业基准。而衡量一个 AI 系统是否真正有效的能力（如：大模型作为裁判 LLM-as-judge、黄金测试集构建、幻觉检测、漂移监控）是拉开候选人差距的关键。


## 核心洞察：RAG + 智能体 = 70% 以上的业务场景

目前最为主流的两种开发模式是：

- **RAG（检索增强生成）**：将大模型与你的数据（文档、数据库）进行链接。
- **智能体 (Agents)**：让大模型能够使用外部工具来完成复杂的任务。

如果你能深入掌握这两种模式，你就能轻松应对绝大多数 AI 工程场景。


## AI 工程师的推荐学习路线

1. **编程与工程基础** —— Python、API 调用、基础 Web 开发（FastAPI / React）
2. **大模型基础** —— 提示词工程、OpenAI/Anthropic API 实践
3. **RAG 开发** —— 向量数据库、向量嵌入 (embeddings)、数据检索模式
4. **开发框架** —— 熟练使用 LangChain 或 LlamaIndex
5. **智能体 (Agents)** —— 学习 LangGraph 与 Agent 编排
6. **生产与工程运维** —— Docker、Kubernetes、CI/CD、监控与评估

**标准的 AI 工程技术栈**：

- **应用层 (APPLICATION)**：React、Next.js、FastAPI
- **AI 编排层 (AI ORCHESTRATION)**：LangChain、LangGraph、LlamaIndex
- **大模型 API 层 (LLM APIS)**：OpenAI、Anthropic、本地开源模型
- **向量数据库层 (VECTOR DATABASES)**：Pinecone、Weaviate、pgvector
- **基础设施层 (INFRASTRUCTURE)**：Docker、K8s、AWS/GCP/Azure
