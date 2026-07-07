# 上机编程与算法面试题

本章内容聚焦于面试中的编程实战：包括现场编码、代码重构、机器学习算法实现以及标准算法轮次。


## 1. 编程面试的两种基本形式

- **渐进式功能开发轮 (Implementation rounds)**：时长 45 到 90 分钟。在一个持续递进、不断追加新需求的复杂情景中现场开发一个完整小系统。
- **算法轮 (Algorithm rounds)**：时长 25 到 70 分钟。考核标准的 LeetCode 式数据结构与算法题。


## 2. 渐进式功能开发轮 (Implementation Rounds)

这类面试时间较长（45-90分钟），要求候选人现场构建、重构或编写出具有一定代码体量的工程模块。面试官重点评估你的代码整洁度、面向对象设计能力、系统可扩展性以及工程判断力。 [^deepthi-sudharsan]

这类面试通常只围绕一个核心题目展开，但会不断追加 **2 到 4 个层级的递进要求 (progressive levels)**。因为后期的功能完全叠加在前期代码之上，如果你的前期架构设计得太死板，写到后面就会被迫大面积重构，从而直接翻车。

### 经典实战题目：
- **开发一个多线程网页爬虫**（包含请求队列、去重与并发控制）。 [^linkjob-anthropic]
- **垃圾代码重构**：给你 100 到 120 行嵌套极深、命名混乱、毫无可读性的意大利面式代码，限时现场将其重构为高内聚、易测试的模块。 [^exponent-openai]
- **从零实现一个内存型 KV 数据库**（先写 SET/GET/DELETE，再追加 TTL 过期时间限制、以及事务控制）。 [^linkjob-anthropic]
- **设计 SQL 引擎 (Design SQL)**：LeetCode 2408 题的工程变种。 [^hello-interview]
- **实现类 Unix 的 `cd` 路径切换命令**（核心考点是支持软链接 Symbolic links 的解析）。 [^hello-interview]
- **内存数据库设计**：在内存中用原生数据结构实现类似于关系型数据库的 JOIN、WHERE 过滤等操作。 [^hello-interview]
- **代币/积分生命周期管理系统 (Credits Management)**：设计一个模块用于追踪用户积分的下发与消费逻辑。需支持不同的过期规则和抵扣权重，需求会不断追加复杂度。 [^exponent-openai]

### ML / AI 专属编程题：
- **Embeddings 故障排查**：现场走读并 Debug 一段在向量嵌入对齐和计算中发生维度漂移或 NaN 异常的代码。 [^promptlayer]
- **手写 Logistic Regression 算法**：仅使用 NumPy，从零实现逻辑回归算法，必须包含随机梯度下降 (SGD)、L2 正则化项以及 Early Stopping（提前停止训练）逻辑。 [^datainterview-mistral]


## 3. 算法轮 (Algorithm Rounds)

短平快的核心轮次（15-60分钟），考查常见的数据结构与算法知识（哈希表、前缀树 Trie、链表、图、贪心算法等）。

### 真实面试真题：
- **行程长度编码 (RLE, Run-Length Encoding)** 算法实现。
- **求出 0 到 100 之间的所有质数**（考察最简算法与时空复杂度）。 [^khushal-kumar]
- **手写 O(1) 复杂度的 LRU 缓存 (LRU Cache)**（经典面试题）。 [^devto-xai]
- **带限制条件的反转链表**（微软应用 AI 岗真题，AI 协作轮：要求候选人通过有效的 Prompt 引导 ChatGPT 写出代码，并快速修改）。 [^reddit-microsoft-aiml]
- **求 Excel 列名算法**：根据给定的列数字返回 Excel 中的字母列名（例如：第 702 列 = "AAA"）。 [^reddit-microsoft-aiml]


## 4. 如何科学备战

### A. 精刷 LeetCode 经典题 [^hello-interview] [^mimansa-jaiswal]
- 刷完 75 到 100 道 Easy/Medium 难度的经典题（如 Hot 100）。
- 重点熟练掌握以下数据结构：哈希表 (Hash Map)、双指针、前缀树 (Trie)、双向链表和图的遍历。

### B. 练习构建“渐进式”个人小项目
- 刻意练习那些能够像搭积木一样不断增加复杂度的项目。这与渐进式面试的套路完全一致。
- **推荐练手项目**：
  - **内存 KV 存储**：第1步写 SET/GET $\rightarrow$ 第2步支持 TTL 过期 $\rightarrow$ 第3步支持数据持久化 $\rightarrow$ 第4步引入并发锁控制。
  - **网络爬虫**：第1步单线程爬取 $\rightarrow$ 第2步引入线程池并发 $\rightarrow$ 第3步加入 Rate Limiter 频率限制 $\rightarrow$ 第4步支持分布式去重。
- 先用最直观的方式写出可运行版本，然后尝试在时间压力下（如限时 20 分钟）强行追加新需求。如果在引入新需求时被迫把大半代码重载，就说明你的架构设计存在重大硬伤，需重新打磨。

### C. 磨炼你的“出声思维 (Think Out Loud)” [^exponent-openai] [^khushal-kumar]
- 现在的面试中，越来越多的企业允许甚至鼓励在编程轮里使用 AI 工具。
- 面试官考核的重点是**你看待问题和使用 AI 的策略**：你是否在输入提示词前就想明白了边界情况？你是否能一眼看出 AI 给出代码中的 Bug？还是你只是在盲目地复制粘贴？
- 无论用不用 AI，写代码时要不停地向面试官同步你的设计意图，这能极大地展示你的技术沟通素养。

### 面试高频雷区：
- **还没沟通清楚输入输出和边界，上来就埋头写代码**。
- **代码结构设计得太死板**，导致面试官抛出 follow-up 新需求时直接卡死崩溃。
- **盲目粘贴 AI 生成的代码**，被面试官追问底层原理时支支吾吾。
- 没有主动向面试官分析时空复杂度或进行极致的代码性能调优。

---

## 引用源说明

[^datainterview-mistral]: [DataInterview - Mistral ML Engineer Interview](https://www.datainterview.com/blog/mistral-machine-learning-engineer-interview)
[^deepthi-sudharsan]: [Medium - Deepthi Sudharsan](https://medium.com/@deepthi.sudharsan/inside-ai-interviews-stories-patterns-and-what-actually-matters-555684c38598)
[^devto-xai]: [dev.to - xAI](https://dev.to/net_programhelp_e160eef28/xai-software-engineer-interview-2026-full-recap-pitfalls-real-prep-tips-2fl0)
[^exponent-openai]: [Medium - Exponent, OpenAI](https://medium.com/exponent/what-its-actually-like-to-interview-at-openai-in-2026-03a646c9436c)
[^hello-interview]: [Hello Interview - OpenAI L5](https://www.hellointerview.com/guides/openai/l5)
[^khushal-kumar]: [Medium - Khushal Kumar](https://kaysnotes.medium.com/my-generative-ai-engineer-interview-experience-got-hired-6b3f1affc4e9)
[^linkjob-anthropic]: [linkjob - Anthropic](https://www.linkjob.ai/interview-questions/anthropic-software-engineer-interview/)
[^mimansa-jaiswal]: [Mimansa Jaiswal](https://mimansajaiswal.github.io/posts/llm-ml-job-interviews-resources/)
[^promptlayer]: [PromptLayer](https://blog.promptlayer.com/the-agentic-system-design-interview-how-to-evaluate-ai-engineers/)
[^reddit-microsoft-aiml]: [Reddit - Microsoft SWE Applied AI/ML Summer 2026](https://www.reddit.com/r/csMajors/comments/1nqfzhq/microsoft_swe_applied_aiml_summer_2026_redmond) (r/csMajors)
