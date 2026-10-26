---
layout: default
title: 前端技术周报 (2026-10-26)
date: 2026-10-26
category: RSS 周报
---

## 📰 前端技术周报 (2026-10-26)

### 📝 本周要点

- **Deno 被 Cloudflare 收购，将并入 workerd** — Deno 官方宣布加入 Cloudflare，Deno 运行时将在一年后结束，Deno Deploy 6个月后关闭，JSR 迁移至 Cloudflare。Ryan Dahl 坦言："为什么重新实现 Node.js？它已经能用了。" [来源: Deno Blog](https://deno.com/blog/cloudflare)
- **TanStack Start 1.0 正式发布** — 经过一年 RC 期，TanStack Start 正式稳定，基于 TanStack Router 的全栈 React/Solid 框架，性能 benchmarks 显示动态请求处理比 Next.js 16.4 快 2.9-8.6 倍 [来源: TanStack Blog](https://tanstack.com/blog/tanstack-start-1-0)
- **tsrs：TypeScript 7 编译器的 Rust 端口** — Cloudflare 和 VoidZero 合作打造，据称速度可达 TypeScript 7.0 的 8 倍，已进入 Oxc 项目，支持 WebAssembly [来源: Cloudflare Blog](https://blog.cloudflare.com/typescript-rust-port/)
- **Next.js 紧急修复两个严重 RCE 漏洞** — 一个与 React Server Components 相关，影响所有 RSC 用户；另一个在图片优化器的 SVG 处理中。需立即升级至 16.4.1 或 15.5.28 [来源: Next.js Blog](https://nextjs.org/blog/nextjs-security-update-october-14-2026)
- **MDN 放弃 React，改用 Web Components 重建前端** — MDN 官方博客宣布前端全面转向 Web Components [来源: JavaScript Weekly #770](https://javascriptweekly.com/issues/770)
- **PHP2Shell：AI 发现影响 70% 互联网的关键 RCE 漏洞** — Wiz 团队利用 AI 在 PHP 中发现了严重影响互联网的远程代码执行漏洞 [来源: Wiz Blog](https://www.wiz.io/blog/php2shell-php-rce)

---

### ⚛️ React / 前端框架

- **TanStack Start 1.0 稳定发布** — 提供 SSR/流式渲染、类型化服务器函数 `createServerFn`、环境感知的 `createIsomorphicFn`。官方提供从 Next.js 和 RC 版本的迁移指南 [来源: TanStack](https://tanstack.com/blog/tanstack-start-1-0) | [链接](https://react.statuscode.com/link/191882/rss)
- **React 19.3 正式释放** — `<ViewTransition>` 和 Fragment Refs 变稳定；新增 `browser()` API 使组件仅在浏览器中渲染，支持 Trusted Types；Server Components 中可直接渲染 `<Context>` [来源: React Blog](https://react.dev/blog/2026/09/09/react-19-3) | [链接](https://jser.info/2026/09/29/react-19-3-pnpm-12-4-vite-plus-1-0/)
- **Remix 3.0 稳定版发布** — 完全重构，不再需要 React [来源: Remix Blog](https://github.com/remix-run/remix/releases/tag/remix%403.0.0) | [链接](https://javascriptweekly.com/issues/805)
- **Preact 11 发布** — 6 年后迎来重大更新：ESM-only、Hydration 2.0、自动 ref 转发，`render()` 第三个参数已移除 [来源: Preact Blog](https://preactjs.com/blog/preact-11/) | [链接](https://javascriptweekly.com/issues/805)
- **SvelteKit 3 发布** — 官方应用框架的清理/精化版本，远程函数仍为实验性功能，提供 `sv migrate` 迁移工具 [来源: Svelte Blog](https://svelte.dev/blog/sveltekit-3-is-here) | [链接](https://javascriptweekly.com/issues/807)
- **Nuxt 4.6** — 迈向服务器无关化，纯 Vite server 构建成为实验性选项，内置 sessions、Vue Vapor 支持，新的 Nuxt CLI 4.0 [来源: Nuxt Blog](https://nuxt.com/blog/v4-6) | [链接](https://javascriptweekly.com/issues/805)
- **Owner 网站从 Next.js 迁移到 Astro** — 10,000+ 餐厅网站迁移后，菜单页 p75 LCP 从 5.4s 降至 0.7s，React 保留为交互式 Islands [来源: Owner Blog](https://building.owner.com) | [链接](https://react.statuscode.com/link/191899/rss)
- **Atelier UI** — 在 React UI 库中混合 WebGL 和 DOM [来源: Codrops](https://tympanus.net/codrops/2026/10/21/atelier-ui-webgl-dom/) | [链接](https://frontender-ua.medium.com/frontend-weekly-digest-489-19-25-october-2026-c4f2a5fbb10d)

---

### 📦 JavaScript / TypeScript

- **tsrs：TypeScript 的 Rust 端口** — Cloudflare × VoidZero 合作，最高 8 倍于 TS 7.0 的速度，使用 `npx tsrs` 即可体验，已进入 Oxc 生态 [来源: Cloudflare Blog](https://blog.cloudflare.com/typescript-rust-port/) | [链接](https://javascriptweekly.com/issues/807)
- **Bun v1.4.3 发布** — 新增内置 TypeScript 类型检查器 `bun check`（基于 TypeScript 7），性能提升 3-6 倍；支持 `--disallow-code-generation-from-strings` 安全选项 [来源: Bun Blog](https://bun.com/blog/bun-v1.4.3) | [链接](https://jser.info/2026/10/16/cloudflaredeno-tanstack-start-1.0-bun-1.4.3-panda-css-2.0/)
- **TypeScript 7.1 Beta 发布** — 新增程序化 API，类型检查 MUI 文档速度提升 1.9 倍，内存减半 [来源: MSFT DevBlogs](https://devblogs.microsoft.com/typescript/announcing-typescript-7-1-beta/) | [链接](https://javascriptweekly.com/issues/807)
- **Node.js v26.12.0 (Current) 发布** — 现可同步加载大多数 ES 模块，配置文件中 stable；v24.22.0 (LTS) 新增 `util.throttle` 和 `util.debounce` [来源: Node.js Blog](https://nodejs.org/en/blog/release/v26.12.0) | [链接](https://jser.info/2026/10/16/cloudflaredeno-tanstack-start-1.0-bun-1.4.3-panda-css-2.0/)
- **Express 5.3.0 发布** — 修复 5 个 CVE 安全漏洞（`qs`、`proxy-addr`、`body-parser` 依赖更新）[来源: GitHub](https://github.com/expressjs/express/releases/tag/v5.3.0)
- **pnpm 12.10 / 12.12** — 新增 `autoDedupe` 依赖去重、`pnpm add --save-types`、Catalogs 支持 `file:`/`link:` [来源: pnpm Blog](https://pnpm.io/blog/releases/12.12.0)
- **WebSockets 性能对比：Node.js 26 vs Bun vs Deno (2026)** — Daniel Lemire 用 C 基准测试，Node 26 延迟接近 C，领先 Bun 和 Deno [来源: Lemire Blog](https://lemire.me/blog/2026/10/10/websocket-servers-in-javascript-node-js-bun-and-deno-in-2026/) | [链接](https://javascriptweekly.com/issues/806)

---

### 🎨 CSS / 样式

- **CSS random() 函数的趣味应用** — 用 `random()` 创建不完美、有机的视觉风格 [来源: Smashing Magazine](https://www.smashingmagazine.com/2026/10/embracing-playful-imperfection-css-random-function/) | [链接](https://frontender-ua.medium.com/frontend-weekly-digest-489-19-25-october-2026-c4f2a5fbb10d)
- **CSS Grid Lanes 原生 Masonry 布局** — 无需 JavaScript 的原生 Masonry 布局方案 [来源: Piccalilli](https://piccalil.li/blog/native-masonry-layouts-with-css-grid-lanes/) | [链接](https://frontender-ua.medium.com/frontend-weekly-digest-489-19-25-october-2026-c4f2a5fbb10d)
- **Interop 2027 的 Top 10 CSS 特性预测** — Josh Comeau 的年度 CSS 展望 [来源: Josh W. Comeau](https://www.joshwcomeau.com/css/interop-2027/) | [链接](https://frontender-ua.medium.com/frontend-weekly-digest-489-19-25-october-2026-c4f2a5fbb10d)
- **OKLCH + CSS 相对颜色函数** — 从基础色生成配色变体 [来源: Ben Frain](https://benfrain.com/colour-variants-from-base-colours-with-oklch-css-relative-color-and-css-functions/)
- **`calc-size()` 让背景图案高度自适应** — 新的 CSS 尺寸计算函数 [来源: Isotope](https://ishadeed.com/article/fit-height-background-pattern-calc-size/) | [链接](https://frontender-ua.medium.com/frontend-weekly-digest-488-12-18-october-2026-4d1ff3be8f89)
- **Panda CSS 2.0 发布** — ESM-only，需要 Node.js 22+；编译器用 Rust/Oxc 重写；新增 `viewTransition()`/`positionTry()` 等函数；新增 `panda doctor`/`panda analyze` 诊断工具 [来源: Panda CSS Blog](https://panda-css.com/blog/panda-css-v2) | [链接](https://jser.info/2026/10/16/cloudflaredeno-tanstack-start-1.0-bun-1.4.3-panda-css-2.0/)
- **Bootstrap 6 Alpha** — 首个重大更新自 2021 年，全面转向现代 CSS，JS 插件 ESM-only [来源: Bootstrap Blog](https://blog.getbootstrap.com/2026/10/08/bootstrap-6-alpha/)

---

### 🛠 工具 / 构建

- **ViteConf 2026 完整回放（10 小时）** — Evan You 主题演讲探讨 Agent 时代的工具链；Vitest 5 更新；Oxc 更快解析器；Void（全栈 SDK）开源 [来源: YouTube](https://www.youtube.com/watch?v=PfyIEgLzNYI) | [链接](https://javascriptweekly.com/issues/807)
- **Lightpanda 1.0** — 用 Zig 从零编写的无头浏览器，内存仅约 35MB，支持 Puppeteer/Playwright 驱动和原生 JavaScript 脚本 [来源: Lightpanda Blog](https://lightpanda.io/blog/posts/lightpanda-1-0) | [链接](https://javascriptweekly.com/issues/807)
- **Effect 4.0** — 核心库重新构建，体积缩小 5 倍，并发任务内存使用减少 86% [来源: Effect Website](https://effect.website/blog/releases/effect/40) | [链接](https://javascriptweekly.com/issues/807)
- **TanStack Charts 1.0** — 声明式、类型安全的图表库，支持 SVG/Canvas 渲染，无需框架绑定 [来源: TanStack](https://tanstack.com/blog/tanstack-charts-1-0)
- **Qwik 2.0 RC** — 可恢复框架的新里程碑版本 [来源: Qwik Blog](https://next.qwik.dev/blog/qwik-2-rc/)
- **Ink 8.0** — TUI 渲染器，现在需要 React 19.3，新增滚动偏移以构建可滚动的编码代理 UI [来源: GitHub](https://github.com/vadimdemedes/ink/releases/tag/v8.0.0)
- **ESLint 10.13** — 持续迭代的新版本 [来源: ESLint Blog](https://eslint.org/blog/2026/10/eslint-v10.13.0-released/)
- **H3 v2** — UnJS HTTP 框架的重大更新 [来源: H3 Blog](https://h3.unjs.io)
- **Maplair 4.0（Leaflet 分叉）** — 功能丰富的树摇可删 Leaflet 分叉，新增旋转、全屏、搜索、热力图等功能 [来源: Maplair](https://maplair.org/2026/10/19/maplair-4.0.0.html)

---

### ⚡ 性能优化

- **Owner.com 从 Next.js 迁移至 Astro + Cloudflare Workers** — 10,000+ 站点迁移，p75 LCP 5.4s → 0.7s，React 保留为交互式 Islands [来源: Owner Blog](https://building.owner.com) | [链接](https://react.statuscode.com/link/191899/rss)
- **Recraft 编辑器性能优化** — 提前加载 9MB WebAssembly 模块，使编辑器性能提升 17%，解决 React 树中 Suspense 导致的模块下载等待问题 [来源: Recraft Blog](https://react.statuscode.com/link/191904/rss)
- **Netlify Edge Function 延迟降低 5 倍** — 从 V8 Isolates 迁移至 Unikraft MicroVMs [来源: Netlify Blog](https://www.netlify.com/blog/edge-functions-firecracker-microvms/)
- **Booking.com 将 Node.js 服务成本降低 38%** — 从 PM2 迁移至 Platformatic Worker Threads，重新设计负载均衡和 worker 配置 [来源: Booking.com Dev Blog](https://medium.com/booking-com-development/node-js-at-scale-rebalanced-how-we-cut-cost-by-38-62ce247a3002)

---

### 🧪 测试 / 质量

- **Miro 将 70,000 个测试从 Jest 迁移至 Vitest** — 在 800 个包的 monorepo 中，两个月完成迁移，主要由 AI 代理完成繁琐工作 [来源: Miro Engineering](https://nothing-else.blog/blog/we-migrated-70000-tests-from-jest-to-vitest-yes-in-2-months) | [链接](https://javascriptweekly.com/issues/807)
- **Zod 3 → 4.5 迁移** — 在日均 1 亿次解析场景下，Worker CPU 使用降低三分之一 [来源: Trigger.dev Blog](https://trigger.dev/blog/zod-4-got-rid-of-a-bunch-of-cpus-for-us)
- **Testing AI-Generated Code：Lint 模式，测试决策** — 结构化 lint 规则和共享 harness 胜过在每个组件旁写测试 [来源: Robin Wieruch](https://react.statuscode.com/link/191902/rss)
- **QUnit 3.0.0** — 原生 ESM 发行，删除 Node.js 16 以下/PhantomJS/AMD 支持，默认测试超时改为 3 秒 [来源: GitHub](https://github.com/qunitjs/qunit/releases/tag/3.0.0)

---

### 🤖 AI / 机器学习

- **REA：逆向工程工具（20万+ GitHub stars）** — 用 AI 从二进制文件逆向重构软件，可复刻原始应用行为 [来源: GitHub](https://github.com/morluto/rea) | [链接](https://mshibanami.github.io/GitHubTrendingRSS/weekly/all.xml)
- **Cloudflare Security Audit Skill** — 六阶段结构化安全审计 coding-agent skill，来自 Cloudflare 漏洞发现系统的单仓起点 [来源: GitHub](https://github.com/cloudflare/security-audit-skill)
- **ts-rust：AI 生成的 TypeScript 7 编译器 Rust 移植** — Theo Browne 用 AI agents 编写，实验性项目，已可运行 [来源: GitHub](https://github.com/pingdotgg/ts-rust)
- **Claude.ai 性能提升 3 倍** — Anthropic 在两周内将 claude.ai 提速 3x [来源: Claude Blog](https://claude.dev/blog/how-we-made-claude-ai-faster/)
- **OpenCode 2.0** — 基于 Bun 的开源编码代理，支持后台子代理、code mode（MCP 工具调用）、vanilla JS 和 Effect 客户端 [来源: Anomaly](https://anoma.ly/notes/opencode-2-0/)
- **Jev 决策模型** — 返回浮点概率而非文本，适用于是非题、选择题和评分场景，浏览器插件可实现语义查找和网页质量评分 [来源: 阮一峰周刊 #414](https://www.ruanyifeng.com/blog/2026/10/weekly-issue-414.html)
- **SynthID 检测器** — 谷歌官方推出的 AI 生成内容识别工具，上传文件即可检测是否含 SynthID [来源: SynthID](https://synthid.com/)

---

### 📚 周刊摘要

#### 阮一峰科技爱好者周刊 #415（2026-10-16）

**封面：3D 版《看不见的城市》** — 用 GPT-6 Astra 和 Claude Opus 5.5 为卡尔维诺名著中的 55 个城市建立可视化 3D 版本。Claude Opus 5.5 的实现远胜于 GPT-6 Astra，忠实还原了原著意境。

**重点文章：**
- **Deno 项目即将结束** — Ryan Dahl 承认 Deno 被 Node.js 兼容性引力束缚，"为什么重新实现 Node.js？它已经能用了" [链接](https://deno.com/blog/cloudflare)
- **我如何用 600 美元训练出一个 Jev 式决策模型** — 在 Qwen3.5 0.8B 和 4B 上微调，让模型在 Mac 本机替代用户操作电脑 [链接](https://deskmind.dev/zh/blog/launch/)
- **AMD 处理器两年内速度提升 50%** — Ryzen 7 系列性能分析 [链接](https://lemire.me/blog/2026/09/18/how-did-amd-ryzen-get-50-faster-in-two-years/)
- **为什么没有 Linux 手机** — SOC 集成度不足是核心原因 [链接](https://amosbbatto.wordpress.com/2026/10/05/linux-phones-alternative/)
- **让 AI 生成的网页看起来像设计师作品** — vibe coding 的视觉优化技巧 [链接](https://railcode.dev/blog/vibe-coded-website)

**工具推荐：**
- **REA** — GitHub 20万星，AI 逆向工程工具，从二进制重新实现软件 [链接](https://github.com/morluto/rea)
- **SynthID 检测器** — 谷歌官方 AI 内容检测工具 [链接](https://synthid.com/)
- **ts-rust** — AI 实现的 Rust 版 TypeScript 编译器 [链接](https://github.com/pingdotgg/ts-rust)
- **Doory** — 浏览器内的开源平面设计工具，开源 Canva 替代品 [链接](https://github.com/shaongitbd/doory)
- **HeadOrbit** — 通过 AirPods 运动传感器控制 Mac，无需摄像头 [链接](https://github.com/Cogria-AI/HeadOrbit)
- **qrypt** — 将网盘挂载为本地文件夹的跨平台命令行工具 [链接](https://github.com/yinzhenyu-su/qrypt)
- **bg2x** — 浏览器本地运行的 AI 图像超分辨率工具，最高放大 4 倍 [链接](https://github.com/isixe/bg2x)
- **Droidline** — 扫码配对操作安卓手机的开源工具，无需 USB 调试 [链接](https://github.com/KnifeLemon/Droidline)

#### JavaScript Weekly #807（2026-10-20）

- **tsrs：TypeScript 的 Rust 端口**（见上）
- **Denos 的遗产：竞争推动 JavaScript 前进** — Darcy Clarke 论述 Deno 和 Bun 如何促使 Node.js 和 npm 采纳最佳实践 [来源: vlt.io](https://www.vlt.io/blog/competition-keeps-javascript-moving)
- **JavaScript 代码经过格式化后会变成另一个程序？** — 37+ 种 JS 处理器间的分歧问题，格式化可能改变程序逻辑 [来源: TrustSig](https://trustsig.eu/blog/javascript-divergence/)
- **如果你不写 Web Components，它们还有未来吗？** — Nolan Lawson 的思考性文章 [来源: Nolan Lawson](https://nolanlawson.com/2026/10/19/do-web-components-have-a-future-if-nobody-is-writing-them/)
- **Leaflet 创作者发布更新** — 计划推出 Leaflet 2.0 [来源: GitHub Issue](https://github.com/Leaflet/Leaflet/issues/10435)

#### JSer.info #781（2026-10-16）

- Cloudflare 收购 Deno 详情，Deno Deploy 6个月后关闭，JSR 迁移至 Cloudflare
- TanStack Start 1.0 稳定发布
- Bun 1.4.3：`bun check` TypeScript 类型检查
- Panda CSS 2.0：Rust/Oxc 编译器重写，ESM-only
- **Preact 11**：ESM-only、Hydration 2.0、自动 ref 转发
- **Next.js 16.4**：Cache Components 默认启用、`navigation()`/`prefetch()` API
- **Node.js v26.11.0**：`process.ref()`/`unref()` 稳定化，npm 11.20.0
- **Express 5.3.0**：安全修复
- **Partytown 1.0**：第三方脚本 Web Worker 执行库正式版
- **QUnit 3.0**：原生 ESM，删除旧时代支持

---

### 🐦 Hacker News 热门

- **TitleArt — 让文字像 1997 年一样**（258 分，39 评论）— 复古文字艺术生成器 [链接](https://titleart.dvy.io/)
- **我将员工数据放入 S&P 500 市值泡沫中可视化**（174 分，47 评论）— Nvidia 市值 5.2 万亿但仅 4.2 万员工，Accenture 81.4 万员工市值仅 1460 亿 [链接](https://bigwhalehunting.com/workforce/)
- **A Truly Modular Keyboard**（174 分，59 评论）— 真正模块化键盘设计 [链接](https://github.com/notaroomba/keybytes)
- **Farol — PR 审批风险地图**（60 分，37 评论）— 帮助 PR 审批者评估风险的可视化工具 [链接](https://github.com/winnin/farol)
- **Hurston-1 开源 TTS** — 专注于美国南方英语和非裔英语口音的语音合成模型（Apache 2.0）[链接](https://huggingface.co/destined/hurston-1)
- **Steal My Bitcoin**（605 分，441 评论）— 针对 PHP RCE 漏洞的互动演示，呼吁安全补丁意识 [链接](https://stealmybitcoin.com/)
- **Corgi — agent/终端多路复用器** — 统一管理多个 AI 编码代理的工具 [链接](https://github.com/danibonbon/corgi)

---

### 🐙 GitHub 热门（本周）

1. **[cloudflare/security-audit-skill](https://github.com/cloudflare/security-audit-skill)** — 六阶段结构化安全审计 coding-agent skill，来自 Cloudflare 漏洞发现系统
2. **[morluto/rea](https://github.com/morluto/rea)** — AI 逆向工程工具，从二进制文件重构软件，20万+ stars
3. **vLLM** — 高吞吐量 LLM  serving 引擎，支持 200+ 模型架构 [链接](https://github.com/vllm-project/vllm)

---

### 📡 其他动态

- **Facebook 取消对 Thread 的算法优先** — Meta 内部调整 [来源: The Verge]
- **Stack Overflow 2026 开发者调查** — JavaScript 连续 12 年位居第一，TypeScript 第 6；30,903 人参与 [来源: Stack Overflow Survey](https://survey.stackoverflow.co/2026)
- **State of Devs 2026 调查结果发布** — 5,000+ 开发者参与，涵盖职业安全、AI 态度、职场等 [来源: State of Devs](https://2026.stateofdevs.com/en-US/)
- **Sindre Sorhus 关闭外部 PR** — 因 AI 垃圾投稿，多位 prolific 维护者受到影响 [来源: BSky](https://bsky.app/profile/sindresorhus.com/post/3mwtgzhv7uk2t)
- **Coinbase 放弃 React Native，转向原生开发** — 称 AI 使原生开发成本降至两倍以内 [来源: LinkedIn](https://www.linkedin.com/posts/adamawolf)
- **JPEG XL 获所有主流浏览器支持** — Firefox 158 最新加入，Jake Archibald 发布 JPEG XL vs AVIF 全面对比 [来源: Jake Archibald](https://jakearchibald.com/2026/jpeg-xl-vs-avif/)
- **Vercel 推出固定费率 CDN 定价** — 针对 Pro 团队的套餐 [来源: GitHub Blog]
- **Chrome 154 响应式 iframe** — `frame-sizing: content-height` 让 iframe 自动适配嵌入内容高度 [来源: Chrome Blog](https://developer.chrome.com/blog/responsive-iframes?hl=en)
- **Firefox 151 支持 Web Serial API** — 可直接在浏览器中访问串口设备 [来源: Mozilla Hacks](https://hacks.mozilla.org/2026/05/web-serial-support-in-firefox/)
- **Pi 1.0 编码代理** — 基于 Node.js 的最小化编码代理，新增 MCP 和 Codemode 支持 [来源: Earendil](https://earendil.com/posts/pi-1-0/)
- **为什么 example.com 现在加载 JavaScript？** — IANA 解释：大多数访问者是自动化程序，不加载 JS 可节省带宽 [来源: Oliver Dunk](https://www.oliverdunk.com/2026/09/30/iana-reply)

---

📅 抓取时间: 2026-10-26 11:30
📡 数据源: 9/10 成功（FE News 当期为 2025-10 存档，非本期）
