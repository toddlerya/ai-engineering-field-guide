# AI 系统设计面试

AI 系统设计面试正迅速演变为一个独立的技术面试类别，它与传统的“软件系统设计（System Design）”以及传统的“机器学习系统设计（MLSD）”均有着明显的区别。这一转变是由生成式大模型产品的爆发驱动的：**现在的重心不再是设计庞大的模型训练流水线，而是围绕现成的商业/开源底座模型设计高可用的流控与编排系统（Orchestration）。**

Doctolib（“AI System Design Interview”）、Sprinter Health（“AI-Focused Systems Design”）以及 Anthropic（考核高并发大模型推理）等公司均设立了专门的 AI 系统设计轮。谷歌、苹果、OpenAI、Cohere、Salesforce 等公司也在现有的系统设计中疯狂加入大模型元素。 [^igotanoffer]

面试官主要考核候选人如何面对非确定性（Non-deterministic）输出设计稳定服务、如何打通数据安全与合规隔离，以及如何让系统在高负载下进行横向扩容（可能需要扩容 5-10 倍，节点数突破 1000+ 台服务器）。


## 1. 结构与时间分配

通常为 **45 到 60 分钟**。你需要在现场主动驱动整个技术演进过程： [^designgurus]
- **理清系统需求、数据规模与边界指标**（约 5 分钟）。
- **画出宏观的系统架构图**（10-15 分钟）。
- **对核心模块进行技术深挖**（如向量索引、Agent 状态管理）（15-20 分钟）。
- **深入讨论系统瓶颈、容错机制与降级策略**（5-10 分钟）。
- 应对面试官追加的 follow-up 情景题。

### 现场呈现形式：
- **白板/虚拟画板现场画图**（如使用 Excalidraw 或 Miro）绘制系统组件及数据流向。
- **纯口头架构阐述**，面试官在过程中就特定区域（如一致性哈希、缓存失效）展开技术拷问。


## 2. 面试高频问题

### A. 大模型应用层系统设计 (AI System Design)
*侧重于大模型 API 的流控、RAG、Agent 编排与工程调优。*

- **高并发客服助手**：如何设计一个能支撑日均 100 万用户的高并发 AI 聊天助手，并详细进行成本与时延折中估算？ [^igotanoffer] [^designgurus] [^process-analysis] [^reddit-swe-to-ai]
- **企业级 Document Q&A / RAG 服务**：如何为一个拥有千万级法律/医学合同文档的企业设计高精度的 RAG 智能问答系统？ [^bhavishya-pandit] [^reddit-eightfold-ai]
- **智能代码辅助 Copilot**：设计类似于 GitHub Copilot 的实时代码补全与推荐系统（侧重极低时延控制）。 [^colin-zhou]
- **医疗语音助手**：设计一个部署在医院病房的语音录入助手（需重点解决噪音干扰、患者隐私合规、超低延迟响应以及医学专业词汇识别）。 [^bhavishya-pandit]
- **合规合同生成器**：设计一个可以自动解析条款并按严格合规标准自动生成法律合同的智能系统。 [^bhavishya-pandit]
- **智能猎头推荐系统**：设计一个 AI 驱动的候选人简历自动筛选与岗位精准推荐系统。 [^colin-zhou] [^bhavishya-pandit]
- **海量票据信息抽取**：设计一个能处理每月 10,000+ 用户上传单据（银行流水、身份证复印件等）的自动化 OCR 与大模型信息清洗系统。 [^igotanoffer]
- **诊疗费率自动申报**：设计一个能够自动读取医生病历笔记，并按照规范将计费代码精准匹配发送给保险公司的系统。 [^igotanoffer]
- **基于记忆的个性化助手**：设计 ChatGPT 跨越不同对话窗口（Cross-conversation）的长期记忆与个性化偏好存储系统。 [^igotanoffer]
- **多步工作流 Agent**：设计一个能够自动协调多名 Agent（如会议日程助手、代码审核助手、营销邮件助手）协同工作的流程引擎。 [^promptlayer]
- **AI 安全内容风控**：设计一个能够实时拦截有害提示词输入、或大模型违规内容生成的安全风控网关（Shield）。 [^igotanoffer]
- **多源数据统一智能检索**：设计一个能横跨邮件、日历、云文档以及即时通讯软件的统一语义搜索引擎。 [^x-avi-chawla-1]
- **AI 实时搜索搜索引擎**：设计类似于 Perplexity.ai 的实时联网大模型问答引擎。 [^colin-zhou]

### B. 底层大模型推理与基建 (AI Serving & Platforms)
*偏向底层硬核工程，涉及 GPU 调度、高并发 Serving。*

- 你们在架构上是如何处理**实时数据流更新 vs 离线批量处理**的？它们各自的技术取舍是什么？ [^proptech-founder-2]
- 针对海量的结构化数据、无结构文本以及流式事件数据，你们是如何设计统一的数据清洗灌入系统的？ [^proptech-founder-1]
- 设计一个日均处理千万级请求的高性能分布式图像生成（如 SD / Flux）流水线。 [^interviewnode]
- 设计一个支持断点续训（Checkpointing）、弹性抢占与高可用调度的分布式 GPU 训练队列系统（支持 10 万+卡并发作业）。 [^reddit-xai-eng]
- 设计一个高可用的大模型托管推理平台（包括动态批处理 Dynamic Batching、GPU 水平扩容、模型版本灰度管理以及输出缓存）。 [^designgurus]


## 3. 什么是 AI 系统设计 vs 传统系统设计

### 核心演变：
传统机器学习的硬伤在于特征工程和漫长的模型训练。而当大模型 API 普及后，**大模型工程的挑战转移到了系统编排、流控降级和 RAG 链路质量治理上**。 [^chip-huyen-books]

### 两者的技术差异对比：

| 考查维度 | 传统机器学习系统设计 (MLSD) | 大模型/AI 系统设计 (GenAI SD) |
|---|---|---|
| **技术重心** | 模型训练、特征提取流水线、参数调优 [^chip-huyen-platform] | 大模型应用编排、上下文工程、数据召回质量 [^chip-huyen-platform] |
| **数据痛点** | 特征工程、实时特征存储、训练-推理偏差 [^yuan-meng] | 文本切片策略、语义检索精准度、向量嵌入对齐 [^yuan-meng] |
| **模型输出** | 确定性的强类型（如概率分值、预测分类） [^brian-kihoon-lee] | 非确定性的自由文本、生成的代码、多模态媒体 [^brian-kihoon-lee] |
| **系统评测** | 固定的验证集评测 (F1-score, AUC, MAP) | 大模型裁判 (LLM-as-judge)、人类评估、实时指标 [^promptlayer] |
| **成本消耗** | 相对高昂的模型训练费，推理费用可控 | 持续高昂的按 Token 收费、向量数据库并发成本 |
| **失败模式** | 特征漂移、过拟合 [^interviewnode] | 严重幻觉、恶意越狱、上下文过长导致遗忘、账单爆炸 [^interviewnode] |
| **迭代周期** | 较慢（重新收集数据并触发模型重训） | 极快（直接修改系统提示词，优化检索算子） |

### 机器学习系统设计 (MLSD) 经典题目：
- 设计一个个性化新闻推荐系统。
- 设计一个线上信用卡防欺诈交易检测系统。
- 设计一个垃圾邮件拦截分类器。
- 设计一个搜索引擎相关性排序系统。
- 设计一个广告点击率 (CTR) 预估系统。

*注：生成式 AI 面试中依然会考查传统的分布式架构知识，但面试官会大幅压缩传统存储的篇幅，而把大量时间用在拷问评测方案、安全防越权、上下文召回妥协以及工具沙箱设计上。 [^igotanoffer]*

### 传统软件系统设计 (System Design) 经典题目 (OpenAI L5等大厂常考)：
- 设计一个分布式 KV 存储系统 (DynamoDB)。 [^colin-zhou]
- 设计一个高并发分布式限流器 (Rate Limiter)。 [^colin-zhou]
- 设计 GitHub Actions 持续集成流水线引擎。 [^hellointerview]
- 设计一个支持全球联机对战的国际象棋系统。 [^hellointerview]
- 设计 Instagram / TikTok / X 的核心 Feed 流系统。 [^colin-zhou]
- 设计 Netflix / YouTube 的全球视频流分发与加速平台。 [^colin-zhou]
- 设计 Uber 派单与打车后台（涉及地理网格匹配、ETA 计算和动态加价）。 [^colin-zhou]
- 设计 WhatsApp / 微信级别的全球即时通讯系统。 [^colin-zhou]
- 设计 Google Docs 多人实时协同编辑系统。 [^colin-zhou]


## 4. 如何通关设计面试

### A. 结构化你的论述步骤
建议在现场的 45 分钟内套用以下五步框架 [^igotanoffer]：
1. **理清边界条件 (5-10分钟)** —— 确认并发量、Token 限制、回答准确度标准、安全护栏红线。
2. **画出宏观数据流 (10-15分钟)** —— 从用户输入 $\rightarrow$ 安全过滤 $\rightarrow$ RAG 检索 $\rightarrow$ 大模型推理 $\rightarrow$ 结果解析输出的完整骨架。
3. **针对核心组件深挖 (20-30分钟)** —— 详解数据切片方案、召回算法、记忆数据库选择、LLM-as-judge 设计。
4. **讨论架构妥协与容错 (10-15分钟)** —— 详述如果大模型挂了怎么优雅降级、首字延迟过高怎么优化、怎么拦截幻觉。
5. **系统总结与未来演进** —— 总结核心风险，指出下一步的技术优化点。

### B. 熟练掌握 4 类核心系统模式 [^interviewnode]
- **RAG 架构** —— 大模型外挂知识库的最佳实践（目前最常考的模式）。
- **反馈闭环 (Feedback loop)** —— 如何将用户点赞、点踩、修改代码等交互数据清洗后，形成持续优化的强化学习数据飞轮。
- **幻觉科学控制** —— 怎么通过检索数据强制约束大模型的瞎编、设计可信度打分算法。
- **成本与延迟极致压缩** —— 语义缓存设计、长文本提示词压缩、多级模型智能路由分流。

### C. 熟知业界大厂的真实生产案例
多阅读各大厂的技术博客，将他们的实践直接作为你面试时的弹药：
- **Doctolib 智能客服**：使用 LangGraph 状态机，将客服工作流设计为有向图上的 specialized agents 协作网络，日均吞吐 1.7 万条消息。 [^doctolib]
- **Uber 推理网关 (GenAI Gateway)**：设计了统一的网关层托管大模型，内部包含自动敏感信息脱敏（PII Redactor），支撑了内部 60+ 个业务场景。 [^uber]
- **Airbnb 智能助理**：深度引入 CoT（思维链）推理链条，并在数据层配置了极严厉的模型护栏监控。 [^airbnb]
- **Perplexity 实时搜索**：日均处理 2 亿次检索，数据索引构建在 Vespa.ai 向量检索上，大模型调用其微调后的 Sonar 专用模型。 [^bytebytego-perplexity]
- **Slack AI 架构**：采用无状态 RAG 检索，将大模型托管在完全隔离的宿主 VPC (escrow VPC) 中，彻底解决企业客户的数据安全顾虑。 [^slack]
- **LinkedIn 智能体平台**：开发了专用的 Agent 状态流转引擎，在数据访问层设计了极其严格的租户沙箱隔离。 [^linkedin]
- **Anthropic 智能体科研系统**：采用 Orchestrator-Worker（编排者-执行者）多智能体架构。由 Opus 模型负责主控规划，Sonnet 模型作为子节点执行具体任务。该场景消耗的 Token 数量高达常规单次聊天的 15 倍。 [^anthropic-multi-agent]
- **DoorDash 自动评测飞轮**：针对复杂的餐饮对话机器人开发了全自动的模拟评测平台，并引入了多层分级的级联 RAG 架构。 [^doordash]

### 面试高频扣分雷区：
- **急于画图**。没问清目标用户是谁、日活多少、对首字延迟要求是多少，上来就画架构图。 [^igotanoffer]
- **把大模型当做数据库**。没有主动设计检索组件，指望大模型把所有的历史数据强行塞进 context window 里硬答。 [^interviewnode]
- **设计“过于理想化”**。整张图上全都是顺畅的运行流，完全没有展示模型挂了怎么退化、费用超标怎么熔断、输出乱码怎么拦截的防错设计。 [^igotanoffer]
- **言必称框架**。只会说“*这里我直接用 LangChain / LangGraph 解决*”，但说不清如果脱离了这些框架，系统底层在做怎样的多线程等待和状态流转。 [^interviewnode]
- **完全没有成本与时延概念**。没有估算单次请求耗费多少 token 费用，忽略了多轮交互在大并发下会导致服务器瞬间宕机或账单爆炸。 [^igotanoffer]
- **忽略安全设计**。允许智能体直接去执行生成的 SQL 或 terminal 命令，没有隔离的沙箱或人工审核逻辑。 [^igotanoffer]
- **将控制流放在提示词里**。试图通过在 prompt 里写“*请不要无限循环*”来约束 Agent，而不是在外部代码层设计计数器限制。 [^techeon]
- **滥用智能体**。对于明明可以用简单状态机（State Machine）或一段 if-else 解决的逻辑，非要引入高成本、不确定性极高的多智能体协作网络。 [^techeon]

---

## 引用源说明

[^igotanoffer]: [IGotAnOffer - Generative AI System Design Interview](https://igotanoffer.com/en/advice/generative-ai-system-design-interview)
[^chip-huyen-books]: [Chip Huyen - AI Engineering](https://huyenchip.com/books/)
[^chip-huyen-platform]: [Chip Huyen - Building a Generative AI Platform](https://huyenchip.com/2024/07/25/genai-platform.html)
[^yuan-meng]: [Yuan Meng - MLE Interviews 2.0](https://www.yuan-meng.com/posts/mle_interviews_2.0/)
[^brian-kihoon-lee]: [Brian Kihoon Lee - ML Eng Interviewing](https://www.moderndescartes.com/essays/ml_eng_interviewing/)
[^promptlayer]: [PromptLayer - The Agentic System Design Interview](https://blog.promptlayer.com/the-agentic-system-design-interview-how-to-evaluate-ai-engineers/)
[^bhavishya-pandit]: [Bhavishya Pandit - 7 Deep-Cut AI System Design Interview Questions](https://bhavishyapandit9.substack.com/p/7-deep-cut-ai-system-design-interview)
[^techeon]: [TechEon - The Complete Agentic AI System Design Interview Guide 2026](https://atul4u.medium.com/the-complete-agentic-ai-system-design-interview-guide-2026-f95d0cfeb7cf)
[^designgurus]: [DesignGurus - OpenAI System Design Interview Questions](https://www.designgurus.io/blog/openai-system-design-interview-questions)
[^hellointerview]: [HelloInterview - OpenAI L5 Interview Guide](https://www.hellointerview.com/guides/openai/l5)
[^interviewnode]: [InterviewNode - GenAI System Design Interview Patterns](https://www.interviewnode.com/post/generative-ai-system-design-interview-patterns-you-should-know)
[^anthropic-multi-agent]: [Anthropic - Multi-Agent Research System](https://www.anthropic.com/engineering/multi-agent-research-system)
[^proptech-founder-1]: [YouTube - Proptech Founder Part 1](https://www.youtube.com/watch?v=leXRiJ5TuQo)
[^doctolib]: [Doctolib - Building an Agentic AI System for Healthcare Support](https://medium.com/doctolib/building-an-agentic-ai-system-for-healthcare-support-a-journey-into-practical-ai-implementation-0afd28d716e6)
[^uber]: [Uber - GenAI Gateway](https://www.uber.com/blog/genai-gateway/)
[^airbnb]: [Airbnb Engineering - Automation Platform v2](https://medium.com/airbnb-engineering/automation-platform-v2-improving-conversational-ai-at-airbnb-d86c9386e0cb)
[^bytebytego-perplexity]: [ByteByteGo - How Perplexity Built an AI Google](https://blog.bytebytego.com/p/how-perplexity-built-an-ai-google)
[^slack]: [Slack Engineering - How We Built Slack AI](https://slack.engineering/how-we-built-slack-ai-to-be-secure-and-private/)
[^linkedin]: [InfoQ - QCon AI LinkedIn](https://www.infoq.com/news/2025/12/qcon-ai-linkedin/)
[^doordash]: [DoorDash - Simulation Evaluation Flywheel](https://careersatdoordash.com/blog/doordash-simulation-evaluation-flywheel-to-develop-llm-chatbots-at-scale/)
[^colin-zhou]: [Medium - Colin Zhou](https://levelup.gitconnected.com/how-i-fought-and-passed-technical-interviews-with-llms-in-2025-f328e9df8e84)
[^process-analysis]: [Process Analysis - Reddit r/cscareerquestions](https://www.reddit.com/r/cscareerquestions/)
[^proptech-founder-2]: [YouTube - Proptech Founder Part 2](https://www.youtube.com/watch?v=Zt-h5BiBWH0)
[^reddit-eightfold-ai]: [Reddit - Need Advice for Eightfold.ai Agentic AI Engineer](https://www.reddit.com/r/developersIndia/comments/1pbaj11/need_advice_for_eightfoldai_agentic_ai_engineer) (r/developersIndia)
[^reddit-swe-to-ai]: [Reddit - From Software Developer to AI Engineer](https://www.reddit.com/r/learnmachinelearning/comments/1pzcw2y/from_software_developer_to_ai_engineer_the_exact/) (r/learnmachinelearning)
[^reddit-xai-eng]: [Reddit - xAI AI Engineer Backend/Infra Interview](https://www.reddit.com/r/leetcode/comments/1pjhw1i/xai_ai_engineer_backendinfra_interview_just/) (r/leetcode)
[^x-avi-chawla-1]: [X - Avi Chawla, Unified Query Engine (Google)](https://x.com/_avichawla/status/1986320178783867036)
