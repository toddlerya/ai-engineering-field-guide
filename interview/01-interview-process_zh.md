# AI 工程师求职面试流程分析

## 统计概要

在分析的 1,765 份招聘需求中，仅有约 80 份（4.5%）在招聘启事中明确给出了结构化的面试流程，涵盖 51 家不同的公司。绝大多数职位描述则完全省略了面试流程的具体说明。

这 51 家公司的详细面试流程描述存放在 [data/job-descriptions/](data/job-descriptions/) 目录中。每个文件均链接了对应的原始 YAML 岗位需求文件。


## 标准面试流程

面试环节的**中位数是 4 个步骤**，大多数公司都集中在 3 到 5 个环节之间。有一些精简的招聘流程仅包含 2 个阶段（如 Lorikeet、Infinity Constellation、Watershed），而最长的流程则达到了 7 个阶段（如 FlowFuse、Roboflow、The College Board）。

最频繁提及的面试环节包括：
1. **HR/猎头电话筛选 (Recruiter/talent screen)**：通常为 15-30 分钟。
2. **技术面试 (Technical interview)**：包含现场编程、系统设计或代码评审。
3. **招聘主管面试 (Hiring manager interview)**：45-60 分钟的技术深挖与业务交流。
4. **行为面试 (Behavioral interview)**：围绕企业价值观与团队文化的沟通。
5. **Take-home 离线编程作业**：通常限时为 2-3 小时（部分公司会给出数天开发期限）。
6. **小组/多人评审 (Panel interview)**：多名面试官同时在线进行复合评估。
7. **CEO/创始人面试**：通常是终面，15-30 分钟。

### 岗位描述中的真实流程示例

**[Doctolib, Senior AI Engineer]**：
1. HR 沟通
2. 功能开发实战面试 (Feature building interview)
3. AI 系统设计面试 (AI system design)
4. 行为面试 (Behavioral interview)
5. 背景调查并下发 Offer

**[PostHog, AI Product Engineer]**：
1. HR 筛选沟通
2. 技术面试 (60 分钟)
3. 联合创始人沟通 (15 分钟)
4. **有偿体验日 (Paid SuperDay)**（全天参与真实工作并支付报酬）

**[FlowFuse, Full Stack Developer (AI)]**：
1. 招聘经理筛选简历
2. 基础电话筛选 (15 分钟)
3. 研发经理沟通 (45 分钟)
4. Take-home 编程作业 (2-3 小时，鼓励使用 AI 助手协作)
5. 与 2-3 名技术团队成员进行技术评审答辩 (60 分钟)
6. 围绕沟通与团队协作的团队面试 (45 分钟)


## 求职候选人的真实经历

整理自 Reddit、X 和个人博客上求职候选人的反馈，还原了各个技术面试轮次的真实细节：

| 面试轮次 | 常见时长 | 候选人反馈的考核细节 |
|-------|----------|-------------------|
| **HR 电话筛选** | 15-30 分钟 | 基础匹配度沟通、薪资期望范围界定 |
| **技术/算法轮** | 45-60 分钟 | LeetCode 式算法题，有时会带有大模型技术背景 |
| **AI/ML 深度拷问** | 45-90 分钟 | 拷问 LLM、RAG、幻觉拦截、微调 vs 提示词工程的折中选择 |
| **离线作业/项目** | 1-7 天 | 开发一个闭环 RAG/Agent 智能体系统，或者多天综合任务 |
| **系统设计轮** | 60 分钟 | 大模型应用的大规模扩容、时延与 Token 成本调优 |
| **行为面试** | 30-60 分钟 | 标准 STAR 话术，考察在模糊不清的 AI 业务环境下的主动权意识 |

*注：并非所有公司都包含上述全部轮次。整体面试轮数通常在 3-6 轮之间，耗时 2-6 周。*

### 部分企业真实面试记录

**[微软, SWE Applied AI/ML 实习生]** [^reddit-microsoft-aiml]：
1. **AI 辅助代码面试 (45分钟)**：允许使用 ChatGPT 来解决编程问题，面试官会动态修改题目限制，并要求候选人现场调整 Prompt 进行二次生成。
2. **纯白板手撕代码 (45分钟)**：严禁使用任何 AI 辅助工具。
3. **行为与技术探讨 (45分钟)**。

**[亚马逊, GenAI Innovation Center L6 级别]** [^reddit-amazon-genai]：
1. **电话初筛**：LeetCode 算法题 + 实用机器学习编程（如使用 NumPy 手写余弦相似度计算）。
2. **标准 SDE 技术评估**：考核数据结构与算法 (DSA) —— 亚马逊没有单独的 MLE（机器学习工程师）职位序列，全部使用标准开发岗考核。
3. **GenAI 深度技术考察**：深入探究 LLM/ViT/DiT 架构细节、模型微调、业务场景构思及 ROI（投资回报率）预估。
4. **全流程穿插亚马逊领导力准则 (LP) 的行为考核**。

**[Eightfold.ai, Agentic AI Engineer]** [^eightfold-medium] [^reddit-eightfold-ai] (2026年1月)：
1. **AI 智能体面试官主持的代码轮 (~60分钟)**：AI 智能体出 2 道题，并根据候选人的回答，交互式追问边界情况与复杂度。
2. **离线作业**：限时 3 天，独立构建一个 AI 智能体 Agent。
3. **技术终面**：与研发经理进行以 DSA（数据结构与算法）为核心的技术交流。

**[LangChain, AI Engineer]** [^reddit-ai-eng-questions]：
1. Take-home 离线作业 (开发一个 Agent 智能体)。
2. 围绕作业设计方案进行技术答辩。
3. 实际 AI 应用的系统设计面试。

**[IBM, AI Engineer (Watsonx)]** [^raghu-teja-1] (2025年1月)：
1. HR 初筛（LinkedIn 投递后等待了约 2 个月）。
2. 技术面试 (75分钟) —— 考察 Python、SQL、Git、简历项目深挖、ML 以及 MLOps 知识。
3. 现场手撕代码 (45分钟) —— 共享白板，3 道 Easy 到 Medium 难度的编程题。

**[Mistral AI, Applied AI Engineer]** [^glassdoor-mistral] (2026年1月)：
1. 大模型理论
2. 编程上机
3. 简历项目深挖
4. 技术经理面试
5. ML 系统设计
6. Take-home 离线编程作业
7. 企业文化与价值观沟通

**[Databricks, AI/ML Engineer]** [^yuan-meng] (2025年底)：
1. 算法面试 (LeetCode-style)。
2. 多层级面向对象设计 (OOP) —— 现场开发一个简易的 KV 存储、聊天室或数据库模型。
3. ML 基础设施设计 —— 包含特征存储（Feature Stores）、分布式训练、高可用模型推理托管。
4. 发放 Offer 前的背景调查（强制要求提供 2-3 名推荐人）。

**[高盛, Applied AI Engineer]** [^reddit-gs-applied-ai] (2025年12月)：
1. 针对生成式 AI/应用 AI 角色的技术面试。
2. 侧重于大模型系统设计与生产环境部署运维。

**[某 AI 工程师实习生面试]** [^x-aryyann8] (2026年1月)：
1. 简历项目深挖。
2. QLoRA 微调原理。
3. RAG 架构设计与时延调优。
4. 模型 Temperature（温度参数）与采样解码策略。
5. 智能体 AI 系统设计。
6. 特征工程扩容与机器学习情景题。

---

[^reddit-microsoft-aiml]: [Reddit - Microsoft SWE Applied AI/ML Summer 2026](https://www.reddit.com/r/csMajors/comments/1nqfzhq/microsoft_swe_applied_aiml_summer_2026_redmond) (r/csMajors)
[^reddit-amazon-genai]: [Reddit - ML Engineer GenAI Amazon](https://www.reddit.com/r/datascience/comments/1jrdrpx/ml_engineer_genai_amazon/) (r/datascience)
[^raghu-teja-1]: [Medium - Raghu Teja, IBM Part 1](https://medium.com/@raghu_teja/how-i-cracked-my-ibm-ai-engineer-interview-part-1-technical-e7e4f73be5c4)
[^eightfold-medium]: [Medium - Inside Eightfold.ai Agentic AI Internship Hiring 2026](https://medium.com/@bhardwajtushar2004/inside-eightfold-ais-agentic-ai-internship-hiring-process-2026-f86dcb625aa8)
[^reddit-eightfold-ai]: [Reddit - Need Advice for Eightfold.ai Agentic AI Engineer](https://www.reddit.com/r/developersIndia/comments/1pbaj11/need_advice_for_eightfoldai_agentic_ai_engineer) (r/developersIndia)
[^reddit-ai-eng-questions]: [Reddit - AI Engineer Interview Questions](https://www.reddit.com/r/ArtificialInteligence/comments/1nybfr8/ai_engineer_interview_questions/) (r/ArtificialIntelligence)
[^janvi-kalra]: [Janvi Kalra - From Software Engineer to AI Engineer](https://newsletter.pragmaticengineer.com/p/from-software-engineer-to-ai-engineer)
[^deepthi-sudharsan]: [Medium - Deepthi Sudharsan, Inside AI Interviews](https://medium.com/@deepthi.sudharsan/inside-ai-interviews-stories-patterns-and-what-actually-matters-555684c38598)
[^reddit-2026-prep]: [Reddit - 2026 Interview Prep](https://www.reddit.com/r/leetcode/comments/1q06zz6/2026_interview_prep) (r/leetcode)
[^glassdoor-mistral]: [Glassdoor - Mistral AI Applied AI Engineer Interviews](https://www.glassdoor.com/Interview/Mistral-AI-Applied-AI-Engineer-Interview-Questions-EI_IE9945031.0,10_KO11,30.htm)
[^yuan-meng]: [Yuan Meng - MLE Interviews 2.0](https://www.yuan-meng.com/posts/mle_interviews_2.0/)
[^reddit-gs-applied-ai]: [Reddit - Applied AI Engineer Goldman Sachs Interview](https://www.reddit.com/r/leetcode/comments/1pexaw3/applied_ai_engineer_goldman_sachs_interview) (r/leetcode)
[^x-aryyann8]: [X - AI Engineer Intern Interview](https://x.com/aryyann8/status/2009314129878896960)
[^reddit-genai-product]: [Reddit - Technical Interview for GenAI Engineer Role](https://www.reddit.com/r/leetcode/comments/1rd6yki/technical_interview_for_genai_engineer_role_for_a) (r/leetcode)
