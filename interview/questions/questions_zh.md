# AI 工程师面试真题库

本题库汇总自 100+ 渠道，包括技术博客、YouTube 视频转录文本、Reddit 讨论帖、Medium 专栏文章以及各大厂官方求职指南。每一道面试真题均提炼自真实的求职经历或备考材料。


## 1. 技术理论面试题 (Technical Questions)

### A. 大模型基础 (LLM Fundamentals)
- 大语言模型（LLM）是如何生成文本的？ [^proptech-founder-2]
- 详细解释 Transformer 架构的自注意力（Self-Attention）机制。 [^proptech-founder-2] [^reddit-genai-consulting] [^reddit-ai-eng-questions]
- 什么是分词（Tokenization）？它是如何影响大模型性能与表现的？ [^fahd-mirza] [^glassdoor-quantiphi] [^glassdoor-asapp]
- 模型预训练（Pre-training）与指令微调（Fine-tuning）在训练数据和目的上有何区别？ [^fahd-mirza] [^reddit-capital-one] [^glassdoor-cognida]
- 解释上下文窗口 (Context Window) 及其在处理长文本时的工程局限性。 [^fahd-mirza] [^exponent-openai-ml]
- 什么是大模型缩放定律 (Scaling Laws)？为什么它对研究和架构师至关重要？ [^fahd-mirza] [^reddit-llm-interview-prep]
- 什么是 Temperature（温度）和 Top-p 采样解码？它们如何具体影响生成的文本？ [^fahd-mirza] [^reddit-genai-consulting] [^x-aryyann8]
- 解释少样本提示（Few-shot learning）与思维链提示（Chain-of-thought prompting）的工作原理。 [^fahd-mirza] [^reddit-genai-consulting] [^reddit-ai-eng-questions]
- 什么是 KV Cache？它是怎么在自回归推理中起到加速作用的？ [^igotanoffer] [^reddit-llm-interview-prep]
- 在解决实际业务问题时，调用生成式 AI 大模型开发与传统式写死逻辑的编程范式有什么本质区别？ [^proptech-founder-1]
- 在非确定性的生成场景下，当面临包含多个大模型调用环节的串行工作流时，你如何确保大模型输出的格式一致性与事实准确性？ [^proptech-founder-1]
- 什么是 RAG 模型？请完整阐述其从数据向量化到最终生成的全流程。 [^khushal-kumar] [^reddit-ai-eng-questions] [^reddit-genai-consulting]
- 什么是向量嵌入 (Embeddings)？ [^khushal-kumar] [^reddit-ai-eng-questions] [^reddit-genai-consulting]
- 文本数据是如何进行切片（Chunking）的？常见分块策略有哪些？ [^khushal-kumar] [^reddit-ai-eng-questions] [^reddit-genai-consulting]
- 判别式模型（Discriminative models）与生成式模型（Generative models）有什么区别？ [^reddit-genai-consulting]
- 什么是 Graph RAG（图 RAG）？它与标准 RAG 架构有什么区别和优势？ [^reddit-ai-eng-questions]
- 大模型智能体中的“自我反思 (Reflection)”机制是指什么？ [^reddit-ai-eng-questions]
- 解释 KL 散度（Kullback-Leibler divergence）。 [^reddit-clear-genai]
- 符号主义 AI (Symbolic AI) 与连接主义 AI (Connectionist AI) 有什么区别？ [^reddit-hiring-process]
- 简述几种常见的文本摘要技术类型，并说明你会在什么情况下使用它们。 [^reddit-hiring-process]
- 在长对话或多步骤任务中，你如何为大模型进行记忆管理 (Memory Management) 与上下文精简控制？ [^reddit-ai-eng-questions]
- 什么是自注意力机制 (Self-attention)？它与多头注意力机制 (Multi-head attention) 有何异同？ [^sundeep-teki]
- 什么是 GQA（Grouped Query Attention，分组查询注意力）？它与标准多头注意力相比有何技术优势？ [^mimansa-jaiswal]
- 什么是 BPE（Byte Pair Encoding）、WordPiece 和 Character-level 字符级分词？它们各有什么技术取舍？ [^fahd-mirza]
- 编码器（Encoder-only）、解码器（Decoder-only）和编解码器（Encoder-decoder）三种 Transformer 架构的区别是什么？各自的适用场景是什么？ [^tidorp] [^hn-46319888] [^reddit-llm-interview-prep]
- 为什么目前即使是非生成式任务（如分类、分类匹配），解码器（Decoder-only）架构也占据了绝对统治地位？ [^reddit-llm-interview-prep]
- 什么是位置编码 (Positional Encoding)？为什么在 Transformer 架构中必不可少？ [^linkjob-openai]
- 什么是 MMLU、BigBench 和 HumanEval 等主流大模型基准评测？它们分别测量什么，各自局限度是什么？ [^fahd-mirza]
- 什么是基于人类反馈的强化学习（RLHF）？它与直接偏好优化（DPO）有何区别？各自适用范围是什么？ [^mimansa-jaiswal]
- 什么是混合专家模型 (MoE，Mixture of Experts)？它是如何提升计算吞吐效率的？ [^mimansa-jaiswal]
- 大模型是如何逐字生成文本的？请详细解释自回归解码（Autoregressive Decoding）过程。 [^hn-46319888] [^llmgenai]
- 介绍 Beam Search、Top-k、Top-p 等常见的解码搜索策略。你会在何时选择哪种策略？ [^mimansa-jaiswal]
- 什么是 FlashAttention？它是怎么在 CUDA/内存层加速自注意力计算的？ [^reddit-llm-interview-prep]
- 为什么大模型推理服务（LLM Inference）通常受限于内存带宽（Memory-bound）而非计算算力？ [^reddit-llm-interview-prep]
- 大模型接口中的停止序列（Stop Sequences）在底层是如何起作用的？ [^reddit-llm-interview-prep]
- 当输入数据超出窗口限制时会发生什么？你会怎么处理长文本输入？ [^hn-46319888] [^llmgenai]
- 将通用的 Tokenizer（分词器）直接应用在法律条文、医学报告等高度特异的垂直领域时，会带来哪些工程风险与性能损耗？ [^x-ali-shohadaee]

### B. RAG（检索增强生成）系统 (RAG Systems)
- 设计一个面向客服助手的 RAG 系统。你如何科学评估和衡量它表现的好坏？ [^process-analysis] [^reddit-genai-consulting]
- 如何设计一个能够支撑全公司千万级文档的智能企业知识库搜索引擎？ [^igotanoffer]
- 设计一个生成式 AI 票据处理流水线，能够解析和识别杂乱的电子邮件、PDF 扫描件和图片，以自动化推进保险理赔申报工作。 [^igotanoffer]
- 你如何保证大模型（如 GPT-4）生成的回答完全 grounded（绑定）在企业提供的私有法律文档库中？ [^interviewnode]
- 设计一个面向公司全员知识库的问答助手。 [^interviewnode]
- 现需要为一份长达数百页的 PDF 财务报表开发问答系统。当你在切片（Chunking）分段时，该怎么解决“全局上下文信息丢失”（例如：第 1 页写明了“单位：千元”，后面页面省略了该单位）的问题？ [^proptech-founder-1]
- 在高并发的聊天系统里，你如何高效地为数百万种商品和用户提问生成并快速检索向量 embeddings？ [^proptech-founder-2]
- 如果检索出的上下文内容里完全没有包含用户问题的答案，你该如何设计架构以防止模型凭空捏造（幻觉）回答？ [^proptech-founder-2]
- 你在过往项目中落地过哪些有代表性的 RAG 系统？ [^igotanoffer]
- 设计一个针对内部开发文档的智能 Q&A 系统。 [^system-design-handbook]
- 你如何从源头保证大模型所接触和引用的文档数据的清洗质量？ [^proptech-founder-2]
- 对比稀疏检索（Sparse Retrieval，如 BM25）与稠密检索（Dense Retrieval，如向量搜索）。各自优缺点是什么？ [^reddit-clear-genai]
- RAG 系统在生产环境下最常见的失效痛点有哪些？你平时是如何进行排障和调优的？ [^reddit-clear-genai] [^reddit-grilled-rag] [^x-athletickoder-2]
- 在多租户或有权限控制的安全场景下，你如何防止用户通过 RAG 提问越权召回他没有读取权限的数据？ [^reddit-grilled-rag]
- 你们在项目中选用过哪些向量数据库？它们各有什么物理特性和技术取舍？ [^reddit-ai-eng-questions] [^promptlayer] [^llmgenai]
- 什么是混合检索 (Hybrid Search)？在什么场景下你会强制把向量检索与传统的关键词检索（BM25）混合使用？ [^designgurus-rag]
- 什么是重排 (Re-ranking)？为什么在向量召回后还需要重排？解释 Cross-Encoder 与 Bi-Encoder 的区别。 [^designgurus-rag]
- 当知识库文章规模突破 1000 万篇以上时，你如何扩容和优化 RAG 系统？请从分片（Sharding）、缓存和语义索引优化展开。 [^bhavishya-pandit]
- 你们的 RAG 系统能检索出高度相关的段落，但用户还是反馈“找不到直接的答案”。你如何从“搜索引擎”将其调优为直接解答的“答案引擎”？ [^hitendra-patel]
- 科学评估一个 RAG 系统，你需要衡量哪些传统的检索指标（如 NDCG、MRR、Precision@K、Recall）？ [^mimansa-jaiswal]
- 在 RAG 系统中，你如何实现精确的引用（Citations）与来源数据源追溯标注？ [^proptech-founder-1]
- 向量近似最近邻检索 (ANN) 的底层原理是什么？请详细解释 HNSW（分层导航小世界）索引的工作原理。 [^designgurus-rag]
- 纯语义向量检索的“死穴”在哪里？请从逻辑否定、时序关系以及超精密匹配举例说明。 [^techeon]
- 什么是语义缓存 (Semantic Caching)？它是如何帮助降低大模型调用成本和首字时延的？ [^designgurus-rag] [^hn-44796765]
- 如何设计一个在多轮连续对话（Multi-turn conversation）中依然能稳定维持检索上下文精度的 RAG 服务？ [^hn-44875256]
- 设计 RAG 系统时，最重要的技术权衡（如时延 vs 准确率、分块大小 vs 召回精度、成本 vs 质量）有哪些？ [^reddit-genai-product]
- 如何在生产环境全面调优和压缩 RAG 服务的整体响应时延？ [^x-aryyann8]

### C. 智能体与工具调用 (Agents and Tool Use)
- 什么是 AI 智能体 (Agent)？它在更大的软件架构里扮演怎样的角色？ [^proptech-founder-1]
- 智能体 Agent 与单向的大模型调用链（LLM Chain）有什么本质的技术区别？ [^process-analysis]
- 是什么特质让一个 AI 系统被定义为“智能体 (Agentic)”？哪些方案只能归类为普通的 API wrapper 包装？ [^techeon] [^reddit-ai-agentic] [^reddit-devsindia-genai] [^hn-43884713] [^hn-42431361] [^x-aryyann8]
- 在什么业务场景下，引入智能体反而是糟糕或过度设计的方案？ [^techeon] [^reddit-csuk-agents]
- 你如何在工程架构上清晰定义、约束和控制智能体的自主执行边界（Autonomy boundaries）？ [^techeon] [^reddit-expdevs-agentic]
- 除了作为大脑的大模型之外，一个完整的智能体系统还必须配备哪些核心工程组件？ [^techeon] [^reddit-expdevs-agentic] [^reddit-ai-agentic]
- 如何设计程序检测并强行终止智能体陷入的“死循环任务规划 (Infinite planning loops)”？ [^techeon] [^reddit-csuk-agents] [^reddit-expdevs-agentic]
- 请拆解一个满足生产部署要求的高可靠智能体架构。 [^techeon] [^reddit-expdevs-agentic] [^reddit-csuk-agents]
- 在智能体架构中，哪些流控制逻辑应该写死在外部的编排代码中（Orchestrator），哪些逻辑应该放手让大模型（LLM）自己决策？ [^techeon] [^reddit-expdevs-agentic] [^reddit-aiagents-prep]
- 如何设计一个能够自我检测、易于排查 Debug 且安全的智能体推理循环？ [^techeon] [^reddit-expdevs-agentic] [^reddit-csuk-agents]
- 对于长期在后台运行（Long-running）的自主智能体，如何优雅地定义和执行任务终止条件（Termination conditions）？ [^techeon]
- 智能体是如何将一个宏大的高层目标，拆解为一步步具体的可执行原子步骤（Sub-steps）的？ [^techeon] [^reddit-csuk-agents]
- 思维链（CoT） vs 思维树（ToT） vs 复杂的有向图规划（Graph Planning）—— 它们的区别与适用场景是什么？ [^techeon]
- 在遇到局部信息缺失、或环境返回的信息不完整时，智能体该怎么调整其规划逻辑？ [^techeon] [^reddit-csuk-agents]
- 智能体在什么情况下能断定一件任务已经彻底“搞定”？ [^techeon]
- 哪些智能体规划逻辑上的失败或死锁，在线上真实生产环境下是最隐蔽、最难被监控软件捕捉到的？ [^techeon] [^reddit-expdevs-agentic]
- 智能体是如何判断何时该调用工具，以及选择调用哪一个工具的？ [^techeon] [^reddit-csuk-agents] [^reddit-aiagents-prep]
- 你如何设计工具的 JSON Schema 说明，才能让大模型极少发生工具调用的参数幻觉？ [^techeon] [^reddit-grilled-rag]
- 为了防止大模型执行恶意的 shell 命令或破坏线上数据库，你如何搭建隔离的执行沙箱 (Sandboxing)？ [^techeon] [^reddit-expdevs-agentic]
- 当智能体调用第三方工具发生接口超时、失败或网络波动时，你如何设计容错、重试以及保证幂等性 (Idempotency)？ [^techeon] [^reddit-expdevs-agentic] [^reddit-csuk-agents] [^reddit-aiagents-prep]
- 允许大模型调用工具会带来哪些核心的安全隐患与越权风险？ [^techeon] [^reddit-expdevs-agentic] [^datainterview-mistral]
- 当智能体为了达成目标而在后台不断触发工具调用和模型请求时，你如何设计保险丝阈值，防止由于大模型死循环导致公司月度 Token 费用瞬间超标？ [^techeon] [^reddit-expdevs-agentic] [^reddit-csuk-agents]
- 无状态智能体与有状态（Stateful）智能体的优缺点和各自适用场景是什么？ [^techeon] [^reddit-expdevs-agentic]
- 怎么实现智能体版本变更控制？如何将出错的智能体行为逻辑回滚到先前的稳定版？ [^techeon]
- 如果让你来设计一套完整的 AI 智能体产品，你会怎么规划其底层的推理循环、工具调用接口、记忆模块设计、编排中间件以及安全护栏？ [^igotanoffer]
- 如何设计一个能够分析客户投诉工单、自动草拟回复并能在遇到复杂问题时自动升级转接人工的智能体系统？ [^promptlayer]
- 如何构建一个能自动联合检索并生成带引用来源研究报告的协作 Agent 系统？ [^promptlayer]
- 如何构建一个能自动走读代码（Code Review）并给出重构和调优建议的辅助 Agent？ [^promptlayer]
- 你如何向非技术的业务部门（Stakeholders）通俗解释智能体系统的工作原理和决策边界？ [^techeon] [^reddit-expdevs-agentic]
- 大模型智能体需要配备哪些类型的记忆体系？请向我通俗解释工作记忆（Working memory）、情景记忆（Episodic memory）、语义记忆（Semantic memory）和程序记忆（Procedural memory）的应用。 [^techeon] [^reddit-expdevs-agentic]
- 在为智能体设计长期记忆存储时，你怎么防止大模型提取了过多的无关陈旧记忆（Noise pollution），导致上下文膨胀和回答退化？ [^techeon]
- 在智能体系统里，如何优雅地实现人机协同模式（Human-in-the-loop）？你会用什么规则触发并将任务移交给人工审核？ [^reddit-expdevs-agentic]
- 对于完全自主运行的后台智能体（Autonomous Agents），你如何在生产环境中追踪和可视化它们的运行轨迹和规划步骤？ [^reddit-expdevs-agentic] [^reddit-csuk-agents]
- 在金融交易、医疗诊断等高度合规且受严格监管的行业里，你该怎么为智能体设计符合审计要求的架构？ [^reddit-expdevs-agentic]
- 在多智能体协作中，你会在什么情况下选择“中心编排模式 (Orchestration)”，在什么情况下选择“去中心化协同模式 (Choreography)”？ [^reddit-expdevs-agentic]
- 在大模型 pipeline 的数据入口层，你如何实现数据脱敏（如自动掩盖手机号、名字等 PII 隐私信息），确保数据不外泄给第三方 API 提供商？ [^reddit-expdevs-agentic]
- 如何评估智能体 Agent 的运行质量？哪些指标是关键的（如工具选择准确率、任务推进行动率、上下文遵循度）？ [^reddit-aiagents-prep]

### D. 模型微调与训练 (Fine-tuning and Training)
- 在微调模型（Fine-tuning）与提示词工程（Prompt Engineering）之间，你是如何进行技术选型的？ [^process-analysis] [^reddit-prep-ai-eng] [^reddit-genai-consulting] [^x-ashutosh-1]
- 什么是参数高效微调（PEFT，如 LoRA）？它的数学原理是什么？在什么情况下选择 LoRA 而非全参数微调？ [^fahd-mirza] [^reddit-genai-consulting] [^x-interviewstack-meta] [^x-aryyann8] [^reddit-llm-interview-prep]
- 什么是 QLoRA？它与 LoRA 的技术差别是什么？你在什么情况下会为了性能或显存去选择 QLoRA？ [^x-aryyann8]
- 什么是人类反馈强化学习（RLHF）？为什么它是解决对齐（Alignment）的核心？ [^proptech-founder-1]
- 针对垂直业务系统，你应该选择自建模型微调，还是选择直接使用提示词 + RAG 的形式？ [^system-design-handbook] [^reddit-prep-ai-eng] [^hn-39748537]
- 如何设计一套训练流程来教一个基座模型学会做复杂的数学推导？请从数据集收集、SFT 监督微调、RL 强化训练以及评测指标设计展开说明。 [^igotanoffer]
- 考虑到高昂的算力和数据标注限制，你会如何为团队设计一套低成本、高效率的开源大模型增量训练/微调流水线？ [^igotanoffer]
- 简述人类反馈强化学习（RLHF）的经典三阶段流程：监督微调 (SFT)、奖励模型训练 (RM) 以及 PPO 策略优化。为什么现在的 DPO（直接偏好优化）能够大幅简化这个流程？ [^proptech-founder-1]
- 什么是指令微调（Instruction Tuning）？它与基础模型的大规模预训练（Pre-training）在数据和目的上有什么区别？ [^hn-46319888] [^llmgenai] [^reddit-llm-interview-prep]
- 什么是投机性解码 (Speculative Decoding)？它是怎么加速自回归模型推理输出的？ [^sundeep-teki]
- 线上用户隐式的交互行为（如修改了 AI 生成的代码、采纳或拒绝了 AI 的建议），如何被清洗并转化为模型二次迭代的微调训练信号？ [^bhavishya-pandit]
- 解释模型量化（Quantization）的原理。在 FP16、INT8 与 INT4 之间，如何在模型大小、推理速度和计算精度上做权衡？ [^raghu-teja-2] [^reddit-llm-interview-prep]

### E. 测试与评估指标 (Evaluation and Metrics)
- 评估大模型生成表现时，你会参考哪些具体的量化指标（Metrics）？ [^proptech-founder-1]
- 你会如何科学地评估一个 Chatbot（聊天机器人）的好坏？有哪些具体的测试维度？ [^process-analysis] [^reddit-clear-genai]
- 什么是模型幻觉（Hallucinations）？你有哪些工程手段来检测并拦截幻觉生成？ [^process-analysis] [^reddit-ai-eng-questions] [^reddit-genai-consulting] [^hn-41541053] [^hn-46873753]
- 如何在一个大模型文档摘要系统中，坚决防止出现捏造的事实错误？ [^interviewnode]
- 如何在一个针对患者医疗问答的 Chatbot 中，科学设防以最大限度地降低模型的医学回答幻觉率？ [^interviewnode]
- 如果一个线上 RAG 客服表现出“用极其自信的语气给出了完全错误的内容”，你该如何去 debug 和排查整个系统链路？ [^process-analysis] [^datainterview-mistral]
- 解释经典的可解释性 AI 工具 LIME 和 SHAP 的工作原理。 [^fahd-mirza]
- 什么是模型幻觉（Hallucinations）？你有哪些工程手段来检测并拦截幻觉生成？ [^system-design-handbook]
- 介绍传统的 NLP 评测指标：Perplexity (困惑度)、ROUGE、BLEU。利用 n-gram 词频匹配的方法去评估大模型生成的段落，存在什么严重的缺陷？ [^fahd-mirza] [^reddit-genai-product] [^reddit-llm-interview-prep]
- 大模型的输出往往是非确定性的（Non-deterministic）。对于这种无法使用断言（assert）的生成场景，你有哪些有效的自动化回归测试手段？ [^reddit-prep-ai-eng]
- 在传统的分类指标（如精确率、召回率）完全不适用的长文本生成场景下，你怎么设计算法量化大模型的准确度？ [^reddit-grilled-rag]
- 除了大模型本身的生成准确度之外，有哪些关乎线上核心业务的工程/运营指标是需要被实时观测的？（如转化率、工单拦截率、P95延迟） [^reddit-eightfold-ai]
- 除了离线的 Golden Dataset 测试外，你如何在生产环境实时评估和监测模型的输出表现？ [^reddit-swe-to-ai]
- 你们团队是如何解决训练数据和推理场景中的偏差/公平性（Bias/Fairness）问题的？请给我讲一个你们做出技术抉择的真实例子。 [^reddit-hiring-process]
- 什么是首字响应时间 (TTFT，Time to First Token)？为什么它对用户交互体验至关重要？ [^proptech-founder-1]
- 线上真实的流量是千变万化的，你如何在生产环境实时量化和监控幻觉率？ [^buildml] [^llmgenai] [^hn-46959695] [^hn-42313401]
- 什么是大模型评测中的“感觉法 (vibes-based evals)”与“硬评测框架 (formal eval framework)”？你平时怎么带团队去写评测用例？ [^exponent-openai]
- 你是如何从零收集和构建一个高质量的评测黄金数据集 (Golden Dataset) 的？怎么用它做系统的回归测试？ [^proptech-founder-1]
- 怎么让你的大模型系统随着运行时间的推移越变越聪明？请描述你设计的用户反馈与持续强化学习闭环。 [^interviewnode]
- 你是怎么界定和选用一个机器学习算法的成功指标（Success metrics）的？ [^raghu-teja-2]
- 怎么实现针对不同系统提示词（Prompts）版本的线上 A/B 测试？ [^hn-44875256]
- 在将新调优的模型全量发布前，你如何设计线上流量灰度测试？请对比 A/B 测试、金丝雀部署、交错流量测试（Interleaved）与影子测试（Shadowing）。 [^x-akshay-pachaar-1]
- 两个模型对同一批数据集分类准确度一模一样，但其中一个模型打出的置信度得分波动很大。你选择哪一个？请向我解释什么是模型校准（Model Calibration）。 [^x-akshay-pachaar-3]
- 线上运行的客服机器人的分类准确度在短短六周内从 95% 暴跌到了 80%。在重新把模型拉去重训之前，你如何去排查并定位其准确率退化的根源？ [^x-ashutosh-2]

### F. 机器学习与经典算法基本功 (ML Fundamentals)
- 你们在算法开发中是如何处理数据清洗、特征提取与特征工程的？ [^fahd-mirza]
- 从底层读写吞吐和计算对齐出发，对比 SQL 关系型数据库与 NoSQL 数据库在处理 AI 训练与推理工作流时的差异。 [^fahd-mirza]
- 如果你拿到的模型在测试集上表现极差，你通常会采取哪几个步骤去系统定位模型的性能缺陷？ [^fahd-mirza]
- 针对一个只需处理单次请求的个人手机智能助理，你应该优化系统的“响应时延 (Latency)”还是“服务吞吐量 (Throughput)”？ [^youtube-short]
- 针对上述只需处理单次请求的手机智能助理，你需要在架构上引入数据并行化（Data Parallelism）计算吗？理由是什么？ [^youtube-short]
- 大语言模型（LLM）是如何生成文本的？ [^process-analysis] [^reddit-genai-consulting]
- 你们在架构上是如何处理实时数据流更新 vs 离线批量处理的？它们各自的技术取舍是什么？ [^proptech-founder-2]
- 针对海量的结构化数据、无结构文本以及流式事件数据，你们是如何设计统一的数据清洗灌入系统的？ [^proptech-founder-1]
- 用最通俗的语言向我解释机器学习中的“偏差-方差折中定理（Bias-Variance Tradeoff）”。 [^reddit-swe-to-ai]
- 为什么在处理普通的二维关系表（Tabular data）结构时，传统的神经网络通常打不过 XGBoost 或 Random Forest 等树模型？ [^reddit-swe-to-ai]
- 聊聊你过去解决真实业务数据不均衡问题（Imbalanced datasets）的实操经验。 [^reddit-swe-to-ai] [^reddit-hiring-process] [^raghu-teja-2]
- 解释循环神经网络（RNN）与长短期记忆网络（LSTM）的结构差别。 [^raghu-teja-2]
- **Bug 排查题**：模型能够跑通，但其 Loss 曲线完全不动（模型学不到任何东西）。你应该怎么去排查代码中潜在的广播机制异常（Broadcasting errors）或矩阵张量维度对齐冲突？ [^sundeep-teki]
- 统计学高频提问：概率密度、常见分布模型、线性回归数学推导、贝叶斯分析、假设检验。 [^mimansa-jaiswal]
- 监督学习（Supervised learning）与无监督学习（Unsupervised learning）的区别是什么？各自的适用场景是什么？ [^hn-29876742] [^tidorp]
- 什么是模型正则化 (Regularization)？对比 L1 正则项、L2 正则项与 Dropout 的防过拟合原理。 [^hn-29876742] [^tidorp]
- 什么是特征归一化 (Feature Scaling)？它为什么对很多梯度下降算法至关重要？对比 Normalization 与 Standardization。 [^x-aryyann8]
- 仅使用 NumPy，现场手写余弦相似度（Cosine Similarity）计算公式。 [^reddit-amazon-genai]

### G. Python 语言与软件工程素养 (Python & SWE)
- 如何在多线程/多进程开发中合理防范和解决死锁与竞态条件（Race conditions）？ [^proptech-founder-2]
- 详细解释 Python 中的全局解释器锁（GIL）。它是怎么阻碍多线程利用多核算力的？ [^proptech-founder-2]
- Python 在处理高并发 IO 请求和 CPU 密集型任务时，有哪些独特的并发处理方案？ [^proptech-founder-2]
- 在使用 Python `asyncio` 进行异步编程时，最容易踩的坑和面临的资源死锁有哪些？ [^proptech-founder-2]
- 什么是 Docker？为什么它是交付 AI 软件的标配？ [^khushal-kumar]
- 在爬虫和自动化数据抓取中，为什么要使用 Selenium？ [^khushal-kumar]
- 聊聊你平时用 Redis 解决过哪些高并发场景？ [^khushal-kumar]
- 详细解释 JavaScript 的事件循环机制（Event Loop）。 [^proptech-founder-1]
- 在写代码调用大模型 API 时，你平时是怎么处理网络重试（Retries）、接口超时（Timeouts）和调用日志记录的？ [^reddit-genai-consulting]
- 目前你经常用哪些 AI 辅助开发工具？能分享一下你喜欢它们的理由吗？ [^reddit-hiring-process]
- 详细解释 Python 中的内存泄漏（Memory leaks）隐患与垃圾回收机制（GC）。 [^raghu-teja-1]
- Python 类方法（`@classmethod`）与静态方法（`@staticmethod`）的区别是什么？各自的使用场景是什么？ [^raghu-teja-1]
- 解释 Python 多重继承下的 `super()` 机制与 MRO（方法解析顺序）。 [^raghu-teja-1]
- “线上环境可没有 VS Code 给你单步断点。” 线上生产环境出了严重的诡异 Bug，你平时用什么工具和手段进行排查？ [^raghu-teja-1]
- 解释 Python 中怎么使用 `asyncio` 库实现高效的并发 I/O 读写。什么时候你应该改用多线程（Threading）或多进程（Multiprocessing）？ [^proptech-founder-1]
- 如何调优一个执行缓慢的 SQL 查询？请写出 SQL 底层的语法执行顺序。 [^raghu-teja-1]
- 你们团队在开发和灰度发布时采用什么 Git 分支治理策略？怎么进行 Git Rebase？遇到 Git Conflict（代码冲突）时你具体的解决步骤是什么？ [^raghu-teja-1]
- 你在项目中接触过 WebRTC 等流式实时音视频技术吗？ [^fahd-mirza-2]

### H. 基础设施与 MLOps
- 如何设计一个高可用的大模型托管推理平台（包括动态批处理 Dynamic Batching、GPU 水平扩容、模型版本灰度管理以及输出缓存）？ [^designgurus]
- 设计一个支持断点续训（Checkpointing）、弹性抢占与高可用调度的分布式 GPU 训练队列系统（支持 10 万+卡并发作业）。 [^designgurus] [^x-akshay-pachaar-2]
- 如何设计一个支持海量数据清洗、向量化和增量导入的 MLOps 数据流水线？ [^designgurus]
- 线上流量突然暴增，你如何设计大模型中间件，在保护后端大模型厂商接口不超限（Rate limited）的前提下优雅限流和削峰填谷？ [^igotanoffer]
- 线上部署的大模型应用，你平时通过哪些系统指标和业务指标来观测服务的健康状况？ [^system-design-handbook]
- 在将大模型和智能体推向线上大规模生产环境时，最大的工程性能瓶颈通常发生在哪里？ [^system-design-handbook]

### I. 成本与延迟极致压缩 (Cost & Latency Optimization)
- 如果你的 AI 应用日均请求量达到 100 万次，你会从哪些架构层面去压缩服务器成本？ [^process-analysis]
- 你有哪些工程手段能帮公司节省大模型的 Token 开销？ [^process-analysis] [^reddit-prep-ai-eng] [^hn-46229585] [^hn-46695170]
- 在系统架构构思初期，你如何为大模型应用进行 Token 预算和月度服务器账单规划？ [^igotanoffer]
- 当遭遇极高并发的流量洗劫时，你如何在架构层保证调用第三方大模型 API 的成本和预算不瞬间失控？ [^interviewnode]
- 有哪些手段能帮公司在系统设计时压缩大模型输入输出的 Token 费用？ [^system-design-handbook]
- 解释大模型推理优化中的“模型量化（Quantization）”与“知识蒸馏（Model Distillation）”原理。 [^fahd-mirza]
- 详述生成式 AI 中的“响应时延 (Latency) - 调用成本 (Cost) - 输出相关度 (Relevancy)”三要素折中铁律。你们在项目中是怎么做好三者平衡的？ [^proptech-founder-2]
- 有哪些常见的手段能有效降低生成式 AI 应用的首字响应时延？ [^proptech-founder-2]
- 成本 vs 回答质量的折中：在什么情况下，一个本地部署的便宜的小参数开源模型就已经“足够好”了？ [^reddit-genai-consulting]
- 请写出通过清理提示词冗余（Prompt trimming）和缓存嵌入（Embedding caching）进行大模型 API 降本的前后对比账单分析。 [^fonzi-ai]
- 详细解释大模型应用中的多级缓存架构：检索缓存、提示词缓存（Prompt cache）与生成响应缓存。 [^interviewnode]
- 什么是模型分层路由 (Model Tiering)？你如何实现当遇到简单问题时分发给低成本小模型，而复杂问题路由给高级大模型的策略？ [^interviewnode] [^hn-42793253] [^hn-47150302]
- 什么是提示词压缩（Prompt Compression）？它又是如何帮公司降低线上账单的？ [^llmgenai] [^hn-46319888] [^hn-44013971]
- 针对大模型推理服务，优化“单次响应延迟 (Latency)”与优化“整体系统吞吐量 (Throughput)”在架构设计上有哪些技术妥协？ [^youtube-short]
- 在一个包含多个串行模型调用的复杂 Agent 流水线里，你如何为每一个步骤做 Benchmark 耗时统计以定位时延瓶颈？ [^proptech-founder-1]
- 试估算一个企业级 RAG 检索服务（如需要检索 30 万份高度机密的法律合同）在生产环境下的月度预算构成。 [^reddit-devsindia-genai]
- 在高并发大模型推理中，显存真正的性能死穴在哪里？PagedAttention（分页注意力）技术是如何解决这一瓶颈的？ [^x-athletickoder-1]

### J. 安全与合规护栏 (Safety & Guardrails)
- 你会在什么时候、在系统架构的什么位置配置大模型护栏组件（LLM Guardrails）？ [^proptech-founder-1]
- 如何设计安全对齐机制，让大模型在不损害日常实用回答能力的前提下，坚决不产生色情、暴力或危害公共安全的违规内容？ [^igotanoffer]
- 怎么搭建一个能够自动过滤和拦截色情、暴力或违反国家政策违规内容的双向安全过滤系统？ [^igotanoffer]
- 面对恶意的提示词注入（Prompt Injection）和越狱套词（Jailbreaking），你有哪些防御机制？ [^system-design-handbook] [^reddit-ai-eng-questions] [^reddit-expdevs-agentic] [^hn-44268335]
- 大模型应用在捕获并拦截模型异常生成时，通常要在代码层做好哪些兜底保护逻辑？ [^proptech-founder-2]
- 解释 Constitutional AI（宪政 AI）与大模型安全对齐的思路。 [^sundeep-teki]
- 怎么处理提示词和系统日志中可能泄露的个人隐私数据（PII）或机密信息？ [^reddit-genai-consulting] [^reddit-expdevs-agentic]
- 在训练数据集清洗与大模型日常交互中，你怎么科学降低模型对特定人群的偏见（Bias）和歧视？ [^reddit-genai-consulting] [^reddit-hiring-process]
- 如何对一个已发布的大模型应用进行恶意的对抗红队测试 (Red-teaming)？ [^sundeep-teki]
- 你们的 Agent 智能体支持生成代码并在线执行。为了防止生成并执行恶意的 `rm -rf` 指令，你如何从系统安全层进行全面设防？ [^proptech-founder-1]


## 2. 系统设计面试真题 (System Design)

### A. 生成式 AI 系统设计 (AI System Design)
- 设计 ChatGPT 聊天系统。 [^igotanoffer]
- 设计 Claude 智能助手后台。 [^igotanoffer]
- 设计一个精简版的移动端少儿英语教学模型。要求能部署在手机本地运行，且具备极强的安全护栏，坚决不能对幼儿说任何不礼貌的脏话。 [^igotanoffer]
- 给你一份由初级开发设计的“大模型推理并发批处理系统”草稿图。请在现场担任架构师，指出其设计中包含哪些严重的并发死锁与性能瓶颈，并说明你将如何重构它。 [^igotanoffer]
- 设计 OpenAI Playground 的后台架构 —— 重点实现支持开发者在线配置多轮历史对话、并随时模拟分支会话流（Threads）的功能。 [^exponent-openai]
- 设计一个高吞吐的实时聊天服务 API（包含低时延流式数据传输、多租户会话 Session 持久化、并发控制以及双向安全过滤网关）。 [^designgurus]
- 设计一个基于文档的 RAG 智能问答系统。 [^bhavishya-pandit]
- 设计一个“绝对零幻觉（基于事实检索）”的在线智能银行客服小助手。 [^bhavishya-pandit]
- 设计一个部署在医院病房的语音录入助手（需重点解决噪音干扰、患者隐私合规、超低延迟响应以及医学专业词汇识别）。 [^bhavishya-pandit]
- 设计一个集成在文本写作编辑器后台的“大模型强化自动批改与用户协同反馈（Active feedback loop）”引擎。 [^bhavishya-pandit]
- 设计一个可以自动解析条款并按严格合规标准自动生成法律合同的智能系统。 [^bhavishya-pandit]
- 设计一个支持千万级文章、高召回、低时延的企业级 AI 文献搜索引擎。 [^bhavishya-pandit]
- 设计一个可以根据求职简历，自动判定其匹配方向并路由派发给公司内部相应研发组的“简历智能路由引擎”。 [^bhavishya-pandit]
- 设计一个 AI 驱动的猎头候选人自动推荐系统。数据基数包含 7.5 亿份个人画像，需支持语义搜索，且单次检索响应时延必须低于 500ms。 [^colin-zhou]
- 如何设计一个能支撑日均 100 万用户的高并发 AI 聊天助手，并详细进行成本与时延折中估算？ [^process-analysis]
- 接上题，如果系统流量从玩具 Demo 暴增到日均千万级，你的系统架构该如何设计横向扩容？ [^process-analysis]
- 设计一个能处理每月 10,000+ 用户上传单据（银行流水、身份证复印件等）的自动化 OCR 与大模型信息清洗系统。详述在遇到模型 API 大面积宕机、或单据排版严重混乱时系统的降级与错误重试逻辑。 [^igotanoffer]
- 设计一个诊疗费率自动申报系统。能够自动读取医生病历笔记，并按照规范将计费代码精准匹配发送给保险公司。 [^igotanoffer]
- 设计一个智能商品导购 Chatbot。能够通过对话逐步摸清用户偏好，并联合检索后台的 SQL 商品库推荐最合适的物品。 [^igotanoffer]
- 设计一个利用大模型进行实时快速自动代码补全的 Autocomplete 引擎。 [^system-design-handbook]
- 设计一个 AI 驱动的法务助手系统。 [^system-design-handbook]
- 设计一个具备长期会话记忆、且能自动润色生成求职简历的 AI 应用。 [^system-design-handbook]
- 设计一个集成在企业 Slack 内部、专门解答员工各种人事考勤问题的 HR 智能小助手。 [^system-design-handbook]
- 设计一个类似于 GitHub Copilot 实时流式自动代码补全的前后端交互服务。 [^system-design-handbook]
- 接上题，继续优化该 Copilot 架构，使其能在高并发下稳定输出代码补全。 [^colin-zhou]
- 设计一个支持日均百万用户排队渲染的 AI 画图服务（如 Midjourney / Stable Diffusion）（涉及推理队列与 GPU 算力弹性调度）。 [^colin-zhou]
- 设计类似于 Perplexity.ai 的实时联网大模型问答引擎。 [^colin-zhou]
- 设计一个“吉卜力画风图像生成器”。包含图片 prompt 接收、模型自动路由路由、GPU 并发推理、算力费用超标防刷以及违规图拦截机制。 [^rohit-verma]
- 为保险投保平台设计一个“动态问卷生成引擎”。后端配置好规则，前端根据用户每次点击的回答自主计算生成后续的问题决策树，无需频繁回传请求给服务器。 [^rohit-verma]
- 设计一个海量用户画像存储系统。需支持多端数据同步、灵活的个人偏好配置，并能支持 1 亿以上用户的批量平滑迁移。 [^linkjob-openai]
- 设计一个超大规模的分布式搜索引擎。能够收录 10 亿级以上文档数据，承载 100 万 QPS 检索，并能支撑每秒 10,000 次以上的大模型并发推理提取。 [^linkjob-anthropic]
- 设计一个高性能混合检索系统（Hybrid Search）。从 1000 万文档库中召回最匹配的 Top-K 结果，系统整体响应延迟必须控制在 50ms 以内。 [^linkjob-anthropic]
- 假设你拥有目标客户端网站的 HTML 重写 API 权限。设计一个自动化 Agent 工作流，能够自动爬取并定位数千个客户网站上的所有死链，并一键完成 HTML 修复替换。 [^proptech-founder-2]
- 针对时延经常发生严重抖动、生成速度较慢的 AI 智能体，你该如何设计优雅的交互前端界面 (UX) 以缓解用户的等待焦虑？ [^igotanoffer]
- 在不破坏用户信任感的前提下，大模型系统发生输出错误、断流或内容违规拦截时，你如何向终端用户呈现友好的报错提示？ [^igotanoffer]
- 设计一个日均处理千万级请求的高性能分布式图像生成流水线。 [^interviewnode]
- 接上题，如果该图文生成服务要扩容支撑全球数亿级用户，你又该怎么对服务层进行架构调优？ [^interviewnode]
- 用原生数据结构，在内存中设计一个支持 SET, GET, BEGIN, ROLLBACK, COMMIT 以及嵌套事务（Nested Transactions）的内存型数据库。 [^devto-xai]
- 设计一个大模型智能推荐系统。 [^reddit-swe-to-ai]
- 设计一个线上信用卡防欺诈交易检测系统。 [^reddit-swe-to-ai]
- 从大模型 API、后端业务路由以及数据流闭环出发，端到端绘制一个智能客服的整体系统架构图。 [^reddit-swe-to-ai]
- 设计一个支持断点续训（Checkpointing）、弹性抢占与高可用调度的分布式 GPU 训练队列系统（支持 10 万+卡并发作业）。 [^reddit-xai-eng]
- 设计一个支持异常气候检测的混合系统设计题（融合经典回归算法与 LLM 推理提取）。 [^reddit-grilled-rag]
- 设计一个包含：数据灌入、文本清洗、语义索引建立、多级检索、大模型生成、自动质量评估、运行 Trace 追踪以及双向安全护栏在内的端到端 RAG 闭环系统。 [^reddit-eightfold-ai]
- 现场现场设计并手写一个并发限流器（Rate-limiter）的核心逻辑代码。 [^reddit-xai-eng]
- 详述大模型应用在扩容至服务数百万日活用户时面临的系统瓶颈：包括延迟与成本的权衡折中、多层批处理机制、语义缓存、流式推送以及线上失败退化方案。 [^reddit-2026-prep]
- 设计 ChatGPT 的跨会话长期记忆存储与偏好同步功能。 [^igotanoffer]
- 设计一个能够自动协调多名 Agent（如会议日程助手、代码审核助手、营销邮件助手）协同工作的流程引擎。 [^promptlayer]
- 设计一个 AI 安全内容风控拦截网关。 [^igotanoffer]
- 设计一个能横跨邮件、日历、云文档以及即时通讯软件的统一语义搜索引擎。 [^x-avi-chawla-1]
- （IBM 真题）详细陈述将一个生成式 AI 构想从立项会讨论、算法开发、评测，一路推向线上正式生产部署的完整软件工程周期。 [^raghu-teja-2]
- 设计一个高可靠的自动化工作流系统。你会从哪些维度去设计其异常处理机制（Error Handling）、可观测性监控与线上 Debug 链路？ [^proptech-founder-1]
- 你们在架构上是如何处理实时数据流更新 vs 离线批量处理的？它们各自的技术取舍是什么？ [^proptech-founder-2]
- 针对海量的结构化数据、无结构文本以及流式事件数据，你们是如何设计统一的数据清洗灌入系统的？ [^proptech-founder-1]

### B. 经典分布式系统设计 (Traditional System Design)
- 设计 GitHub Actions 持续集成流水线引擎。 [^hello-interview]
- 设计 Slack 即时通讯后台。 [^hello-interview]
- 设计一个支持全球联机对战的国际象棋系统。 [^hello-interview]
- 设计一个支撑海量并发的分布式支付网关系统。 [^hello-interview]
- 设计一个具备高可靠重试与异步通知机制的 Webhook 回调推送系统。 [^hello-interview]
- 设计 TinyURL（短链生成与重定向系统）。 [^colin-zhou]
- 设计 Instagram / TikTok 的 Feed 流（关注、发布、时间线推送）。 [^colin-zhou]
- 设计 Twitter / X 的核心架构（涉及高并发发帖、时间线合并、关注者路由及热搜算法）。 [^colin-zhou]
- 设计 Netflix / YouTube 的全球视频流分发与加速平台。 [^colin-zhou]
- 设计 Uber 派单与打车后台（涉及地理网格匹配、ETA 计算和动态加价）。 [^colin-zhou]
- 设计 WhatsApp / 微信级别的全球即时通讯系统。 [^colin-zhou]
- 设计一个分布式 KV 存储系统 (DynamoDB / Cassandra)。 [^colin-zhou]
- 设计 Google Docs 多人实时协同编辑系统。 [^colin-zhou]
- 设计 Yelp / 谷歌地图的“附近商家/周边定位”语义搜索引擎。 [^colin-zhou]
- 设计一个高并发分布式限流器 (Rate Limiter)。 [^colin-zhou]
- 设计 Discord 实时音视频及文字聊天服务器（考核支持数百万人同时在线的多人语音频道架构）。 [^colin-zhou]
- 设计符合 PCI 合规要求、高一致性、无资金错账的 Stripe 支付扣款平台。 [^colin-zhou]
- 设计一个支持行星级任务调度的分布式批处理引擎（如 AWS Batch 架构）。 [^colin-zhou]
- 设计一个分布式推送服务。要求日均能够下发 10 亿次消息推送，且消息丢失率低于 1%。 [^colin-zhou]
- 设计一个满足强一致性（Strong consistency）要求的分布式数据库（类似 Google Spanner / CockroachDB）。 [^colin-zhou]
- 设计高频交易系统（HFT）后台的极速撮合交易引擎。 [^colin-zhou]
- **线上排障情景题**：公司的 P99 响应延迟在一夜之间从正常的 50ms 暴涨到了 2,000ms。你在没有任何线索的情况下，怎么一步一步通过监控去排查并解决这个问题？ [^colin-zhou]
- 设计一个支持千万级长连接并发的全球 WebSocket 推送服务。 [^colin-zhou]
- 设计一个支持多区域部署、且能在零宕机下灰度分发的“分布式特性开关与配置中心 (Feature Flag)”。 [^colin-zhou]

### C. 线上故障与应急响应 (System Troubleshooting)
- 系统的 P95 响应延迟在短短几分钟内从正常的 100ms 飙升到了 2,000ms。作为值班负责人，你如何通过几板斧快速定位性能瓶颈？ [^linkjob-anthropic]
- 当遭遇 10 倍于平时的突发流量洗劫时，你如何采取限流和降级手段保护系统不彻底崩溃？ [^hello-interview]
- 如果公司的核心机房突然整体断电宕机 6 个小时，你的全球灾备冗余架构怎么保证数据不丢失、并且平滑将流量切走？ [^hello-interview]


## 3. 上机编程与算法面试题 (Coding Problems)

### A. 数据结构与算法 (DSA)
- **Trie + DFS 找单词**：在字符网格上进行单词搜索（LeetCode Medium 题变种）。 [^devto-xai]
- **双向链表手写 LRU 缓存**：使用哈希表 + 双向链表手写实现 O(1) 复杂度的 LRU 缓存。 [^devto-xai]
- **求出 0 到 100 之间的所有质数**。 [^khushal-kumar]
- **判断两个字符串是否互为字母异位词 (Anagrams)**。 [^khushal-kumar]
- **序列化与反序列化二叉树**：要求极致优化传输显存，并考虑版本升级后的向前/向后兼容性。 [^rohit-verma]
- **设计 SQL 引擎 (Design SQL)**：LeetCode 2408 题。 [^hello-interview]
- **基于时间戳的键值存储 (Time Based Key-Value Store)**：LeetCode 981 题。 [^hello-interview]
- **实现类 Unix 的 `cd` 路径切换命令**（核心考点是支持软链接 Symbolic links 的解析）。 [^hello-interview]
- **带限制条件的反转链表**（微软应用 AI 岗真题，AI 协作轮：要求候选人通过有效的 Prompt 引导 ChatGPT 写出代码，并快速修改）。 [^reddit-microsoft-aiml]
- **求 Excel 列名算法**：根据给定的列数字返回 Excel 中的字母列名（例如：第 702 列 = "AAA"）。 [^reddit-microsoft-aiml]
- **重建树形结构**：根据给定的数组序列（其中 `index = 节点值`，`value = 父节点`）现场重建二叉树（LeetCode Medium 题）。 [^reddit-microsoft-aiml]
- **CodeSignal GCA 现场测试**：70 分钟手撕 4 道题（包括两道 Medium-Hard 题、一道图遍历、以及一道结合位运算的贪心算法）。 [^reddit-xai-eng]
- **双系统混合编程题**：第 1 部分手撕一个并查集 (Union Find) 算法；第 2 部分使用 PyTorch/DistilBERT 编写脚本分类 CSV 格式文本的积极/消极情绪。要求代码完全跑通 5 个自带的测试用例。 [^reddit-ai-eng-questions-2]
- **任务执行器设计**：仅使用 HashMap/TreeMap 设计一个银行核心交易记账系统，且能够支持暂停、恢复特定批次任务的执行。 [^reddit-2026-prep]
- **gRPC 超时 Debug**：一段 gRPC 线上服务频繁超时的代码。要求现场添加异步隔离边界，设计重试、死信队列及幂等性，并使用线程池进行吞吐扩容。 [^exponent-mock]
- **序列化深度讨论（无代码）**：现场深入剖析常见序列化协议（Protobuf vs JSON）、压缩算法选择、流式数据传输设计以及网络防数据损毁重传策略（微软资深岗位考核）。 [^rohit-verma]

### B. OpenAI 专属编程真题
- 内存型 KV 数据库的序列化与反序列化设计。 [^hello-interview]
- **内存数据库设计**：在内存中用原生数据结构实现类似于关系型数据库的 JOIN、WHERE 过滤等操作。 [^hello-interview]
- **带时间旅行的 KV 存储**：实现一个能支持读取历史任意时间戳快照的 Versioned KV 数据库。 [^linkjob-openai]
- **积分生命周期管理系统 (Credits Management)**：设计一个模块用于追踪用户积分的下发与消费逻辑。需支持不同的过期规则和抵扣权重，需求会不断追加复杂度。 [^exponent-openai]
- **垃圾代码重构 (Refactoring)**：给你 100 到 120 行嵌套极深、命名混乱、毫无可读性的意大利面式代码。限时现场将其重构，要求结构清晰、易测试，且确保已有测试用例完全通过。 [^exponent-openai]

### C. Anthropic 专属编程真题
- **4-Level 渐进式开发**：
  - **Level 1**：写出基本的 SET/GET/DELETE。
  - **Level 2**：追加 SCAN 和前缀匹配过滤功能。
  - **Level 3**：引入带时间戳的写入与 TTL 过期机制。
  - **Level 4**：设计底层的网络数据压缩存储与存储空间熔断管理。 [^linkjob-anthropic]

### D. 机器学习与 AI 算法实现
- **1-NN分类器手写**：现场从零写出 1-NN 分类器（最简 KNN 算法）以及一个前馈神经网络。 [^linkjob-openai]
- **Transformer 底层排障**：给你一段写好的 Transformer 代码，要求现场 Debug 其中的位置编码（Positional Embedding）维度错误以及 KV Cache 缓存泄漏 Bug。 [^linkjob-openai]
- **PyTorch 完形填空**：补全给定的 PyTorch 神经网络前向传播代码，并分析其空间复杂度。 [^linkjob-openai]
- **多头注意力手写**：仅通过大脑记忆，在白板上手撕 Multi-Head Attention 计算逻辑。 [^sundeep-teki]
- **Transformer 层手写**：仅通过大脑记忆，在白板上手写出 Transformer Layer 的全套前向传播。 [^sundeep-teki]
- **LoRA 算子手写**：从零开始写出 LoRA 适配器（Adapter）的参数更新矩阵计算。 [^yuan-meng]
- **高并发大模型请求批处理**：写一段高性能的多线程代码，对海量大模型 API 调用请求进行并发分批（Batching）发送与错误重试。 [^promptlayer]
- **向量对齐 Debug**：走读并 Debug 一段在向量嵌入对齐和计算中发生维度漂移或 NaN 异常的代码。 [^promptlayer]
- **数据清洗脚本编写**：编写 Python 脚本将杂乱的业务文本清洗并导出为符合大模型微调格式的 JSONL 数据集。 [^promptlayer]
- **财报异步总结 gRPC 服务**：编写一个 gRPC 微服务，异步接收财报文件，采用多线程并发总结，并处理超时退化与异常捕获。 [^exponent-mock]
- **NumPy 手撕神经网络**：仅使用 NumPy，手写实现基本的神经网络、LSTM 以及循环神经网络（RNN）结构。 [^mimansa-jaiswal]
- **GQA分组注意力手写**：实现带缓存的注意力机制（Cached Attention）以及分组查询注意力（Grouped Query Attention）算子。 [^mimansa-jaiswal]
- **解码搜索策略手写**：使用 NumPy 从零写出 Beam Search (束搜索)、Top-K 与 Top-P 采样解码算法。 [^mimansa-jaiswal] [^datainterview-mistral]
- **自回归生成与采样**：手写自回归解码生成流程，并引入 Top-P 采样机制。 [^datainterview-mistral]
- **逻辑回归与 SGD 手写**：仅使用 NumPy，从零实现带 L2 正则项与 Early Stopping 机制的逻辑回归模型，并手写随机梯度下降（SGD）更新公式。 [^datainterview-mistral]
- **交叉验证手写**：手写实现分层 K 折交叉验证数据集切分算法（Stratified K-fold）。 [^datainterview-mistral]

### E. 数据采集与流式处理
- **高速度 JSON 总结**：限时 30 分钟。给你一个结构极其复杂的 JSON 文件，要求现场用 Python 编写脚本提取特定规律的内容，并自动请求大模型进行信息总结（允许使用浏览器和 ChatGPT 辅助）。 [^khushal-kumar]
- **高可靠多线程爬虫**：设计并手写一个并发网页爬虫。要求能够遵守 robots.txt 规范、具备 Rate-limiting 频率限制、能够自动识别并跳过循环引用，同时保证爬取数据的时效性。 [^linkjob-anthropic]


## 4. 行为面试真题 (Behavioral Questions)

### A. 简历项目深度答辩
- 请为我拆解一个你之前从零构建到上线的完整 AI 项目。 [^process-analysis] [^reddit-2026-prep]
- 分享一个最让你有成就感的项目，并详述你在其中扮演的角色。 [^fahd-mirza] [^reddit-2026-prep]
- 在你过往的经历中，最具技术挑战性的 AI 项目是什么？ [^igotanoffer]
- 讲一个你在生产环境下，通过优化系统架构成功为公司拦截大模型幻觉、或缩减大模型 Token 开销的真实例子。 [^process-analysis]
- 描述一次你为了提升系统效率或扩容性能，而对现有流程或工作流进行重构的经历。 [^proptech-founder-1]
- 描述一个你攻克过的、极具挑战性的提示词工程（Prompt Engineering）难题。 [^proptech-founder-1]
- **你们的项目真的写了评测脚本吗？还是全凭感觉调优？** [^exponent-openai]
- 现场向技术评审委员会陈述你最满意的一个项目：包括核心决策、折中选择、翻车故障以及未来重构打算。 [^reddit-2026-prep]
- 详细拆解你过往简历中写到的系统架构。（苹果、Discord、Anduril 常见考题） [^exponent-behavioral]
- 聊聊你最近/最满意的一个项目，以及你在开发中遇到的最大技术难题。（Meta 常见考题） [^igotanoffer-meta]
- 讲一个你曾经跨越过的重大技术障碍。 [^exponent-behavioral]
- 聊聊你职业生涯中最值得骄傲的工程成就。（Meta 常见考题） [^igotanoffer-meta]
- 你过去手写过的 Prompt 最复杂到什么程度？在此基础上开发过什么复杂的产品？ [^khushal-kumar]

### B. 冲突解决与团队协作
- 讲一个你在技术讨论中与同事产生严重技术冲突的真实经历。你最后是怎么处理的？ [^exponent-openai]
- 在开发 AI 产品时，你平时是如何与非技术的产品、运营部门协同并定义产品边界的？ [^fahd-mirza]
- 在高度扁平、且处于多时区分布式办公的团队中，你平时是怎么进行协作与排期的？ [^fahd-mirza]
- 聊聊你在项目中遇到技术冲突时的解决思路。 [^rohit-verma]
- 讲一次你不同意组内成员的架构方向，并最终说服他采纳你意见的经历。 [^interviewnode-behavioral]
- 讲一个你曾经面对并搞定过的某位“极难沟通的同事”。（Meta 常见考题） [^igotanoffer-meta]
- 聊聊你曾经面对并搞定过的某位“极难沟通的业务方（Stakeholder）”。 [^exponent-behavioral]
- 讲一次你必须向完全不懂技术/算法的业务人员解释复杂模型底层逻辑的经历。 [^interviewnode-behavioral]
- 讲一次你成功说服别人放弃原有主张、改用你的架构设计方案的经历。 [^exponent-behavioral]
- 谈谈你以往共事过的同事中，哪一类技术风格的人是你最不喜欢合作的？（Visa 常见考题） [^exponent-behavioral]
- 描述一次你通过极佳的技术沟通，在一片混乱和需求不明确的环境下带领团队理清思路的经历。（Anthropic 常见考题） [^prachub-anthropic]
- 讲一个你克服跨团队沟通障碍，推动 AI 产品按时上线的经历。（OpenAI 常见考题） [^exponent-openai-behavioral]

### C. 技术领导力与所有权 (Leadership & Ownership)
- 你平时在远程办公中带教过组员吗？你是怎么带的？ [^fahd-mirza]
- 描述一次你作为主要技术负责人，架构了一套高并发复杂系统并带领团队攻克硬核技术瓶颈的经历。 [^hello-interview]
- 讲讲你是怎么在日常工作中带教（Mentor）组员并帮助他晋升为资深开发的。 [^hello-interview]
- 讲一次你展现卓越领导力的经历。（OpenAI 研发主管常见考题） [^igotanoffer-openai]
- 讲一次你作为主要负责人驱动某项复杂技术交付、或在面临重大难题时主动承担并兜底的经历。 [^interviewnode-behavioral]
- 讲一次你在别人都没站出来时，自己出于强烈的责任感主动去处理某个疑难杂症的经历。 [^interviewnode-behavioral]
- 讲一次你为了追求长线收益，而在短期内被迫做出妥协或牺牲的经历。 [^exponent-behavioral]
- 面对每天涌来的大量复杂任务，你平时是如何科学进行优先级排期的？ [^exponent-behavioral]
- 当项目面临高度风险和未知的技术盲区时，你作为技术骨干如何稳定军心并成功交付？（Anthropic 常见考题） [^prachub-anthropic]
- 作为技术主管，你是如何在项目的交付速度与技术债之间做权衡的？（OpenAI 研发主管常见考题） [^igotanoffer-openai]
- 作为主管，你平时是通过什么手段去激发和规划组员的长期职业晋升道路的？（OpenAI 研发主管常见考题） [^igotanoffer-openai]
- 讲一次你面临极其紧迫的上线排期压力时，如何妥协范围并按时完成交付的经历。 [^exponent-behavioral]
- 详细阐述你的技术管理哲学、开发执行逻辑以及如何建立团队的极客文化。（Anthropic 常见考题） [^prachub-anthropic]

### D. 复杂技术决策制定 (Technical Decision-Making)
- 针对内容创作任务，你更倾向于选用哪家厂商的 API 模型？说说你的理由。 [^promptlayer]
- 你怎么评价 Cursor, Windsurf 和 Claude Code 这些 AI 编码助手的优缺点？ [^promptlayer]
- 最近哪一篇大模型学术论文或行业技术进展最让你感到兴奋？ [^promptlayer]
- 聊聊你业余时间折腾过的 AI Side Projects 细节。 [^promptlayer]
- 为什么在当时选择方案 A，而不是更主流的方案 B？ [^exponent-openai]
- 线上部署大模型时，你当时是用什么指标去评估并挑选推理模型的？ [^exponent-openai]
- 你平时对哪些大模型框架比较熟悉？写过哪些项目？ [^reddit-ai-eng-questions]
- 你们项目里用了什么大模型？平时跟哪些云服务商合作？ [^reddit-ai-eng-questions]
- 讲一次你解决过的最棘手的技术 Bug，你是如何排查和抽丝剥茧最终定位问题的？ [^exponent-behavioral]
- 讲一次你在项目中因为技术判断失误（如选错了向量库或低估了模型推理延迟）导致项目延期的惨痛教训。你从中学到了什么？（Anthropic 真题） [^linkjob-anthropic]
- 如果项目进行到一半，你突然发现基于当前大模型的能力这个方案在技术上完全行不通（Unfeasible），你会怎么应对？（Anthropic 真题） [^linkjob-anthropic]
- 描述一次你需要在一周甚至更短的时间内，迅速上手并掌握一门全新编程语言或技术栈的经历。 [^interviewnode-behavioral] [^x-allie-miller]
- 你们在架构上是如何处理实时数据流更新 vs 离线批量处理的？它们各自的技术取舍是什么？ [^proptech-founder-2]

### E. 失败反思与技术精进
- 聊聊你开发过的最难的项目。 [^rohit-verma]
- 如果能让你从头重新设计这个系统，你会做出哪些不同的架构改变？ [^exponent-openai]
- 讲一次你收到上级或组员对你的技术差评（Negative feedback）时的经历。你当时作何反应？ [^exponent-behavioral]
- 聊聊你职业生涯中犯过的最严重的技术错误。你从中学到了什么？ [^interviewnode-behavioral]
- 聊一个你主导过的、但最终失败了的技术架构项目。你的核心反思是什么？（Anthropic 真题） [^interviewquery-anthropic]
- 描述一次大模型解决方案线上严重幻觉或退化导致线上翻车的事故。你们当时是怎么拦截和恢复的？（Google DeepMind 真题） [^educative-deepmind]
- 你认为我们公司在这场面试后，出于什么合理的技术担忧，**不应该录用你**？（谷歌、Visa 真题） [^exponent-behavioral]
- 讲一次你在任务面临死胡同时，被迫“打破常规思维（Think outside the box）”最终解决战斗的经历。 [^interviewnode-behavioral]

### F. AI 原生开发价值观
- 面对日新月异的技术，你平时是通过哪些渠道和方法，实时跟进前沿的 AI 技术动态的？ [^process-analysis] [^exponent-behavioral] [^x-michael-taiwo]
- 在开发 AI 产品时，你平时是如何与非技术的产品、运营部门协同并定义产品边界的？ [^process-analysis]
- 讲一个你在机器学习项目中，主动发现并纠正其中潜在道德/隐私合规（Ethical concerns）风险的经历。 [^interviewnode-behavioral]
- 讲一次你在技术选型中，坚持“安全第一（Safety-first）”而驳回了高风险技术方案的经历。（Anthropic 真题） [^interviewquery-anthropic]
- 讲一次你在大模型架构中预先识别出重大性能退化风险，并主动推进重构的经历。（Mistral 真题） [^datainterview-mistral]
- 讲一个你成功帮公司砍掉大模型 Token 费用或响应时延的真实案例。 [^fonzi-ai]
- 面对极不确定的算法指标和不断变化的业务需求，你平时是如何在 ML 团队中带大家推进迭代的？ [^interviewnode-behavioral]
- 你平时在日常开发中是如何使用 Cursor / Copilot 等 AI 编码工具提升工作流效率的？ [^youtube-proptech]
- 你是否曾经极富创意地把大模型引入到一个原本被认为根本不需要大模型参与的传统关系表中，并取得了不错的成效？ [^reddit-devsindia-genai]
- 大模型生成的代码和文字，你会进行交叉验证核对，还是直接选择相信？能分享一下你平时核对大模型输出的心得吗？ [^x-michael-taiwo]

### G. 企业价值观与动机
- 为什么选择我们公司？ [^exponent-openai] [^rohit-verma]
- 为什么在这个节点选择离职跳槽？ [^rohit-verma]
- 介绍一下你自己。 [^exponent-behavioral]
- 请为我走读和走读一遍你的简历。（OpenAI 常见考题） [^igotanoffer-openai]
- 谈谈你过去的每一次离职选择和职业跨越，这与你的职业价值观有什么内在关联？（Anthropic 常见考题） [^prachub-anthropic]
- 当大模型安全准则（AI safety）与业务团队追求的产品上线进度发生激烈冲突时，你通常如何处理？（Anthropic 常见考题） [^prachub-anthropic]
- （针对算法研究岗位）你为什么想要进入工业界做模型研究，而不是留在学术界？ [^deepthi-sudharsan]

### H. AI 面试官（智能体）追问高频提问
*（Eightfold.ai 等公司采用 AI 智能体面试时的机器人追问套路）*
- 针对你刚才的代码实现，你如何处理并发和各种边界 edge cases？ [^eightfold]
- 除了这套设计，你当时还对比过什么其它的代码逻辑方案？ [^eightfold]
- 请现场推导你刚才所写核心算法的时间复杂度与空间复杂度。 [^eightfold]
- 为什么在这个环节选用了这个特定的数据结构？ [^eightfold]


## 5. 项目深度探究 (Project Deep Dive) 真题

*（注：此轮次通常需要候选人现场投屏，针对一个既往的核心项目，向专家组进行 25-45 分钟的详细技术汇报并接受技术质询。）*

### 开场提问
- 现场演示并为我详细剖析你简历里写到的最具技术难度的项目。（OpenAI 真题 —— 45分钟结对工程师汇报） [^exponent-openai]
- 请深度剖析一个你拥有绝对所有权（Owned end-to-end）的项目，并陈述你在里面做出的最关键的架构抉择。（Anthropic 真题 —— 25分钟展示 + 20分钟盘问） [^prachub-anthropic]
- 谈谈你最引以为傲的项目以及你在其中的核心技术输出。（OpenAI 常见考题） [^igotanoffer-openai]
- 聊聊你最近/最满意的一个项目，以及你在开发中遇到的最大技术难题。（Meta 常见考题） [^igotanoffer-meta]

### 面试官追问细节 (Follow-up Probes)
- 为什么在当时选择方案 A，而不是更主流的方案 B？ [^exponent-openai]
- 你们的项目真的写了评测脚本吗？还是全凭感觉调优？（OpenAI 追问） [^exponent-openai]
- 你当时对比过什么其他的备选架构？为什么最终驳回了它们？ [^exponent-openai] [^hello-interview]
- 如果业务需求突变或系统流量暴增 100 倍，你的系统架构该如何做适配扩容？ [^hello-interview]
- 如果能让你从头重新设计这个系统，你会做出哪些不同的架构改变？ [^exponent-openai]
- 项目开发中，最难的一个技术选型决定是什么？你是怎么下决心的？ [^exponent-openai]
- 你的架构方案上线后真的起效了吗？有哪些业务指标（Metrics）可以向我证明？ [^exponent-openai]
- 你在项目中做出了哪些技术妥协？系统线上运行至今，你依然觉得这些妥协是合理的吗？ [^prachub-anthropic]
- 你是如何向非技术的业务部门或 Stakeholders 汇报和推销你的技术决策的？ [^prachub-anthropic]
- 如果再给你多两个月时间，你会继续在哪些技术方向上做深度的探索？ [^hello-interview]
- 模型部署上线后，你是如何监控线上数据漂移（Drift）或模型质量退化的？ [^linkjob-anthropic]
- 谈谈你在系统中为检索延迟 vs 上下文长度、模型微调 vs 提示词工程、以及算力成本 vs 生成精度这几对冲突所做出的设计取舍。 [^hello-interview]


## 6. Take-Home 离线作业真题

*关于候选人实际提交的 100+ 个 GitHub 真实作业仓库的完整索引，请查阅 [GitHub 离线作业数据集](../data/sources/github-repos.md)。*

### A. RAG 与文档问答系统
- **PDF 诊疗诊断系统**：用户上传 PDF 格式的验血报告，大模型自动抓取解析报告中的各项医疗数据，联网匹配医学博客文章生成一份健康建议（限时数小时内提交）。 [^khushal-kumar]
- **生产级客服 RAG 系统**：仅使用开源大模型与向量数据库，搭建一个支持 100+ 用户并发在线、延迟低于 2 秒、配备线上监控和 Token 成本核算的客服 Chatbot。 [^devto-mai-chi-bao]
- **多跳转索问答**：构建一个能自动处理多跳提问（Multi-hop question）并附带出处引用的企业知识库问答系统。 [^promptlayer]
- **标准 cited RAG 服务**：构建一个 RAG 问答机器人。能够上传 PDF/文档，在向量数据库中生成 embeddings，并针对提问进行回答，回答必须强制附带出处引用（Citations）。 [^gh-rokomari] [^gh-streamkar] [^gh-dge-1] [^gh-dge-2] [^gh-bmw] [^gh-ncapek]
- **屎山代码重构 (RAG Refactoring)**：将一个包含大量全局变量且毫无单元测试的 RAG 遗留系统，在保持其外部所有 API 行为不变的前提下，重构为整洁、模块化、可 mocks 测试的优秀架构（FastAPI + LangGraph 架构）。 [^gh-bithealth-1] [^gh-bithealth-2] [^gh-bithealth-3] [^gh-bithealth-4] [^gh-bithealth-5]
- **合规文档助手**：开发一个基于公司合规手册的 RAG 问答机器人，所有回答必须附带条文来源。系统附带一个包含 7 个典型测试问题的评测包，量化评估输出准确度。 [^gh-neura-dynamics]

### B. 智能体 Agent 开发
- **高分自主 Agent**：在限时 3 天内，使用 OpenAI/Claude 开发一个能体现出色工程直觉、条理清晰的自主运行智能体（Eightfold.ai 真题）。 [^eightfold]
- **用户账单分析邮件 Agent**：构建一个能读取客户 CSV 表单、自动统计分析其账单订阅状态、并生成个性化推荐营销邮件的 Agent。 [^promptlayer]
- **Python 代码审查智能体**：开发一个能够遍历审查 Python 文件、定位语法 Bug 和性能隐患并给出重构建议的代码审查 Agent。 [^promptlayer]
- **会议预约 Agent**：基于 LangGraph + Streamlit 前端 + FastAPI 后端，实现一个能够调用谷歌日历 API 并能智能帮用户预约/取消日程的会议助手。 [^process-analysis]
- **极速客服 Agent（YC 孵化器真题）**：限时 1.5 小时内，开发一个贴合初创公司业务的客服 Agent。若提交的文件中完全没有写自动评测逻辑（Evals），面试直接挂掉。 [^reddit-yc-assignment]
- **本地开源 Agent 搭建**：使用本地运行的开源模型建立一个具备可观测性追踪面板的自主智能体。 [^reddit-yc-assignment]
- **带 bash 执行的工具 Agent**：构建一个智能体，支持大模型自动查询数据库、检索文档并在后台执行 bash 命令行。所有涉及 bash 命令的操作必须在执行前弹出，由用户手动点击确认。 [^gh-curling-ai]
- **项目管理分析 Agent**：使用“主模型 + 灾备模型”的“双模型架构（Dual-LLM）”，自动从 Monday.com 中提取项目看板数据并转换为商业简报。 [^gh-skylark]
- **纯开源政务问答 RAG (GovGPT)**：开发一个专门处理政务公开信息的智能体 RAG 系统，要求全栈 100% 采用开源技术（Ollama + CrewAI + pgvector），且采用 RAGAS 评测标准打分。 [^gh-govgpt]
- **智能广告策划 Agent**：设计并交付一个可以通过对话自动完成广告词生成与投放的 TikTok 广告策划 Agent。 [^gh-tiktok-agent]

### C. 多智能体协作系统
- **5-Agent 协同创作流水线**：选题调研 Agent $\rightarrow$ 撰写 Agent $\rightarrow$ 内容编辑 Agent $\rightarrow$ SEO 优化 Agent $\rightarrow$ 发布排版 Agent。输入 JSON 后自动产出精美的 FAQ 等页面。 [^gh-kasparro]
- **超轻量级工作流状态机引擎**：自行编写一个支持有向图节点跳转、状态持久化管理、逻辑分支判断和工具调用的微型 Agent 引擎。要求单次运行步骤限制在 50 步以内，且系统内核必须具备底层的“无限死循环自我熔断机制”。 [^gh-tredence-1] [^gh-tredence-2] [^gh-tredence-3] [^gh-tredence-4] [^gh-tredence-5] [^gh-tredence-6]
- **CBT 智能疗愈 Agent**：开发一个包含 5 个 Agent 协同工作的 CBT 心理治疗系统。必须集成敏感词风控过滤和隐私脱敏技术。 [^gh-cerina]

### D. 评测系统 (Evaluation)
- **大模型幻觉自动评测插件**：开发一个轻量级的评测工具，能对给定的文本生成进行自动幻觉检测。 [^hn-42182365]
- **四阶段睡前故事创作流水线**：Spec 需求制定 Agent $\rightarrow$ 故事撰写 Agent $\rightarrow$ 大模型裁判 Agent $\rightarrow$ 重写调优 Agent。系统要求在 gpt-3.5-turbo 模型下稳定运行，如果裁判不通过，最多允许触发 2 次自动迭代重写。 [^gh-hippocratic-1] [^gh-hippocratic-2] [^gh-hippocratic-3] [^gh-hippocratic-4]
- **合规财务看板 Agent**：构建一个面向企业账单订阅的财务分析 Agent。智能体需要能够根据用户提问，自动对账单进行聚合统计（如求和、求平均）。系统禁止大模型直接接触原始数据行以保护隐私，并重点评测准确度与安全越权拦截。 [^gh-cohere]
- **零幻觉客服 Chatbot**：构建一个完全受限在已知 FAQ 知识库内的在线客服 Agent，提供 2 份使用不同技术栈的候选人高分提交进行对比。 [^gh-spur-1] [^gh-spur-2]

### E. 数据清洗与信息解析抽取
- **非规范成绩单 OCR 强类型抽取**：使用 FastAPI + Docker + Gemini 1.5 Flash 搭建 API 服务。能够识别排版极度混乱且包含手写签名的成绩单图片，将其中的表格和签名状态稳定提取为结构化的标准 JSON 数据。 [^gh-trestle]
- **医生面诊语音总结 API**：将面诊过程中医生与患者的长篇现场对话录音/文本，自动清洗并提炼为标准的 SOAP 格式电子病历。 [^gh-emitrr-1] [^gh-emitrr-2]
- **屎山重构**：将一个包含大量全局变量且毫无单元测试的遗留系统，在保持其外部所有 API 行为不变的前提下，重构为整洁、模块化、可 mocks 测试的优秀架构。 [^gh-bithealth-1]
- **智能法务合同审核**：输入一份长篇法务合同，自动识别并提取核心起止日期，提取出合同中的潜在法务风险（如自动续订陷阱、无限责任免责条款、竞业协议、知识产权归属等），生成总结报告。 [^gh-legal-doc]

### F. 语音与多端交互
- **印度方言实时电话会议听写**：设计并实现一个针对印度英语口音的财报电话会议流式听写与要点总结系统。 [^gh-voice-ai]
- **新加坡出行语音智能体**：开发一个基于语音问答界面的新加坡公交出行智能体。 [^gh-hrytos]
- **Telegram 投资理财教练**：限时 3 天。设计一个 Telegram 投资理财教练机器人，包含严格的数据风控过滤，坚决不提供任何个股推荐。 [^gh-pineos]
- **带会话持久化的客服 Chatbot**：使用 OpenAI 开发一个在线客服机器人，要求能够完整保留多轮对话会话 Session 状态。 [^gh-spur-1] [^gh-spur-2]
- **智能裁判 Agent**：开发一个支持“石头剪刀布”卡牌游戏规则自动判定的 AI 裁判 Agent，并包含游戏规则评测体系。 [^gh-upliance-1] [^gh-upliance-2]

### G. 全栈 AI-First 业务应用
- **高维 AI-First 客户关系管理 (CRM) 平台**：前端采用 React/Redux 构建美观页面，后端采用 FastAPI，引入 LangGraph 并编写 5 个以上可执行工具。要求提交完整的 GitHub 代码仓库并录制 10-15 分钟的 Loom 演示视频讲解你的系统架构。（预估开发时间 60 小时）。 [^process-analysis]
- **带验证功能的登录页**：开发一个带表单校验功能的标准用户登录页面（预估耗时 2-3 小时）。 [^devto-aidi-rivera]
- **心理健康 MVP 应用**：构建一个满足生产级合规要求的在线疗愈心理助手，集成脱敏、安全风控与评测。 [^gh-mindwell]
- **高性能大模型路由网关**：开发一个高可用的 LLM 路由中间件。要求具备：智能语义路由、二级缓存（完全匹配缓存 + 向量语义缓存）、多家大模型厂商的健康监测与自动灾备切换、分布式追踪。（日均请求量设计：10万+次）。 [^gh-zuneko]
- **AI 协同模拟 NPC 引擎**：为模拟招聘系统设计 3 名性格迥异的 AI 模拟同事。 [^gh-edtronaut]
- **LLM 打分预测系统**：构建一个大模型反馈评测打分系统，包含可视化后台面板。 [^gh-fynd]
- **markdown 自动转 PPT 幻灯片**：实现用户 markdown 文件的一键解析切分并转换为 PPT 网页展示，附带 Token 消耗统计。 [^gh-gamma]
- **新闻排重与语义簇聚类流水线**：针对体育新闻数据，设计包含：字面去重、语义去重、大模型主导的聚类（Clustering）流水线。 [^gh-krisp]
- **商品聚合流水线**：实现多数据源的商品数据自动映射与清洗。 [^gh-deel]
- **D&D卡牌游戏智能体**：采用 LangGraph 构建一个包含“跑团城主 (DM) Agent + 多个 Player Agent”的多智能体跑团游戏。评分维度：功能健全度占比 30%、挑战完成度占比 30%、上下文工程占比 25%、代码质量占比 15%。 [^gh-context-engineering]
- **大模型记忆与人设控制器**：纯基于开源大模型，构建一个长期会话记忆管理与性格转化（如切换为幽默、严谨、同理心等风格）的 API。 [^gh-gupshup]

### H. 融合目标公司实际业务
- **Roboflow 真题**：在作业中被要求必须调用 Roboflow 的计算机视觉（CV）服务构建一个识别系统，并在终面上向其 CTO 进行演示技术辩论。 [^process-analysis]

### I. 极限性能优化作业
- **TPU 级性能优化（Anthropic 真题）**：给你一段模拟 TPU 矩阵计算的 Python 代码，限时 4 小时。要求候选人深入底层进行极致优化，压缩单次矩阵计算的时延（目前本题目已在开源社区发布，可用于练习）。 [^process-analysis]

### J. OpenAI 48 小时极速技术项目
- **48 小时实战**：在通过 HR 沟通的第二天，会收到一份限时 48 小时内提交的技术作业。只考核真实业务场景的功能编写，不考算法脑筋急转弯。 [^linkjob-openai]

### K. 面试排坑警告：警惕初创公司的免费咨询套路 (Red Flags)
求职候选人反馈的极其无礼且不合理的大量作业要求：
- 第一轮技术初筛，就直接给候选人布置“限时 72 小时，必须交付包含完整 RAG、Agents 和全套 UI 的系统”。 [^process-analysis]
- 某初创公司要求候选人把其公司积累数年的财报数据进行一键清洗、自动产出股票走势预测和动态图表，且必须使用完全免费的大模型 API。候选人识破后直接退赛，指出“这完全是在利用面试白嫖免费的顾问成果（unpaid mini-consulting project）”。 [^process-analysis-fr]
- 现场面试限时 45 分钟，要求候选人写完 3 个极具技术挑战的复杂并发项目。 [^process-analysis]

---

## 参考文献与数据源说明

[^proptech-founder-1]: [YouTube - Proptech Founder Part 1](https://www.youtube.com/watch?v=leXRiJ5TuQo)
[^proptech-founder-2]: [YouTube - Proptech Founder Part 2](https://www.youtube.com/watch?v=Zt-h5BiBWH0)
[^fahd-mirza]: [YouTube - Fahd Mirza](https://www.youtube.com/watch?v=yr5dRHrnbCo)
[^exponent-mock]: [YouTube - Exponent Mock Interview](https://www.youtube.com/watch?v=ZE_YEn-okfk)
[^youtube-short]: [YouTube Short](https://www.youtube.com/shorts/Nc1y9tYV2WM)
[^igotanoffer]: [igotanoffer - Generative AI System Design Interview](https://igotanoffer.com/en/advice/generative-ai-system-design-interview)
[^interviewnode]: [InterviewNode - GenAI System Design Patterns](https://www.interviewnode.com/post/generative-ai-system-design-interview-patterns-you-should-know)
[^system-design-handbook]: [System Design Handbook](https://www.systemdesignhandbook.com/guides/generative-ai-system-design-interview/)
[^process-analysis]: [Process Analysis - Reddit r/cscareerquestions](https://www.reddit.com/r/cscareerquestions/)
[^process-analysis-fr]: [Process Analysis - Reddit r/developpeurs](https://www.reddit.com/r/developpeurs/)
[^techeon]: [Medium - TechEon Agentic Guide](https://atul4u.medium.com/the-complete-agentic-ai-system-design-interview-guide-2026-f95d0cfeb7cf)
[^promptlayer]: [PromptLayer](https://blog.promptlayer.com/the-agentic-system-design-interview-how-to-evaluate-ai-engineers/)
[^khushal-kumar]: [Medium - Khushal Kumar](https://kaysnotes.medium.com/my-generative-ai-engineer-interview-experience-got-hired-6b3f1affc4e9)
[^exponent-openai]: [Medium - Exponent/Jacob Simon, OpenAI](https://medium.com/exponent/what-its-actually-like-to-interview-at-openai-in-2026-03a646c9436c)
[^colin-zhou]: [Medium - Colin Zhou](https://levelup.gitconnected.com/how-i-fought-and-passed-technical-interviews-with-llms-in-2025-f328e9df8e84)
[^rohit-verma]: [Medium - Rohit Verma, Microsoft](https://medium.com/@rohitverma_87831/microsoft-senior-engineer-interview-experience-2026-the-offer-that-took-me-three-attempts-e0d6e052bdb1)
[^eightfold]: [Medium - Eightfold.ai](https://medium.com/@bhardwajtushar2004/inside-eightfold-ais-agentic-ai-internship-hiring-process-2026-f86dcb625aa8)
[^designgurus]: [DesignGurus](https://www.designgurus.io/blog/openai-system-design-interview-questions)
[^bhavishya-pandit]: [Bhavishya Pandit](https://bhavishyapandit9.substack.com/p/7-deep-cut-ai-system-design-interview)
[^sundeep-teki]: [Sundeep Teki](https://www.sundeepteki.org/advice/the-ultimate-ai-research-engineer-interview-guide-cracking-openai-anthropic-google-deepmind-top-ai-labs)
[^yuan-meng]: [Yuan Meng](https://www.yuan-meng.com/posts/mle_interviews_2.0/)
[^hello-interview]: [Hello Interview - OpenAI L5](https://www.hellointerview.com/guides/openai/l5)
[^linkjob-openai]: [linkjob - OpenAI](https://www.linkjob.ai/interview-questions/openai-loop-interview)
[^linkjob-anthropic]: [linkjob - Anthropic](https://www.linkjob.ai/interview-questions/anthropic-software-engineer-interview/)
[^devto-xai]: [dev.to - xAI](https://dev.to/net_programhelp_e160eef28/xai-software-engineer-interview-2026-full-recap-pitfalls-real-prep-tips-2fl0)
[^devto-mai-chi-bao]: [dev.to - Mai Chi Bao](https://dev.to/mrzaizai2k/how-i-aced-my-llm-interview-building-a-rag-chatbot-2p6f)
[^devto-aidi-rivera]: [dev.to - Aidi Rivera](https://dev.to/aidiri/learn-from-my-mistakes-my-first-take-home-code-challenge-778)
[^reddit-ai-eng-questions]: [Reddit - AI Engineer Interview Questions](https://www.reddit.com/r/ArtificialInteligence/comments/1nybfr8/ai_engineer_interview_questions/) (r/ArtificialIntelligence)
[^reddit-ai-eng-questions-2]: [Reddit - AI Engineer Interview Questions, TonyStank-1704 comment](https://www.reddit.com/r/ArtificialInteligence/comments/1nybfr8/ai_engineer_interview_questions/) (r/ArtificialIntelligence)
[^reddit-hiring-process]: [Reddit - What's the AI Engineering Hiring Process Like?](https://www.reddit.com/r/cscareerquestions/comments/1lmwq1e/whats_the_ai_engineering_hiring_process_like/) (r/cscareerquestions)
[^reddit-prep-ai-eng]: [Reddit - How to Prepare for AI Engineering Interviews](https://www.reddit.com/r/datascience/comments/1ovf9k2/how_to_prepare_for_ai_engineering_interviews/) (r/datascience)
[^reddit-eightfold-ai]: [Reddit - Need Advice for Eightfold.ai Agentic AI Engineer](https://www.reddit.com/r/developersIndia/comments/1pbaj11/need_advice_for_eightfoldai_agentic_ai_engineer) (r/developersIndia)
[^reddit-clear-genai]: [Reddit - How to Clear Interviews in AI/GenAI/RAG/LLM](https://www.reddit.com/r/generativeAI/comments/1p4yrjk/how_to_clear_interviews_in_ai_gen_rag_llm/) (r/generativeAI)
[^reddit-grilled-rag]: [Reddit - Got Grilled in an ML Interview for LangGraph/RAG Projects](https://www.reddit.com/r/LangChain/comments/1k662xc/got_grilled_in_an_ml_interview_today_for_my/) (r/LangChain)
[^reddit-genai-consulting]: [Reddit - Interview Questions Gen AI (consulting)](https://www.reddit.com/r/learnmachinelearning/comments/1ppgsf3/interview_questions_gen_ai) (r/learnmachinelearning)
[^reddit-swe-to-ai]: [Reddit - From Software Developer to AI Engineer](https://www.reddit.com/r/learnmachinelearning/comments/1pzcw2y/from_software_developer_to_ai_engineer_the_exact/) (r/learnmachinelearning)
[^reddit-microsoft-aiml]: [Reddit - Microsoft SWE Applied AI/ML Summer 2026](https://www.reddit.com/r/csMajors/comments/1nqfzhq/microsoft_swe_applied_aiml_summer_2026_redmond) (r/csMajors)
[^reddit-xai-eng]: [Reddit - xAI AI Engineer Backend/Infra Interview](https://www.reddit.com/r/leetcode/comments/1pjhw1i/xai_ai_engineer_backendinfra_interview_just/) (r/leetcode)
[^reddit-2026-prep]: [Reddit - 2026 Interview Prep](https://www.reddit.com/r/leetcode/comments/1q06zz6/2026_interview_prep) (r/leetcode)
[^reddit-yc-assignment]: [Reddit - What Is Your Interview Assignment for AI Engineers?](https://www.reddit.com/r/ycombinator/comments/1jnfijm/what_is_your_interview_assignment_for_ai_engineers/) (r/ycombinator)
[^mimansa-jaiswal]: [Mimansa Jaiswal](https://mimansajaiswal.github.io/posts/llm-ml-job-interviews-resources/)
[^buildml]: [BuildML](https://buildml.substack.com/p/top-24-llm-questions-asked-at-deepmind)
[^hn-46319888]: [HN - LLM Interview Questions](https://news.ycombinator.com/item?id=46319888)
[^hn-29876742]: [HN - Deep Learning Interviews Book](https://news.ycombinator.com/item?id=29876742)
[^llmgenai]: [GitHub - LLM Interview Questions](https://github.com/llmgenai/LLMInterviewQuestions)
[^tidorp]: [GitHub - TidorP/MLJobSearch2025](https://github.com/TidorP/MLJobSearch2025)
[^designgurus-rag]: [DesignGurus - RAG System Design](https://www.designgurus.io/blog/system-design-for-rag)
[^hitendra-patel]: [Medium - Hitendra Patel](https://medium.com/@hitendrapatel)
[^raghu-teja-1]: [Medium - Raghu Teja, IBM Part 1](https://medium.com/@raghu_teja/how-i-cracked-my-ibm-ai-engineer-interview-part-1-technical-e7e4f73be5c4)
[^raghu-teja-2]: [Medium - Raghu Teja, IBM Part 2](https://medium.com/@raghu_teja/how-i-cracked-my-ibm-ai-engineer-interview-part-2-ml-scenarios-88af2b46282e)
[^fahd-mirza-2]: [YouTube - Fahd Mirza (Upwork)](https://www.youtube.com/watch?v=fahd-mirza-upwork)
[^zen-van-riel]: [Zen Van Riel](https://zenvanriel.com/ai-engineer-blog/ai-engineering-interview-big-tech-guide/)
[^fonzi-ai]: [Medium - Fonzi AI](https://medium.com/fonzi-ai/what-ive-learned-from-sitting-in-on-50-ai-engineer-interviews-c493696453c4)
[^github-repos]: [GitHub Repos: AI Engineering Interview Assignments](../data/sources/github-repos.md)
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
[^gh-tredence-2]: [GitHub - tredence submission 2](https://github.com/search?q=tredence+ai+engineer&type=repositories)
[^gh-tredence-3]: [GitHub - tredence submission 3](https://github.com/search?q=tredence+ai+engineer&type=repositories)
[^gh-tredence-4]: [GitHub - tredence submission 4](https://github.com/search?q=tredence+ai+engineer&type=repositories)
[^gh-tredence-5]: [GitHub - tredence submission 5](https://github.com/search?q=tredence+ai+engineer&type=repositories)
[^gh-tredence-6]: [GitHub - tredence submission 6](https://github.com/search?q=tredence+ai+engineer&type=repositories)
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
[^gh-emitrr-2]: [GitHub - Emitrr submission 2](https://github.com/search?q=emitrr+ai+engineer&type=repositories)
[^gh-legal-doc]: [GitHub - Files.Invis](https://github.com/Udaykeerthan67/Files.Invis)
[^gh-mindwell]: [GitHub - mindwell-assignment-2026](https://github.com/mathemage/mindwell-assignment-2026)
[^gh-voice-ai]: [GitHub - voice-ai-assignment](https://github.com/Viren-55/voice-ai-assignment)
[^gh-hrytos]: [GitHub - Transport-Query-Agent](https://github.com/vaishnavip-23/Transport-Query-Agent)
[^gh-pineos]: [GitHub - investment_coach_bot](https://github.com/anuradhabudhar214-tech/investment_coach_bot)
[^gh-upliance-1]: [GitHub - RPS-Plus-Al-Judge](https://github.com/Thejas10042001/RPS-Plus-Al-Judge)
[^gh-upliance-2]: [GitHub - upliance.ai_assignment](https://github.com/dsulzd/upliance.ai_assignment)
[^gh-zuneko]: [GitHub - Smart-LLM-Router-Observability-Platform](https://github.com/Sushma-Sangolli/Smart-LLM-Router-Observability-Platform)
[^gh-edtronaut]: [GitHub - AI-Coworker-Engine](https://github.com/jerichosuguru/AI-Coworker-Engine)
[^gh-fynd]: [GitHub - fynd-ai-feedback-system](https://github.com/pranaymanapure/fynd-ai-feedback-system)
[^gh-gamma]: [GitHub - gamma-project](https://github.com/audoir/gamma-project)
[^gh-krisp]: [GitHub - krisp_ai_engineer_role_task](https://github.com/Artush-Baghdasaryan/krisp_ai_engineer_role_task)
[^gh-deel]: [GitHub - deel-assignment](https://github.com/kamran-14/deel-assignment)
[^gh-context-engineering]: [GitHub - context-engineering-takehome](https://github.com/jkbrooks/context-engineering-takehome)
[^gh-gupshup]: [GitHub - GUPPSHUPP_Founding_AI_Engineer_Assignment](https://github.com/amityadav108/GUPPSHUPP_Founding_AI_Engineer_Assignment)
[^exponent-behavioral]: [Exponent - ML Engineer Behavioral Questions](https://www.tryexponent.com/questions?role=ml-engineer&type=behavioral)
[^exponent-openai-behavioral]: [Exponent - OpenAI Behavioral Questions](https://www.tryexponent.com/questions?company=openai&type=behavioral)
[^igotanoffer-openai]: [IGotAnOffer - OpenAI](https://igotanoffer.com/en/advice/openai-interview-questions)
[^igotanoffer-meta]: [IGotAnOffer - Meta ML Engineer](https://igotanoffer.com/blogs/tech/facebook-machine-learning-engineer-interview)
[^interviewnode-behavioral]: [InterviewNode - Behavioral Guide for ML Engineers](https://www.interviewnode.com/post/acing-the-behavioral-interview-a-guide-for-ml-engineers-by-interviewnode)
[^prachub-anthropic]: [Prachub - Anthropic Behavioral & Leadership](https://prachub.com/companies/anthropic/categories/behavioral-and-leadership)
[^interviewquery-anthropic]: [InterviewQuery - Anthropic](https://www.interviewquery.com/interview-guides/anthropic)
[^educative-deepmind]: [Educative - Google DeepMind](https://www.educative.io/blog/google-deepmind-interview-questions)
[^deepthi-sudharsan]: [Medium - Deepthi Sudharsan](https://medium.com/@deepthi.sudharsan/inside-ai-interviews-stories-patterns-and-what-actually-matters-555684c38598)
[^youtube-proptech]: [YouTube - PropTech Mock Interview](https://www.youtube.com/watch?v=proptech-mock)
[^reddit-expdevs-agentic]: [Reddit - Agentic AI System Design Interview](https://www.reddit.com/r/ExperiencedDevs/comments/1r78ipa/agentic_ai_agents_system_design_interview) (r/ExperiencedDevs, Feb 2026)
[^reddit-csuk-agents]: [Reddit - AI Engineering Agents Interview Prep](https://www.reddit.com/r/cscareerquestionsuk/comments/1qmybi3/ai_engineering_agents_interview_prep) (r/cscareerquestionsuk, Jan 2026)
[^reddit-aiagents-prep]: [Reddit - Interview Prep: Deep Learning to Agentic Systems](https://www.reddit.com/r/AI_Agents/comments/1qrxchn/interview_prep_deep_learning_agentic_systems_what) (r/AI_Agents, Jan 2026)
[^reddit-ai-agentic]: [Reddit - What Agentic AI Am I Supposed to Learn?](https://www.reddit.com/r/ArtificialInteligence/comments/1rceuef/what_agentic_ai_am_i_even_supposed_to_learn) (r/ArtificialIntelligence, Feb 2026)
[^reddit-devsindia-genai]: [Reddit - Generative AI Engineer Interview Prep](https://www.reddit.com/r/developersIndia/comments/1oq5fdi/got_an_interview_tomorrow_for_a_generative_ai) (r/developersIndia, Nov 2025)
[^datainterview-openai]: [DataInterview - OpenAI AI Engineer Interview](https://www.datainterview.com/blog/openai-ai-engineer-interview)
[^datainterview-mistral]: [DataInterview - Mistral ML Engineer Interview](https://www.datainterview.com/blog/mistral-machine-learning-engineer-interview)
[^hn-39748537]: [HN - RAG vs. Fine-Tuning](https://news.ycombinator.com/item?id=39748537)
[^hn-41541053]: [HN - LLMs Will Always Hallucinate](https://news.ycombinator.com/item?id=41541053)
[^hn-42182365]: [HN - Best Take-Home Coding Tasks](https://news.ycombinator.com/item?id=42182365)
[^hn-42268158]: [HN - Technical Interviews in the LLM Era](https://news.ycombinator.com/item?id=42268158)
[^hn-42313401]: [HN - Automated Reasoning to Remove LLM Hallucinations](https://news.ycombinator.com/item?id=42313401)
[^hn-42431361]: [HN - Agentic LLM Systems in Production](https://news.ycombinator.com/item?id=42431361)
[^hn-42793253]: [HN - AI Orchestration and LLM Routing](https://news.ycombinator.com/item?id=42793253)
[^hn-43884713]: [HN - Is an AI Agent Just an LLM Wrapper?](https://news.ycombinator.com/item?id=43884713)
[^hn-44013971]: [HN - Compress Long LLM Prompts](https://news.ycombinator.com/item?id=44013971)
[^hn-44268335]: [HN - Design Patterns for Securing LLM Agents](https://news.ycombinator.com/item?id=44268335)
[^hn-44796765]: [HN - Sleipner.ai LLM Cost Reduction](https://news.ycombinator.com/item?id=44796765)
[^hn-44875256]: [HN - Interview Questions for AI Product Engineering](https://news.ycombinator.com/item?id=44875256)
[^hn-46229585]: [HN - LLM API Costs in Production](https://news.ycombinator.com/item?id=46229585)
[^hn-46695170]: [HN - Reduce LLM Token Costs with TOON](https://news.ycombinator.com/item?id=46695170)
[^hn-46873753]: [HN - Are LLM Failures Structurally Unavoidable?](https://news.ycombinator.com/item?id=46873753)
[^hn-46959695]: [HN - Early Detection of LLM Hallucinations via ONTOS](https://news.ycombinator.com/item?id=46959695)
[^hn-47150302]: [HN - InferShrink Model Routing](https://news.ycombinator.com/item?id=47150302)
[^x-akshay-pachaar-1]: [X - Akshay Pachaar, ML Deployment Testing (Netflix)](https://x.com/akshay_pachaar/status/1990034795909582860)
[^x-akshay-pachaar-2]: [X - Akshay Pachaar, Distributed Training (Google)](https://x.com/akshay_pachaar/status/1992571349332804081)
[^x-akshay-pachaar-3]: [X - Akshay Pachaar, Model Calibration (Apple)](https://x.com/akshay_pachaar/status/1994020936488734823)
[^x-ali-shohadaee]: [X - Ali Shohadaee, Domain-Specific Tokenization (Anthropic)](https://x.com/alishohadaee/status/2012176441287348231)
[^x-allie-miller]: [X - Allie K. Miller, Adaptability Interview Questions](https://x.com/alliekmiller/status/1967970071248015679)
[^x-ashutosh-1]: [X - Ashutosh Maheshwari, Fine-Tuning vs. Prompting](https://x.com/asmah2107/status/1977413874702745794)
[^x-ashutosh-2]: [X - Ashutosh Maheshwari, Model Drift Diagnosis (Databricks)](https://x.com/asmah2107/status/1990649811964735512)
[^x-athletickoder-1]: [X - athleticKoder, PagedAttention and LLM Serving](https://x.com/athleticKoder/status/1967925267864928669)
[^x-athletickoder-2]: [X - athleticKoder, RAG System Diagnostics](https://x.com/athleticKoder/status/2002355874786873383)
[^x-avi-chawla-1]: [X - Avi Chawla, Unified Query Engine (Google)](https://x.com/_avichawla/status/1986320178783867036)
[^x-interviewstack-meta]: [X - InterviewStack.io, Meta LoRA Question](https://x.com/gnan54796/status/2007302142550565123)
[^x-michael-taiwo]: [X - Michael Taiwo, AI Literacy Interview Questions](https://x.com/AskMichaelTaiwo/status/1987201166157946887)
[^x-aryyann8]: [X - AI Engineer Intern Interview](https://x.com/aryyann8/status/2009314129878896960) (Jan 2026)
[^reddit-genai-product]: [Reddit - Technical Interview for GenAI Engineer Role](https://www.reddit.com/r/leetcode/comments/1rd6yki/technical_interview_for_genai_engineer_role_for_a) (r/leetcode)
[^reddit-amazon-genai]: [Reddit - ML Engineer GenAI Amazon](https://www.reddit.com/r/datascience/comments/1jrdrpx/ml_engineer_genai_amazon/) (r/datascience)
[^glassdoor-quantiphi]: [Glassdoor - Quantiphi ML Engineer Interview](https://www.glassdoor.com/Interview/NLP-related-question-tokenization-fine-tuning-ML-LIFE-CYCLE-QTN_8617277.htm)
[^glassdoor-asapp]: [Glassdoor - ASAPP AI/ML Research Intern Interview](https://www.glassdoor.com/Interview/ASAPP-AI-ML-Research-Intern-Interview-Questions-EI_IE1501287.0,5_KO6,27.htm)
[^reddit-capital-one]: [Reddit - Capital One Data Science Interview](https://www.reddit.com/r/datasciencecareers/comments/1ojegp4/capital_one_data_science_interview) (r/datasciencecareers, Oct 2025)
[^glassdoor-cognida]: [Glassdoor - Cognida.ai Software Engineer Interview](https://www.glassdoor.com/Interview/Cognida-ai-Software-Engineer-Interview-Questions-EI_IE7907039.0,10_KO11,28.htm) (Jan 2026)
[^exponent-openai-ml]: [Exponent - OpenAI ML Engineer Questions](https://www.tryexponent.com/questions?role=ml-engineer&type=technical)
[^reddit-llm-interview-prep]: [Reddit - LLM Interview Prep](https://www.reddit.com/r/MachineLearning/comments/1ein9vh/d_llm_interview_prep) (r/MachineLearning)
