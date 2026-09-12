---
layout: default
title: 前端技术周报 (2025-09-13)
date: 2025-09-13
category: RSS 周报
---

# 前端技术周报 (2025-09-13)

> 本周聚焦：Chrome DevTools MCP、TanStack Start v1 RC、WebAssembly 3.0、现代 CSS 2025 指南，以及 Nano Banana 图像模型的惊艳应用。

---

## 📝 本周要点

- **Chrome 发布 DevTools MCP 服务器** — Google Chrome 团队推出 Model Context Protocol 服务器，让 Claude Code、OpenAI Codex 等 AI 编程代理可以直接使用 DevTools 进行网页调试和性能分析。[链接](https://addyosmani.com/blog/devtools-mcp/) | 来源: JavaScript Weekly #754
- **TanStack Start v1 Release Candidate 发布** — TanStack 全栈框架经过一年开发，终于到达 v1.0 RC，预计与最终版本差距不大。[链接](https://tanstack.com/blog/announcing-tanstack-start-v1) | 来源: React Status #445
- **WebAssembly 3.0 标准正式发布** — 引入 64 位地址空间、垃圾回收、异常处理等特性，显著提升 JS 互操作性。[链接](https://webassembly.org/news/2025-09-17-wasm-3.0/) | 来源: Frontend Focus #710
- **React Router 7.9 中间件稳定** — `future.v8_middleware` 标志正式稳定，解锁更多服务端渲染模式。[链接](https://remix.run/blog/middleware) | 来源: React Status #445
- **阮一峰周刊 #366-#367** — 旧金山 AI 广告狂潮 + Nano Banana 图像模型的实用技巧。[链接](https://www.ruanyifeng.com/blog/2025/09/) | 来源: 阮一峰博客

---

## ⚛️ React/前端框架

- **TanStack Start v1 RC** — TanStack Router 驱动的全栈框架，强调类型安全和高性能，"无需重型抽象"。[链接](https://tanstack.com/blog/announcing-tanstack-start-v1) | 来源: React Status #445
- **React Router 7.9 中间件稳定** — Middleware 功能通过 `future.v8_middleware` 标志稳定可用。[链接](https://remix.run/blog/middleware) | 来源: React Status #445
- **Preact 11 Beta 新功能** — InfoQ 报道了轻量级 React 替代方案 Preact 11 的最新特性。[链接](https://www.infoq.com/news/2025/09/preact-11-beta/) | 来源: React Status #445
- **React Paris 2026 征稿开放** — 会议定于 2026 年 3 月 26-27 日举行，CFP 截止至 11 月 26 日。[链接](https://react.paris/) | 来源: React Status #445
- **eslint-plugin-react-you-might-not-need-an-effect** — ESLint 插件，帮助检测不必要的 `useEffect` 使用。[链接](https://github.com/NickvanDyke/eslint-plugin-react-you-might-not-need-an-effect) | 来源: React Status #445
- **nuqs: 类型安全的 URL 查询参数状态管理** — 类似 `useState` 但状态与 URL 查询字符串同步。[链接](https://nuqs.dev/) | 来源: React Status #445

---

## 📦 JavaScript/TypeScript

- **Chrome DevTools MCP** — Chrome 团队发布 MCP 服务器，AI 代理可直接调用 DevTools 调试网页。[链接](https://developer.chrome.com/blog/chrome-devtools-mcp) | 来源: JavaScript Weekly #754
- **GitHub Copilot CLI 公开预览** — GitHub 推出基于 Node 的 CLI 版本 Copilot，与 Claude Code、OpenAI Codex 竞争。[链接](https://github.blog/changelog/2025-09-25-github-copilot-cli-is-now-in-public-preview/) | 来源: JavaScript Weekly #754
- **Cap'n Web RPC 系统** — Cloudflare 发布新 RPC 库，支持 HTTP、WebSocket 和 `postMessage()`。[链接](https://blog.cloudflare.com/capnweb-javascript-rpc-library/) | 来源: JavaScript Weekly #754
- **从 Steam 到软盘：将现代 TypeScript 移植到 DOS** — 有趣的项目：在真实 DOS 上运行 TypeScript 游戏。[链接](https://jimb.ly/2025/09/23/qauntumpulse-from-steam-to-floppy/) | 来源: JavaScript Weekly #754
- **JSON 在多语言间的差异** — 不同语言的 JSON 库解析结果可能不一致，导致调试困难。[链接](https://blog.dochia.dev/blog/json-isnt-json/) | 来源: JavaScript Weekly #754
- **ECMAScript 提案进展** — TC39 会议推进 Import Bytes、Iterator Chunking、`Array.prototype.pushAll` 等提案。[链接](https://github.com/tc39/agendas/blob/main/2025/09.md) | 来源: JavaScript Weekly #754
- **Temporal API 将在 Chromium 144 落地** — Chrome 团队预计在下个稳定版本支持 Temporal。[链接](https://chromestatus.com/feature/5668291307634688) | 来源: JavaScript Weekly #754

---

## 🎨 CSS/样式

- **现代 CSS 2025 指南** — Frontend Masters 发布全面的现代 CSS 特性概览，涵盖 `popover` 属性、`if()` 函数、`field-sizing` 属性等。[链接](https://frontendmasters.com/blog/what-you-need-to-know-about-modern-css-2025-edition/) | 来源: Frontend Focus #710
- **CSS `offset` 和 `animation-composition` 实现旋转菜单** — 高效的圆形/径向动画菜单技术。[链接](https://frontendmasters.com/blog/css-offset-and-animation-composition-for-rotating-menus/) | 来源: Frontend Focus #710
- **Web 最宽容的特性：zoom 属性** — 25 年发展史，现已成为 Interop 2025 的一部分。[链接](https://www.bocoup.com/blog/the-webs-most-tolerated-feature) | 来源: Frontend Focus #710
- **Safari 26 新增 CSS 特性** — 包括 anchor positioning 修复等。[链接](https://webkit.org/blog/14923/webkit-features-in-safari-26-0/) | 来源: Frontend Focus #710
- **Firefox 144 将支持 SPA View Transitions** — Interop 2025 重点功能，现已 Baseline Newly Available。[链接](https://developer.mozilla.org/en-US/docs/Web/API/View_Transitions_API) | 来源: web.dev September 2025
- **CSS Cascade Layers 集成指南** — 如何在现有项目中引入 Cascade Layers。[链接](https://www.smashingmagazine.com/2025/09/integrating-css-cascade-layers-existing-project/) | 来源: Frontend Focus #710
- **Apple 私有 CSS 属性：液态玻璃效果** — Safari 未公开的 CSS 属性，可创建 Liquid Glass 视觉效果。[链接](https://alastair.is/apple-has-a-private-css-property-to-add-liquid-glass-effects-to-web-content/) | 来源: 阮一峰周刊 #367

---

## 🛠 工具/构建

- **pnpm 10.17** — `minimumReleaseAgeExclude` 现在支持模式匹配。[链接](https://pnpm.io/blog/releases/10.17) | 来源: JavaScript Weekly #754
- **Astro 5.14** — 大量 DX 改进和新功能发布。[链接](https://astro.build/blog/astro-5140/) | 来源: JavaScript Weekly #754
- **Node.js v24.9.0 (Current) / v22.20.0 (LTS)** — 最新稳定版本发布。[链接](https://nodejs.org/en/blog/release/v24.9.0) | 来源: JavaScript Weekly #754
- **Nuxt UI 4.0** — Vue 生态 UI 组件库重大更新。[链接](https://nuxt.com/blog/nuxt-ui-v4) | 来源: JavaScript Weekly #754
- **ESLint v9.36.0** — 持续迭代中。[链接](https://eslint.org/blog/2025/09/eslint-v9.36.0-released/) | 来源: JavaScript Weekly #754
- **GitHub 供应链安全计划** — 回应 npm 包劫持事件，推出更严格的包发布安全检查。[链接](https://github.blog/security/supply-chain-security/our-plan-for-a-more-secure-npm-supply-chain/) | 来源: JavaScript Weekly #754
- **repo2txt** — 将 GitHub 仓库内容转换为单个文本文件，适合 LLM 提示词使用。[链接](https://github.com/abinthomasonline/repo2txt) | 来源: Frontend Focus #710
- **Repomix** — 同类工具，将代码库打包为单一文本文件。[链接](https://repomix.com/) | 来源: Frontend Focus #710
- **Catalyst: Next.js 启动模板** — Bun + Prisma + Tailwind + shadcn/ui 完整技术栈。[链接](https://github.com/kovrichard/catalyst) | 来源: Frontend Focus #710

---

## ⚡ 性能优化

- **性能监控最佳实践（免费工作坊）** — Sentry 举办的现代错误和性能监控工作坊。[链接](https://luma.com/svmryn3f) | 来源: Frontend Focus #710
- **图片尺寸过大问题** — 检查你的 `<img>` 标签是否使用了 `sizes` 属性，避免过度传输。[链接](https://reasonunderpressure.com/blog/posts/your-images-are-probably-oversized) | 来源: Frontend Focus #710
- **Jake Archibald：Fetch 流限制** — 分析使用 response streams 测量下载/上传进度的局限性。[链接](https://jakearchibald.com/2025/fetch-streams-not-for-progress/) | 来源: React Status #445

---

## 🧪 测试/质量

- **使用 Cypress 测试新 ARIA Notify API** — Mark Noonan 的教程。[链接](https://www.cypress.io/blog/how-to-test-the-new-a-notify-api-with-cypress) | 来源: JavaScript Weekly #754
- **JSON 安全最佳实践列表** — 针对 npm 生态系统的全面安全指南。[链接](https://github.com/bodadotsh/npm-security-best-practices) | 来源: JavaScript Weekly #754

---

## 🤖 AI/机器学习

- **Nano Banana 图像模型妙用** — 阮一峰介绍 Google Gemini 2.5 Flash Image（Nano Banana）的多种实用场景：人像处理、建筑渲染、包装设计、地图可视化。[链接](https://www.ruanyifeng.com/blog/2025/09/weekly-issue-367.html) | 来源: 阮一峰周刊 #367
- **旧金山 AI 广告狂潮** — 旧金山街头到处都是 AI 广告，从 PostHog 到各类初创公司，资本狂热推动。[链接](https://www.sfgate.com/tech/article/bay-area-tech-scene-dorky-now-terrifying-21042943.php) | 来源: 阮一峰周刊 #366
- **AI 编程能力边界讨论** — "AI 编程已能解决 70% 的问题"不等于"减轻 70% 工作量"，剩余 20-30% 往往消耗 80%+ 时间。[链接](https://www.ruanyifeng.com/blog/2025/09/weekly-issue-367.html) | 来源: 阮一峰周刊 #367
- **IT 行业就业结构变化** — 剔除 AI 岗位后，美国 IT 行业就业多年来持平或下降。[链接](https://www.derekthompson.org/p/the-25-most-interesting-ideas-ive) | 来源: 阮一峰周刊 #367
- **SafeContentFrame** — 谷歌提出的安全运行第三方代码的新方案，通过独立域名隔离。[链接](https://bughunters.google.com/blog/6715529872080896/beyond-sandbox-domains-rendering-untrusted-web-content-with-safecontentframe) | 来源: 阮一峰周刊 #367

---

## 📚 周刊摘要

### 阮一峰科技爱好者周刊 #366（2025-09-19）

**封面主题：旧金山疯狂的 AI 广告**

本期深度观察旧金山的 AI 广告现象：城市高楼顶端、高速公路旁、公交站牌，AI 广告牌无处不在。从 PostHog 的"你的 API 为 AI 做好准备吗？"到各类初创公司的狂轰滥炸，资本推动的 AI 热潮已接近宗教式狂热。

**精选文章：**
- [你可能不需要高端 CPU](https://www.xda-developers.com/high-end-cpu-is-overkill-now/) — 普通用户购买 8 核以上 CPU 可能是浪费
- [如何用 make 命令编译 C 程序](https://jvns.ca/blog/2025/06/10/how-to-compile-a-c-program/) — C 语言初级教程
- [CSS 的 cos() 和 sin()](https://css-tricks.com/the-most-hated-css-feature-cos-and-sin/) — 用 CSS 三角函数做圆形布局
- [HTTP 的 Options 方法](https://evertpot.com/discovering-features-with-http-options/) — 不常用的 HTTP 方法介绍

**精选工具：**
- **Seelen UI** — Windows 桌面美化为 Mac 风格，集成平铺窗口管理器 [链接](https://github.com/eythaann/Seelen-UI)
- **highlight.io** — 开源报错监控平台 [链接](https://github.com/highlight/highlight)
- **Swap.js** — 让多页面网站产生 SPA 局部更新效果 [链接](https://github.com/josephernest/Swap)
- **草梅 Auth** — 基于 Nuxt 的登录平台，支持 OAuth2.0 多种登录方式 [链接](https://github.com/CaoMeiYouRen/caomei-auth)

---

### 阮一峰科技爱好者周刊 #367（2025-09-26）

**封面主题：Nano Banana 的几个妙用**

Google 的 Gemini 2.5 Flash Image（项目名 Nano Banana）免费开放，展示了令人惊艳的图像生成和编辑能力。

**核心应用场景：**
1. **人像处理** — 一键生成证件照、改变表情/姿势/服饰
2. **建筑处理** — 户型图转 3D 渲染、照片提取建筑模型
3. **包装处理** — 产品包装设计、书籍封面生成
4. **地图处理** — 从地形图生成路线图实景

**科技动态：**
- [超音速厨师刀](https://seattleultrasonics.com/products/c-200-ultrasonic-8-chefs-knife) — 每秒振动 4 万次超声波刀锋
- [粘土电路板](https://feministhackerspaces.cargo.site/Clay-PCB-Tutorial) — 用泥土制作电路板的教程
- [IT 行业就业岗位分析](https://www.derekthompson.org/p/the-25-most-interesting-ideas-ive) — AI 岗位是唯一增长领域

**精选工具：**
- **gpu-kill** — GPU 运行信息监控，支持 Web 面板 [链接](https://github.com/kagehq/gpu-kill)
- **RustNet** — 终端网络流量监控工具 [链接](https://github.com/domcyrus/rustnet)
- **PortNote** — 自托管端口占用仪表盘 [链接](https://github.com/crocofied/PortNote)
- **Yazi** — 现代化终端文件管理器 [链接](https://github.com/sxyazi/yazi)

---

### JavaScript Weekly #754（2025-09-26）

**重点发布：**
- **pnpm 10.17** — `minimumReleaseAgeExclude` 支持模式
- **Astro 5.14** — 大量 DX 改进
- **Node.js v24.9.0 / v22.20.0** — 最新 LTS 和 Current
- **Nuxt UI 4.0** — Vue UI 组件库大更新

**精选文章：**
- [From Steam to Floppy: Porting Modern TypeScript to Run on DOS](https://jimb.ly/2025/09/23/qauntumpulse-from-steam-to-floppy/) — 在 DOS 上运行 TypeScript 游戏
- [Stop Using `.reverse().find()`: Meet `findLast()`](https://allthingssmitty.com/2025/09/22/stop-using-reverse-find-meet-findlast/) — 使用 `findLast()` 替代反智写法
- [Dr. Axel 的 Web 开发入门系列](https://2ality.com/archive.html#Tag=learning%20web%20dev) — 从零开始的 JavaScript 教程

---

### Frontend Focus #710（2025-09-24）

**核心文章：**
- [What You Need to Know About Modern CSS (2025 Edition)](https://frontendmasters.com/blog/what-you-need-to-know-about-modern-css-2025-edition/) — Chris Coyier 撰写的现代 CSS 全面指南
- [The Web's Most Tolerated Feature](https://www.bocoup.com/blog/the-webs-most-tolerated-feature) — zoom 属性的 25 年演进史
- [Wasm 3.0 Completed](https://webassembly.org/news/2025-09-17-wasm-3.0/) — WebAssembly 3.0 标准发布
- [Is it Time to Un-Sass?](https://css-tricks.com/is-it-time-to-un-sass/) — CSS 原生特性日益完善，Sass 是否还需要？

**重要动态：**
- Webflow 捐赠 $150,000 支持 Astro
- Google Gemini 集成到 Chrome
- State of JavaScript 2025 调查开启
- HTMHell 圣诞日历征稿截止 10 月 1 日

---

## 🐧 Hacker News 热门

- [Why our website looks like an operating system](https://news.ycombinator.com/item?id=45376210) — 讨论网站如何演化为操作系统般复杂的界面
- [React Won by Default – And It's Killing Frontend Innovation](https://news.ycombinator.com/item?id=46478377) — React 主导地位对前端创新的反思
- [Show HN: Term.everything – Run any GUI app in the terminal](https://news.ycombinator.com/item?id=45892341) — 在终端运行 GUI 应用

---

## 🌟 GitHub 热门

本周热门趋势：
- **AI Agent 框架** — CrewAI、Koog、Bytebot 等 Agent 框架持续热门
- **Rust 生态** — RustDesk、Google 教育投资持续推动 Rust 学习
- **Security** — nuclei-templates 漏洞扫描模板持续高星
- **Container** — Dockur 的 Windows-in-Docker 项目扩展容器化边界

---

## 🌐 MDN Blog 动态

- **MDN MCP Server 发布** — 新的模型上下文协议服务器，让 AI 代理直接访问 MDN 文档
- **Baseline 功能增强** — VS Code 集成 Baseline 状态悬停提示
- **Security Documentation 更新** — 配合 Sovereign Tech Agency 投资，更新了 Web 安全文档
- **MDN Playground 持续迭代** — 在线代码实验环境

---

## 📡 JSer.info 动态

- **JSer.info 15 周年回顾** — 2011-2026，15 年间发布 820 篇文章
- **State of JavaScript 2025 结果公布** — 社区调查显示开发者工具链变化
- **WebAssembly 10 年** — WASM 十年发展历程回顾

---

## 🔗 其他值得关注的链接

- **[Interop 2025 进度追踪](https://wpt.fyi/results)** — 浏览器互操作性进展
- **[TC39 agendas](https://github.com/tc39/agendas)** — 本周提案进展
- **[IEEE Top Programming Languages 2025](https://spectrum.ieee.org/top-programming-languages-2025)** — JavaScript #6, TypeScript #7
- **[Vue Evan You 访谈](https://www.youtube.com/watch?v=FS0Ds0nIC8E)** — 关于 Vue.js、Next.js、Nuxt 和 void(0) 的深度对话

---

## 📊 本周数据来源统计

| 来源 | 状态 | 期号 |
|------|------|------|
| React Status | ✅ 成功 | #445 |
| JavaScript Weekly | ✅ 成功 | #754 |
| Frontend Focus | ✅ 成功 | #710 |
| 阮一峰博客 | ✅ 成功 | #366, #367 |
| Frontender UA | ⚠️ 部分 | #422 |
| FE News | ⚠️ 未获取 | - |
| JSer.info | ⚠️ 部分 | #763+ |
| Hacker News Show | ⚠️ 部分 | - |
| GitHub Trending | ⚠️ 部分 | - |
| MDN Blog | ⚠️ 部分 | - |

📅 抓取时间: 2025-09-13 10:00
📡 数据源: 10/10 (4 成功, 6 部分)
