# Awesome AI Engineering 优秀资源库

这里精心收集了 AI 工程领域的各类优质资源：从业人员真实的面试故事、系统设计指南、大厂技术博客、书籍推荐、实战课程以及生产落地案例等。

这些资源是我在调研和撰写 [AI 工程实践指南 (AI Engineering Field Guide)](README_zh.md) 时所参考的文献。在整理过程中，我发现这份资源列表本身就具有极高的独立参考价值，因此决定将其单独发布。

---

## 1. AI 工程师面试实战经历 (AI Interview Experiences)

- [Mimansa Jaiswal：2024 年秋季 LLM/ML 岗位面试记录（流程篇）](https://mimansajaiswal.github.io/posts/llm-ml-job-interviews-fall-2024-process/) —— 记录了在 Anthropic、OpenAI、Meta、Apple 等 20 多家公司的真实面试流程。
- [Mimansa Jaiswal：LLM/ML 岗位面试（资源篇）](https://mimansajaiswal.github.io/posts/llm-ml-job-interviews-resources/) —— 备战大模型面试的推荐资源与策略。
- [Mai Chi Bao：我如何通过构建一个 RAG 聊天机器人斩获大模型面试](https://dev.to/mrzaizai2k/how-i-aced-my-llm-interview-building-a-rag-chatbot-2p6f) —— 面试得分 9/10，包含非常详尽的技术实现方案拆解。
- [Janvi Kalra：从软件工程师转型为 AI 工程师的求职之旅](https://newsletter.pragmaticengineer.com/p/from-software-engineer-to-ai-engineer) —— 投递并面试了 46 家机构的真实故事，收录于 Pragmatic Engineer 周报。
- [2026 年在 OpenAI 面试是怎样的体验](https://medium.com/exponent/what-its-actually-like-to-interview-at-openai-in-2026-03a646c9436c) —— Exponent 发布的候选人真实 OpenAI 求职体验。
- [Dr. Sundeep Teki：AI 研究工程师求职面试指南](https://www.sundeepteki.org/advice/the-ultimate-ai-research-engineer-interview-guide-cracking-openai-anthropic-google-deepmind-top-ai-labs) —— 助力攻克 OpenAI、Anthropic、DeepMind 等顶级 AI 实验室的面试通关秘籍。
- [Tushar Bhardwaj：解析 Eightfold.ai 2026 年智能体 AI 实习生招聘流程](https://medium.com/@bhardwajtushar2004/inside-eightfold-ais-agentic-ai-internship-hiring-process-2026-f86dcb625aa8) —— 包含 AI 主导的代码面试、为期 3 天的 Agent 构建作业以及 DSA 算法轮次。
- [Kay 的笔记：我的生成式 AI 工程师面试拿到 Offer 经历](https://kaysnotes.medium.com/my-generative-ai-engineer-interview-experience-got-hired-6b3f1affc4e9) —— 包含分析血检报告的 Take-home 作业实战。
- [我如何通过 IBM AI 工程师面试](https://levelup.gitconnected.com/how-i-cracked-my-ibm-ai-engineer-interview-part-1-technical-9e75284344e5) —— 详细的技术面试流程复盘。
- [Deepthi Sudharsan：AI 面试内幕——真实经历、模式总结及考察重心](https://medium.com/@deepthi.sudharsan/inside-ai-interviews-stories-patterns-and-what-actually-matters-555684c38598) —— 基于 50+ 轮真实面试经验的归纳总结。
- [Fonzi AI：旁听 50+ 场 AI 工程师面试后我学到了什么](https://medium.com/fonzi-ai/what-ive-learned-from-sitting-in-on-50-ai-engineer-interviews-c493696453c4) —— 从面试官角度审视哪些特质能让候选人脱颖而出。


## 2. 软件工程师在 AI 方向的面试故事 (SWE in AI - Interview Experiences)

- [Rohit Verma：2026 年微软资深工程师面试复盘（历经三次尝试终拿 Offer）](https://medium.com/@rohitverma_87831/microsoft-senior-engineer-interview-experience-2026-the-offer-that-took-me-three-attempts-e0d6e052bdb1) —— 包含 AI 系统设计轮次（构建吉卜力风格图像生成器）。
- [我如何在 2025 年利用大模型备战并通关技术面试](https://levelup.gitconnected.com/how-i-fought-and-passed-technical-interviews-with-llms-in-2025-f328e9df8e84) —— 如何使用 LLM 备考 AI 系统设计（涉及 RAG、向量库、大模型服务托管等）。
- [xAI 软件工程师 2026 面试全回顾](https://dev.to/net_programhelp_e160eef28/xai-software-engineer-interview-2026-full-recap-pitfalls-real-prep-tips-2fl0) —— 真实的避坑指南与备战技巧。


## 3. 架构经验与技术模式 (Architecture Lessons & Patterns, 2025-2026)

- [DataA.dev：从 AI 实验原型到生产环境落地现实](https://www.dataa.dev/2026/01/01/from-ai-pilots-to-production-reality-architecture-lessons-from-2025-and-what-2026-demands/) —— 指出 70% 的生成式 AI 项目最终未能走出 POC 概念验证阶段，写于 2026 年 1 月。
- [FlowHunt：上下文工程指南](https://www.flowhunt.io/blog/context-engineering/) —— 详述从提示词工程向上下文工程（Context Engineering）的演进，写于 2025 年。
- [LangWatch：2025/2026 年度 RAG 终极蓝图](https://langwatch.ai/blog/the-ultimate-rag-blueprint-everything-you-need-to-know-about-rag-in-2025-2026)
- [TensorZero：逆向剖析 Cursor 的 LLM 客户端实现](https://www.tensorzero.com/blog/reverse-engineering-cursors-llm-client)
- [后生成式 AI 时代的机器学习系统设计（Medium 连载）](https://medium.com/machine-learning-system-design-post-genai/machine-learning-system-design-post-genai-part-1-071af68b0ce4)
- [PromptLayer：提示词路由与工作流工程](https://blog.promptlayer.com/prompt-routers-and-flow-engineering-building-modular-self-correcting-agent-systems/) —— 如何构建模块化、具备自我纠错能力的智能体系统。
- [Alex Ewerlof：AI 系统工程最佳实践模式](https://blog.alexewerlof.com/p/ai-systems-engineering-patterns) —— 整理了 30 多种工程架构模式，写于 2025 年 11 月。
- [Hacker News 热议：生产环境中的智能体系统](https://news.ycombinator.com/item?id=42431361) —— 探讨什么是真正的“Agentic”，并引用了 Cursor、Intercom Fin、Devin 等真实案例。
- [Hacker News 热议：模型微调 vs 提示词工程](https://news.ycombinator.com/item?id=36069936) —— 探讨何时应当微调、何时使用提示词，以及各自的成本权衡。
- [Hacker News 热议：提示词注入——最坏的情况会怎样？(Simon Willison)](https://news.ycombinator.com/item?id=35572290) —— 探讨如何实现数据与指令的隔离，建立架构层面的防线。


## 4. 面试真题汇总 (Interview Question Collections)

- [TechEon：2026 智能体 AI 系统设计面试全攻略](https://atul4u.medium.com/the-complete-agentic-ai-system-design-interview-guide-2026-f95d0cfeb7cf) —— 详述智能体架构模式、自主边界设定、记忆系统、工具调用和评估方法，写于 2026 年 1 月。
- [KDnuggets：AI 工程师必考的 10 道智能体 AI 面试题](https://www.kdnuggets.com/10-essential-agentic-ai-interview-questions-for-ai-engineers)
- [DataCamp：2026 年最核心的 30 道 RAG 面试题](https://www.datacamp.com/blog/rag-interview-questions)
- [DataCamp：2026 年最核心的 30 道智能体 AI 面试题](https://www.datacamp.com/blog/agentic-ai-interview-questions)
- [Hao Hoang：大语言模型（LLM）核心面试 50 题](https://drive.google.com/file/d/1cUxKspEXgQ64s4OFEw0kabf_qNauOPiH/view) —— 深入探讨大模型底层原理，写于 2025 年 5 月。
- [LLM 面试真题题库 (Lovable App)](https://llm-interview-questions.lovable.app/) —— 汇集了求职候选人反馈的高频理论面试题。
- [GitHub 仓库：RAG 面试问答汇总中心](https://github.com/KalyanKS-NLP/RAG-Interview-Questions-and-Answers-Hub) —— 整理了 100+ 道 RAG 核心问题与答案。
- [GitHub 仓库：60 道生成式 AI 面试题](https://github.com/aishwaryanr/awesome-generative-ai-guide/blob/main/interview_prep/60_gen_ai_questions.md) —— 摘自优秀的 awesome-generative-ai-guide 仓库。


## 5. AI 系统设计指南与面试框架 (AI System Design Guides)

- [PromptLayer：智能体系统设计面试](https://blog.promptlayer.com/the-agentic-system-design-interview-how-to-evaluate-ai-engineers/) —— Jared Zoneraich 撰写，分析如何科学考核和筛选 AI 工程师，写于 2025 年 7 月。
- [Bhavishya Pandit：7 道极具深度的 AI 系统设计面试题](https://bhavishyapandit9.substack.com/p/7-deep-cut-ai-system-design-interview) —— 剖析前沿的线上实战难题，写于 2025 年 7 月。
- [Chip Huyen：如何构建生成式 AI 开发平台](https://huyenchip.com/2024/07/25/genai-platform.html) —— 业界大牛撰写的标杆级实践参考，详细阐述了 5 层架构设计。
- [InterviewNode：生成式 AI 系统设计面试常见模式](https://www.interviewnode.com/post/generative-ai-system-design-interview-patterns-you-should-know) —— 提供可复用的架构蓝图，写于 2025 年 11 月。
- [InterviewNode：攻克机器学习面试 Take-Home 编程作业](https://interviewnode.com/post/cracking-ml-take-home-assignments-real-examples-and-best-practices) —— 分析了 Meta、Amazon、OpenAI 等大厂的作业实例和评审指标。
- [System Design Handbook 系统设计手册](https://www.systemdesignhandbook.com/) —— 包含针对 [GenAI 架构](https://www.systemdesignhandbook.com/guides/generative-ai-system-design-interview/)、[智能体设计](https://www.systemdesignhandbook.com/guides/agentic-system-design/)、[AI 系统](https://www.systemdesignhandbook.com/guides/ai-system-design/) 以及 [LLM 系统](https://www.systemdesignhandbook.com/guides/llm-system-design/) 的面试指南。
- [Anthropic 系统设计面试通关指南](https://www.systemdesignhandbook.com/guides/anthropic-system-design-interview/)。
- [HelloInterview：OpenAI L5 级别面试备考指南](https://www.hellointerview.com/guides/openai/l5)。
- [IGotAnOffer：生成式 AI 系统设计面试（含谷歌、苹果、OpenAI 真题）](https://igotanoffer.com/en/advice/generative-ai-system-design-interview)。
- [Design Gurus 面试课](https://www.designgurus.io/) —— 涵盖 [OpenAI 系统设计](https://www.designgurus.io/blog/openai-system-design-interview-questions) 以及 [RAG 系统设计](https://www.designgurus.io/blog/system-design-for-rag)。


## 6. 生产环境下的 AI 系统：企业工程案例 (Case Studies)

### 案例库合集
- [Evidently AI：800+ 机器学习与大模型系统设计案例](https://www.evidentlyai.com/ml-system-design) —— 覆盖 150+ 家公司，支持多标签检索过滤。
- [GitHub 仓库：500+ 生成式 AI / 大模型 / 传统 ML 生产案例](https://github.com/themanojdesai/genai-llm-ml-case-studies) —— 收集了百余家大厂的实践。
- [GitHub 仓库：AI 系统设计实战指南](https://github.com/ombharatiya/ai-system-design-guide) —— 持续维护的开源文档。
- [GitHub 仓库：AIE 随书配套资源](https://github.com/chiphuyen/aie-book/blob/main/resources.md) —— 支撑 Chip Huyen 新书《AI Engineering》的参考资料。
- [ZenML：287 个大模型运维 (LLMOps) 生产实践案例](https://www.zenml.io/blog/llmops-in-production-287-more-case-studies-of-what-actually-works)。

### Anthropic 实践
- [构建高效的智能体应用](https://www.anthropic.com/research/building-effective-agents) —— 剖析工作流 (workflows) 与智能体 (agents) 的区别，给出可组合的技术模式，写于 2024 年 12 月。
- [揭秘 Anthropic 的多智能体科研系统实现](https://www.anthropic.com/engineering/multi-agent-research-system) —— 详细解析 Orchestrator-Worker（编排者-执行者）设计模式，写于 2025 年 6 月。
- [AI 智能体的有效上下文工程 (Context Engineering)](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents) —— 探讨系统提示词、工具定义以及样例编排，写于 2025 年 9 月。
- [Contextual Retrieval 上下文检索技术](https://www.anthropic.com/news/contextual-retrieval) —— 通过为分块数据注入上下文，降低了 49% 的检索失败率，写于 2024 年 9 月。
- [Anthropic 工程博客全归档索引](https://www.anthropic.com/engineering)。

### Doctolib 实践
- [构建面向医疗健康辅助的智能体系统](https://medium.com/doctolib/building-an-agentic-ai-system-for-healthcare-support-a-journey-into-practical-ai-implementation-0afd28d716e6) —— 介绍日均处理 1.7 万条消息的 LangGraph 智能体应用“Alfred”。
- [从 RAG 检索增强向 Agent 演进：Doctolib 实践复盘（第二篇）](https://medium.com/doctolib/part-2-from-rag-to-agents-doctolibs-journey-to-revolutionize-customer-care-6b14da40f5ae)。

### Meta 实践
- [Meta 基础设施的演进与 AI 浪潮的碰撞](https://engineering.fb.com/2025/09/29/data-infrastructure/metas-infrastructure-evolution-and-the-advent-of-ai/) —— 写于 2025 年 9 月。
- [扩展大模型推理：张量并行、上下文并行与混合专家并行](https://engineering.fb.com/2025/10/17/ai-research/scaling-llm-inference-innovations-tensor-parallelism-context-parallelism-expert-parallelism/) —— 写于 2025 年 10 月。
- [构建 Meta 的生成式 AI 基础设施](https://engineering.fb.com/2024/03/12/data-center-engineering/building-metas-genai-infrastructure/) —— 写于 2024 年 3 月。

### Uber 实践
- [GenAI Gateway 统一智能网关](https://www.uber.com/blog/genai-gateway/) —— 托管了 60+ 个业务场景的大模型底层平台。
- [从预测性 AI 向生成式 AI 的演进](https://www.uber.com/blog/from-predictive-to-generative-ai/) —— 详细解析其 Michelangelo 平台架构的迭代。
- [Uber 是如何优化大模型训练的](https://www.uber.com/blog/open-source-and-in-house-how-uber-optimizes-llm-training/)。
- [大模型提示词工程工具链 (Prompt Engineering Toolkit)](https://www.uber.com/blog/introducing-the-prompt-engineering-toolkit/)。

### Airbnb 实践
- [Airbnb 自动化平台 v2：优化对话式 AI 服务](https://medium.com/airbnb-engineering/automation-platform-v2-improving-conversational-ai-at-airbnb-d86c9386e0cb)。

### Perplexity 实践
- [设计并评估一个 AI-First 的搜索 API](https://research.perplexity.ai/articles/architecting-and-evaluating-an-ai-first-search-api)。
- [Perplexity 是如何打造 AI 谷歌搜索的 (ByteByteGo)](https://blog.bytebytego.com/p/how-perplexity-built-an-ai-google) —— 解析日均处理 2 亿次请求的 Vespa.ai RAG 架构。
- [Perplexity 是如何击败谷歌大模型搜索的 (Vespa.ai)](https://blog.vespa.ai/perplexity-show-what-great-rag-takes/)。

### LinkedIn 实践
- [开发生成式 AI 产品的心路历程](https://www.linkedin.com/blog/engineering/generative-ai/musings-on-building-a-generative-ai-product)。
- [QCon AI 2025 大会分享：LinkedIn AI 平台架构](https://www.infoq.com/news/2025/12/qcon-ai-linkedin/) —— 指出在系统构建中，智能体与上下文设计的重要度远超模型选择，写于 2025 年 12 月。
- [LinkedIn 生成式 AI 技术栈演进 (ByteByteGo)](https://blog.bytebytego.com/p/the-evolution-of-linkedins-generative)。

### Netflix 实践
- [在 Netflix 支持多样化机器学习系统运行](https://netflixtechblog.com/supporting-diverse-ml-systems-at-netflix-2d2e6b6d205d)。
- [Netflix 是如何超算加速 AI/ML 研发效率的](https://netflixtechblog.com/supercharging-the-ml-and-ai-development-experience-at-netflix-b2d5b95c63eb) —— 详细解析 Maestro 工作流调度器，写于 2025 年。

### Spotify 实践
- [Spotify 后台自动编码 Agent “Honk” 实践](https://engineering.atspotify.com/2025/11/spotifys-background-coding-agent-part-1) —— 已自动合并 1,500+ 个 AI 生成的 PR，写于 2025 年 11 月。
- [Spotify 是如何利用生成式 AI 标注音乐音轨的 (ByteByteGo)](https://blog.bytebytego.com/p/how-spotify-uses-genai-and-ml-to)。

### Shopify 实践
- [使用多模态大模型维护全球商品目录](https://shopify.engineering/leveraging-multimodal-llms) —— 日均推理次数高达 4,000 万次，收录于 ICLR 2025。
- [构建世界一流的商品搜索引擎](https://shopify.engineering/world-class-product-search)。

### Slack 实践
- [我们是如何构建安全与隐私兼备的 Slack AI 的](https://slack.engineering/how-we-built-slack-ai-to-be-secure-and-private/) —— 详细剖析了无状态 RAG 以及隔离的 Escrow VPC。

### DoorDash 实践
- [用于大规模大模型聊天机器人的模拟与评估飞轮](https://careersatdoordash.com/blog/doordash-simulation-evaluation-flywheel-to-develop-llm-chatbots-at-scale/)。
- [大模型辅助的个性化推荐框架](https://careersatdoordash.com/blog/doordash-kdd-llm-assisted-personalization-framework/) —— 详细解析层级 RAG。

### Grab 实践
- [LLM-Kit：支持生产环境快速交付的大模型中间件](https://engineering.grab.com/supercharging-llm-application-development-with-llm-kit) —— 支持了内部数百个 GenAI 应用。
- [用于单据解析的多模态大模型 (ByteByteGo)](https://blog.bytebytego.com/p/how-grab-built-a-vision-llm-to-scan)。

### Pinterest 实践
- [大模型辅助的搜索相关度精细评估系统](https://medium.com/pinterest-engineering/llm-powered-relevance-assessment-for-pinterest-search-b846489e358d) —— 写于 2025 年 12 月。

### Notion 实践
- [Notion 围绕 Agentic AI 进行的底层架构重构 (OpenAI 官方案例)](https://openai.com/index/notion/) —— 采用中心推理模型协调子智能体。
- [为 RAG 扩容底层数据基础设施 (ZenML)](https://www.zenml.io/llmops-database/scaling-data-infrastructure-for-ai-features-and-rag) —— 数据块从 200 亿行跃升至 2,000 亿行。
- [如何开发一款 AI 驱动的产品 (Braintrust)](https://www.braintrust.dev/blog/notion) —— 剖析日均拦截 30 个 AI 层面 Bug 的实操。

### Cohere 实践
- [图解 RAG 系统架构设计](https://cohere.com/blog/rag-architecture) —— 详细解释交叉编码重排 (cross-encoder reranking)、Embed-v4 等，写于 2025 年 2 月。

### Databricks 实践
- [如何构建高质量的 RAG 生产系统](https://www.databricks.com/blog/building-high-quality-rag-applications-databricks)。
- [构建、优化与部署知识图谱 RAG (GraphRAG) 系统](https://www.databricks.com/blog/building-improving-and-deploying-knowledge-graph-rag-systems-databricks)。

### 云厂商最佳实践
- [AWS：架构卓越的 AI 体系最佳实践 (re:Invent 2025)](https://aws.amazon.com/blogs/architecture/architecting-for-ai-excellence-aws-launches-three-well-architected-lenses-at-reinvent-2025/) —— 发布了三套大模型 Well-Architected 评估透镜。
- [AWS：亚马逊内部评估智能体系统的真实经验分享](https://aws.amazon.com/blogs/machine-learning/evaluating-ai-agents-real-world-lessons-from-building-agentic-systems-at-amazon/)。
- [Google Cloud：2025 年关于 Agent 和可信度的反思与总结](https://cloud.google.com/transform/ai-grew-up-and-got-a-job-lessons-from-2025-on-agents-and-trust)。
- [微软 Build 2025：迎接智能体网络新时代 (Open Agentic Web)](https://blogs.microsoft.com/blog/2025/05/19/microsoft-build-2025-the-age-of-ai-agents-and-building-the-open-agentic-web/)。


## 7. 官方面试参考指南 (Company Official Interview Guides)

- [OpenAI 官方求职面试指南](https://openai.com/interview-guide/) —— 官方出品，内含系统设计轮次的详细评估指标。
- [Doctolib 官方技术面试流程说明](https://careers.doctolib.com/blog/hiring-advice/tech-interview-guide/)。
- [Doctolib 协作式功能开发轮次面试指南](https://careers.doctolib.com/blog/hiring-advice/all-about-our-feature-building-interview/) —— 结对协作编程轮次。
- [Datadog 面试中关于 AI 工具的使用政策](https://careers.datadoghq.com/candidate-experience/interviewing-at-datadog-ai-guidelines/) —— 规范求职者使用 AI 助手的红线。
- [CDW 面试 AI 工具倡导通告](https://www.cdwjobs.com/pages/ai-applicant-notice) —— 鼓励合理使用 AI 工具并给出框架指导。
- [Oscar Health 面试 AI 使用红线说明](https://www.hioscar.com/careers/ai-guidelines) —— 简历允许使用 AI 润色，但若有夸大事实或作弊将直接取消资格。
- [Invisible Technologies 分阶段 AI 使用面试指引](https://invisibletech.ai/ai-interview-guidelines)。
- [Anthropic 关于候选人使用 AI 工具的官方政策](https://www.anthropic.com/candidate-ai-guidance)。
- [Anthropic 开源的性能工程考核 Take-Home 原题](https://github.com/anthropics/original_performance_takehome) —— 必须将消耗压到 1,487 周期以内才能通过的硬核挑战。
- [Arcan-Tech 2025 年 AI 工程师技术面试作业](https://github.com/Arcan-Tech/interview-test-aiengineer-2025) —— 真实作业：根据 git diff 预测代码变更的传播路径，限时 4 小时且必须 Docker 化运行。
- [Zapier 招聘中如何与 AI 结对协作的指南](https://zapier.com/l/jobs/ai-at-zapier) —— 鼓励合作使用并给出评分标准。
- [AssemblyAI 官方候选人 AI 使用指引](https://www.assemblyai.com/candidate-ai-guidance)。
- [SandboxAQ 官方面试 AI 辅助政策](https://www.sandboxaq.com/ai-in-interviews)。


## 8. 书籍推荐 (Books)

- **《AI Engineering》** (O'Reilly, 2025) —— Chip Huyen 著。涵盖基础模型、提示词设计、RAG、智能体及模型评测。
- **《LLM Engineer's Handbook》** (Packt, 2024) —— Paul Iusztin 与 Maxime Labonne 著。详述大模型应用从概念原型到生产部署、性能优化的全流程。
- **《Generative AI System Design Interview》** (ByteByteGo, 2024) —— Ali Aminian 与 Hao Sheng 著。汇总了 10 个高频的真实大模型系统设计面试题。
- **《What We Learned from a Year of Building with LLMs》** (Applied LLMs, 2024) —— 6 位业内资深技术专家的联手总结。


## 9. 推荐课程 (Courses)

- [AI Engineering Buildcamp: From RAG to Agents](https://maven.com/alexey-grigorev/from-rag-to-agents) —— Alexey Grigorev 授课，为期 9 周的生产级大模型开发高强度实战营。
- [LLM Zoomcamp](https://github.com/DataTalksClub/llm-zoomcamp/) —— DataTalks.Club 举办的免费开源 LLM/RAG 课程。
- [Systematically Improving RAG Applications](https://maven.com/applied-llms/rag-playbook) —— Jason Liu 授课。
- [Educative: Grokking Generative AI System Design](https://www.educative.io/courses/generative-ai-system-design) —— 介绍 SCALED 面试拆解框架与系统模拟。
- [Shreya Shankar：为啥你需要坚定维护大模型评测系统](https://www.lennysnewsletter.com/p/building-eval-systems-that-improve-cec) —— 收录于 Lenny's Newsletter。
- [大模型评测（Evals）为何成为当下最火热、最具含金量的新技能](https://www.lennysnewsletter.com/p/why-ai-evals-are-the-hottest-new-skill) —— 收录于 Lenny's Newsletter。


## 10. 技术社区 (Communities)

- [AI Shipping Labs](https://aishippinglabs.com/) —— 实行邀请制的大模型开发者社区，聚焦系统落地与同行结对协作。
- [DataTalks.Club](https://datatalks.club/) —— 拥有 8 万多名成员的庞大数据科学社区，提供免费的 ML Zoomcamp 等精品开源课。
- [MLOps Community](https://mlops.community/) —— 聚集了大量研究 ML/LLM 部署、AI 工程和 Agents 线上生产架构的工程师。
- [Hugging Face 官方 Discord 频道](https://huggingface.co/discord-community) —— 拥有 20 多万成员的全球最大的开源 AI/ML 协作与讨论中心。
- [Reddit - r/MachineLearning 社区](https://www.reddit.com/r/MachineLearning/) —— 学术交流与业界动态发布的核心版块。
- [Reddit - r/LocalLLaMA 社区](https://www.reddit.com/r/LocalLLaMA/) —— 聚焦于本地运行、微调及优化开源大模型的活跃技术社区。


## 11. 播客与访谈录音 (Podcast Interviews)

- [Paul Iusztin：AI 工程师的技能栈、Agent、LLMOps 以及如何交付 AI 产品](https://datatalks.club/podcast/s23e01-ai-engineering-skill-stack-agents-llmops-and-how-to-ship-ai-products.html) —— 探讨如何超越简单的 API 调用构建作品集，收录于 DataTalks.Club。
- [Ranjitha Kulkarni：开发智能体 AI 系统——工具、数据检索与科学评测](https://datatalks.club/podcast/building-agentic-ai-engineering-tooling-retrieval-evaluation.html) —— 智能体设计实战、上下文工程、RAG 的折中妥协与评测方法，收录于 DataTalks.Club。
- [Micheal Lanham：从游戏 AI 到 LLM 智能体——多智能体系统 20 年的演化历程](https://datatalks.club/podcast/from-game-ai-to-modern-ai-agents.html) —— 讲解智能体编排模式（顺序、编排、协作）和转型指导，收录于 DataTalks.Club。
- [通关数据科学求职面试的全流程经验分享](https://www.youtube.com/watch?v=jYYR1fH8k7o) —— 涵盖人脉社交、投递、技术各轮次考察及薪资谈判。
- [资深工程师分享：大模型 AI 工程师面试高频提问](https://www.youtube.com/watch?v=leXRiJ5TuQo) —— 经历 22 轮面试官经历的复盘，详解“时延-成本-相关性”三角定律与 HyDE 检索。
- [Exponent：FAANG 资深工程师主持的 AI 辅助编码模拟面试](https://www.youtube.com/watch?v=C6CdzcU7I18) —— 演示如何使用 Claude Code 协同完成编码，包含面试官对于 AI 使用的评分细则。
- [Fahd Mirza：如何备战 AI/LLM 工程师面试](https://www.youtube.com/watch?v=Zt-h5BiBWH0) —— 剖析英伟达、谷歌、亚马逊面试中的必考概念。
- [微软 AI 工程师 ML 模拟面试实录](https://www.youtube.com/watch?v=ZE_YEn-okfk) —— 实时音频转录系统设计与 Manager 级别回馈。


## 12. 业界核心领军人物 (Key Practitioner Voices)

- [Chip Huyen](https://huyenchip.com/) —— 畅销书《Designing ML Systems》与《AI Engineering》的作者，斯坦福大学讲师。
- [Eugene Yan](https://eugeneyan.com/writing/llm-patterns/) —— Anthropic 技术专家，总结了大模型系统常见技术模式与[如何进行技术面试](https://eugeneyan.com/writing/how-to-interview/)的指导。
- [Shreya Shankar](https://www.sh-reya.com/) —— AI 评估领域研究者，代表作 [《坚定维护 AI 评测的合理性 (In Defense of AI Evals)》](https://www.sh-reya.com/blog/in-defense-ai-evals/)。
- [Hamel Husain](https://hamel.dev/blog/posts/evals/) —— 前 Airbnb/GitHub 核心工程师，大模型评测权威，代表作 [《LLM 评测 FAQ》](https://hamel.dev/blog/posts/evals-faq/) 与 [《大模型作为裁判 (LLM-as-Judge)》](https://hamel.dev/blog/posts/llm-judge/)。
- [Swyx (Shawn Wang)](https://www.latent.space/p/ai-engineer) —— Latent Space 创办者，代表作 [《AI 工程师的崛起 (Rise of the AI Engineer)》](https://www.latent.space/p/ai-engineer) 与 [《智能体工程 (Agent Engineering)》](https://www.latent.space/p/agent)。
- [Andrej Karpathy：2025 大语言模型年度盘点](https://karpathy.bearblog.dev/year-in-review-2025/) —— 写于 2025 年 12 月。
- [Pragmatic Engineer 专访 Chip Huyen：探讨 AI 工程的现状与未来](https://newsletter.pragmaticengineer.com/p/ai-engineering-with-chip-huyen)。
- [Gergely Orosz：2025 年利用 LLM 辅助软件开发路线展望](https://newsletter.pragmaticengineer.com/p/software-engineering-with-llms-in-2025)。


## 13. Hacker News & Reddit 深度技术讨论

- [Show HN：面向 AI 产品工程师的高水准面试题库](https://news.ycombinator.com/item?id=44875256) —— 包含 500 多道面试题，按 4 个难度层级拆解了从提示词到智能体架构的知识点。
- [100 道大模型面试真题汇总](https://news.ycombinator.com/item?id=46319888) —— 聚焦模型底层架构与推理工程。
- [Eugene Yan：如何面试并筛选优秀的 ML/AI 工程师](https://eugeneyan.com/writing/how-to-interview/) —— 企业招聘时的核心考察指标。
- [Ask HN：2025 年底的典型技术面试是什么样的？](https://news.ycombinator.com/item?id=45904921) —— 探讨大模型时代如何调整开发岗位的面试形式。
- [Ask HN：在大模型时代，你怎么做技术编码面试？](https://news.ycombinator.com/item?id=42268158) —— 探讨面试形式向“审查并重构 AI 生成代码”转变的实践。
- [Ask HN：LeetCode 手撕代码面试要凉了吗？](https://news.ycombinator.com/item?id=44878265) —— 围绕 LeetCode 面试有效性的激烈交锋。
- [r/leetcode：xAI 工程师（后端与底座）求职面试流程全复盘](https://www.reddit.com/r/leetcode/comments/1pjhw1i/xai_ai_engineer_backendinfra_interview_just/) —— 包含 2 道 Medium 级手撕题和分布式系统架构拷问。
- [r/LangChain：我的 LangGraph 智能体项目在机器学习面试中被面试官狂怼](https://www.reddit.com/r/LangChain/comments/1k662xc/got_grilled_in_an_ml_interview_today_for_my/) —— 评审专家组对其多轮迭代评测的合理性进行狂轰滥炸式提问。
- [r/cscareerquestions：AI 工程师真实的求职流程是怎样的？](https://www.reddit.com/r/cscareerquestions/comments/1lmwq1e/whats-the_ai_engineering_hiring_process_like/) —— 模型路由选择、应对过拟合等高频问题。
- [r/cscareerquestions：Take-home 面试作业允许用 AI 吗？](https://www.reddit.com/r/cscareerquestions/comments/1ggsp30/take_assignment_use_ai/) —— 探讨在离线作业中合理运用 Copilot 的边界。
- [r/cscareerquestions：离线编程作业完全是一场闹剧](https://www.reddit.com/r/cscareerquestions/comments/1b25o1e/take_home_assessments_are_a_joke/) —— 候选人抱怨某些超长作业的心声。
- [r/datascience：如何科学备战 AI 工程师面试？](https://www.reddit.com/r/datascience/comments/1ovf9k2/how_to_prepare_for_ai_engineering_interviews/) —— 系统设计考点与 OpenAI 的经典落地案例分析。
- [r/ycombinator：你们公司给 AI 工程师出什么面试题？](https://www.reddit.com/r/ycombinator/comments/1jnfijm/what_is_your_interview_assignment_for_ai_engineers/) —— 众多初创公司创始人分享各自的筛选策略。
- [r/developersIndia：我的印度机器学习工程师面试汇总复盘](https://www.reddit.com/r/developersIndia/comments/1q065gd/my_ml_engineer_interviews_compilation_along_with/)。
- [r/developersIndia：Eightfold.ai 智能体 AI 工程师面试避坑指南](https://www.reddit.com/r/developersIndia/comments/1pbaj11/need_advice_for_eightfoldai_agentic_ai_engineer) —— 第一轮包含硬核的 AI 机器监考挑战。
- [r/LocalLLaMA：因为没用 LangChain/LangGraph，我面试被挂了？](https://www.reddit.com/r/LocalLLaMA/comments/1ow3anq/rejected_for_not_using_langchainlanggraph/) —— 围绕是否绑定特定开发框架的技术辩论。
- [r/learnmachinelearning：挂了人生第一场机器学习手撕算法面试](https://www.reddit.com/r/learnmachinelearning/comments/1gvceaj/failed_first_coding_machine_learning_interview/) —— 探讨被要求从零手写反向传播的场景。
- [r/usajobs：美国财政部 AI 工程师 Take-home 作业提交后惨遭 Ghost 默拒](https://www.reddit.com/r/usajobs/comments/1qoolmw/am_i_being_ghosted_after_a_takehome_assignment_for/)。
- [r/developpeurs：面试官居然要求我在作业里构建一个完整的 LLM 智能体](https://www.reddit.com/r/developpeurs/comments/1m84v47/on_ma_demand%C3%A9_de_construire_un_agent_llm_complet/) —— 探讨面试作业的工作量边界。
- [r/ArtificialInteligence：AI 工程师高频面试真题与流程归纳](https://www.reddit.com/r/ArtificialInteligence/comments/1nybfr8/ai_engineer_interview_questions/)。
- [r/datascience：挂了一个只会滔滔不绝谈大模型的候选人](https://www.reddit.com/r/datascience/comments/15t69mt/failed_an_interviewee_because_they_wouldnt_shut/) —— 警示录：大模型炒作与工程落地能力错位的负面典型。
- [r/datascience：亚马逊 L6 级大模型工程师面试经验分享](https://www.reddit.com/r/datascience/comments/1jrdrpx/ml_engineer_genai_amazon/) —— 针对 GenAI 创新中心的通关复盘。
- [r/generativeAI：如何通关 AI/GenAI/RAG/LLM 方向面试](https://www.reddit.com/r/generativeAI/comments/1p4yrjk/how_to_clear_interviews_in_ai_gen_rag_llm/) —— 提供包含基础概念、系统设计、口头表达与质量评测的四维准备框架。
- [r/learnmachinelearning：我如何通关 AI 工程师面试](https://www.reddit.com/r/learnmachinelearning/comments/1pwvb5a/how_i_cracked_an_ai_engineer_role/) —— 从普通软开转型为 AI 开发者的详细学习路径。
- [r/learnmachinelearning：生成式 AI 常见面试考核方向](https://www.reddit.com/r/learnmachinelearning/comments/1ppgsf3/interview_questions_gen_ai) —— 梳理了咨询公司常见的大模型技术考核象限。
- [r/ExperiencedDevs：这种离线 Take-home 作业正在成为招聘常态吗？](https://www.reddit.com/r/ExperiencedDevs/comments/1nyzx77/is_this_type_of_takehome_assignment_becoming_the/) —— 吐槽某些创业公司借面试套白嫖代码作业的讨论。
- [r/datascience：2025 年技术面试现状全景剖析](https://www.reddit.com/r/datascience/comments/1p1dklk/state_of_interviewing_2025_heres_how_tech/) —— 数据驱动型分析，梳理了 2020-2025 五年间技术面试形式的变迁。
- [r/csMajors：微软 2026 暑期 Applied AI/ML 实习面试](https://www.reddit.com/r/csMajors/comments/1nqfzhq/microsoft_swe_applied_aiml_summer_2026_redmond) —— 包含人工与 AI 混合的多轮编码考核。
- [r/leetcode：2026 面试备战（14年+工作经验老兵）](https://www.reddit.com/r/leetcode/comments/1q06zz6/2026_interview_prep) —— 资深架构师视角下，如何准备高并发和大模型 API 集成考点。
- [r/MachineLearning：备战谷歌 DeepMind Gemini 团队面试](https://www.reddit.com/r/MachineLearning/comments/1k8gy12/d_preparing_for_a_deepmind_gemini_team_interview/) —— 包含分布式训练、系统架构与文化匹配轮。


## 14. 行业招聘市场数据与趋势

- [InterviewQuery：2025 AI 求职趋势分析](https://www.interviewquery.com/p/ai-interview-trends-tech-hiring-2025) —— 指出 AI 招聘需求飙升 240%，大模型相关问题翻了三倍。
- [LockedIn AI：硅谷大厂（OpenAI/Anthropic/谷歌/Scale AI）高频大模型面试题汇总](https://www.lockedinai.com/blog/llm-ai-engineer-interview-questions-silicon-valley)。
- [InterviewNode：2026 机器学习面试新演变](https://www.interviewnode.com/post/ai-interview-evolution-what-2026-will-look-like-for-ml-engineers) —— 解析混合 AI 系统打分的面试趋势。
- [Pragmatic Engineer：技术招聘是否走到了历史拐点？](https://blog.pragmaticengineer.com/tech-hiring-is-this-an-inflection-point/) —— 针对通过 AI 简历造假和面试作弊泛滥的技术博弈分析。
- [Interviewing.io 独家调研：AI 是如何重构面试流程的](https://interviewing.io/blog/how-is-ai-changing-interview-processes-not-much-and-a-whole-lot) —— 对 67 位 FAANG 面试官进行调研，发现“几乎没有公司因为大模型流行而彻底放弃算法轮”。
- [Karat 报告：迎接 2025 —— AI 是如何改写软件开发岗位招聘的](https://karat.com/how-ai-is-changing-software-engineer-hiring-heading-into-2025/)。
- [Indeed 招聘实验室：2025 年度 AI 行业岗位重塑报告](https://www.hiringlab.org/2025/09/23/ai-at-work-report-2025-how-genai-is-rewiring-the-dna-of-jobs/) —— 生成式 AI 是如何深刻重写不同工作岗位的技能构成的。


## 15. 传统机器学习系统设计与面试 (ML System Design & Interviews)

此部分收集传统的机器学习（非生成式 AI）面试准备资源 —— 涉及经典系统设计、ML 基础设施以及 ML 工程师岗位备战。

### 从业者经验
- [Yuan Meng：机器学习面试 2.0 版](https://www.yuan-meng.com/posts/mle_interviews_2.0/) —— 记录了Databricks、Notion、OpenAI、Netflix 的真实面试，并重点记录了新出现的“ML 基础设施”与“大模型应用开发”轮次。
- [Yuan Meng：机器学习基础设施系统设计面试专题](https://www.yuan-meng.com/posts/ml_infra_interviews/) —— 解析 Netflix、Snap、Notion、DoorDash 的 ML Infra 面试真题。
- [Brian Kihoon Lee：关于 AI/ML 工程师招聘的反思](https://www.moderndescartes.com/essays/ml_eng_interviewing/) —— 探讨传统系统设计面试的局限，并给出优化替代方案。
- [Aliaksei Mikhailiuk：通关机器学习系统设计面试](https://towardsdatascience.com/cracking-machine-learning-system-design-interviews/) —— 作者为 Snap 技术 Lead，写于 2025 年 11 月。
- [Mengliu Zhao：2024 年 ML 工程师面试生存指南](https://towardsdatascience.com/2024-survival-guide-for-machine-learning-engineer-interviews-e74eccef4645/) —— 生成式 AI 浪潮下传统 ML 岗位的面试变迁。
- [我如何斩获 4 份数据科学 Offer 并在被裁两个月内让收入翻倍的经验](https://medium.com/data-science/how-i-got-4-data-science-offers-and-doubled-my-income-2-months-after-being-laid-off-b3b6d2de6938)。
- [横扫数据科学 Take-home 作业面试的 12 项心法](https://medium.com/data-science/how-to-crush-your-data-take-home-interview-a0b9f7c97d6) —— 总结自 4 年作业评审经验。

### 框架指南
- [Chip Huyen：机器学习系统设计经典习题集](https://huyenchip.com/machine-learning-systems-design/exercises.html)。
- [Backprop：FAANG 大厂 ML 系统设计通关框架](https://www.trybackprop.com/blog/ml_system_design_interview)。
- [HelloInterview：快速冲刺机器学习系统设计面试](https://www.hellointerview.com/learn/ml-system-design/in-a-hurry/introduction) —— 结构化表达框架。
- [Exponent：2026 版机器学习系统设计指南](https://www.tryexponent.com/blog/machine-learning-system-design-interview-guide) —— 由 Meta ML 工程师亲自撰写。

### 传统 ML 图书
- **《Designing Machine Learning Systems》** (O'Reilly, 2022) —— Chip Huyen 著。详细剖析传统机器学习生命周期。
- **《Machine Learning System Design Interview》** (2022) —— Ali Aminian 与 Alex Xu 著。包含 10 个经典的传统 ML 设计面试题。

### 经典案例库
- [GitHub 仓库：机器学习面试系统设计专项](https://github.com/alirezadir/machine-learning-interviews/blob/main/src/MLSD/ml-system-design.md)。
