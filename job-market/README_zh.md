# 招聘市场数据 (Job Market Data)

从 builtin.com 抓取的 4,894 份 AI 工程师招聘岗位数据（2026年1月 - 6月），涵盖洛杉矶（全球）、纽约、伦敦、阿姆斯特丹、柏林和印度地区。

基于本数据集的分析结果和核心洞察，请参阅 [角色定位分析 (role/)](../role/README_zh.md)。


## 目录结构

- [data_structured/](data_structured/) —— 存放按抓取日期 `YYYY-MM-DD/` 归档的结构化 YAML 数据文件。
- [data_raw/](data_raw/) —— 存放按抓取日期 `YYYY-MM-DD/` 归档的原始抓取文本数据。
- [analysis.ipynb](analysis.ipynb) —— 用于进行数据统计分析的 Jupyter Notebook 笔记本。
- [_internal/](_internal/) —— 抓取脚本、处理脚本以及用于流水线运行的中间 CSV 文件。


## 核心数据摘要

- **3,567 个岗位 (72.9%)** 属于纯 AI 开发 (AI-First) —— 涉及 RAG、智能体、大模型应用编排。
- **1,199 个岗位 (24.5%)** 属于 AI 支撑 (AI-Support) —— 涉及开发平台、基础设施、工具链开发。
- **91 个岗位 (1.9%)** 属于冠以“AI 工程师”头衔的传统机器学习角色。
- 涉及 1,954 家去重企业，其中招聘岗位最多的公司为：Capital One (91个)、Citi (74个)、Optum (58个)。

**最热门技能统计**：
- **编程语言**：Python (83.7%), TypeScript (21.3%), Java (17.6%)
- **大模型核心**：RAG (34.1%), LLMs (17.7%), 提示词工程 (15.9%)
- **云与运维**：AWS (40.0%), Docker (35.2%), Kubernetes (29.4%)
- **框架与算法**：LangChain (23.8%), PyTorch (20.9%), SQL (25.8%)


## 数据格式说明

在 `data_structured/YYYY-MM-DD/` 目录下的每个结构化 YAML 文件都包含以下字段：

```yaml
title: Senior AI/Data Engineer           # 职位头衔
company: WorkWave                        # 招聘公司
location: USA                            # 工作地点
work_type: FULL_TIME                     # 工作类型 (全职/兼职/合同等)
level: Expert/Leader                     # 资深等级 (专家/Leader/初级等)
skills: [Python, AWS, Airflow, dbt]      # 提取出的技能标签
company_size: 1,000 Employees            # 企业规模
compensation: $160,000 - $180,000/year   # 薪资待遇范围
description: |                           # 岗位完整详情描述
  Full job description...
posted_date: 2026-01-18                  # 发布日期
url: https://builtin.com/job/...         # 原始招聘链接
source: Built In                         # 抓取来源
```
