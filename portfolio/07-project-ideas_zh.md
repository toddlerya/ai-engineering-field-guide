# 项目创意与灵感

阅读本页面，了解如何在不同行业领域中进行项目题材的选择与技术选型。

> [!WARNING]
> **请勿直接抄袭这些项目。**  
> 应当把这些实例作为研究样本，学习它们的：
> - 业务行业 (domain)
> - 对标公司 (companies)
> - 招聘要求 (job descriptions)
> - 技术博客或产品文档 (blogs or docs)
> - 待解决的核心痛点 (problems)
> - 具有相似创意的真实开源仓库
> - 技术方案与选型 (technology choices)


## 摸排实操练习步骤

对于任何一个行业领域，都可以遵循以下步骤进行摸排：
1. 精读该领域的招聘需求。
2. 研读对标公司的技术博客或产品文档。
3. 列出这些公司在日常业务中需要解决的痛点。
4. 挑选其中一个具体痛点。
5. 寻找相关的公开数据集或合成数据。
6. 构建一个简易的 MVP 闭环版本。
7. 补充测试用例、评测脚本、日志记录和一份详尽的 README。


## 1. 金融领域 (Finance)

### 对标公司与信息源：
- **Capital One**：[Senior Lead AI Engineer, GenAI Platform Services](https://builtin.com/job/senior-lead-ai-engineer-gen-ai-platform-services/9420327), [技术博客](https://www.capitalone.com/tech/blog/)
- **Wells Fargo**：[Lead Specialty AI Java Software Engineer](https://builtin.com/job/lead-specialty-ai-java-software-engineer-electronic-trading/9879596), [开发者中心](https://developer.wellsfargo.com/)
- **BlackRock**：[Rust AI Engineer](https://builtin.com/job/rust-ai-engineer-director/9629914), [工程博客](https://engineering.blackrock.com/)

### 业务中需要解决的痛点：
- 横向对比动辄数百页的漫长金融报告。
- 从上市申报或电话财报会中自动提取潜在商业风险。
- 生成包含精准事实引用的研究摘要。
- 监控行业政策或金融合规变动。
- 将分析师的提问路由分发到正确的数据源。

### 推荐研读的开源仓库：
- **[SEC Insights](https://github.com/run-llama/sec-insights)**
  - **行业领域**：金融分析
  - **核心痛点**：金融分析师需要快速检索 SEC 申报文件，而不想手动阅读每一份超长报告。
  - **技术方案**：针对 SEC 文档开发 RAG（检索增强生成）系统，并配有金融定制的前端 UI。
- **[Invoice Extract and Reconcile](https://github.com/run-llama/template-workflow-extract-reconcile-invoice)**
  - **行业领域**：财务运营 (FinOps)
  - **核心痛点**：财务团队需要从发票中提取字段，并对照账期协议进行对账。
  - **技术方案**：结构化字段提取、规范的 Schema 定义、置信度度量、决策依据溯源以及人工审核 UI。

### 候选项目创意：
- 电话财报会风险自动提取器
- SEC 申报文件横向对比助手
- 发票智能提取与对账校验工具
- 金融监管政策变动监测器
- 带精确原文引用的分析师研究助手

### 推荐技术选型：
- 使用 **RAG** 来处理政策法规和申报文档。
- 使用 **结构化输出 (Structured Output)** 提取表单和发票字段。
- 编写专门校验**引用准确性**与**字段提取精度**的评测集。
- 记录接口延迟、Token 成本以及检索失败（未召回）的日志。


## 2. 医疗健康 (Healthcare)

### 对标公司与信息源：
- **Optum**：[Senior AI/ML Engineer](https://builtin.com/job/senior-ai-ml-engineer/9555837), [技术与自动化洞察](https://business.optum.com/en/insights/technology-automation.html)
- **GE HealthCare**：[Senior AI Engineer, Intelligent Automation](https://builtin.com/job/senior-ai-engineer-intelligent-automation/9641768), [科研博客](https://research.gehealthcare.com/blog/)
- **Commure**：[Senior Software Engineer, AI Integrations](https://www.builtinla.com/job/senior-software-engineer-ai-integrations/9835679), [官方博客](https://www.commure.com/blog/)

### 业务中需要解决的痛点：
- 确保病患在检索医疗内容时的安全度（绝不能提供错误或高危的医疗建议）。
- 对门诊病历或行政办公便签进行摘要总结。
- 对病患发来的咨询留言进行智能分类。
- 将病患诉求分流派发到对应的科室/业务流中。
- 从手写或电子表单中提取结构化字段。

### 推荐研读的开源仓库：
- **[Claims RAG Assistant](https://github.com/ayusyagol11/claims-rag-assistant)**
  - **行业领域**：医疗与保险理赔
  - **核心痛点**：工伤理赔审核员需要直接从理赔材料中获取可信的解答。
  - **技术方案**：文档导入、RAG、答案源归因引用、Streamlit 界面以及包含 20 个问题的自动化评测集。
- **[HR Policy LLM RAG Assistant](https://github.com/galafis/hr-policy-llm-rag-assistant)**
  - **行业领域**：合规政策问答
  - **核心痛点**：员工需要获得百分之百可信的制度回答，并伴有超出边界时的安全拒答逻辑。
  - **技术方案**：RAG、大模型护栏（Guardrails）、FastAPI 后端、Streamlit 前端、Docker 部署、自动化测试与评测。

### 候选项目创意：
- 病患咨询留言智能分类分流助手
- 医疗保健政策安全检索助手
- 保险理赔智能问答辅助工具
- 门诊复诊指导语自动生成器
- 入院登记表单信息结构化提取器

### 推荐技术选型：
- 使用 **RAG** 检索政策和医疗指南。
- 引入**安全拒答（Refusal）**逻辑，拦截非法的处方或诊断建议。
- 使用 **结构化输出** 进行表单清洗和业务路由分流。
- 编写专门评测 **RAG 忠实度（Groundedness）** 与 **安全拦截率** 的评测集。


## 3. 法律与合规 (Legal and Regulatory)

### 对标公司与信息源：
- **Thomson Reuters**：[Senior Software Engineer, AI Legal CoCounsel FDE](https://builtin.com/job/senior-software-engineer-ai-legal-cocounsel-fde/9090355), [TR 实验室](https://www.thomsonreuters.com/en/about-us/labs)
- **Wolters Kluwer**：[Enterprise Software Engineer, GenAI](https://builtin.com/job/enterprise-software-engineer-python-azure-aws-gen-ai/9827155), [AI 研究页](https://www.wolterskluwer.com/en/about-us/artificial-intelligence)
- **Diligent**：[Forward Deployment Engineer](https://builtin.com/job/technical-pre-sales-prototyper-forward-deployment-engineer/8775074), [AI 治理博客](https://www.diligent.com/resources/blog/ai-governance)

### 业务中需要解决的痛点：
- 审查漫长的商业合同。
- 从法务文书中提取高风险条款。
- 检索庞大且经常更新的法律条文。
- 提炼长篇幅法庭判决书或起诉书。
- 给出支持审计、必须百分之百附带原文依据的可信回复。

### 推荐研读的开源仓库：
- **[ExtractThinker](https://github.com/enoch3712/ExtractThinker)**
  - **行业领域**：文档智能解析
  - **核心痛点**：法务团队需要从 PDF 和扫描版合同图像中提取强类型的规范数据。
  - **技术方案**：OCR 文字识别、大模型抽取、强类型 Schema 校验以及批量处理流。
- **[Invoice Extract and Reconcile](https://github.com/run-llama/template-workflow-extract-reconcile-invoice)**
  - **行业领域**：文档比对审计
  - **核心痛点**：法务审计人员需要自动找出文档间的细微出入、获取置信度并指出比对依据。
  - **技术方案**：字段提取、冲突比对算法以及人工审核复核界面。

### 候选项目创意：
- 合同高风险条款自动审查助手
- 企业政策合规性智能校验器
- 带精确引用的法律文书摘要生成器
- 行业监管条例变动智能追踪器
- 法务提取审批流队列管理系统

### 推荐技术选型：
- 使用 **结构化输出** 提取条款和特定文本域。
- 使用 **RAG** 索引法典和监管源文件。
- 设计 **人机协同（Human-in-the-loop）** 机制，确保高风险决策交由专业法务人员复核。
- 编写专门评测 **抽取精确度** 和 **原文匹配度** 的回归评测集。


## 4. 网络安全 (Cybersecurity)

### 对标公司与信息源：
- **CrowdStrike**：[Senior AI Engineer](https://builtin.com/job/sr-ai-engineer-remote-ind/9716390), [工程博客](https://www.crowdstrike.com/en-us/blog/author.crowdstrike-engineering/)
- **Arctic Wolf**：[Senior Staff Developer, AI SOC Automation](https://builtin.com/job/senior-staff-developer-ai-soc-automation/9592723), [官方博客](https://arcticwolf.com/resources/blog/)
- **Cisco**：[Gen AI Software Engineer](https://builtin.com/job/gen-ai-software-engineer-python-devops-frontend/9882427), [开发者文档](https://developer.cisco.com/)

### 业务中需要解决的痛点：
- 自动概括成百上千条系统报警日志。
- 用人话解释系统检测到的可疑或异常入侵活动。
- 对安全事件进行智能定级与分类。
- 将突发警报路由分派到对应的防御响应工作流 (playbooks) 中。
- 减轻安全运维中心（SOC）值班分析师的信息过载。

### 推荐研读的开源仓库：
- **[Vercel Express Issue Triage Agent](https://github.com/vercel-labs/express-issue-triage-agent-template)**
  - **行业领域**：事件分流处理
  - **核心痛点**：维护人员需要自动对新提交的异常进行分类、分流并起草自动回复。
  - **技术方案**：Webhook 监听、自动分类器、标签匹配以及生成式文本响应。
- **[Agentic RAG](https://github.com/tohio/agentic-rag)**
  - **行业领域**：动态 RAG 检索
  - **核心痛点**：值班人员检索到的信息可能需要动态调用外部工具进行时间/IP 查询。
  - **技术方案**：RAG、智能路由、动态时间/接口查询、链路追踪、评测集、Docker 和 Streamlit。

### 候选项目创意：
- 网络安全警报智能概括工具
- 安全事件自动评级与分流助手
- 异常异地登录行为的解释与梳理工具
- 应急响应处置预案（Playbook）智能检索系统
- 系统漏洞报告严重性自动分类器

### 推荐技术选型：
- 使用 **分类模型（Classification）** 判定严重等级和路由派发。
- 使用 **RAG** 检索对应的安全应急处置预案。
- 使用 **工具调用** 在安全数据库中反查 IP、MAC 或时间戳等额外上下文。
- 记录详尽的决策日志和中间状态链路追踪（Traces）。


## 5. 开发者工具 (Developer Tools)

### 对标公司与信息源：
- **JetBrains**：[Senior Software Developer, IntelliJ AI](https://builtin.com/job/senior-software-developer-intellij-ai/9646277), [AI 博客](https://blog.jetbrains.com/ai/)
- **Grafana Labs**：[Staff AI Engineer](https://builtin.com/job/staff-ai-engineer-grafana-ai-ml-usa-remote/9886859), [工程博客](https://grafana.com/blog/engineering/)
- **Coinbase**：[Staff Software Engineer, AI Platform](https://www.builtinla.com/job/staff-software-engineer-ai-platform-team/9889856), [技术博客](https://www.coinbase.com/blog/landing/engineering)

### 业务中需要解决的痛点：
- 自动分类、筛选并排查 Issue。
- 自动化评审 Pull Requests (PR)。
- 用直观的语言解释代码提交（Commit）带来的具体变更。
- 根据 Commit 历史自动编写 Release Notes 版本发布志。
- 检索庞大杂乱的内部工程开发设计文档。

### 推荐研读的开源仓库：
- **[Repo Assistant](https://github.com/guillermoscript/repo-assistant)**
  - **行业领域**：研发效率工具
  - **核心痛点**：开源维护人员需要快速识别是否有重复提交的 GitHub Issue。
  - **技术方案**：GitHub App 集成、文本 Embedding 向量计算、Supabase 存储以及 `pgvector` 向量检索。
- **[Qodo PR Agent](https://github.com/qodo-ai/pr-agent)**
  - **行业领域**：代码审核工具
  - **核心痛点**：研发团队需要对提交的代码改动进行自动化的初步 PR 评审。
  - **技术方案**：PR 代码比对分析、自动写评论、概括改动要点并实现自动化审查流。
- **[Open Code Review](https://github.com/spencermarx/open-code-review)**
  - **行业领域**：代码安全与审查
  - **核心痛点**：代码评审员需要工具协助发现代码变更中可能隐藏的逻辑漏洞或 Bug。
  - **技术方案**：多智能体协作评审工作流。

### 候选项目创意：
- 重复 GitHub Issue 自动检索与拦截器
- 自动 PR 代码评审与安全审查助手
- 版本发布日志（Release Notes）智能生成器
- 语音一键转 GitHub Issue 自动整理机器人
- 内部研发架构设计文档智能检索助手

### 推荐技术选型：
- 使用 **向量嵌入 (embeddings)** 进行重复度匹配与语义去重。
- 使用 **工具调用** 读写 GitHub API。
- 使用 **结构化输出** 规范自动打上的 Label 或评论内容。
- 针对路由派发、数据解析和权限验证编写严格的单元测试。


## 6. 电商与二手交易市场 (E-Commerce)

### 对标公司与信息源：
- **Airbnb**：[Staff Software Engineer, Marketplaces Intelligence](https://www.builtinla.com/job/staff-software-engineer-marketplaces-intelligence-data-and-ai/9609308), [技术博客](https://airbnb.tech/blog/)
- **eBay**：[AI Platform Engineer](https://builtin.com/job/ai-platform-engineer/9345591), [创新故事](https://innovation.ebayinc.com/stories/)
- **Toast**：[Principal Software Engineer, AI Pod](https://builtin.com/job/principal-software-engineer-ai-pod-dublin-ireland/9611924), [技术博客](https://technology.toasttab.com/)

### 业务中需要解决的痛点：
- 协助卖家快速创建吸引人的商品上架描述。
- 自动扩充和丰富平台商品库的标签。
- 对卖家发布的商品进行智能分类。
- 识别平台上的恶意重复铺货或盗图行为。
- 优化商铺和商品的语义搜索与个性化推荐。

### 推荐研读的开源仓库：
- **[LISTING-INTELLIGENCE](https://github.com/KazKozDev/LISTING-INTELLIGENCE)**
  - **行业领域**：商品上架优化
  - **核心痛点**：卖家上架商品时需要优化文案、做 SEO 并校验是否违反平台合规禁售条例。
  - **技术方案**：计算机视觉、OCR 文字识别、多模态大模型、FastAPI、React 以及合规自检规则。
- **[eBay Listing Automation](https://github.com/jjshay/ebay-listing-automation)**
  - **行业领域**：电商上架自动化
  - **核心痛点**：卖家希望通过拍照直接生成完整的规范商品详情页。
  - **技术方案**：多模态识别、结构化输出上架字段、Docker 镜像打包以及 eBay 官方 API 深度集成。
- **[AWS AI-Powered Product Catalog](https://github.com/aws-samples/sample-ai-powered-product-catalog)**
  - **行业领域**：商品目录自动化
  - **核心痛点**：运营团队需要从海量厂商图片中提取商品参数，创建规范的商品类目目录。
  - **技术方案**：AWS Bedrock、Streamlit、S3 存储、AWS Lambda、Step Functions 和 DynamoDB 配合。

### 候选项目创意：
- 商品智能图文生成与质量评估器
- 商品自动归类与重复铺货判定系统
- 平台违禁品上架自动审查器
- 基于厂商图片与说明的数据抽取扩充流
- 电商搜索召回效果自动化评估器

### 推荐技术选型：
- 使用 **多模态视觉模型（Vision Model）** 解析商品图片。
- 使用 **结构化输出** 规范商品属性字段。
- 使用 **确定性验证逻辑** 校验价格范围、必填项和违禁敏感词。
- 编写评测集，评估属性抽取准确率与合规检测率。


## 开源仓库学习自查清单

当你分析以上推荐的开源仓库时，请自问：
- [ ] 它属于什么行业领域？
- [ ] 它解决了什么具体的痛点？
- [ ] 它的目标用户是谁？
- [ ] 系统接收什么格式的输入？产生什么格式的输出？
- [ ] 它是怎么证明/评测最终的输出是可靠的？
- [ ] 系统中哪些部分是传统的确定性逻辑代码？哪些部分才真正需要大模型参与？
- [ ] 它编写了什么规格的单元测试或大模型评测？
- [ ] 如果让你来重构，怎么做才能让这个代码仓库变得更强、更严谨？

*把这些自查出来的感悟，应用到你自己的项目规划书中去。*
