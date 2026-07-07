# 面试原始数据与支持文件

本目录存放了用于整理 `interview/questions_zh.md` 以及其它面试指南的全部背景研究数据。库中的每一道面试真题均可追溯至真实的互联网源头。


## 目录结构

```
data/
├── sources/                  # 汇总的所有来源链接列表
│   ├── interview-stories.md       # 第一人称视角的真实求职经历 (Medium, dev.to, 博客等)
│   ├── discussion-threads.md      # 58 场 Reddit + 46 场 HN 技术社区讨论帖索引
│   ├── blogs-and-guides.md        # 各种大模型面试通关指南与技术文章
│   ├── github-repos.md            # 从 GitHub 上搜集到的 65+ 份真实离线作业仓库
│   ├── interview-prep-repos.md    # GitHub 上的面试备战和刷题仓库
│   ├── community-links.md         # 主流技术社区及 Subreddit 论坛版块
│   ├── all-links.md               # 完整的超链接库 (整理出的每一个真实 URL)
│   ├── github-search-methodology.md  # 说明我们是如何在 GitHub 上检索真实作业的
│   └── research-approach.md       # 介绍本指南在调研时使用的高级搜索工具
├── fetched/                  # 实际下载/抓取并本地缓存的网页内容
│   ├── reddit-posts/              # 通过 Arctic-Shift 接口抓取的 10 篇 Reddit 帖子 (.md + .json)
│   └── grok-responses/            # 带有引用源的 8 份 Grok API 搜索结果 (.json)
├── link-summaries/           # 进行交叉对比与校验的结果
│   ├── techeon-corroboration-map.md   # 对 27 道真题进行了信源校验 (20道已被确凿证据证实)
│   ├── agent-questions-research.md    # 由其它 AI 智能体协助抓取和验证的链接结果
│   ├── APPROACHES.md                  # 详细阐述从各个平台批量抓取网页的方法
│   ├── reddit-*.md, hn-*.md 等        # 针对特定平台的抓取结果汇总
│   └── blind-*.md, x-*.md             # 整理的 TeamBlind 匿名论坛与 Twitter 帖子摘要
├── job-descriptions/         # 收录的 51 份 YAML 格式的 AI 工程师招聘岗位原始描述
└── research-exports/         # ChatGPT、Gemini、Grok 等 AI 助手对话的原始研究日志导出
```


## 核心数据源文件说明

| 文件路径 | 包含什么内容 |
|------|-----------------|
| `sources/discussion-threads.md` | 104 篇包含直接求职体验的 Reddit + HN 讨论帖。每一条都包含 URL、热度分值以及一行内容简述。 |
| `sources/interview-stories.md` | 来自拿到 Offer 的工程师的第一人称视角复盘博客（Medium、dev.to 等），附带摘要和超链接。 |
| `sources/github-repos.md` | 整理的 65+ 个来自 GitHub 的真实离线面试作业仓库，注明了公司名称、发布日期、内容描述与 URL。 |
| `sources/blogs-and-guides.md` | 各大厂面试备战文章、RAG 指南与行业分析汇总表。 |
| `link-summaries/techeon-corroboration-map.md` | 将 27 道智能体 AI 真题与 Reddit 上的实证进行映射对比，其中 20 道已被完全证实。 |


## 如何复现抓取

### 1. 抓取 Reddit 帖子 (免费，无需登录 Token)

利用 Arctic-Shift 开放 API。在 `interview/_internal/` 目录下运行：

```bash
cd interview/_internal

# 抓取单篇帖子
uv run python fetch_reddit.py 'https://www.reddit.com/r/ExperiencedDevs/comments/1r78ipa/...'

# 批量抓取
uv run python fetch_reddit.py --batch ../data/reddit-urls-to-fetch.txt
```
*抓取结果（`.md` 与 `.json` 格式）将保存在 `data/fetched/reddit-posts/` 中。*

### 2. 使用 Grok 进行联网检索 (付费，需配置 x.ai API Key)

```bash
cd interview/_internal

uv run python xai_search.py \
  '你的联网搜索 Prompt 描述。告诉它去检查哪些数据源 (Reddit, HN, X, Medium)。
   要求返回具体的 URL 和原文引用。告诉它如果没有检索到结果，就诚实回答。' \
  --tools web_search,x_search \
  --system '指定研究助手的角色与质量准则' \
  --label '描述性文件名标签'
```
*搜索结果（完整 JSON）将保存在 `data/fetched/grok-responses/` 中。*

### 3. 遇到网页防火墙时的提取技巧

- **Jina Reader**：在原 URL 前加上 `https://r.jina.ai/<URL>` 进行 Markdown 提取。
- **谷歌快照**：访问 `https://webcache.googleusercontent.com/search?q=cache:<URL>`。
- **Wayback Machine 网页档案馆**：访问 `https://web.archive.org/web/<URL>`。

### 4. 抓取 Hacker News 讨论

使用 Hacker News 官方 JSON 接口：`https://hacker-news.firebaseio.com/v0/item/<ID>.json`。


## 脚注来源列表

在 `interview/questions_zh.md` 的最底部定义了完整的 50+ 个核心脚注信息 —— 涵盖 YouTube 视频、Medium 专栏、Reddit、Hacker News、大模型求职指南网站、开源 GitHub 仓库以及 datainterview.com。
