# 大模型与机器学习理论面试题

本章内容汇总自 Reddit、X 以及各大技术博客中，求职候选人在真实 AI 工程师面试中被问到的**理论概念类问题**（包括：“什么是 X？”、“X 是如何工作的？”、“请解释 Y”）。


## 1. 理论面试环节形式

通常为 **45 到 60 分钟的口头技术交流**。面试官会抛出一系列概念性或情景模拟问题，来探测你对大模型/机器学习底层的真实理解。该环节一般不包含上机编程或现场写算法，完全是双向的口头深入讨论。

理论概念很少作为一个完全独立的面试轮次出现。它们通常被揉进其它轮次中：如系统设计、项目深挖或专门的 AI/ML 技术初筛。虽然少数公司会有标明为“LLM 理论”或“AI 深度拷问”的轮次，但更常见的情况是，当你在聊项目时随口提到某个概念，面试官会立即打断并就该概念进行追问，以此测试你的知识深度。


## 2. 核心面试真题

### A. 大模型应用基础 (LLM Practice)
*侧重于大模型的外在行为控制与调用机制，不涉及太深层的神经网络数学推导。*

- 大语言模型（LLM）是如何生成文本的？ [^proptech-founder-2]
- 什么是 Temperature（温度）和 Top-p 采样解码？它们如何具体影响模型的输出？ [^fahd-mirza] [^reddit-genai-consulting] [^x-aryyann8]
- 什么是上下文窗口 (Context Window)？当输入数据超出窗口限制时会发生什么？你会怎么处理长文本输入？ [^fahd-mirza] [^exponent-openai-ml] [^hn-46319888] [^llmgenai]
- 在长对话或多步骤任务中，你如何为大模型进行记忆管理 (Memory Management) 与上下文精简控制？ [^reddit-ai-eng-questions]

### B. RAG（检索增强生成）系统 (RAG Systems)
*将大模型与企业私有知识库连接，使其基于特定数据进行回答。*

- 什么是 RAG？请完整阐述其从数据向量化到最终生成的全流程。 [^khushal-kumar] [^reddit-ai-eng-questions] [^reddit-genai-consulting]
- 传统的关键字/全文检索 vs 向量语义检索。这两者有什么区别？你会在什么场景下分别使用它们？ [^reddit-clear-genai]
- 现需要为一份长达数百页且包含大量图表的 PDF 财务报表开发问答系统，你会如何设计其文档解析和切片（Chunking）流水线？ [^proptech-founder-1]
- 如果检索出的上下文内容里完全没有包含用户问题的答案，你该如何设计架构以防止模型凭空捏造（幻觉）回答？ [^proptech-founder-2]
- RAG 系统在生产环境下最常见的失效痛点有哪些？你平时是如何进行排障和调优的？ [^reddit-clear-genai] [^reddit-grilled-rag] [^x-athletickoder-2]
- 在 RAG 系统中，你如何实现精确的引用（Citations）与来源追溯标注？ [^proptech-founder-1]
- 什么是语义缓存 (Semantic Caching)？它是如何帮助降低成本和延迟的？ [^designgurus-rag] [^hn-44796765]
- 当知识库文章规模突破 1000 万篇以上时，你如何扩容和优化 RAG 系统？ [^bhavishya-pandit]
- 设计 RAG 系统时，最重要的技术权衡（Trade-offs）有哪些？ [^reddit-genai-product]

### C. 智能体与工具调用 (Agents and Tool Use)
*基于大模型推理、能自主决策并使用外部工具的复杂闭环系统。*

- 是什么特质让一个 AI 系统被定义为“智能体 (Agentic)”？ [^techeon] [^reddit-ai-agentic] [^reddit-devsindia-genai] [^hn-43884713] [^hn-42431361] [^x-aryyann8] [^process-analysis]
- 除了作为大脑的大模型之外，一个完整的智能体系统还必须配备哪些核心工程组件？ [^techeon] [^reddit-expdevs-agentic] [^reddit-ai-agentic]
- 智能体是如何判断何时该调用工具，以及选择调用哪一个工具的？ [^techeon] [^reddit-csuk-agents] [^reddit-aiagents-prep]
- 在什么业务场景下，引入智能体反而是糟糕或过度设计的方案？ [^techeon] [^reddit-csuk-agents]
- 你如何向非技术的业务部门（Stakeholders）通俗解释智能体系统的工作原理和决策边界？ [^techeon] [^reddit-expdevs-agentic]
- 如何设计程序检测并强行终止智能体陷入的“死循环任务规划 (Infinite planning loops)”？ [^techeon] [^reddit-csuk-agents] [^reddit-expdevs-agentic]
- 对于长期在后台运行（Long-running）的自主智能体，如何优雅地定义和执行任务终止条件（Termination conditions）？ [^techeon]
- 为了防止大模型生成恶意的 shell 命令或进行非法删库，你如何为工具执行过程搭建安全的沙箱隔离环境 (Sandboxing)？ [^techeon] [^reddit-expdevs-agentic]
- 当智能体调用第三方工具发生接口超时、失败或网络波动时，你如何设计容错、重试以及保证幂等性 (Idempotency)？ [^techeon] [^reddit-expdevs-agentic] [^reddit-csuk-agents] [^reddit-aiagents-prep]
- 允许大模型调用工具会带来哪些核心的安全隐患与越权风险？ [^techeon] [^reddit-expdevs-agentic] [^datainterview-mistral]
- 如何设计一个能够分析客户投诉工单、自动草拟回复并能在遇到复杂问题时自动升级转接人工的智能体系统？ [^promptlayer]
- 如何构建一个能自动走读代码（Code Review）并给出重构和调优建议的辅助 Agent？ [^promptlayer]

### D. 系统测试与质量评估 (Testing and Evaluation)
*由于大模型生成的非确定性（Non-deterministic），这是 AI 工程中最难也最关键的 QA 环节。*

- 在非确定性的生成场景下，你如何确保大模型输出的格式一致性与事实准确性？ [^proptech-founder-1]
- 你会如何科学地评估一个 Chatbot（聊天机器人）的好坏？有哪些具体的测试维度？ [^process-analysis] [^reddit-clear-genai] [^exponent-openai] [^reddit-grilled-rag]
- 评估大模型生成表现时，你会参考哪些具体的量化指标（Metrics）？ [^proptech-founder-1] [^fahd-mirza] [^reddit-genai-product] [^reddit-llm-interview-prep]
- 你是如何从零收集和构建一个高质量的评测黄金数据集 (Golden Dataset) 的？ [^proptech-founder-1]
- 什么是模型幻觉（Hallucinations）？你有哪些工程手段来检测并拦截幻觉生成？ [^process-analysis] [^reddit-ai-eng-questions] [^reddit-genai-consulting] [^hn-41541053] [^hn-42313401] [^hn-46873753] [^system-design-handbook] [^interviewnode]
- 如何在一个大模型文档摘要系统中，坚决防止出现捏造的事实错误？ [^interviewnode]
- 如果一个线上 RAG 客服表现出“用极其自信的语气给出了完全错误的内容”，你该如何去 debug 和排查整个系统链路？ [^process-analysis] [^datainterview-mistral]
- 如何科学评估一个复杂的 RAG 多级数据检索流水线？ [^mimansa-jaiswal]
- 如何评估智能体 Agent 的运行质量？哪些指标是关键的（如工具选择准确率、任务推进行动率、上下文遵循度）？ [^reddit-aiagents-prep]

### E. 线上监控 (Monitoring)
*服务上线部署后的实时观测。*

- 大模型系统上线后，哪些业务指标与技术指标是需要被实时监控的？ [^reddit-eightfold-ai]
- 除了离线的 Golden Dataset 测试外，你如何在生产环境实时评估和监测模型的输出表现？ [^reddit-swe-to-ai]
- 在将新调优的模型全量发布前，你如何设计线上流量灰度测试（如蓝绿部署、影子模型）？ [^x-akshay-pachaar-1] [^hn-44875256]
- 线上真实的流量是千变万化的，你如何在生产环境实时量化和监控幻觉率？ [^buildml] [^llmgenai] [^hn-46959695] [^hn-42313401]
- 对于完全自主运行的后台智能体（Autonomous Agents），你如何在生产环境中追踪和可视化它们的运行轨迹和规划步骤？ [^reddit-expdevs-agentic] [^reddit-csuk-agents]

### F. 成本与时延优化 (Cost and Latency Optimization)
*让大模型应用速度更快、服务器账单更便宜。*

- 有哪些常见的手段能有效降低生成式 AI 应用的首字响应时延？ [^proptech-founder-2]
- 什么是首字响应时间 (TTFT，Time to First Token)？为什么它对用户体验至关重要？ [^proptech-founder-1]
- 在一个包含多个串行模型调用的复杂 Agent 流水线里，你如何为每一个步骤做 Benchmark 耗时统计以定位时延瓶颈？ [^proptech-founder-1]
- 你有哪些工程手段能帮公司节省大模型的 Token 开销？ [^process-analysis] [^reddit-prep-ai-eng] [^hn-46229585] [^hn-46695170] [^system-design-handbook]
- 成本 vs 回答质量的折中：在什么情况下，一个本地部署的便宜的小参数开源模型就已经“足够好”了？ [^reddit-genai-consulting] [^proptech-founder-2]
- 什么是模型分层路由 (Model Tiering)？你如何实现当遇到简单问题时分发给低成本小模型，而复杂问题路由给高级大模型的策略？ [^interviewnode] [^hn-42793253] [^hn-47150302]
- 如果你的 AI 应用日均请求量达到 100 万次，你会从哪些架构层面去压缩服务器成本？ [^process-analysis] [^fonzi-ai]
- 试估算一个企业级 RAG 检索服务（如需要检索 30 万份高度机密的法律合同）在生产环境下的月度预算构成。 [^reddit-devsindia-genai]

### G. 系统安全与合规 (Safety and Guardrails)
*防止你的 AI 系统被黑客利用、套词或产生破坏性的危害。*

- 你会在什么时候、在系统架构的什么位置配置大模型护栏组件（LLM Guardrails）？ [^proptech-founder-1]
- 怎么处理提示词和系统日志中可能泄露的个人隐私数据（PII）或机密信息？ [^reddit-genai-consulting] [^reddit-expdevs-agentic]
- 面对恶意的提示词注入（Prompt Injection）和越狱套词（Jailbreaking），你有哪些防御机制？ [^system-design-handbook] [^reddit-ai-eng-questions] [^reddit-expdevs-agentic] [^hn-44268335]
- 怎么搭建一个能够自动过滤和拦截色情、暴力或违反国家政策违规内容的双向安全过滤系统？ [^igotanoffer]
- 你们的 Agent 智能体支持生成代码并在线执行。为了防止生成并执行恶意的 `rm -rf` 指令，你如何从系统安全层进行全面设防？ [^proptech-founder-1]

---

## 3. 经典机器学习基础 (ML Fundamentals)

传统的机器学习理论（如监督/无监督学习、过拟合与欠拟合、正则化、特征工程、传统模型架构、统计学基础等）。

这部分不是 AI 工程师的考核重点，但在某些偏底层的岗位中依然会考。关于传统 ML 理论的面试题，请直接参考：
- [Data Science Interview Questions (alexeygrigorev)](https://github.com/alexeygrigorev/data-science-interviews)


## 4. 垂直深度主题 (Specialized Topics)

*以下主题在常规的 AI 工程师面试中**不会默认考查**。*

只有当岗位需求（JD）里明确提到需要模型训练、或者该岗位属于前沿算法实验室的研究型工程师（Research Engineer）时，才会被深入问到。如果岗位只要求编写大模型应用，一般不会拷问这些底层细节。

### A. 模型微调与训练 (Fine-tuning and Training)
- 在微调模型（Fine-tuning）、提示词工程（Prompt Engineering）与 RAG 架构之间，你是如何进行技术选型的？ [^process-analysis] [^reddit-prep-ai-eng] [^reddit-genai-consulting] [^x-ashutosh-1] [^system-design-handbook] [^hn-39748537]
- 什么是指令微调（Instruction Tuning）？它与基础模型的大规模预训练（Pre-training）在数据和目的上有什么区别？ [^hn-46319888] [^llmgenai] [^reddit-llm-interview-prep]
- 什么是参数高效微调（PEFT，如 LoRA）？它的数学原理是什么？在什么情况下选择 LoRA 而非全参数微调？ [^fahd-mirza] [^reddit-genai-consulting] [^x-interviewstack-meta] [^x-aryyann8] [^reddit-llm-interview-prep]
- 简述人类反馈强化学习（RLHF）的经典三阶段流程：监督微调 (SFT)、奖励模型训练 (RM) 以及 PPO 策略优化。为什么现在的 DPO（直接偏好优化）能够大幅简化这个流程？ [^proptech-founder-1]
- 解释模型量化（Quantization）的原理。在 FP16、INT8 与 INT4 之间，如何在模型大小、推理速度和计算精度上做权衡？ [^raghu-teja-2] [^reddit-llm-interview-prep]
- 线上用户隐式的交互行为（如修改了 AI 生成的代码、采纳或拒绝了 AI 的建议），如何被清洗并转化为模型二次迭代的微调训练信号？ [^bhavishya-pandit]
- 如何设计一套训练流程来教一个基座模型学会做复杂的数学推导？请从数据集收集、SFT 监督微调、RL 强化训练以及评测指标设计展开说明。 [^igotanoffer]

### B. 大模型底层理论 (LLM Theory)
- 详细解释 Transformer 架构的自注意力（Self-Attention）机制。 [^proptech-founder-2] [^reddit-genai-consulting] [^reddit-ai-eng-questions] [^process-analysis] [^sundeep-teki]
- 编码器（Encoder-only）、解码器（Decoder-only）和编解码器（Encoder-decoder）三种 Transformer 架构的区别是什么？各自的适用场景是什么？ [^tidorp] [^hn-46319888] [^reddit-llm-interview-prep]
- 什么是 KV Cache？它是怎么在自回归生成（Autoregressive Generation）中起到加速推理作用的？其内存消耗公式如何计算？ [^igotanoffer] [^reddit-llm-interview-prep]
- 什么是混合专家模型（MoE，Mixture of Experts）？它是怎么在保证计算量的同时，将模型参数规模推向万亿级的？ [^mimansa-jaiswal]
- 什么是 BPE（Byte Pair Encoding）、WordPiece 和 Character-level 字符级分词（Tokenization）？它们在处理未登录词（OOV）时各自的技术妥协是什么？ [^fahd-mirza]

---

## 5. 备战心法

- **实践经验重于理论背诵**：面试官更看重你是怎么评测系统、怎么处理脏数据、怎么在生产环境降低服务器账单的，而不是让你背诵 Transformer 的公式。
- **重点复盘 RAG 与 Agents**：确保你能流利且条理清晰地讲述 RAG 系统的全链路优化细节，以及智能体在死循环控制、工具容错沙箱上的设计方案。
- **牢记设计妥协 (Trade-offs)**：面对每一个问题，不要仅仅给出一个“正确答案”，要习惯使用“*如果看重延迟，方案 A 更好，但其劣势是...；如果看重预算，方案 B 能够通过语义缓存降低 50% 成本，但代价是...*”的架构师视角进行陈述。

---

## 引用源说明

[^bhavishya-pandit]: [Bhavishya Pandit](https://bhavishyapandit9.substack.com/p/7-deep-cut-ai-system-design-interview)
[^buildml]: [BuildML](https://buildml.substack.com/p/top-24-llm-questions-asked-at-deepmind)
[^datainterview-mistral]: [DataInterview - Mistral ML Engineer Interview](https://www.datainterview.com/blog/mistral-machine-learning-engineer-interview)
[^designgurus-rag]: [DesignGurus - RAG System Design](https://www.designgurus.io/blog/system-design-for-rag)
[^exponent-openai]: [Medium - Exponent/Jacob Simon, OpenAI](https://medium.com/exponent/what-its-actually-like-to-interview-at-openai-in-2026-03a646c9436c)
[^exponent-openai-ml]: [Exponent - OpenAI ML Engineer Questions](https://www.tryexponent.com/questions?role=ml-engineer&type=technical)
[^fahd-mirza]: [YouTube - Fahd Mirza](https://www.youtube.com/watch?v=yr5dRHrnbCo)
[^fonzi-ai]: [Medium - Fonzi AI](https://medium.com/fonzi-ai/what-ive-learned-from-sitting-in-on-50-ai-engineer-interviews-c493696453c4)
[^hn-39748537]: [HN - RAG vs. Fine-Tuning](https://news.ycombinator.com/item?id=39748537)
[^hn-41541053]: [HN - LLMs Will Always Hallucinate](https://news.ycombinator.com/item?id=41541053)
[^hn-42313401]: [HN - Automated Reasoning to Remove LLM Hallucinations](https://news.ycombinator.com/item?id=42313401)
[^hn-42431361]: [HN - Agentic LLM Systems in Production](https://news.ycombinator.com/item?id=42431361)
[^hn-42793253]: [HN - AI Orchestration and LLM Routing](https://news.ycombinator.com/item?id=42793253)
[^hn-43884713]: [HN - Is an AI Agent Just an LLM Wrapper?](https://news.ycombinator.com/item?id=43884713)
[^hn-44268335]: [HN - Design Patterns for Securing LLM Agents](https://news.ycombinator.com/item?id=44268335)
[^hn-44796765]: [HN - Sleipner.ai LLM Cost Reduction](https://news.ycombinator.com/item?id=44796765)
[^hn-44875256]: [HN - Interview Questions for AI Product Engineering](https://news.ycombinator.com/item?id=44875256)
[^hn-46229585]: [HN - LLM API Costs in Production](https://news.ycombinator.com/item?id=46229585)
[^hn-46319888]: [HN - LLM Interview Questions](https://news.ycombinator.com/item?id=46319888)
[^hn-46695170]: [HN - Reduce LLM Token Costs with TOON](https://news.ycombinator.com/item?id=46695170)
[^hn-46873753]: [HN - Are LLM Failures Structurally Unavoidable?](https://news.ycombinator.com/item?id=46873753)
[^hn-46959695]: [HN - Early Detection of LLM Hallucinations via ONTOS](https://news.ycombinator.com/item?id=46959695)
[^hn-47150302]: [HN - InferShrink Model Routing](https://news.ycombinator.com/item?id=47150302)
[^igotanoffer]: [igotanoffer - Generative AI System Design Interview](https://igotanoffer.com/en/advice/generative-ai-system-design-interview)
[^interviewnode]: [InterviewNode - GenAI System Design Patterns](https://www.interviewnode.com/post/generative-ai-system-design-interview-patterns-you-should-know)
[^khushal-kumar]: [Medium - Khushal Kumar](https://kaysnotes.medium.com/my-generative-ai-engineer-interview-experience-got-hired-6b3f1affc4e9)
[^llmgenai]: [GitHub - LLM Interview Questions](https://github.com/llmgenai/LLMInterviewQuestions)
[^mimansa-jaiswal]: [Mimansa Jaiswal](https://mimansajaiswal.github.io/posts/llm-ml-job-interviews-resources/)
[^process-analysis]: [Process Analysis - Reddit r/cscareerquestions](https://www.reddit.com/r/cscareerquestions/)
[^promptlayer]: [PromptLayer](https://blog.promptlayer.com/the-agentic-system-design-interview-how-to-evaluate-ai-engineers/)
[^proptech-founder-1]: [YouTube - Proptech Founder Part 1](https://www.youtube.com/watch?v=leXRiJ5TuQo)
[^proptech-founder-2]: [YouTube - Proptech Founder Part 2](https://www.youtube.com/watch?v=Zt-h5BiBWH0)
[^raghu-teja-2]: [Medium - Raghu Teja, IBM Part 2](https://medium.com/@raghu_teja/how-i-cracked-my-ibm-ai-engineer-interview-part-2-ml-scenarios-88af2b46282e)
[^reddit-ai-agentic]: [Reddit - What Agentic AI Am I Supposed to Learn?](https://www.reddit.com/r/ArtificialInteligence/comments/1rceuef/what_agentic_ai_am_i_even_supposed_to_learn) (r/ArtificialIntelligence, Feb 2026)
[^reddit-ai-eng-questions]: [Reddit - AI Engineer Interview Questions](https://www.reddit.com/r/ArtificialInteligence/comments/1nybfr8/ai_engineer_interview_questions/) (r/ArtificialIntelligence)
[^reddit-aiagents-prep]: [Reddit - Interview Prep: Deep Learning to Agentic Systems](https://www.reddit.com/r/AI_Agents/comments/1qrxchn/interview_prep_deep_learning_agentic_systems_what) (r/AI_Agents, Jan 2026)
[^reddit-clear-genai]: [Reddit - How to Clear Interviews in AI/GenAI/RAG/LLM](https://www.reddit.com/r/generativeAI/comments/1p4yrjk/how_to_clear_interviews_in_ai_gen_rag_llm/) (r/generativeAI)
[^reddit-csuk-agents]: [Reddit - AI Engineering Agents Interview Prep](https://www.reddit.com/r/cscareerquestionsuk/comments/1qmybi3/ai_engineering_agents_interview_prep) (r/cscareerquestionsuk, Jan 2026)
[^reddit-devsindia-genai]: [Reddit - Generative AI Engineer Interview Prep](https://www.reddit.com/r/developersIndia/comments/1oq5fdi/got_an_interview_tomorrow_for_a_generative_ai) (r/developersIndia, Nov 2025)
[^reddit-eightfold-ai]: [Reddit - Need Advice for Eightfold.ai Agentic AI Engineer](https://www.reddit.com/r/developersIndia/comments/1pbaj11/need_advice_for_eightfoldai_agentic_ai_engineer) (r/developersIndia)
[^reddit-expdevs-agentic]: [Reddit - Agentic AI System Design Interview](https://www.reddit.com/r/ExperiencedDevs/comments/1r78ipa/agentic_ai_agents_system_design_interview) (r/ExperiencedDevs, Feb 2026)
[^reddit-genai-consulting]: [Reddit - Interview Questions Gen AI (consulting)](https://www.reddit.com/r/learnmachinelearning/comments/1ppgsf3/interview_questions_gen_ai) (r/learnmachinelearning)
[^reddit-genai-product]: [Reddit - Technical Interview for GenAI Engineer Role](https://www.reddit.com/r/leetcode/comments/1rd6yki/technical_interview_for_genai_engineer_role_for_a) (r/leetcode)
[^reddit-grilled-rag]: [Reddit - Got Grilled in an ML Interview for LangGraph/RAG Projects](https://www.reddit.com/r/LangChain/comments/1k662xc/got_grilled_in_an_ml_interview_today_for_my/) (r/LangChain)
[^reddit-llm-interview-prep]: [Reddit - LLM Interview Prep](https://www.reddit.com/r/MachineLearning/comments/1ein9vh/d_llm_interview_prep) (r/MachineLearning)
[^reddit-prep-ai-eng]: [Reddit - How to Prepare for AI Engineering Interviews](https://www.reddit.com/r/datascience/comments/1ovf9k2/how_to_prepare_for_ai_engineering_interviews/) (r/datascience)
[^reddit-swe-to-ai]: [Reddit - From Software Developer to AI Engineer](https://www.reddit.com/r/learnmachinelearning/comments/1pzcw2y/from_software_developer_to_ai_engineer_the_exact/) (r/learnmachinelearning)
[^sundeep-teki]: [Sundeep Teki](https://www.sundeepteki.org/advice/the-ultimate-ai-research-engineer-interview-guide-cracking-openai-anthropic-google-deepmind-top-ai-labs)
[^system-design-handbook]: [System Design Handbook](https://www.systemdesignhandbook.com/guides/generative-ai-system-design-interview/)
[^techeon]: [Medium - TechEon Agentic Guide](https://medium.com/@techeon/the-complete-agentic-ai-system-design-interview-guide-2026)
[^tidorp]: [GitHub - TidorP/MLJobSearch2025](https://github.com/TidorP/MLJobSearch2025)
[^x-akshay-pachaar-1]: [X - Akshay Pachaar, ML Deployment Testing (Netflix)](https://x.com/akshay_pachaar/status/1990034795909582860)
[^x-aryyann8]: [X - AI Engineer Intern Interview](https://x.com/aryyann8/status/2009314129878896960) (Jan 2026)
[^x-ashutosh-1]: [X - Ashutosh Maheshwari, Fine-Tuning vs. Prompting](https://x.com/asmah2107/status/1977413874702745794)
[^x-athletickoder-2]: [X - athleticKoder, RAG System Diagnostics](https://x.com/athleticKoder/status/2002355874786873383)
[^x-interviewstack-meta]: [X - InterviewStack.io, Meta LoRA Question](https://x.com/gnan54796/status/2007302142550565123)
