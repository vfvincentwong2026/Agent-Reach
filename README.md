<div align="center">

<h1>👁️ Agent Reach</h1>

**给你的 AI Agent 一键装上互联网能力**

<sub>接入方式会换代，你不用操心 —— 我们替你选好、装好、体检好。</sub>

<br/>

[![Trendshift #1](https://trendshift.io/api/badge/repositories/24387)](https://trendshift.io/repositories/24387)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.10+-green.svg?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Stars](https://img.shields.io/github/stars/Panniantong/agent-reach?style=for-the-badge)](https://github.com/Panniantong/agent-reach/stargazers)

<br/>

[快速开始](#-快速开始) · [能用它做什么](#-装好就能用) · [支持平台](#-支持哪些平台) · [安全与隐私](#-安全与隐私) · [English](docs/README_en.md)

</div>

---

## ⚡ 一句话安装

把下面这句话**直接复制给你的 AI Agent**（Claude Code / OpenClaw / Cursor / Windsurf 都行）：

```text
帮我安装 Agent Reach：https://raw.githubusercontent.com/Panniantong/agent-reach/main/docs/install.md
```

几分钟后，它就能读推特、搜 Reddit、看 YouTube、刷小红书了。

> 🔄 **已装过？更新也是一句话：**
> ```text
> 帮我更新 Agent Reach：https://raw.githubusercontent.com/Panniantong/agent-reach/main/docs/update.md
> ```

> ⚠️ **OpenClaw 用户**：安装前需开启 exec 权限，否则 Agent 无法执行命令。
> ```bash
> openclaw config set tools.profile "coding"
> ```
> 然后重启 Gateway（`openclaw gateway restart`）并开新对话。其他平台（Claude Code / Cursor / Windsurf 等）不受此限制。

---

## 🎯 它解决什么问题

你的 Agent 能写代码、改文档、管项目 —— 但让它去网上找点东西，就抓瞎了：

| 你说 | 以前 | 装了 Agent Reach |
| :--- | :--- | :--- |
| "看看这个 YouTube 教程讲了啥" | ❌ 拿不到字幕 | ✅ 提取字幕 |
| "推特上大家怎么评价这个产品" | ❌ API 要付费 | ✅ 直接搜 |
| "Reddit 上有没有人遇到过同样的 bug" | ❌ 服务器 IP 被 403 | ✅ 登录态读取 |
| "小红书上这个品的口碑" | ❌ 必须登录 | ✅ 复用你已有会话 |
| "B站这个技术视频总结一下" | ❌ 被风控全拦 | ✅ `bili-cli` 无登录可搜可读 |
| "全网搜一下最新 LLM 框架对比" | ❌ 要么付费要么质量差 | ✅ Exa 语义搜索 |
| "这个网页写了啥" | ❌ 一堆 HTML 标签 | ✅ 干净正文 |
| "订阅这几个 RSS，有更新告诉我" | ❌ 自己装库写代码 | ✅ 开箱即用 |

每个平台都有自己的门槛 —— 付费 API、反爬封锁、登录账号、数据清洗。**Agent Reach 把这些统统打包成一句话。**

---

## 🚀 快速开始

### Step 1 · 装

复制给你的 Agent：

```text
帮我安装 Agent Reach：https://raw.githubusercontent.com/Panniantong/agent-reach/main/docs/install.md
```

Agent 会自己完成剩下的所有事情。

<details>
<summary><b>它会做什么？（点击展开）</b></summary>

<br/>

1. **安装 CLI** —— 从本仓库安装 `agent-reach` 命令行（自带 yt-dlp、feedparser）
2. **检查基建** —— Node.js、gh CLI、mcporter 是否齐全，缺什么告诉你
3. **按授权安装** —— 只有显式传 `--system` 才装系统依赖、接入 Exa
4. **检测环境** —— 判断本地还是服务器，给出对应配置建议
5. **按授权注册 SKILL** —— 只有 `--system` 才写入 Agent skills 目录，默认只检查不改文件
6. **问你要不要更多** —— 默认只激活 6 个零配置渠道；需登录的（小红书、Twitter、Reddit 等）会列菜单让你点名

</details>

### Step 2 · 体检

```bash
agent-reach doctor
```

一条命令告诉你每个渠道**当前走哪条路、哪个通、哪个不通、怎么修**。

### Step 3 · 用

不需要记任何命令，直接对 Agent 说话即可。

---

## 💬 装好就能用

**零配置可用**（装完直接说）：

- "帮我看看这个链接" → 读任意网页
- "这个 GitHub 仓库是做什么的" → 读公开仓库 + 搜索
- "这个 YouTube 视频讲了什么" → 提取字幕
- "B站搜一下 AI 教程" → 无登录可搜
- "全网搜一下 LLM 框架对比" → Exa 语义搜索
- "订阅这个 RSS" → 解析订阅源
- "V2EX 最近有什么热门帖子" → 直接读

**需登录解锁**（对 Agent 说一句话即可）：

| 你说 | 解锁能力 |
| :--- | :--- |
| "帮我配 Twitter" | 搜推文、时间线、读长文 |
| "帮我配 Reddit" | 搜索 + 读帖子和评论 |
| "帮我配 B站" | 字幕提取 |
| "帮我配小红书" | 搜索、阅读、评论 |
| "帮我配 Facebook" | 搜索、主页、Feed、群组 |
| "帮我配 Instagram" | 用户搜索、Profile、最近帖子 |
| "帮我配 LinkedIn" | Profile、公司页面、职位搜索 |
| "帮我配 Boss直聘" | 搜索岗位 + JD 全文 |
| "帮我配雪球" | 股票行情、搜索、热门榜 |
| "帮我配小宇宙播客" | 播客音频转文字 |
| "帮我登录 GitHub" | 私有仓库、提 Issue/PR、Fork |

> **不知道怎么配？不用查文档。** 直接告诉 Agent「帮我配 XXX」，它会一步步引导你。

---

## 📡 支持哪些平台

### 🟢 开箱即用（零配置）

| 平台 | 能力 |
| :--- | :--- |
| 🌐 **任意网页** | Jina Reader 阅读正文 |
| 📺 **YouTube** | 字幕提取 + 视频搜索 |
| 📡 **RSS / Atom** | 阅读任意订阅源 |
| 🔍 **全网搜索** | Exa 语义搜索（免费、无需 Key） |
| 📦 **GitHub 公开仓库** | 读取 + 搜索 |
| 📺 **B站** | 搜索 + 视频详情（`bili-cli`，无需登录） |
| 💻 **V2EX** | 热门帖、节点帖、帖子详情+回复、用户信息 |

### 🟡 配置后解锁（需登录态）

| 平台 | 解锁能力 | 配置方式 |
| :--- | :--- | :--- |
| 📦 **GitHub 私有** | 私有仓库、Issue/PR、Fork | 对 Agent 说「帮我登录 GitHub」 |
| 🐦 **Twitter/X** | 搜索、时间线、长文 | 对 Agent 说「帮我配 Twitter」 |
| 📖 **Reddit** | 搜索 + 帖子 + 评论 | 桌面装 OpenCLI 用浏览器登录态 |
| 📘 **Facebook** | 搜索、主页、Feed、群组 | 桌面装 OpenCLI（复用 Chrome 登录态） |
| 📷 **Instagram** | 用户搜索、Profile、Explore | 桌面装 OpenCLI（复用 Chrome 登录态） |
| 📕 **小红书** | 搜索、阅读、评论 | OpenCLI 复用 Chrome 会话 |
| 💼 **LinkedIn** | Profile、公司、职位搜索 | 对 Agent 说「帮我配 LinkedIn」 |
| 🎯 **Boss直聘** | 岗位搜索 + JD 全文 | 对 Agent 说「帮我配 Boss直聘」 |
| 📈 **雪球** | 行情、搜索、热门榜 | 对 Agent 说「帮我配雪球」 |
| 🎙️ **小宇宙播客** | 音频转文字 | 对 Agent 说「帮我配小宇宙播客」 |
| 📺 **B站字幕** | 字幕提取 | 对 Agent 说「帮我配 B站」 |

<sub>💡 表格会随平台策略变化更新。`agent-reach doctor` 永远告诉你**当前走的是哪条路**。</sub>

---

## 🔒 安全与隐私

| 措施 | 说明 |
| :--- | :--- |
| 💰 **完全免费** | 所有工具开源、所有 API 免费。唯一可能花钱的是服务器代理（~$1/月），本地电脑不需要 |
| 🔐 **凭据本地存储** | Cookie / Token 只存在 `~/.agent-reach/config.yaml`，权限 `600`（仅所有者可读写），**不上传不外传** |
| 🛡️ **默认安全** | `agent-reach install` 默认**只检查环境，不修改系统**；只有显式 `--system` 才安装依赖、写入配置 |
| 👀 **完全开源** | 代码透明，随时可审查。所有依赖也是开源项目 |
| 🔍 **Dry Run** | `agent-reach install --dry-run` 预览所有操作，不做任何改动 |
| 🧩 **可插拔** | 不信任某个组件？换掉对应 channel 文件即可，不影响其他 |

### 🍪 Cookie 使用建议

> ⚠️ **封号风险提醒**：使用 Cookie 登录的平台（Twitter、小红书等），通过脚本/API 调用**存在被检测并封号的风险**。请务必使用**专用小号**，不要用主账号。

原因有二：

1. **封号风险** —— 平台可能检测到非正常浏览器的 API 调用行为
2. **安全风险** —— Cookie 等同于完整登录权限，小号可在凭据泄露时限制影响范围

### 📦 安装方式速查

| 方式 | 命令 | 适合场景 |
| :--- | :--- | :--- |
| 默认安全检查 | `agent-reach install --env=auto` | 所有环境；只读检查 |
| 显式装系统依赖 | `agent-reach install --env=auto --system` | 你明确允许修改当前机器 |
| 仅预览 | `agent-reach install --env=auto --dry-run` | 先看看会做什么 |

### 🗑️ 卸载

```bash
agent-reach uninstall
```

清除：`~/.agent-reach/`（含所有 token/cookie）、各 Agent 的 skill 文件、mcporter 中的 MCP 配置。

```bash
agent-reach uninstall --dry-run       # 只预览
agent-reach uninstall --keep-config   # 保留 token 配置，只删 skill
pip uninstall agent-reach             # 卸载 Python 包本身
```

---

## ❓ 常见问题

<details>
<summary><b>需要花钱吗？</b></summary>

<br/>
不需要。所有工具开源、所有 API 免费。唯一可能花钱的是**部署在服务器上时的代理**（~$1/月），本地电脑跑不需要。

</details>

<details>
<summary><b>会泄露我的 Cookie 吗？</b></summary>

<br/>
不会。Cookie 只存在你本机 `~/.agent-reach/config.yaml`，权限 600，不上传不外传。代码完全开源可审查。

</details>

<details>
<summary><b>某个平台突然不能用了怎么办？</b></summary>

<br/>
跑 `agent-reach doctor` 看诊断。每个平台都是「首选 + 备选」多后端路由，某个接入方式失效会自动切到下一个 —— 你不用管。

</details>

<details>
<summary><b>兼容哪些 Agent？</b></summary>

<br/>
Claude Code、OpenClaw、Cursor、Windsurf……**任何能跑命令行的 Agent** 都能用。

</details>

<details>
<summary><b>我可以只装其中几个平台吗？</b></summary>

<br/>
可以。默认只激活 6 个零配置渠道，其余需登录的会列菜单让你点名，只装你选的。

</details>

---

## 📖 进阶：它是怎么设计的

> 以下内容面向想深入了解或二次开发的用户，**普通使用者可跳过**。

<details>
<summary><b>设计理念</b></summary>

<br/>

**Agent Reach 是一个能力层（capability layer），不是又一个工具。**

它比任何具体实现高一层 —— 负责**选型、安装、体检、路由**，不负责底层读取本身。读取由 Agent 直接调用上游工具完成，没有包装层。

你给新 Agent 装环境时，总要花时间找工具、装依赖、调配置 —— Twitter 用什么读？Reddit 怎么登录？小红书的 CLI 停更了换什么？每次都要重新踩一遍。

Agent Reach 做的事很简单：**当下最稳的接入方式，我们替你选好、装好、体检好。**

</details>

<details>
<summary><b>每个平台 = 首选 + 备选的有序后端列表</b></summary>

<br/>

换接入方式 = 调整列表顺序，不是重写代码。`agent-reach doctor` 会告诉你每个平台**当前在用哪个后端**。

```text
channels/
├── web.py          → Jina Reader
├── twitter.py      → twitter-cli ▸ OpenCLI ▸ bird
├── youtube.py      → yt-dlp
├── github.py       → gh CLI
├── bilibili.py     → bili-cli ▸ OpenCLI ▸ 搜索 API
├── reddit.py       → OpenCLI ▸ rdt-cli
├── facebook.py     → OpenCLI（桌面浏览器登录态）
├── instagram.py    → OpenCLI（桌面浏览器登录态）
├── xiaohongshu.py  → OpenCLI ▸ xiaohongshu-mcp ▸ xhs-cli
├── linkedin.py     → mcp-server-linkedin ▸ Jina Reader
├── rss.py          → feedparser
├── exa_search.py   → Exa via mcporter
└── __init__.py     → 渠道注册（doctor 检测用）
```

每个渠道文件按序**真实探测**各候选后端（不只是看命令存不存在），第一个完整可用的当选；坏掉的会给出修复处方。

</details>

<details>
<summary><b>当前选型（基于真机实测定期复核）</b></summary>

<br/>

| 场景 | 首选 | 备选 | 为什么这么选 |
| :--- | :--- | :--- | :--- |
| 读网页 | Jina Reader | — | 免费，不需要 API Key |
| 读推特 | twitter-cli | OpenCLI | 实测搜索稳定；OpenCLI 走浏览器登录态兜底 |
| Reddit | OpenCLI（桌面） | rdt-cli | 匿名接口已被封、官方 API 审批制 |
| Facebook | OpenCLI（桌面） | — | Graph/Groups API 权限收紧 |
| Instagram | OpenCLI（桌面） | 官方 Graph API | instaloader 类路径不稳定 |
| YouTube | yt-dlp | — | 154K Star，仍是最佳 |
| B站 | bili-cli | OpenCLI ▸ 搜索 API | yt-dlp 被风控 412 封死（2026-06 实测） |
| 搜全网 | Exa via mcporter | — | AI 语义搜索，MCP 接入免 Key |
| GitHub | gh CLI | — | 官方工具，认证后完整 API 能力 |
| 读 RSS | feedparser | — | Python 生态标准选择 |
| 小红书 | OpenCLI（桌面） | xiaohongshu-mcp ▸ xhs-cli | OpenCLI 只用用户已有会话 |
| LinkedIn | mcp-server-linkedin | Jina Reader | MCP 服务，浏览器自动化 |

</details>

---

## ⭐ 支持这个项目

这个项目我每天在用，所以会一直维护：

- 有新渠道需求 → 陆续加
- 每个渠道尽量保证**能用、好用、免费**
- 平台改了反爬或 API → 我想办法解决

为 Web 4.0 基建贡献一份力量。**Star 一下，下次需要的时候能找到。** ⭐

---

## 💼 业务合作

我在承接 Agent 相关的定制与落地合作。

如果你在企业生产、运营、市场、投研、数据处理、内容处理等流程里，有希望用 Agent 自动化的环节，欢迎交流。**不需要你已经想清楚方案** —— 只要你有真实流程、真实问题，我可以一起判断能不能解决、怎么做。

加微信请备注：`业务 + 你想让 Agent 帮你做什么`
Builder 备注：`Builder + 你在做什么`
只想进群备注：`加群`

<p align="center">
  <img src="docs/wechat-group-qr.jpg" width="280" alt="WeChat QR">
</p>

> 🐛 **Bug 反馈 / 功能请求**请走 [GitHub Issues](https://github.com/Panniantong/Agent-Reach/issues)，更容易跟踪。

---

## 🙏 致谢

[OpenCLI](https://github.com/jackwener/opencli) · [twitter-cli](https://github.com/public-clis/twitter-cli) · [rdt-cli](https://github.com/public-clis/rdt-cli) · [xiaohongshu-mcp](https://github.com/xpzouying/xiaohongshu-mcp) · [xhs-cli](https://github.com/jackwener/xiaohongshu-cli) · [bili-cli](https://github.com/public-clis/bilibili-cli) · [yt-dlp](https://github.com/yt-dlp/yt-dlp) · [Jina Reader](https://github.com/jina-ai/reader) · [Exa](https://exa.ai) · [mcporter](https://github.com/nicobailon/mcporter) · [feedparser](https://github.com/kurtmckee/feedparser) · [mcp-server-linkedin](https://github.com/stickerdaniel/linkedin-mcp-server)

## 📮 联系

- 📧 **Email:** pnt01@foxmail.com
- 🐦 **Twitter/X:** [@Neo_Reidlab](https://x.com/Neo_Reidlab)

## 🔗 友情链接

- [Agent Skills Hub](https://agentskillshub.top/) — 133,000+ Claude 技能和 MCP 服务器，全部安全分级、质量评分，每 8 小时刷新
- [AtomGit 镜像](https://atomgit.com/qq_51337814/Agent-Reach) — 国内访问与克隆

## 📜 License

[MIT](LICENSE)

<div align="center">

<br/>

<a href="https://www.star-history.com/?type=date&repos=Panniantong%2FAgent-Reach">
  <img alt="Star History Chart" src="https://api.star-history.com/chart?repos=Panniantong/Agent-Reach&type=date&legend=top-left" />
</a>

<br/>
<br/>

<sub>Made with ❤️ for the Agent era</sub>

</div>
