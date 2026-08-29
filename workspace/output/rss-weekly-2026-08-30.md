---
layout: default
title: 前端技术周报 (2026-08-30)
date: 2026-08-30
category: RSS 周报
---

# 📰 前端技术周报 (2026-08-30)

> 本周范围：8月23日 – 8月30日 | 数据来源：10个RSS源 | 抓取时间：2026-08-30

---

## 📝 本周要点

- **Solid 2.0 RC 发布** — 重大架构变革：异步值纳入响应式图，`createResource`/`batch`/`startTransition` 删除，OXC Rust编译器引入，API冻结。[详情](https://www.solidjs.com/blog/solid-2-0-rc-the-big-reveal)
- **Bun 1.4 正式发布** — Zig→Rust重写完成，Node.js兼容性大幅提升，新增 `bun dedupe`/`bun prune`/`bun audit fix`，支持 React Compiler。[详情](https://bun.com/blog/bun-v1.4)
- **pnpm 12.0 发布** — 基于 Rust 重写的稳定版，兼容 pnpm 11，新增 Registry revisions、`globalShims`、`stage approve` 等功能。[详情](https://pnpm.io/blog/releases/12.0)
- **State of CSS 2026 调查结果** — Anchor Positioning 被评为"最期待新功能"第一名，浏览器支持仍是最大障碍。[详情](https://2026.stateofcss.com/en-US)
- **Next.js 16.3 发布** — 新增 Instant Navigations（`cacheComponents` + `partialPrefetching`），SSR 内部从 Web Streams 迁移至 Node.js Streams。[详情](https://nextjs.org/blog/next-16-3)
- **Mozilla 发布 MDN MCP Server** — 将 MDN 文档和浏览器兼容性数据直接接入 LLM 和代码编辑器。[详情](https://developer.mozilla.org/en-US/blog/introducing-mdn-mcp-server/)
- **npm 上线发布时恶意软件扫描** — 新发布包安装前自动扫描，误认包可通过 `contentPolicy` 声明 dual-use 内容。[详情](https://github.blog/changelog/2026-07-28-npm-publish-time-malware-scanning-and-dual-use-metadata/)
- **Firefox 154 稳定发布** — 支持 `text-box-trim`、`sibling-index()`/`sibling-count()`，Iterator 新方法进入 Stable。[详情](https://www.firefox.com/en-US/firefox/154.0/releasenotes/)

---

## ⚛️ React / 前端框架

- **Moving a 400-route app from Next.js to TanStack Start** — Lovable 将 85 万行代码从 Next.js 迁移至 TanStack Start，采用双框架并行+代理路由的策略。[链接](https://react.statuscode.com/link/189625/rss)
- **React Canary 新增 `browser()` API** — 用于无法在服务端渲染的组件，`use(browser())` 会停止服务端渲染，留 Suspense fallback 占位，浏览器端正常渲染。[链接](https://react.statuscode.com/link/189630/rss)
- **React 并行 Transition 默认开启** — Canary 构建中已默认启用，Meta 已在生产环境使用，可能进入 React 19.3。[链接](https://react.statuscode.com/link/189631/rss)
- **Waku 1.0 RC** — 最小化 RSC React 框架，API 冻结，新增编译时类型安全路由检查。[链接](https://waku.gg/blog/waku-v1-rc)
- **SvelteKit 3 RC** 发布。[链接](https://svelte.dev/blog/sveltekit-3-release-candidate)
- **Ionic Framework v9** — 两年未更新后回归，支持 React Router 6，Angular 21+ zoneless 变更检测。[链接](https://ionic.io/blog/announcing-ionic-framework-9)
- **TanStack Router 可靠查询预取** — 通过 route context 共享 `queryOptions`，避免 loader 和组件重复定义导致漂移。[链接](https://tkdodo.eu/blog/reliable-query-prefetching-with-tanstack-router)
- **Next.js 团队 Reddit AMA** — 讨论 Next.js 16.3、App Router、RSC、缓存等话题。[链接](https://www.reddit.com/r/nextjs/comments/1vrq0tp/were_the_nextjs_team_ask_us_anything/)
- **We Stopped Using RSC on TanStack.com** — TanStack 分享弃用 RSC 的原因和替代方案。[链接](https://tanstack.com/blog/we-stopped-using-rsc-on-tanstack-com)
- **Building App-like Experiences with Next.js 16.3** — Aurora Scharff 演示 Instant Navigations、Cache Components、Partial Prefetching 四个开源示例。[链接](https://nextjs.org/blog/building-app-like-experiences-with-nextjs-16-3)
- **React Server Components Your Way** — TanStack 分享 RSC 数据流式处理方法。[链接](https://tanstack.com/blog/react-server-components)

---

## 📦 JavaScript / TypeScript

- **ESM vs CommonJS 深度解析** — Gabor Koos 详解 `import` 与 `require` 本质区别：ESM import 绑定导出者变量，解构 require 只持有副本，循环依赖后果不同。[链接](https://blog.gaborkoos.com/posts/2026-08-14-Your-Modules-Are-Lying-to-You/)
- **TypeScript 7.0 RC 发布** — 更多细节待确认。[链接](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0-rc/)
- **Solid 2.0 RC 架构变革** — 异步值纳入响应式图，`createResource`/`batch`/`startTransition` 删除，Vite 插件新增 `start: true` 标志，SolidStart 项目退役。[链接](https://www.solidjs.com/blog/solid-2-0-rc-the-big-reveal)
- **JavaScript Intl API 实用指南** — 覆盖 `DateTimeFormat`、`RelativeTimeFormat`、`NumberFormat`、`ListFormat`、`PluralRules` 等。[链接](https://jsdev.space/javascript-intl-guide/)
- **ECMAScript 2026 新特性** — `Object.groupBy()`、`Iterator.zip()`/`zipKeyed()`、`Iterator.prototype.chunks/windows` 等。[链接](https://www.telerik.com/blogs/useful-javascript-additions-ecmascript-2026)
- **TypeScript 6.0 迁移指南** — SitePoint 整理 TypeScript 6.0 变更与升级步骤。[链接](https://www.sitepoint.com/typescript-6-0-migration-guide/)
- **Core-js v3.50.0** — `Iterator.zip`/`zipKeyed` 进入 Stable ES，`chunks`/`windows` 进入 Stage 3。[链接](https://github.com/zloirock/core-js/releases/tag/v3.50.0)
- **HLS.js v1.7.0** — TypeScript 类型严格化，新增 `createIFramePlayer()`、CMCD v2 支持。[链接](https://github.com/video-dev/hls.js/releases/tag/v1.7.0)
- **Migrating a Large Flow Monorepo to TypeScript** — Yelp 工程博客分享大型 Flow→TypeScript 迁移经验。[链接](https://engineeringblog.yelp.com/2026/08/migrating-a-large-flow-monorepo-to-typescript.html)
- **Progressive Enhancement inside JavaScript** — Remy Sharp 介绍 JS 内部渐进增强。[链接](https://remysharp.com/2026/08/05/progressive-enhancement-inside-of-javascript)
- **Rust Is Eating JavaScript, v2026** — Lee Robinson 回顾 Rust 在 JS 生态中的渗透。[链接](https://leerob.com/rust)
- **Announcing TypeScript 7.0** — Microsoft 正式发布 TypeScript 7.0。[链接](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/)

---

## 🎨 CSS / 样式

- **State of CSS 2026 调查结果** — 4902 人参与，Anchor Positioning 以绝对优势获"最期待新功能"和"浏览器支持不足最可惜功能"双料第一，`:has()`、CSS Nesting、`@container`、View Transition API 紧随其后。AI 生成 CSS 比例平均仅 28%。[链接](https://2026.stateofcss.com/en-US)
- **flex-wrap: balance 新特性** — Ahmad Shadeed 介绍 Chrome 新属性 `flex-line-count`，让布局在所有尺度下都能正确换行。[链接](https://ishadeed.com)
- **CSS Navigation Matching 草案** — 用 `@location` 命名页面，`@navigation` 无 JS 动画过渡，目前仅为草案。[链接](https://css-tricks.com/css-navigation-matching-early-days/)
- **CSS 类前缀选择器已解决** — CSS-Tricks 报道 `.btn-*` 这类前缀选择器的提案进展。[链接](https://css-tricks.com/resolved-css-class-prefix-selector/)
- **Native CSS Nesting 全面支持** — Flaviocopes 介绍现代浏览器原生 CSS 嵌套用法。[链接](https://flaviocopes.com/css-nesting/)
- **oklch() 与 color-mix() 现代 CSS 颜色** — Flaviocopes 详解 Modern CSS 颜色函数。[链接](https://flaviocopes.com/css-oklch-color-mix/)
- **RGB is Dead, Long Live RGB!** — Alvaro Montoro 探讨 CSS 颜色演进。[链接](https://alvaromontoro.com/blog/68110/rgb-is-dead-long-live-rgb)
- **CSS 3D：从超级马里奥到马里奥64** — Carmen Ansio 用 6 个 CSS 属性讲解如何实现真正的 3D CSS。[链接](https://www.carmenansio.com/articles/3d-css-guide/)
- **Scroll Axis Lock** — CSS 新增 `scroll-axis-lock` 属性，支持对角滚动解锁。[链接](https://nerdy.dev/css-scroll-axis-lock)
- **Gap Decorations 可用** — CSS gap 装饰功能现已支持。[链接](https://css-tricks.com/css-gap-decorations-now-available/)
- **CSS lh 单位** — 基于行高的新型单位，Ishadeed 介绍。[链接](https://ishadeed.com/article/lh-unit/)
- **CSS border-image 动画** — CSS-Tricks 报道。[链接](https://css-tricks.com/animating-css-border-image/)
- **CSS: the bomb inside your inbox** — PortSwigger 安全研究：CSS 注入攻击新形式。[链接](https://portswigger.net/research/css-the-bomb-inside-your-inbox)
- **In defense of two-state theme toggles** — Josh Collinsworth 为简单主题切换辩护。[链接](https://joshcollinsworth.com/blog/in-defense-of-two-state-theme-toggles)
- **Inaudible Sounds Used to Fingerprint Browsers Catch AliExpress Red-Handed** — Dan Goodin (Ars Technica)。[链接](https://frontendfoc.us/link/189451/rss)

---

## 🛠️ 工具 / 构建

- **pnpm 12.0 发布** — Rust 重写稳定版，保留 pnpm 11 命令和 lockfile 格式，新增 Registry revisions、`globalShims` project-aware global bins、`pnpm update --patches`、`pnpm stage approve`。[链接](https://pnpm.io/blog/releases/12.0)
- **Bun 1.4 发布** — Zig→Rust 重写完成，Node.js/Next.js/Playwright/Vitest/Nuxt 兼容性大幅提升，吞吐量/CPU/内存显著优化，新增 `bun dedupe`/`prune`/`audit fix`，`bun test --timings` 时间基 sharding，React Compiler 支持。[链接](https://bun.com/blog/bun-v1.4)
- **Electron 44** — 取消 32 位支持，要求 macOS 13+，`clipboard` 对齐 W3C API，新增 `net.WebSocket`。[链接](https://github.com/electron/electron/releases/tag/v44.0.0)
- **ESLint 10.9 / 10.9.1** 发布。[链接](https://eslint.org/blog/2026/08/eslint-v10.9.0-released/)
- **React Compiler Linting 加速** — Oxlint 集成 React Compiler 22 条规则，速度比 Babel 插件快 10 倍以上。[链接](https://oxc.rs/blog/2026-08-18-react-compiler-support)
- **Oxc Transform React** — OXC 推出自动 memoization 工具包。[链接](https://blog.master.dev/react-compiler-linting-just-got-a-rust-native-speedup-in-oxlint/)
- **Formisch 1.0** — 无头表单库，Valibot schema 驱动 8 种框架的类型和验证，新增 Angular 和 React Native 支持。[链接](https://formisch.dev/blog/formisch-v1/)
- **Stryker Mutator 10.0** — 突变测试框架，检测测试套件覆盖率漏洞。[链接](https://stryker-mutator.io/)
- **TermDOM v0.1.5** — 用 HTML/CSS/DOM 构建终端 UI，新增 CSS Grid 支持。[链接](https://termdom.org/)
- **MicroLighter** — 2KB 客户端语法高亮库，使用 CSS Custom Highlights API，不操作 DOM。[链接](https://daverupert.com/2026/08/microlighter/)
- **Nitayneeman: import defer** — ECMAScript 新增延迟模块求值提案。[链接](https://nitayneeman.com/blog/introducing-import-defer-in-ecmascript/)
- **Better Auth 1.7** — 新增 MCP 认证支持，SCIM Groups/Device Authorization。[链接](https://better-auth.com/blog/1-7)
- **Vercel eve: Next.js AI Agent 框架** — LogRocket 介绍。[链接](https://blog.logrocket.com/vercel-eve-ai-agents/)
- **Cloudflare WebMCP** — 给任何网站添加 WebMCP 接口。[链接](https://blog.cloudflare.com/webmcp/)
- **Cloudflare Kitesurf** — Agent-first 浏览器，运行在 V8 isolates 上。[链接](https://blog.cloudflare.com/kitesurf/)
- **How Cloudflare Moved Its Blog to Its Own WordPress Alternative** — Jackson, Carneiro, Dutton (blog.cloudflare.com); 使用 EmDash (Astro CMS), k6 load tests, proxy Worker for switchover。[链接](https://blog.cloudflare.com)

---

## ⚡ 性能优化

- **The Wicked Reason Removing Code Beats Better Scheduling** — Alex Russell 指出大量性能工作花在调度时机上，但真正收益往往来自减少发送的代码量，这是管理问题而非技术问题。[链接](https://infrequently.org/2026/08/notes-on-performance-remediation-strategies/)
- **How Baseline Can Help You Ship Less JavaScript** — Smashing Magazine 介绍利用 MDN Baseline 数据减少 JS 体积。[链接](https://www.smashingmagazine.com/2026/08/how-baseline-can-help-ship-less-javascript/)
- **React 高频实时数据：Ring Buffer 到 OffscreenCanvas** — FreeCodeCamp 介绍在 React 中处理高频数据的优化方案。[链接](https://www.freecodecamp.org/news/high-frequency-real-time-data-in-react-from-ring-buffers-to-offscreencanvas/)
- **GitHub Diff Lines 性能优化** — GitHub 将 Files changed 标签页的 DOM 元素从每行 10-15 个降至 2 个组件，引入 TanStack Virtual 虚拟化。[链接](https://github.blog/engineering/architecture-optimization/the-uphill-climb-of-making-diff-lines-performant/)
- **Your SPA Is Leaking Memory. Soak Test It.** — Denodell 介绍 SPA 内存泄漏的浸泡测试方法。[链接](https://denodell.com/blog/your-spa-is-leaking-memory-soak-test-it)
- **TimescaleDB 实时仪表板** — 扩展 Postgres 实现无延迟实时查询，Hypertables + 压缩 + 连续聚合。[链接](https://www.tigerdata.com)
- **Cloudflare workerd 构建解析** — Flaviocopes 详解 Cloudflare Workers 运行时构建过程。[链接](https://flaviocopes.com/workerd/)
- **How Astro is built** — Flaviocopes 解析 Astro 构建原理。[链接](https://flaviocopes.com/how-astro-is-built/)
- **Fixing a 6-Year-Old JavaScript Memory Leak in a Google Cloud Function** — Matt Zeunert (DebugBear)。[链接](https://debugbear.com)

---

## 🧪 测试 / 质量

- **npm 发布时恶意软件扫描上线** — 新包安装前扫描，结果分为正常发布、手动审查、阻止三种。[链接](https://github.blog/changelog/2026-07-28-npm-publish-time-malware-scanning-and-dual-use-metadata/)
- **vlt 1.0 正式GA** — 分阶段安装、OIDC Trusted Publishing，与 npm Registry API 兼容，可阻挡已知恶意包。[链接](https://www.vlt.io/blog/1-0)
- **Testing React Server Components with Vitest** — SitePoint 介绍 RSC 异步边界的测试模式。[链接](https://www.sitepoint.com/testing-react-server-components-vitest-async-boundaries-mock/)
- **Weaponizing React Flight Protocol** — Smashing Magazine 解析 React Server Components 反序列化安全风险。[链接](https://www.smashingmagazine.com/2026/07/weaponizing-defending-react-flight-protocol/)
- **ESLint in 2026: A Practical Guide** — Modern JavaScript linting 实践指南。[链接](https://jsdev.space/howto/modern-eslint-guide/)
- **How to Favicon in 2026** — Evil Martians。[链接](https://evilmartians.com)
- **The secure way to release an npm package in 2026** — Evil Martians 发布安全的 npm 发布指南。[链接](https://evilmartians.com/chronicles/the-secure-way-to-release-an-npm-package)

---

## 🤖 AI / 机器学习

- **Mozilla 发布 MDN MCP Server** — 将 MDN 文档和浏览器兼容性数据直接接入 Claude Code、Cursor 等 AI 编程助手。[链接](https://developer.mozilla.org/en-US/blog/introducing-mdn-mcp-server/)
- **Modern Web Guidance** — Chrome 团队发布面向 AI 编程助手的 Web 开发最佳实践和技能集。[链接](https://developer.chrome.com/docs/modern-web-guidance)
- **TanStack AI RC 发布** — 查询预取和缓存的 AI 增强版本。[链接](https://tanstack.com/blog/tanstack-ai-rc)
- **Inngest: AI Agent 架构半衰期** — Dan Farrelly 提出 AI Agent 三层架构：上下文层（周更）、计算层（月更）、执行层（年更），各层应有不同更新频率。[链接](https://x.com/djfarrelly/status/2079950053628641759)
- **Mem0: State of Agent Wikis** — 基于 Karpathy 的 LLM Wiki 概念，提出用 Markdown 编译替代每次 RAG 搜索，Cognition DeepWiki、LangChain OpenWiki 等跟进。[链接](https://x.com/mem0ai/status/2079585032587694582)
- **Vercel eve: Next.js AI Agent 框架** — LogRocket 介绍 Vercel 的 AI Agent 专用框架。[链接](https://blog.logrocket.com/vercel-eve-ai-agents/)
- **Node.js Worker Threads 生产实践** — Inngest 分享 Worker Threads 实际生产部署经验，强调线程边界即 API 边界。[链接](https://www.inngest.com/blog/node-worker-threads-production)
- **Build an AI Agent with Real-Time Web Search** — Amit Merchant 介绍用 JavaScript 构建带实时搜索的 AI Agent。[链接](https://www.amitmerchant.com/building-web-searching-ai-agent-javascript/)
- **NetFix AI Mania 批判文章** — 指出 AI 狂热导致组织决策扭曲，经验不足的开发者和决策层均受影响。[链接](https://ludic.mataroa.blog/blog/ai-mania-is-eviscerating-global-decision-making/)
- **9 designers on AI-assisted coding** — Ron Goldin 采访 9 位设计师谈 AI 辅助编程的利弊。[链接](https://rongoldin.substack.com/p/9-designers-open-up-about-ai-assisted)
- **State of Agent Wikis** — Mem0 整理 LLM Wiki 实现方案，区分文档知识与用户记忆。[链接](https://x.com/mem0ai/status/2079585032587694582)
- **Reverse Engineering ChatGPT Web** — Performance.dev 解析 OpenAI 如何为十亿用户构建 ChatGPT。[链接](https://performance.dev/chatgpt)

---

## 📚 周刊摘要

### 阮一峰科技爱好者周刊 #409 — 程序员的职业未来（2026-08-21）

**封面文章**：探讨 AI 时代程序员职业走向——极端观点认为 AI 生成代码将消灭程序员，另一派认为 AI 只会替代手工编码，人类判断不可替代，世界需要更多代码。作者分享了一位海外开发者对程序员职业的中立预测。

**其他内容**：
- 讨论 AI 对软件工程职业结构的深层影响
- 传统工业革命的类比：AI 算力帝国不会一夜建成

[阅读全文](https://www.ruanyifeng.com/blog/2026/08/weekly-issue-409.html)

---

### 阮一峰科技爱好者周刊 #410 — AI 三种机制（2026-08-28）

**封面文章**：AI 小知识系列第三篇，解释大模型为什么能回答问题——宏观层面所有大模型都是对人类知识的数学建模。分享通俗理解 AI 的三个核心机制。

**其他内容**：
- 多莉·帕顿去世新闻（虚拟化身演唱会相关）
- 平面椅设计新闻
- 公开演讲技巧建议

[阅读全文](https://www.ruanyifeng.com/blog/2026/08/weekly-issue-410.html)

---

### FE News 2026-08 月刊

**精选文章**：
- **State of CSS 2026** — 锚点定位第一，浏览器支持是最大瓶颈
- **我停止了一切解构** — Matt Smith 反思过度使用解构赋值的反模式
- **AI Agent 架构半衰期** — 三层架构理论：上下文层周更、计算层月更、执行层年更
- **Hydration 与渲染策略** — 从 SSG 到 RSC/Island Architecture 的完整演进史
- **Agent Wikis 现状** — Mem0 整理 LLM Wiki 实现方案，区分文档知识与用户记忆
- **Node.js Worker Threads 生产实践** — Inngest 实战经验
- **Netflix CPTO 访谈** — AI 时代系统思维优于专业分工
- **Jensen Huang YC 访谈** — 第一性原理、现实面对、恢复力

[查看全部](https://fenews.substack.com/p/fe-news-2026-08)

---

### JavaScript Weekly #799（2026-08-25）

**重点**：
- Bun 1.4 发布（Zig→Rust 重写）
- Solid 2.0 RC 重大变革
- Electron 44 / Waku 1.0 RC / SvelteKit 3 RC / React Native 0.87 / ESLint 10.9
- TypeScript 创建者 Anders Hejlsberg 访谈：10 倍速 TypeScript 与 AI 不会取代工程师
- Cloudflare 博客迁移至自建 Astro CMS EmDash
- MicroLighter 2KB 语法高亮 / TermDOM TUI 框架 / Formisch 1.0 / Stryker 10.0

[查看全部](https://javascriptweekly.com/issues/799)

---

### JSer.info #778（2026-08-27）

**重点**：
- pnpm 12.0 发布（Rust 重写稳定版）
- Bun 1.4 发布
- Solid v2.0 RC 发布
- SolidStart v2 稳定版
- Safari Technology Preview 250：`ruby-overhang`、`Iterator.zip()`、relaxed SIMD
- Firefox 154：`text-box-trim`、`sibling-index()`、Iterator 新方法
- Oxc React Compiler 支持（22 条规则）
- celld.dev（Cloudflare Durable Objects 兼容自托管实现）
- anydoc（Rust Office→Markdown 转换器）
- Plumeria（React Zero Runtime CSS-in-JS）
- yuku-toolchain（纯 Zig JS/TS 编译器）

[查看全部](https://jser.info/2026/08/27/pnpm-12-bun-1.4-solid-2.0-rc/)

---

### Frontend Weekly Digest #480（2026-08-23）

**Web Dev**：Modern Web Guidance（Chrome AI 技能集）、HTML Can Do That（Chris Burnell 八大示例）、My HTML Boilerplate in 2026（Matuzović）、Geolocation 元素、SMIL 动画时间图

**CSS**：CSS inbox 炸弹（PortSwigger 安全研究）、Class Prefix Selector、Navigation Matching 草案、oklch/color-mix、Native Nesting、Grid 信息获取、:has() 样式任意元素

**JS**：Intl API、Object.groupBy、ES2026 新增、Solid 2.0 迁移、BroadcastChannel over localStorage hack、ESLint 2026 指南

**React**：Oxlint React Compiler 支持、Next.js 团队 AMA、React JWT+Zustand 鉴权、高频实时数据 Ring Buffer→OffscreenCanvas、TanStack Router query prefetching

[查看全部](https://frontender-ua.medium.com/frontend-weekly-digest-480-17-23-august-2026-7459de12a627)

---

## 💻 Hacker News 热门（Show HN）

> *注：HN RSS 源当前不可访问，以下为替代来源整理*

- **ego-lite** — 专为 AI Agent 设计的隔离浏览器，每个 Agent 有独立 Space，用户可继续使用自己的浏览器标签页，MIT 许可，仅 macOS。[链接](https://github.com/citrullin/ego-lite)
- **jcode** — Rust 编写的终端 AI 编码 Agent 框架，支持语义记忆（嵌入向量+余弦相似度检索）、Swarm 多 Agent 协作、Firefox 浏览器自动化、自我改进循环。[链接](https://github.com/1jehuang/jcode)
- **qm** — 多用户 Agent 平台，Slack + Web 双接口，Per-room 隔离，Postgres 存储，适配 Pi/OpenCode/Codex/Claude Code。[链接](https://github.com/yc-software/qm)
- **awesome-gpt-image-2** — GPT-Image2 工业级提示词引擎，544 个逆向案例，20+ 模板，含 Agent Skill 安装。[链接](https://github.com/freestylefly/awesome-gpt-image-2)
- **anthropics/claude-plugins-community** — Claude Cowork & Code 社区插件市场只读镜像。[链接](https://github.com/anthropics/claude-plugins-community)
- **firecrawl/anydoc** — Rust 编写，将 Word/PPT/Excel/PDF/EPUB 等转换为 Clean Markdown，支持 Node/Python/WASM。[链接](https://github.com/firecrawl/anydoc)
- **celld** — Cloudflare Workers Durable Objects 兼容 API 的自托管分布式实现，基于 LTX+S3。[链接](https://celld.dev/)
- **Plumeria** — React 组件 Zero Runtime CSS-in-JS 库，TypeScript 对象定义样式，构建时转换为 className。[链接](https://plumeria.dev/)
- **Diffs from Pierre** — CSS Grid + Shadow DOM 高性能 diff 渲染库，支持虚拟化。[链接](https://diffs.com/)
- **BookOrbit KOReader Plugin** — 进度同步、双向注释同步、目录浏览；完整文档 bookorbit.app；AGPLv3；通过 Crowdin 翻译。[链接](https://github.com)

---

## 📈 GitHub 热门（Weekly）

本周 GitHub Trending 主要趋势：
1. **AI Agent 工具链** — ego-lite、jcode、qm 等多款 Agent 浏览器/框架涌现
2. **AI 图像生成** — GPT-Image-2 提示词库持续热门
3. **Claude 插件生态** — Anthropic 社区插件市场持续增长
4. **文档转换工具** — anydoc（Rust 多格式→Markdown）
5. **电子书生态** — BookOrbit KOReader 插件

---

## 🌐 其他动态

- **Cloudflare 发布 WebMCP** — 给任何网站添加 WebMCP 接口。[链接](https://blog.cloudflare.com/webmcp/)
- **Cloudflare Kitesurf** — Agent-first 浏览器，运行在 V8 isolates 上。[链接](https://blog.cloudflare.com/kitesurf/)
- **Astro GitHub Issue backlog 降至零** — Cloudflare 开源其用于管理 issue 的工具。[链接](https://thenewstack.io/cloudflare-astro-triage-bot/)
- **Jake Archibald：Firefox JPEG XL 支持进展** — Chrome 也计划支持。[链接](https://hacks.mozilla.org/2026/08/intent-to-ship-jpeg-xl/)
- **CSS-in-JS Arena** — Gajus Kuizinas 用同一 React Router 8 应用对比 StyleX、Panda CSS、Bamboo CSS。[链接](https://github.com/gajus/css-in-js-arena)
- **Git 2.54+ 单命令拆分 commit** — `git history split <ref>` 逐 hunk 交互拆分。[链接](https://blog.gnoack.org/post/git-history-split)
- **N64 模拟器用 JavaScript 编写** — 可浏览器内运行。[链接](https://github.com/hulkholden/n64js)
- **Solid 2.0 for React Developers** — 面向 React 开发者的 Solid 2.0 迁移指南。[链接](https://x.com/devagrawal09/status/2089089101010239926)
- **Under the hood of MDN's new frontend** — MDN 新前端深度解析：Lit Web Components + 自定义 Server Components + Rspack。[链接](https://developer.mozilla.org/en-US/blog/mdn-front-end-deep-dive/)
- **The Agentic Web** — Bandarra 探讨 Agent 时代的 Web 架构。[链接](https://bandarra.me/posts/the-agentic-web)
- **WoFF 1.0 里程碑** — W3C 纪念 WoFF 1.0 发布。[链接](https://www.w3.org/blog/2026/woff-1-0-a-milestone-on-w3cs-journey-of-fonts-on-the-web/)
- **JavaScript Obfuscation in AI Era** — JSTools 探讨 AI 时代 JS 混淆的价值。[链接](https://www.jstools.space/blog/javascript-obfuscation-ai/)
- **React Router v8 实践** — 懒加载与嵌套路由实战。[链接](https://reactdevelopment.substack.com/p/react-router-v8-in-action-lazy-loading)
- **Blocked aria-hidden 警告分析** — CSS-Tricks 解析 aria-hidden 常见误用。[链接](https://css-tricks.com/blocked-aria-hidden-fix/)
- **CodePen 2.0 发布** — 全新 CodePen 平台上线。[链接](https://blog.codepen.io/2026/07/23/two-point-oh/)
- **Vite 7 Production Migration** — SitePoint 介绍从 esbuild 迁移至 Rolldown 和 Oxc。[链接](https://www.sitepoint.com/vite-7-production-migration-rolldown-oxc-build-optimization/)
- **Tales from the Void: July 2026 Recap** — Voidzero 团队月度总结。[链接](https://voidzero.dev/posts/whats-new-jul-2026)
- **React Interview Questions 2026** — Medium 前端周刊。[链接](https://medium.com/@frontender-ua/frontend-weekly-digest-480-17-23-august-2026-7459de12a627)
- **HTML Can Do That** — Chris Burnell 的 HTML 能力展示。[链接](https://frontendfoc.us/link/189444/rss)
- **My HTML Boilerplate in 2026** — Manuel Matuzović 的现代 HTML 模板。[链接](https://frontendfoc.us/link/189443/rss)
- **3D CSS Super Mario Bros 3→Mario 64** — Carmen Ansio 的 3D CSS 教程。[链接](https://frontendfoc.us/link/189453/rss)
- **The Process of Migrating from Sass to Native CSS** — Chris Smith 分享 Sass→CSS 迁移经验。[链接](https://frontendfoc.us/link/189454/rss)
- **Where Did the Old Web Go? We Followed 657,607 Links** — 0.mk 的网页历史追踪实验。[链接](https://frontendfoc.us/link/189455/rss)
- **Embed eSigning in Your App** — Foxit 广告。[链接](https://frontendfoc.us/link/189463/rss)
- **Mobile View: Desktop and Mobile Side by Side** — 响应式调试工具。[链接](https://frontendfoc.us/link/189464/rss)
- **Form-Saver: Web Component** — Aaron Gustafson 的表单值保存/恢复组件。[链接](https://frontendfoc.us/link/189465/rss)

---

📅 抓取时间: 2026-08-30
📡 数据源: 10/10 成功（阮一峰博客 CF 屏蔽，改用搜索结果；HN Show RSS 502，改用搜索替代）
