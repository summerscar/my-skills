---
layout: default
title: 前端技术周报 (2026-05-24)
date: 2026-05-24
category: RSS 周报
---

## 📰 前端技术周报 (2026-05-24)

### 📝 本周要点

- **Google I/O 2026: "Agentic Web" 时代** - 发布 WebMCP 标准、HTML-in-Canvas API、Baseline Checker、Modern Web Guidance AI 技能
- **财富正在向 AI 集中** - 内存、储存、CPU、服务器等 AI 相关股价暴涨，三星可能成为今年最赚钱公司
- **npm RFC: install scripts 应改为 opt-in** - GitHub 提出 npm 是唯一默认运行 install scripts 的主流包管理器，已成安全弱点
- **Mini Shai-Hulud: 300+ 恶意 npm 包** - TanStack 事件后更多恶意包被发布，包括 antv 家族和 timeago.js
- **Dr. Axel 博客因 AI 爬虫而下线** - JavaScript 传奇人物 Axel Rauschmayer 因不堪 AI 爬虫压力，将博客和 JS 书籍从网上移除

---

### ⚛️ React/前端框架

- **Component Party: UI 框架的 Rosetta Stone** - 使用代码片段比较众多框架（包括 React、Vue、Svelte、Angular、Ember 等）执行常见任务。近期更新扩展了 Angular 和 Svelte 覆盖范围，并新增了 Ripple 和 Ember Polaris。来源: React Status | [链接](https://react.statuscode.com/issues/475)

- **TanStack RSC: 一种不同且可论证更好的实现** - "实现方式截然不同，在我看来比你可能在 Next.js 中看到的 RSC 实现更好。" 来源: React Status | [链接](https://react.statuscode.com/issues/475)

- **Storybook 10.4** - 前端组件工作坊新增首类 TanStack React 支持、更简洁的 React Native 设置，以及让 AI 代理自动在复杂应用中设置 Storybook 的能力。来源: React Status | [链接](https://react.statuscode.com/issues/475)

- **Reddit r/reactjs 讨论: 为什么人们从 Next.js 迁移到 TanStack Start** - 社区讨论 Next.js vs TanStack Start 的选择。来源: React Status | [链接](https://react.statuscode.com/issues/475)

- **Redux Toolkit v2.12.0 / React Redux 9.3.0** - Redux 生态系统更新。来源: React Status | [链接](https://react.statuscode.com/issues/475)

- **用 AI Agent 迁移 Express 应用到 Next.js** - Google 的 James 展示如何使用 Agent 技能将遗留 Express.js 应用现代化到 Next.js App Router、TypeScript、MongoDB、Zod 和 shadcn/ui。来源: React Status | [链接](https://react.statuscode.com/issues/475)

- **Mark Erikson 的 Agent 设置、工作流和工具** - Redux 维护者分享他的日常开发工作流，包括使用 OpenCode（开源的 JavaScript 驱动的编码代理）、如何管理知识库、任务等。来源: React Status | [链接](https://react.statuscode.com/issues/475)

- **GL-React v6: 用 React 创建 WebGL Shader** - 提供直接使用 React 和 JSX 创建 WebGL shader 的抽象。有大量示例和完整代码可参考。来源: React Status | [链接](https://gre.github.io/gl-react/)

- **Expo SDK 56 发布** - 从 React Web 到原生 iOS 应用的真实体验。Expo UI 现在被认为可用于生产环境。来源: React Status | [链接](https://try.expo.dev)

- **Hot Updater: React Native 的自托管 OTA 更新** - 在无需应用商店提交的情况下部署更新。最新更新新增 bundle diffing 以实现更小、更高效的更新。来源: React Status | [链接](https://hot-updater.dev)

- **Relay 21.0: Meta 的 React 数据获取框架** - Relay，Facebook 自身使用的声明式 GraphQL 数据获取框架，新增首类 TypeScript 支持、新的错误处理能力，以及**实验性 React Server Components 支持**。来源: React Status | [链接](https://react.statuscode.com/issues/475)

- **SVAR Calendar: React、Svelte 和 Vue 的日历组件** - 灵活的日历组件，MIT 许可核心和扩展商业版本。来源: React Status | [链接](https://svar.dev)

- **Rockpack 8.0.0** - 快速设置具有完整 SSR 支持、打包、linting 和测试的 React 应用的工具。v8.0 现在支持 ESLint 10、TypeScript 6 和 Tailwind CSS v4。来源: React Status | [链接](https://react.statuscode.com/issues/475)

- **React Native Zip Archive 8.0** - React Native 应用的 zip 归档功能。来源: React Status | [链接](https://react.statuscode.com/issues/475)

---

### 📦 JavaScript/TypeScript

- **npm RFC: 是时候让 npm 的 install scripts 变为 opt-in 了** - npm 是唯一默认运行依赖安装脚本（如 postinstall）的主流包管理器，它们已成为太大的安全弱点。来源: JavaScript Weekly | [链接](https://github.com/github/rfcs/pull/121)

- **npq: 使 npm install 更安全的工具** - 站在 npm 前面并在安装前审计包，包括 pre/post install 脚本的存在。来源: JavaScript Weekly | [链接](https://github.com/npm/npq)

- **Mini Shai-Hulud 攻击: 300+ 恶意 npm 包被发布** - "Shai-Hulud" 类 npm 生态攻击持续发酵。今天又有数百个包——包括来自 antv 家族和 timeago.js 的流行包——被攻陷。来源: JavaScript Weekly | [链接](https://safedep.io/blog/another-shai-hulud-attack-hits-npm-with-300-new-packages/)

- **Dr. Axel 的博客下线了（暂时）** - JavaScript 传奇人物和前 JS Weekly 编辑 Axel Rauschmayer 因不堪 AI 爬虫压力，已将他的博客和 JavaScript 书籍从网上移除。来源: JavaScript Weekly | [链接](https://javascriptweekly.com/issues/786)

- **Bun 的 Rust 重写进展** - 尽管曾淡化其重要性，但 Bun 的基于 Rust 的重写已合并。不过对 AI 移植代码的质量存在疑问。来源: JavaScript Weekly | [链接](https://github.com/oven-sh/bun/pull/15609)

- **Deno 团队预告 Deno 2.8** - 本周发布，包含显著的 Node.js 兼容性改进、import defer、TypeScript 6.0.3 支持。来源: JavaScript Weekly | [链接](https://javascriptweekly.com/issues/786)

- **新的 `<install>` HTML 元素** - Chrome 和 Edge 团队正在开发用于浏览器渲染 PWA "可信安装按钮" 的新 HTML 元素。来源: JavaScript Weekly | [链接](https://javascriptweekly.com/issues/786)

- **Express.js 全新改版** - 包括新站点、logo 和改进的文档。来源: JavaScript Weekly | [链接](https://expressjs.com)

- **Angular 22 Release Candidate** - 最终版本预计 6 月初发布。预计包含基于 signal 的表单和 OnPush 变更检测策略成为默认。来源: JavaScript Weekly | [链接](https://javascriptweekly.com/issues/786)

- **Bun 1.3.14** - 替代 JS 运行时新增 Bun.Image、更多 HTTP/2 和 HTTP/3 支持、以及更多 Node 兼容性改进。来源: JavaScript Weekly | [链接](https://bun.com/blog/bun-v1.3.14)

- **ESLint Config Inspector 3.0** - 用于检查和理解 ESLint flat 配置的可视化工具。来源: JavaScript Weekly | [链接](https://javascriptweekly.com/issues/786)

- **TypeORM 1.0、ESLint 10.4.0、Relay 21.0、Rolldown 1.0.1** - 多个重要库更新。来源: JavaScript Weekly | [链接](https://javascriptweekly.com/issues/786)

- **ShadowRealm API 简介** - 介绍进行中的 TC39 提案，用于在具有自己全局对象和内部函数的隔离"伪域"中运行 JavaScript。来源: CSS Tricks | [链接](https://css-tricks.com/soon-we-can-finally-banish-javascript-to-the-shadowrealm/)

- **JSer.info #771 摘要** - Node.js 26.0.0、Rolldown 1.0、Jest v30.4.0、Chrome 148/149、StyleX 0.18、AVA 8.0、Electron 42 发布。来源: JSer.info | [链接](https://jser.info/2026/05/11/node.js-26.0.0-rolldown-1.0-jest-v30.4.0/)

---

### 🎨 CSS/样式

- **Google I/O 2026: 15 项前端更新** - Google I/O 大会聚焦于"agentic web 时代"。包含值得注意的开发者公告：WebMCP 标准提案、DevTools 自动调试、HTML-in-Canvas API、Baseline Checker 工具、直接在 Chrome 中使用 AI skills。来源: Frontend Focus | [链接](https://developer.chrome.com/blog/15-updates-from-google-io-2026/)

- **HTML-in-Canvas API 深度探索** - "我不得不说，我对此感到非常兴奋"。Vittorio Retrivi 热情地探讨了这个新 API 的工作原理，以及通过一些实际演示它能实现什么。来源: Frontend Focus | [链接](https://frontendfoc.us/link/185403/rss)

- **用 Modern Web Guidance 构建** - I/O 上同时宣布的还有这套新的"常青和专家审核"的 AI skills。它与大量流行的编码代理配合使用，可以协助 UX、性能、可访问性、布局等方面的最佳实践和模式。来源: Frontend Focus | [链接](https://developer.chrome.com/blog/modern-web-guidance)

- **从 Tailwind 迁移，学习结构化我的 CSS** - Julia Evans 分享在使用 Tailwind 八年后，如何将她的两个站点迁移回语义化 HTML 和原生 CSS——以及在此过程中学到了什么关于 CSS 结构的知识。来源: Frontend Focus | [链接](https://jvns.ca/blog/2026/05/19/moving-away-from-tailwind-css/)

- **Firefox 151 开发者发布说明** - 此版本昨日发布——终于为桌面端带来了 Document Picture-in-Picture API 支持，以及 `@container` CSS at-rule 现在支持 `style()` 查询。来源: Frontend Focus | [链接](https://developer.mozilla.org/en-US/docs/Mozilla/Firefox/Releases/151)

- **CSS gap decorations 登陆 Chromium** - Chrome 和 Edge 的即将版本将支持 CSS gap decorations——一种简单的方式来为 grid、flexbox 和多列布局之间的 gaps 设置样式，无需伪元素或 borders。来源: Frontend Focus | [链接](https://developer.chrome.com/blog/gap-decorations-stable)

- **使用 CSS round() 实现更好的流体尺寸** - Ahmad Shadeed 介绍了如何使用支持良好的 CSS `round()` 函数来创建可预测的流体尺寸。它与 `clamp()` 配合使用，可以在尺寸、排版和间距方面提供帮助。结果是更清晰、更易于维护的字体缩放，以及更精致的响应式布局。来源: Frontend Focus | [链接](https://ishadeed.com/article/css-round/)

- **6 亿+ 人从右向左书写：你的应用需要两个修复** - 提醒：数亿人从右向左书写，然而许多开发工具却将此视为事后考虑。大多数情况下，修复很简单：只需两个 HTML 属性。来源: Frontend Focus | [链接](https://evilmartians.com/chronicles/600-million-people-write-right-to-left-two-fixes-your-app-needs)

- **七种仅用 CSS 指定主题颜色的方式** - 涵盖 CSS 实现主题颜色的多种方法，包括自动、浅色和深色全部处理——以及调色板变量。来源: Frontend Focus | [链接](https://chrismorgan.info/blog/seven-ways-of-specifying-per-theme-colours-in-only-css/)

- **跨文档视图过渡：没人提及的陷阱** - 从技术角度看设置原生视图过渡时需要注意的一些陷阱（包括实现的变化），以及克服它们的实际步骤。来源: Frontend Focus | [链接](https://css-tricks.com/cross-document-view-transitions-the-gotchas-nobody-mentions/)

---

### 🛠 工具/构建

- **CodeGraph: Claude Code/Codex/Cursor/OpenCode 的预索引代码知识图谱** - 更少 token、更少工具调用、100% 本地。平均节省 35% 成本、59% token、49% 时间、70% 工具调用。来源: GitHub Trending | [链接](https://github.com/colbymchenry/codegraph)

- **Orval: 从 OpenAPI/Swagger 规范生成类型安全客户端** - 给定有效的 OpenAPI v3 或 Swagger v2 规范，为 React、Vue、Svelte、Solid 应用等生成模型、请求、hooks 和 mocks。来源: JavaScript Weekly | [链接](https://orval.dev)

- **Brownies: 带变更事件的浏览器存储** - 一个微小的 API，覆盖 cookies、localStorage、sessionStorage 和 IndexedDB。类型化值自动保存，你可以获得 `subscribe()` 用于变更事件。来源: JavaScript Weekly | [链接](https://github.com/franciscop/brownies)

- **Pica 10.0: 浏览器中的高质量图像调整** - 高质量的浏览器内图像调整，依赖 WASM 和 Web Workers，或必要时回退到纯 JS。v10 是一次现代化构建（2021 年以来首次），新增 ESM 和分离构建，并迁移到 TypeScript。来源: Frontend Focus | [链接](https://github.com/nodeca/pica)

- **Critical 8.0: 从 HTML 提取和内联关键路径 CSS** - 流行的、生产就绪的库。8.0 版本几天前刚发布。来源: Frontend Focus | [链接](https://github.com/addyosmani/critical)

- **phantom-ui: 提供结构感知骨架加载器的 Web Component** - 兼容任何框架，通过在运行时测量 DOM 工作。来源: Frontend Focus | [链接](https://github.com/frankaejkatappaja/phantom-ui)

---

### 📚 周刊摘要

#### 阮一峰科技爱好者周刊 #397

**本期主题：财富正在向 AI 集中**

- **主题文章：财富正在向 AI 集中** - AI 相关的所有东西最近都在上涨。内存、储存、CPU、服务器、液冷、光通信、变压器……股价全部在涨，更不要提前期已经涨过的芯片、模型、算力了，甚至铜和铝也在涨。世界第三大内存厂商 SK 海力士今年每个员工平均可拿到约 610 万人民币奖金。OpenAI 去年向 600 个员工回购了 66 亿美元的股票，平均每人拿到近 1000 万美元。

- **别用 AI 估算碳水含量** - 医生实验发现：四个大模型给出的回答不一样。同一张照片多次提交给同一个模型，回答也不一样。Gemini 2.5 Pro 估计值从 55 克到 484 克，整整相差了 429 克！

- **微软淘汰短信验证码** - 改用 Passkey、一次性时间码（TOTP）、以及验证过的邮件地址。Passkey 将是 Windows 11 以后主要的验证方式。

- **亚马逊供应链服务 (ASCS)** - 把自己的货运、配送、仓储和包裹运输向用户开放。让人想起 2006 年亚马逊开放 AWS。

**科技动态**：
- Google 提出重新定义鼠标指针，使其可视化 AI 操作流程
- 铜价上涨使旧铜线回收成为大生意
- 芝加哥送货机器人占用行人道引发居民抗议

**文章推荐**：
- GitHub Pages 有域名盗用问题
- JavaScript ShadowRealm API 简介
- Firefox 配置指南
- 被撤销证书的检查机制
- 临时性基础设施

**工具推荐**：
- **Abogen** - 将 ePub/PDF/text 文件转成有声书的跨平台桌面应用
- **FFmpeg Explorer** - 可视化生成 FFmpeg 命令的网页应用
- **Stock SDK** - 获取股票行情的开源 JavaScript SDK
- **Zephyr** - 开源的 Mihomo/Clash 跨平台桌面客户端
- **DimCut** - 开源剪辑软件，将时间轴折叠成多行
- **NotchNotes** - 隐藏在 Macbook 刘海里面的便签工具
- **Forgejo** - Gitea 分叉，可用来搭建自己的 Git 服务器
- **Web Visual Editor** - 实时编辑预览 HTML 文件的 VS Code 插件

**AI 相关**：
- **Remove-AI-Watermarks** - 移除 AI 图片水印的命令行工具
- **AVC** - 将 AI Agent 终端确认文字变成可交互网页弹窗
- **Lucarne** - 把本地运行的 AI Agent 接到微信 / Telegram

来源: 阮一峰 | [链接](http://www.ruanyifeng.com/blog/2026/05/weekly-issue-397.html)

---

### 🔒 安全

- **npm install scripts 应改为 opt-in** - GitHub 提出 RFC，因为 postinstall 脚本已成为主要安全弱点。来源: JavaScript Weekly | [链接](https://github.com/github/rfcs/pull/121)

- **Mini Shai-Hulud: 300+ 恶意 npm 包** - TanStack 事件后更多恶意包被发现，包括流行的 antv 家族和 timeago.js。来源: JavaScript Weekly | [链接](https://safedep.io/blog/another-shai-hulud-attack-hits-npm-with-300-new-packages/)

- **TanStack 加固措施** - npm 供应链事件后的安全改进。来源: React Status | [链接](https://tanstack.com/blog/npm-supply-chain-compromise-postmortem)

- **Electron 42 安全改进** - 不再在 postinstall 下载二进制文件以增强安全性。来源: JavaScript Weekly | [链接](https://www.electronjs.org/blog/electron-42-0)

---

### 🤖 AI/机器学习

- **Modern Web Guidance (Google)** - 新的"常青和专家审核"的 AI skills，协助 UX、性能、可访问性、布局等最佳实践。来源: Frontend Focus | [链接](https://developer.chrome.com/blog/modern-web-guidance)

- **Mark Erikson 的 Agent 工作流** - Redux 维护者分享他如何使用 OpenCode，以及如何管理他的知识库、任务等。来源: React Status | [链接](https://blog.isquaredsoftware.com/2026/05/agent-workflow-tools-setup/)

- **AI 估算碳水不可靠** - 实验发现 GPT-5.4、Claude Sonnet 4.6、Gemini 2.5 Pro/3.1 Pro 对同一张照片的估计值波动极大，从 55 克到 484 克不等。来源: 阮一峰 | [链接](https://www.diabettech.com/i-asked-ai-to-count-my-carbs-27000-times-it-couldnt-give-me-the-same-answer-twice/)

- **HTML-in-Canvas API** - Google I/O 发布的新 API，让 AI 更容易渲染内容到 canvas。来源: Frontend Focus | [链接](https://frontendfoc.us/link/185403/rss)

---

### ⭐ GitHub/开源热门

- **colbymchenry/codegraph** - 预索引代码知识图谱，为 Claude Code、Codex、Cursor、OpenCode 提供更少 token、更少工具调用、100% 本地的语义代码智能。平均节省 35% 成本、70% 工具调用。来源: GitHub Trending | [链接](https://github.com/colbymchenry/codegraph)

- **unprovable/ShadowCat** - 通过二维码在浏览器中传输文件。160 分，61 评论。来源: Hacker News | [链接](https://github.com/unprovable/ShadowCat)

- **Agent.email** - AI 代理的邮箱注册服务，通过 curl 注册，用人的 OTP 认领。来源: Hacker News | [链接](https://news.ycombinator.com/item?id=48225596)

- **Freenet** - 用于去中心化应用的 P2P 平台，从头开始重新设计。374 分，268 评论。来源: Hacker News | [链接](https://freenet.org)

- **helvesec/rmux** - 带有 Playwright 风格 SDK 的可编程终端多路复用器。188 分，92 评论。来源: Hacker News | [链接](https://github.com/helvesec/rmux)

- **kageroumado/phosphene** - 逆向工程 Apple 的视频壁纸。425 分，106 评论。来源: Hacker News | [链接](https://github.com/kageroumado/phosphene)

- **antoinezambelli/forge** - LLM 工具调用的可靠层，将 8B 模型从 53% 提升到 99%。676 分，251 评论。来源: Hacker News | [链接](https://github.com/antoinezambelli/forge)

- **zakirullin/files.md** - Obsidian 的开源替代。720 分，355 评论。来源: Hacker News | [链接](https://github.com/zakirullin/files.md)

- **stephenlthorn/auto-identity-remove** - macOS 的自动数据经纪人选择退出工具。325 分，135 评论。来源: Hacker News | [链接](https://github.com/stephenlthorn/auto-identity-remove)

- **MinishLab/semble** - AI 代码搜索，比 grep 少用 98% 的 token。444 分，150 评论。来源: Hacker News | [链接](https://github.com/MinishLab/semble)

---

### 🔬 Hacker News Show 精选

- **Show HN: ShadowCat – 通过二维码在浏览器中传输文件** - 160 分，61 评论。来源: Hacker News | [链接](https://github.com/unprovable/ShadowCat)

- **Show HN: Agent.email – 通过 curl 注册，用人的 OTP 认领** - 94 分，105 评论。为 AI 代理提供专用邮箱。来源: Hacker News | [链接](https://news.ycombinator.com/item?id=48225596)

- **Show HN: Freenet，用于去中心化应用的 P2P 平台** - 374 分，268 评论。全球去中心化键值存储，键是定义值状态的 WebAssembly 合约。来源: Hacker News | [链接](https://freenet.org)

- **Show HN: 我花了 4 年精通离线密码破解** - 265 分，59 评论。14 到 18 岁期间的深度研究。来源: Hacker News | [链接](https://news.ycombinator.com/item?id=48221896)

- **Show HN: Rmux – 带有 Playwright 风格 SDK 的可编程终端多路复用器** - 188 分，92 评论。~90% 的 tmux 命令兼容，类型化异步 Rust SDK。来源: Hacker News | [链接](https://github.com/helvesec/rmux)

- **Show HN: 我逆向工程了 Apple 的视频壁纸** - 425 分，106 评论。Phosphene 开源项目。来源: Hacker News | [链接](https://github.com/kageroumado/phosphene)

- **Show HN: Forge – Guardrails 将 8B 模型从 53% 提升到 99%** - 676 分，251 评论。本地模型的多步骤代理任务可靠层。来源: Hacker News | [链接](https://github.com/antoinezambelli/forge)

- **Show HN: Files.md – Obsidian 的开源替代** - 720 分，355 评论。来源: Hacker News | [链接](https://github.com/zakirullin/files.md)

- **Show HN: 自动数据经纪人选择退出** - 325 分，135 评论。来源: Hacker News | [链接](https://github.com/stephenlthorn/auto-identity-remove)

- **Show HN: Semble – 比 grep 少用 98% token 的代码搜索** - 444 分，150 评论。结合静态 Model2Vec 嵌入和 BM25。来源: Hacker News | [链接](https://github.com/MinishLab/semble)

---

📅 抓取时间: 2026-05-24 17:30
📡 数据源: 11/11 成功
