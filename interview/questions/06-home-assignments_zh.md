# Take-Home 离线编程作业与试工

本章内容聚焦于 AI 工程师面试中的离线编程作业（Take-home assignments）、有偿试工（Paid work trials）以及异步技术评估。

数据基于 1,765 份招聘需求、GitHub 上 100+ 份求职候选人实际提交的代码仓库，以及多位资深开发者的真实经验总结。

在明确给出面试流程的 51 家公司中，有 **17 家 (33%)** 将离线作业作为硬性筛选环节。另有 **5 家** 公司采用有偿实战试工代替传统面试。通过分析 100+ 个 GitHub 真实作业仓库，我们总结出目前企业考查作业的几大核心主题：
- **RAG 检索增强系统 (占比 40%+)** —— 涉及多格式文档上传解析、向量数据库配置、引用源归标注。
- **智能体 Agent 系统 (占比 30%+)** —— 涉及工具调用、多步自回归推理、多智能体协同流。
- **对话式 AI (占比 20%+)** —— 智能客服机器人、实时互动 Agent、语音助手。
- **结构化信息抽取 (占比 15%)** —— PDF 解析、发票与成绩单 handwriting 手写体抽取、表单强类型转化。
- **大模型裁判评测 (占比 10%+)** —— 编写应用的同时，必须配套编写一套大模型裁判 (LLM-as-judge) 的自动打分脚本。


## 1. 离线作业的形式

通常要求候选人在拿到题目后的 **2 到 7 天** 内，利用业余时间异步完成。你需要提交完整的代码库、设计文档说明、甚至是一个可以直接在线预览部署的网页。随后，公司会安排一轮 **45 到 90 分钟的作业答辩轮 (Defense round)**，由 2-3 名技术人员针对你的设计进行代码走读与疯狂提问。 [^fonzi-ai]

虽然实际提交截止期有数天，但绝大部分题目在设计上都是“限时 2-4 小时”能写完的体量。企业重点考察的是你在时间约束下的技术选型决断、代码工程规范以及设计文档的易读性，而非花里胡哨的炫技。

几乎没有公司在作业阶段明确禁止使用 AI，反而有部分敏捷团队在题目中明确注明“*强烈推荐且允许使用 Cursor / Github Copilot 协同开发以提升速度*”。


## 2. 真实离线作业题目分类大观

### A. RAG 与文档问答系统 (最为高频，占比 40%+)
- **标准 cited RAG 服务**：构建一个 RAG 问答机器人。能够上传 PDF/文档，在向量数据库中生成 embeddings，并针对提问进行回答，回答必须强制附带出处引用（Citations）。当检索出的内容无法回答问题时，必须能够返回“我无法找到相关信息”的兜底，坚决不能胡编乱造。 [^gh-rokomari] [^gh-streamkar] [^gh-dge-1] [^gh-dge-2] [^gh-bmw] [^gh-ncapek]
- **公司合规文档助手**：开发一个基于公司合规手册的 RAG 问答机器人，所有回答必须附带条文来源。系统附带一个包含 7 个典型测试问题的评测包（划分为：完全可答、部分可答、超出范围不可答三类），要求输出系统在这 7 个问题上的评测打分。 [^gh-neura-dynamics]
- **多跳 RAG 系统**：设计并实现一个支持“多跳转索 (multi-hop query)”的 RAG 问答系统，即需要大模型自动联合检索并理解多个不同的文档段落，才能合并得出正确答案。 [^promptlayer]
- **零幻觉客服 Chatbot**：构建一个完全受限在已知 FAQ 知识库内的在线客服 Agent，要求所有生成的文字绝对不能超出 FAQ 数据范围。 [^gh-spur-1] [^gh-spur-2]
- **生产级高并发 RAG**：设计一个使用开源模型微调的客服 Chatbot。系统指标要求：支持 100+ 用户并发在线，响应时延控制在 2 秒以内，配备链路监控看板。 [^mai-chi-bao]
- **PDF 压缩 CLI 工具**：编写一个命令行工具 (CLI)，支持用户传入不同的模型参数和文本分块（Chunking）大小，对长篇 PDF 文档进行智能摘要。 [^fonzi-ai]
- **屎山代码重构 (RAG Refactoring)**：给你一个写得极其混乱、包含大量全局全局变量且毫无单元测试的 RAG 遗留系统，要求在保持其外部所有 API 行为（API contracts）不变的前提下，将其重构为整洁、模块化、可轻松 mock 测试的优秀架构。 [^gh-bithealth-1] [^gh-bithealth-2] [^gh-bithealth-3] [^gh-bithealth-4] [^gh-bithealth-5]
- **纯开源政务问答 RAG (GovGPT)**：开发一个专门处理政务公开信息的智能体 RAG 系统，要求全栈 100% 采用开源技术（Ollama + CrewAI + pgvector），并且必须集成到 OpenWebUI 前端。系统质量需要通过 RAGAS 评测标准（真实度 Faithfulness、回答相关度 Answer Relevancy、检索精准度 Context Precision）进行打分。 [^gh-govgpt]

### B. 智能体 Agent 与工具调用 (占比 30%+)
- **沙箱级命令执行 Agent**：构建一个智能体，支持大模型自动查询数据库、检索文档并在后台执行 bash 命令行。所有涉及 bash 命令的操作必须在执行前弹出，由用户手动点击确认。 [^gh-curling-ai]
- **项目管理看板 AI 助手**：为 Monday.com 开发一个智能体应用，采用“双模型架构（Dual-LLM）”，将看板上的任务流数据清洗并转化为结构化的业务进展简报。 [^gh-skylark]
- **交通路况智能体**：为新加坡公交出行开发一个智能体，能够自动请求官方提供的 7 个公开 API（涉及实时公交到站、地铁故障、道路交通拥堵等），并根据用户的自然语言问题自动规划路线。 [^gh-hrytos]
- **合规财务看板 Agent**：构建一个面向企业账单订阅的财务分析 Agent。智能体需要能够根据用户提问，自动对账单进行聚合统计（如求和、求平均）。系统禁止大模型直接接触原始数据行以保护隐私，且检测并坚决拒绝任何试图索要 PII 敏感数据（如用户邮箱、信用卡号）的 Prompt 注入行为。 [^gh-cohere]
- **大模型幻觉自动评测插件**：开发一个轻量级的评测工具，能对给定的文本生成进行自动幻觉检测。 [^fonzi-ai]

### C. 多智能体协作系统 (Multi-Agent Systems)
- **多智能体文章撰写流水线**：开发一个包含 5 个核心智能体角色（选题调研 Agent、撰写 Agent、内容编辑 Agent、SEO 优化 Agent、发布排版 Agent）的协作系统。输入产品 JSON 数据后，多智能体自动生成 FAQ 文档、产品介绍页以及竞品横评页，并要求输出格式为严格的强类型 JSON。 [^gh-kasparro]
- **超轻量级工作流状态机引擎**：自行编写一个支持有向图节点跳转、状态持久化管理、逻辑分支判断和工具调用的微型 Agent 引擎。要求单次运行步骤限制在 50 步以内，且系统内核必须具备底层的“无限死循环自我熔断机制”，随附高覆盖率的单元测试。 [^gh-tredence-1] [^gh-tredence-2] [^gh-tredence-3] [^gh-tredence-4] [^gh-tredence-5] [^gh-tredence-6]
- **5-Agent 心理疗愈系统**：构建一个用于 CBT（认知行为疗法）心理咨询的协作多智能体系统。5 个 Agent 分别负责疗愈练习生成、内容挑剔评审、重写调优。系统必须包含“人工审核关卡 (Human-in-the-loop)”，在最终交付给用户前必须经过人类确认。 [^gh-cerina]
- **四阶段睡前故事创作流水线**：Spec 需求制定 Agent $\rightarrow$ 故事撰写 Agent $\rightarrow$ 大模型裁判 Agent $\rightarrow$ 重写调优 Agent。系统要求在 gpt-3.5-turbo 模型下稳定运行，如果裁判不通过，最多允许触发 2 次自动迭代重写。 [^gh-hippocratic-1] [^gh-hippocratic-2] [^gh-hippocratic-3] [^gh-hippocratic-4]

### D. 数据清洗与信息解析抽取
- **非规范成绩单 OCR 强类型抽取**：开发一个 API 服务，能够识别排版极度混乱且包含手写签名的成绩单图片，将其中的表格和签名状态稳定提取为结构化的标准 JSON 数据。 [^gh-trestle]
- **医生面诊语音总结 API**：将诊疗过程中医生与患者的长篇现场对话录音/文本，自动清洗并提炼为符合医疗合规格式的电子病历。 [^gh-emitrr-1] [^gh-emitrr-2]
- **智能法务合同审核**：输入一份长篇法务合同，自动识别并提取核心起止日期，提取出合同中的潜在法务风险（如自动续订陷阱、无限责任免责条款、竞业协议、知识产权归属等），生成总结报告。 [^gh-legal-doc]
- **面向足球新闻的排重与分类流水线**：针对海量的体育新闻数据，设计包含：字面完全去重、基于语义向量的排重、大模型主导的簇分类（Clustering）流水线。系统产出需提供 ARI、NMI 和 homogeneity 指标打分。 [^gh-krisp]
- **高并发商品聚合清洗引擎**：从 4 个不同的非规范供货商处拉取 1,000+ 种杂乱的商品数据。将其清洗规范为统一的内部格式，并在进程中异步调用有严格速率限制（Rate-limited）的第三方富化 API（采用令牌桶限流算法）。系统需包含 AI 级别的重复商品判定，提供 CLI 与 Web API 两种使用入口。 [^gh-rokomari]
- **财报电话会议实时提取与 SSE 推送**：利用 Whisper 实时对企业财报电话会议的流式音频进行听写，并在后台实时提炼关键的财务信号（如营收数据、来年预期、潜在风险），通过 SSE (Server-Sent Events) 技术实时推送给前端页面。 [^gh-voice-ai]

### E. 全栈大模型应用设计
- ** markdown 自动转幻灯片演示**：设计一个 Web 应用，支持用户传入长篇 markdown 文本，系统根据用户制定的 slide 数量限制，在单次大模型 API 调用下（文档大小可达 150K Token），智能切分段落并转换生成排版优美的 PPT 网页展示。Next.js + OpenAI 栈。 [^gh-gamma]
- **高性能大模型路由网关**：开发一个高可用的 LLM 路由中间件。要求具备：智能语义路由、二级缓存（完全匹配缓存 + 向量语义缓存）、多家大模型厂商的健康监测与自动灾备切换、分布式链路追踪。性能指标：QPS $\ge 100$，P95 响应时延 $\le 2$ 秒，缓存命中率 $\ge 40\%$。 [^gh-zuneko]
- **AI 协同模拟 NPC 引擎**：为模拟招聘系统设计 3 名性格迥异的 AI 模拟同事。系统还需包含一个“总控 Agent (Director Agent)”，通过向量语义相似度（阈值设定为 0.85）实时监测候选人与 AI 的对话是否陷入了死循环，并主动打破循环。FastAPI + Claude API + FAISS。 [^gh-edtronaut]
- **全栈 AI-First 客户关系管理 (CRM) 系统**：前端采用 React/Redux 构建美观页面，后端采用 FastAPI，引入 LangGraph 并编写 5 个以上可执行工具。要求提交完整的 GitHub 代码仓库并录制 10-15 分钟的 Loom 演示视频讲解你的系统架构。 [^fonzi-ai]


## 3. 2026 年中新增趋势（Legal Document AI 与智能编译器）

在 2026 年第二季度的 GitHub 最新作业普查中，涌现出几类极具代表性的硬核作业题目：

### A. 法律智能工作流与“改动中学习 (Improvement from edits)”
法律大模型应用成为高频独立题材：
- **三级级联抽取系统**：要求 ingest 杂乱的法律诉状文件，进行精确的三级语义定位，自动生成包含引用源的法务草稿。更重要的是，系统必须支持**根据法务专家的现场修改行为进行迭代自适应调优**的闭环流。 [^gh-labib-legal] [^gh-takey-legal] [^gh-sufian-legal] [^gh-cloud-legal]

### B. 智能编译器与大模型 SQL 调优 (LLM Infrastructure)
- **NL-to-App 编译器**：开发一个能直接把自然语言（Natural Language）应用描述，编译转化为实际可运行系统的“编译器”。系统禁止简单地把 prompt 丢给模型写代码，必须包含结构化、强校验的中间表示（Intermediate Representation）转换和静态语法校验。 [^gh-ai-compiler]
- **大模型数据库调优流水线**：开发一个高可用的 LLM-driven SQL 自动生成与优化流水线。包含 Token 消耗监控、SQL 语法在线验证、可观测性 tracing 日志以及 benchmark 测试。 [^gh-genai-labs-1]


## 4. 哪些公司在 GitHub 上发布了官方作业题库？

你可以在以下公司公开的招聘代码库中，查阅他们的原始面试要求：
- [ML6 (laine)](https://github.com/ml6team/laine-engineer-coding-challenge) —— 大模型评测与 AI 开发编码挑战。
- [Jaseci Labs](https://github.com/jaseci-labs/take-home-ai-engineer) —— 针对 AI 软件工程师的离线作业。
- [Jitera](https://github.com/Jitera-Interviews/genai-takehome) —— 针对生成式 AI 角色的离线技术评估。
- [AuxoAI](https://github.com/AuxoAI-Hiring/ai-engineer-assignment) —— 经典的 AI 工程师作业。
- [Coginis Research](https://github.com/CoginisResearch/ai-engineer-challenge) —— 针对 AI 产品工程师的编码挑战。
- [Future Research](https://github.com/future-research/candidate-assessment) —— 包含完整的评测数据集和 Agent 开发说明。
- [Go Fig AI](https://github.com/go-fig-ai/take-home-inbox-triage) —— 包含人工审核关卡的收件箱智能分类 Agent。
- [Cerebras](https://github.com/danielkim-cerebras/ai-model-quality-challenge) —— 模型质量与性能优化挑战。
- [Bloom](https://github.com/radialreview/bloom-coffee-ai) —— 为现成的咖啡订购应用扩展一个 AI 自动接单模块。


## 5. 如何把作业写到极致

从成功通关者的反馈中总结出的高分作业准则： [^fonzi-ai] [^interviewnode] [^reddit-yc-assignments]

- **第一步永远是写评测 (Evals First)**：在动手写具体的业务代码前，先写一个自动评测脚本（如 Ragas、LLM-as-judge）。YC 孵化器投资的很多初创公司表示，这是区分资深和菜鸟的头号信号：**“如果候选人提交的作业里没有评测逻辑，在我们这里直接就是 Red Flag（危险信号）。”** [^reddit-yc-assignments]
- **配置要灵活可控**：把各种超参数（如切片大小、大模型型号、检索阈值）写入统一的配置文件或 CLI 参数中，展示你对系统的控制力。 [^fonzi-ai]
- **编写高质量的技术决策与 Trade-off 文档**：在 README 中向面试官讲清楚你驳回了哪些备选方案、为什么选择这一套设计、如果时间允许下一步要怎么优化。
- **单元测试必不可少**：哪怕题目没有硬性要求，也必须随附核心函数的单元测试和 Mock 数据。 [^devto-aidi]
- **注重生产细节**：在代码中编写严密的异常捕获（try-except）、链路 tracing 点、以及优雅的崩溃兜底。
- **随附一段 Loom 视频录屏**：录制 3 到 5 分钟的视频演示系统运行，并精简讲解你的核心技术主张。这能极大节省面试官的评审时间，瞬间提升好感度。 [^fonzi-ai]
- **为作业答辩轮做好防守准备**：准备好在随后的视频会上面对 2-3 名技术人员，逐行解释你的设计意图并应对面试官故意追加的技术刁难。

---

## 引用源说明

[^devto-aidi]: [dev.to - Learn From My Mistakes: My First Take-Home Code Challenge](https://dev.to/aidiri/learn-from-my-mistakes-my-first-take-home-code-challenge-778)
[^exponent-openai]: [Medium - Exponent, OpenAI](https://medium.com/exponent/what-its-actually-like-to-interview-at-openai-in-2026-03a646c9436c)
[^fonzi-ai]: [Medium - Fonzi AI](https://medium.com/fonzi-ai/what-ive-learned-from-sitting-in-on-50-ai-engineer-interviews-c493696453c4)
[^goncharov-anthropic]: [Blog - Goncharov, Anthropic Interview](https://blog.goncharov.page/i-failed-my-anthropic-interview-and-came-to-tell-you-all-about-it-so-you-dont-have-to)
[^interviewnode]: [InterviewNode - Cracking ML Take-Home Assignments](https://interviewnode.com/post/cracking-ml-take-home-assignments-real-examples-and-best-practices)
[^khushal-kumar]: [Medium - Khushal Kumar](https://medium.com/@khushalkumar/my-generative-ai-engineer-interview-experience-got-hired-f8a027e070b0)
[^linkjob-anthropic]: [LinkJob - Anthropic Software Engineer Interview](https://www.linkjob.ai/interview-questions/anthropic-software-engineer-interview/)
[^linkjob-openai]: [LinkJob - OpenAI Loop Interview](https://www.linkjob.ai/interview-questions/openai-loop-interview)
[^mai-chi-bao]: [Dev.to - Mai Chi Bao, RAG Chatbot Interview](https://dev.to/mrzaizai2k/how-i-aced-my-llm-interview-building-a-rag-chatbot-2p6f)
[^promptlayer]: [PromptLayer - The Agentic System Design Interview](https://blog.promptlayer.com/the-agentic-system-design-interview-how-to-evaluate-ai-engineers/)
[^reddit-yc-assignments]: [Reddit - What Is Your Interview Assignment for AI Engineers?](https://www.reddit.com/r/ycombinator/comments/1jnfijm/what_is_your_interview_assignment_for_ai_engineers/) (r/ycombinator)
[^tushar-eightfold]: [Medium - Tushar Bhardwaj, Eightfold.ai](https://medium.com/@bhardwajtushar2004/inside-eightfold-ais-agentic-ai-internship-hiring-process-2026-f86dcb625aa8)
[^gh-rokomari]: [GitHub - RokomariTask](https://github.com/gazitanbhir/RokomariTask)
[^gh-streamkar]: [GitHub - Streamkar-Chatbot](https://github.com/Tejasv2002/Streamkar-Chatbot)
[^gh-dge-1]: [GitHub - DGE-assignment](https://github.com/nazar-zhcet26/DGE-assignment)
[^gh-dge-2]: [GitHub - DGE_RAG_APP](https://github.com/Youssef-Matloob/DGE_RAG_APP)
[^gh-bmw]: [GitHub - bmw-ai-engineer-case-study](https://github.com/SHUBHAM-max449/bmw-ai-engineer-case-study)
[^gh-ncapek]: [GitHub - ai_engineer_interview_2025](https://github.com/ncapek/ai_engineer_interview_2025)
[^gh-bithealth-1]: [GitHub - bithealth-crfc](https://github.com/verneylmavt/bithealth-crfc)
[^gh-bithealth-2]: [GitHub - bithealth_home_assesment](https://github.com/fakhrulnurmulyana/bithealth_home_assesment)
[^gh-bithealth-3]: [GitHub - bithealth-assesment](https://github.com/futurebiomedeng/bithealth-assesment)
[^gh-bithealth-4]: [GitHub - bithealthtest](https://github.com/Nerrad07/bithealthtest)
[^gh-bithealth-5]: [GitHub - TechnicalTest-Bithealth](https://github.com/jnny04/TechnicalTest-Bithealth)
[^gh-neura-dynamics]: [GitHub - Company-Policy-Assistant](https://github.com/LAWSA07/Company-Policy-Assistant---Neura-Dynamics)
[^gh-curling-ai]: [GitHub - hiring-challenge-alpha](https://github.com/Curling-AI/hiring-challenge-alpha)
[^gh-skylark]: [GitHub - skylark-bi-insight-agent](https://github.com/venki-byte/skylark-bi-insight-agent)
[^gh-govgpt]: [GitHub - govgpt-agentic-rag](https://github.com/AsharAhmad/govgpt-agentic-rag)
[^gh-tiktok-agent]: [GitHub - AI-Engineer-Assignment](https://github.com/ShitalMagar-dev/AI-Engineer-Assignment)
[^gh-kasparro]: [GitHub - kasparro-ai-agentic-content-generation](https://github.com/rak-shi/kasparro-ai-agentic-content-generation-system-Rakshitha_Valipireddy)
[^gh-tredence-1]: [GitHub - Minimal-Workflow-Agent-Enigne-Tredence](https://github.com/abhishuman18/Minimal-Workflow-Agent-Enigne-Tredence-)
[^gh-cerina]: [GitHub - Cerina-Health-AI-Engineer-Role-Task](https://github.com/mad-99/Cerina-Health-AI-Engineer-Role-Task)
[^gh-hippocratic-1]: [GitHub - hippocratic-ai-bedtime-stories](https://github.com/tasnimhossen/hippocratic-ai-bedtime-stories)
[^gh-hippocratic-2]: [GitHub - agent_deployment_bedtime_stories](https://github.com/pranav-gilda/agent_deployment_bedtime_stories)
[^gh-hippocratic-3]: [GitHub - hippocratic-ai](https://github.com/zoyerz/hippocratic-ai)
[^gh-hippocratic-4]: [GitHub - AI-Agent-Deployment-Engineer-Takehome](https://github.com/reonrash/AI-Agent-Deployment-Engineer-Takehome)
[^gh-cohere]: [GitHub - cohere_sales_agent](https://github.com/Aaronxvc/cohere_sales_agent)
[^gh-spur-1]: [GitHub - spur-live-chat-agent](https://github.com/selvamsmk/spur-live-chat-agent)
[^gh-spur-2]: [GitHub - spur-ai-chat](https://github.com/richiesinhala/spur-ai-chat)
[^gh-trestle]: [GitHub - Trestle_AI_Engineer_Intern_Assignment](https://github.com/gulmittal/Trestle_AI_Engineer_Intern_Assignment-)
[^gh-emitrr-1]: [GitHub - Physician-Notetaker](https://github.com/Iammilansoni/Physician-Notetaker)
[^gh-legal-doc]: [GitHub - Files.Invis](https://github.com/Udaykeerthan67/Files.Invis)
[^gh-mindwell]: [GitHub - mindwell-assignment-2026](https://github.com/mathemage/mindwell-assignment-2026)
[^gh-voice-ai]: [GitHub - voice-ai-assignment](https://github.com/Viren-55/voice-ai-assignment)
[^gh-hrytos]: [GitHub - Transport-Query-Agent](https://github.com/vaishnavip-23/Transport-Query-Agent)
[^gh-pineos]: [GitHub - investment_coach_bot](https://github.com/anuradhabudhar214-tech/investment_coach_bot)
[^gh-context-engineering]: [GitHub - context-engineering-takehome](https://github.com/jkbrooks/context-engineering-takehome)
[^gh-gupshup]: [GitHub - GUPPSHUPP_Founding_AI_Engineer_Assignment](https://github.com/amityadav108/GUPPSHUPP_Founding_AI_Engineer_Assignment)
[^gh-upliance-1]: [GitHub - RPS-Plus-Al-Judge](https://github.com/Thejas10042001/RPS-Plus-Al-Judge)
[^gh-upliance-2]: [GitHub - upliance.ai_assignment](https://github.com/dsulzd/upliance.ai_assignment)
[^gh-gamma]: [GitHub - gamma-project](https://github.com/audoir/gamma-project)
[^gh-zuneko]: [GitHub - Smart-LLM-Router-Observability-Platform](https://github.com/Sushma-Sangolli/Smart-LLM-Router-Observability-Platform)
[^gh-edtronaut]: [GitHub - AI-Coworker-Engine](https://github.com/jerichosuguru/AI-Coworker-Engine)
[^gh-fynd]: [GitHub - fynd-ai-feedback-system](https://github.com/pranaymanapure/fynd-ai-feedback-system)
[^gh-krisp]: [GitHub - krisp_ai_engineer_role_task](https://github.com/Artush-Baghdasaryan/krisp_ai_engineer_role_task)
[^gh-deel]: [GitHub - deel-assignment](https://github.com/kamran-14/deel-assignment)
[^gh-labib-legal]: [GitHub - Legal-Document-AI-Workflow](https://github.com/Labib98989/Legal-Document-AI-Workflow)
[^gh-takey-legal]: [GitHub - Legal-AI-Assessment](https://github.com/Takey-Osman/Legal-AI-Assessment)
[^gh-sufian-legal]: [GitHub - legal-ai-assessment](https://github.com/sufian07/legal-ai-assessment)
[^gh-cloud-legal]: [GitHub - grounded-legal-drafting](https://github.com/cloud-007/grounded-legal-drafting)
[^gh-quorium]: [GitHub - quorium-rag-chatbot](https://github.com/mohamed-sabbar/quorium-rag-chatbot)
[^gh-itj]: [GitHub - itj-rag-challenge](https://github.com/StevenCole01/itj-rag-challenge)
[^gh-ntt-rag]: [GitHub - ntt-rag](https://github.com/utkusayan/ntt-rag)
[^gh-neostats]: [GitHub - riviera-paradise](https://github.com/whoisreethick/riviera-paradise)
[^gh-trinamix]: [GitHub - scm-assistant-bot](https://github.com/anujdevsingh/scm-assistant-bot)
[^gh-gotyme]: [GitHub - tymebank-document-extraction](https://github.com/thabangTheActuaryCoder/tymebank-document-extraction)
[^gh-go-fig]: [GitHub - take-home-inbox-triage](https://github.com/go-fig-ai/take-home-inbox-triage)
[^gh-yuno]: [GitHub - yuno-agent-platform](https://github.com/ashok1995/yuno-agent-platform)
[^gh-refundpilot]: [GitHub - refundpilot-ai-agent](https://github.com/Jatin29AFK/refundpilot-ai-agent)
[^gh-agentcollect]: [GitHub - AgentCollect-Challenge](https://github.com/noopurdiv/AgentCollect-Challenge)
[^gh-neon]: [GitHub - Neon_assesment](https://github.com/Nithinreddyyarradla/Neon_assesment)
[^gh-spotter]: [GitHub - spotter](https://github.com/melmallow/spotter)
[^gh-karthik]: [GitHub - ai-engineer-coding-challenge](https://github.com/KarthikTools/ai-engineer-coding-challenge)
[^gh-genai-labs-1]: [GitHub - gal-assignment](https://github.com/abhishekDeshmukh74/gal-assignment)
[^gh-genai-labs-2]: [GitHub - genai-labs](https://github.com/bhvbhushan/genai-labs)
[^gh-genai-labs-3]: [GitHub - SQLToText-project](https://github.com/bondmojo/SQLToText-project)
[^gh-vantagescore]: [GitHub - vantagescore-credit-intelligence-platform](https://github.com/Jash-stack/vantagescore-credit-intelligence-platform)
[^gh-aegis]: [GitHub - aegis-ai-engineer-assignment](https://github.com/UmairQureshi20/aegis-ai-engineer-assignment)
[^gh-shl]: [GitHub - shl-assessment-recommendation](https://github.com/rasmirajesh/shl-assessment-recommendation)
[^gh-camplight]: [GitHub - camplight-llm-task](https://github.com/RadoslavGenov/camplight-llm-task)
[^gh-ai-compiler]: [GitHub - ai-app-compiler](https://github.com/VijaySaravanaPandi/ai-app-compiler)
[^gh-cql-translator]: [GitHub - CQL-Translator](https://github.com/jpower3145/CQL-Translator)
[^gh-cerebras]: [GitHub - ai-model-quality-challenge](https://github.com/danielkim-cerebras/ai-model-quality-challenge)
[^gh-novelty]: [GitHub - ai-engineering-assignment](https://github.com/nickusevich/ai-engineering-assignment)
[^gh-eloquentai]: [GitHub - Embeddable-Chat-Widget-EloquentAI](https://github.com/joaoscheuermann/Embeddable-Chat-Widget-EloquentAI)
[^gh-fleetio]: [GitHub - fleet-weekly-digest](https://github.com/vnponce/fleet-weekly-digest)
[^gh-zap]: [GitHub - zap-onboarding-ai](https://github.com/shaiaviv/zap-onboarding-ai)
[^gh-adobe]: [GitHub - creative-automation-pipeline](https://github.com/jtdman/creative-automation-pipeline)
