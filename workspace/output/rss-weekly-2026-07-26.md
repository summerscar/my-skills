---
layout: default
title: 前端技术周报 (2026-07-26)
date: 2026-07-26
category: RSS 周报
---

## 📰 前端技术周报 (2026-07-26)


### 📝 本周要点

1. **TypeScript 7.0 正式发布** — Go 语言重写的 tsc 原生编译器正式上线，号称"10x 更快"。但 API 尚未完全开放，部分工具（如 Vue）可能暂时无法使用。
   来源: JavaScript Weekly #794 / JSer.info #776 | [链接](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/)

2. **npm 12 正式发布，安装脚本默认关闭** — 重大安全改进：生命周期脚本（postinstall 等）默认不再运行。
   来源: JavaScript Weekly #794 | [链接](https://github.blog/changelog/2026-07-08-npm-install-time-security-and-gat-bypass2fa-deprecation/)

3. **Bun 用 Rust 重写，消耗 $165k API 费用** — Bun 创始人分享将 JavaScript 运行时从 Zig 移植到 Rust 的完整故事。
   来源: JavaScript Weekly #794 | [链接](https://bun.com/blog/bun-in-rust)

4. **React 19.2.8/19.1.9/19.0.8 发布修复 DoS 漏洞** — 修复了通过特制请求触发服务器函数端点的 DoS 漏洞。
   来源: React Status #484 | [链接](https://github.com/react/react/releases/tag/v19.2.8)

5. **Next.js 正式启动安全发布计划** — 每月一次定期安全公告，首次于 7 月 20 日发布。
   来源: JSer.info #776 | [链接](https://nextjs.org/blog/next-security-release-program)

6. **Vue 3.6 进入 RC 阶段，Vapor Mode 功能完成** — 两年前预告的 Vapor Mode 现已功能完备准备就绪。
   来源: JavaScript Weekly #795 | [链接](https://github.com/vuejs/core/releases/tag/v3.6.0-rc.1)

7. **Nuxt 4.5 发布：Vite 8、Rspack 2、SSR 流式渲染** — 为 Nuxt 5 做准备，Nuxt 3 将于 7 月 31 日结束生命周期。
   来源: JavaScript Weekly #795 | [链接](https://nuxt.com/blog/v4-5)


### React/前端框架

- **"状态管理"的绝对状态** — Alex Russell 撰文批评 Redux、MobX、Zustand 和 React 本身只是"传播状态"而非"管理状态"，真正的状态管理需要像 CRDT 和同步引擎那样处理时间和冲突。Redux 维护者 Mark Erikson 已反驳。
  React Status #484 | [链接](https://infrequently.org/2026/07/state-management/)

- **shadcn/ui 新增 React Aria 组件基座** — 现在可以在 shadcn/ui 中选择 React Aria 作为基座，与 Base UI 和 Radix 并列。同时新增了 Toast 组件。
  React Status #484 | [链接](https://ui.shadcn.com/docs/changelog/2026-07-react-aria)

- **Shopify 从 React 迁移到 Preact + Web Components** — 在 64KB 硬预算限制下，将五个 React 收银台小部件改为 Preact 和 Web Components。
  React Status #484 | [链接](https://shopify.engineering/upgrading-checkout-blocks-app-to-polaris-web-components)

- **Preact 11.0 Beta 2 发布** — 维护者称"Preact 11 的最后几个 beta 之一"，迁移指南已就绪。
  JavaScript Weekly #795 | [链接](https://github.com/preactjs/preact/releases/tag/11.0.0-beta.2)

- **Angular 切换为年度发布节奏** — v23 计划于 2027 年 6 月发布，v22 已正式发布带来 signal-based forms 和 OnPush 默认变更检测。
  JavaScript Weekly #795 | [链接](https://github.com/angular/angular/pull/69817)

- **TanStack Router v1** — 从 React Router 迁移到类型安全文件路由的详细指南。
  Frontender #475 | [链接](https://www.sitepoint.com/tanstack-router-v1-migration-react-router-file-based/)

- **Fate 1.0: 面向 React 的新数据框架** — 前 Jest 负责人 Christoph Nakazawa 打造。
  JavaScript Weekly #786 | [链接](https://fate.technology/posts/fate-1.0)

### JavaScript/TypeScript

- **TypeScript 7.0 正式发布** — Go 语言 tsc 编译器发布，`target: es5` 和 `baseUrl` 等废弃配置将报错。新增 `--checkers`/`--builders` 并行控制选项。
  JSer.info #776 / JavaScript Weekly #794 | [链接](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/)

- **npm 12 正式发布** — 安装脚本默认关闭、Git 和远程 URL 依赖默认禁止。2FA 绕过 Granular Access Token 将逐步失效。
  JavaScript Weekly #794 | [链接](https://github.com/npm/cli/releases/tag/v12.0.0)

- **Bun 用 Rust 重写完成** — 使用 AI 辅助（Claude Code）将 Zig 代码移植到 Rust，消耗约 $165,000 API 费用。
  JavaScript Weekly #794 | [链接](https://bun.com/blog/bun-in-rust)

- **Node.js 26.5.0 发布** — 支持通过 import attributes 导入文本文件，新增 blob.textStream()。
  JavaScript Weekly #794 | [链接](https://nodejs.org/en/blog/release/v26.5.0)

- **ECMAScript 2026 已获批** — Array.fromAsync、原生 Uint8Array 等新特性。
  JavaScript Weekly #793 | [链接](https://javascriptweekly.com/issues/793)

- **Ant: 9MB 二进制文件的 JavaScript 运行时** — 用 C 语言编写，不依赖 V8/JavaScriptCore/SpiderMonkey。
  JavaScript Weekly #794 | [链接](https://antjs.org/)

- **ShadowRealm 提案** — TC39 提案，允许在隔离环境中运行第三方代码。
  JavaScript Weekly #786 | [链接](https://css-tricks.com/soon-we-can-finally-banish-javascript-to-the-shadowrealm/)

### CSS/样式

- **用 CSS Subgrid 重建 FIFA 世界杯积分表** — Ahmad Shadeed 使用 CSS Grid、Subgrid 实现响应式复杂布局。
  Frontend Focus #751 | [链接](https://frontendfoc.us/link/188270/rss)

- **Firefox 153 发布** — 支持 Picture-in-Picture API、popover="hint" 改进、Native Containers 预览。Mozilla 尝试将发布周期缩短为两周。
  Frontend Focus #751 | [链接](https://frontendfoc.us/link/188273/rss)

- **CSS 锚点定位入门** — Josh W. Comeau 的全面教程。
  Frontender #474 | [链接](https://www.joshwcomeau.com/css/anchor-positioning/)

- **CSS border-shape 属性即将到来！** — 强大新属性详细介绍。
  Frontender #474 | [链接](https://css-tricks.com/get-ready-for-the-powerful-css-border-shape-property/)

- **CSS 容器查询 + Subgrid 布局三部曲已全浏览器支持** — 所有主流浏览器均已支持。
  Frontender #472 | [链接](https://www.sitepoint.com/css-container-queries-subgrid-the-layout-trilogy-thats-now-in-every-browser/)

- **OKHST: 可预测的颜色生成系统** — 用于真实界面的可预测颜色生成方法。
  Frontender #475 | [链接](https://tenphi.me/blog/okhst-predictable-color-generation/)

### 工具/构建

- **Vite 7 生产迁移：从 esbuild 到 Rolldown 和 Oxc** — 详细介绍 Vite 7 构建工具链迁移路径。
  Frontender #475 | [链接](https://www.sitepoint.com/vite-7-production-migration-rolldown-oxc-build-optimization/)

- **ESLint 官方 Codemod 迁移工具** — 自动化 ESLint 版本迁移（v8->v9，v9->v10）。
  JavaScript Weekly #795 | [链接](https://eslint.org/blog/2026/07/eslint-codemod-migrations/)

- **Astro 7.1 发布** — 更精细的 CSP 控制、分页 URL 完全控制。
  Frontend Focus #751 | [链接](https://astro.build/blog/astro-710/)

- **WebStorm 2026.2 发布** — 增加 TypeScript 7 支持，改进 Svelte 和 Vue 支持。
  JavaScript Weekly #795 | [链接](https://blog.jetbrains.com/webstorm/2026/07/webstorm-2026-2/)

- **Flint: 微软图表规范编译器** — 将声明式 JSON 规范编译为 Vega-Lite、ECharts 或 Chart.js，面向 AI Agent 场景。
  JavaScript Weekly #795 | [链接](https://microsoft.github.io/flint-chart/)

- **LiteRT.js: Google 的高性能 Web AI 推理库** — 性能优于 TensorFlow.js，浏览器中直接运行 AI 模型。
  JavaScript Weekly #794 | [链接](https://developers.googleblog.com/litertjs-googles-high-performance-web-ai-inference/)

### 性能优化与测试

- **何时阻塞主线程是有意义的** — Smashing Magazine 探讨何时故意阻塞主线程反而提升体验。
  Frontender #475 | [链接](https://www.smashingmagazine.com/2026/07/when-makes-sense-block-main-thread/)

- **Figma 在 Canvas 中构建无障碍** — 从零重建屏幕阅读器支持、键盘导航和焦点管理。
  Frontend Focus #751 | [链接](https://frontendfoc.us/link/188272/rss)

- **Shadscan: shadcn 组件确定性 UI 审计** — 60 项检查，无需 AI 或 API 密钥。
  React Status #484 | [链接](https://www.shadscan.com/)

### AI/机器学习

- **Mark Erikson 的 AI 开发工作流** — Redux 维护者分享 AI 辅助开发工作流，包括使用 OpenCode 编码代理。
  JavaScript Weekly #786 | [链接](https://blog.isquaredsoftware.com/2026/05/ai-thoughts-part-2-agent-workflow-tools/)

- **ReactBench: 编码 Agent 评测基准** — 基于构建可用 React 应用的能力评估，GPT 5.6 暂时领先。
  JavaScript Weekly #795 | [链接](https://www.reactbench.com/)

- **Dr. Axel Rauschmayer 因 AI 爬虫关闭博客** — 前 JS Weekly 编辑因被 AI 爬虫淹没而移除博客和书籍。
  JavaScript Weekly #786 | [链接](https://2ality.com/)

### 周刊摘要

#### 阮一峰科技爱好者周刊 #404 — 你需要知道的 AI 内存知识

**核心主题：本地运行 AI 模型的内存瓶颈**

- **独立显卡（RTX 5090）**：104.8 TFLOPS，32GB 显存，约 3 万元。算力极强但显存小，70B 4-bit 模型（需 32.6GB）跑不动。
- **板载芯片组（AMD Strix Halo / Ryzen AI Max+ 395）**：14.8 TFLOPS，128GB 统一内存，约 2 万元。算力只有 1/7 但内存容量大。
- 关键认知：内存容量 x 内存带宽 = 实际体验。板载芯片组弱点在带宽（256GB/s vs RTX 1792GB/s），40GB 模型每秒只能生成约 6 个 Token。
- 苹果 M 系列、AMD Strix Halo、NVIDIA DGX Spark、Intel Core Ultra、高通 Snapdragon X 均采用统一内存架构。

来源: 阮一峰博客 | [链接](https://www.ruanyifeng.com/blog/2026/07/weekly-issue-404.html)

#### JSer.info #776 — TypeScript 7.0、npm 12、Next.js 安全策略

- TypeScript 7.0：Go 移植的原生 tsc 发布，废弃配置报错，新增并行控制，但程序 API 尚未公开
- npm 12：allowScripts 默认禁用，--allow-git/--allow-remote 默认为 none
- Next.js：每月一次安全发布，首次 7 月 20 日

来源: JSer.info | [链接](https://jser.info/2026/07/17/typescript-7.0-npm-12-next-js-security-release/)

#### FE News (Naver) 2026-05 月刊

- Node.js v26.0.0 正式发布，Temporal API 默认启用
- React 生态可持续基金会成立

来源: FE News | [链接](https://fenews.substack.com/p/fe-news-2026-05)

### Hacker News 热门

- **Bribes.fyi** — 出行前了解目的地情况。65 分，47 评论。 [链接](https://bribes.fyi/before-you-go)
- **Brolly** — 纯文本天气预报网站，极简主义设计。 [链接](https://brolly.sh)

### GitHub 热门

- **bojieli/ai-agent-book** — 《深入理解 AI Agent：设计原理与工程实践》开源书籍。 [链接](https://github.com/bojieli/ai-agent-book)

### 其他动态

- **Vercel 收购 Better Auth 团队** [链接](https://vercel.com/blog/vercel-acquires-better-auth)
- **Mini Shai-Hulud 攻击：300+ 恶意 npm 包发布** [链接](https://safedep.io/mini-shai-hulud-strikes-again-314-npm-packages-compromised/)
- **MDN 推出 MCP 服务器** [链接](https://developer.mozilla.org/en-US/blog/introducing-mdn-mcp-server/)
- **Cloudflare 推出 Precursor 客户端验证系统** [链接](https://blog.cloudflare.com/introducing-precursor/)
- **Babylon Lite: 更快更小的 WebGPU 专用 3D 引擎** [链接](https://doc.babylonjs.com/lite/)
- **Framework Benchmarks: 多框架对比工具** [链接](https://framework-benchmarks.as93.net/)

---

📅 抓取时间: 2026-07-26 22:00
📡 数据源: 10/10 成功
