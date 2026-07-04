---
layout: default
title: 前端技术周报 (2026-07-05)
date: 2026-07-05
category: RSS 周报
---

## 📰 前端技术周报 (2026-07-05)

### 📝 本周要点

1. **Meta 开源 Astryx 设计系统** — 160+组件、8年内部开发、StyleX 驱动
2. **Dan Abramov 加入 Next.js 团队** — 兼职参与 Next.js 16.3
3. **TypeScript 7.0 RC 发布** — Go 编译器，VS Code 构建提速4倍
4. **Next.js 16.3 预览** — SSR 导航如 SPA 般即时
5. **Astro 7.0 正式发布** — Rust 编译器 + Vite 8，构建快15-61%
6. **Babel 8.0.0** — ESM-only，不再默认 ES5
7. **npm v12 预览** — 默认禁用 install 脚本
8. **Deno 2.9** — 桌面应用支持，冷启动快2倍

### ⚛️ React/前端框架

- **Meta 发布 Astryx 设计系统** — 160+组件，React+StyleX，主题/模板/工具完备
  来源: React Status #481 | [链接](https://react.statuscode.com/link/187432/rss)
- **Dan Abramov 加入 Next.js 团队** — 兼职加入 Vercel
  来源: React Status #481 | [链接](https://react.statuscode.com/link/187135/rss)
- **Next.js 16.3 预览：即时导航** — opt-in 行为，SPA 般 SSR 导航
  来源: React Status #480 | [链接](https://react.statuscode.com/link/187131/rss)
- **Linear → StyleX 迁移** — 页面渲染快30%，AI 迁移10万行
  来源: React Status | [链接](https://www.skovhus.dev/blog/moving-linear-from-styled-components-to-stylex)
- **shadcn/ui 聊天组件** — MessageScroller/Bubble/Attachment
  来源: React Status #481 | [链接](https://react.statuscode.com/link/187452/rss)
- **React Router v8** — ESM-only、v6 EOL
  来源: JSer.info #774 | [链接](https://remix.run/blog/react-router-v8)
- **Ant Design 6.5** — 更小包体积，DESIGN.md for AI
  来源: React Status #481 | [链接](https://react.statuscode.com/link/187460/rss)
- **Expo SDK 57** — RN 0.86 进入 Expo
  来源: React Status #481 | [链接](https://react.statuscode.com/link/187467/rss)
- **spartan/ui 1.0** — Angular 版 shadcn/ui
  来源: JS Weekly #792 | [链接](https://spartan.ng/)

### 📦 JavaScript/TypeScript

- **TypeScript 7.0 RC** — Go 编译器，VS Code 36s→5s
  来源: JS Weekly #792 / JSer.info #774 | [链接](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0-rc/)
- **Babel 8.0.0** — ESM-only、Node 24+、不编译 ES5
  来源: JSer.info #774 | [链接](https://babeljs.io/blog/2026/06/16/8.0.0/)
- **npm v12 预览** — 默认禁 install 脚本
  来源: JSer.info #774 | [链接](https://github.blog/changelog/2026-06-09-upcoming-breaking-changes-for-npm-v12/)
- **Deno 2.9** — deno desktop、冷启动 x2、Node 26 兼容
  来源: JS Weekly #792 | [链接](https://deno.com/blog/v2.9)
- **pnpm 11.7** — frozenStore、Rust Pacquet 解析器
  来源: JSer.info #774 | [链接](https://pnpm.io/blog/releases/11.7)
- **Biome v2.5** — 500 Lint 规则、跨文件 CSS
  来源: JSer.info #774 | [链接](https://biomejs.dev/blog/biome-v2-5/)
- **Nub：Node.js 工具箱** — Zod 作者开发
  来源: JS Weekly #792 | [链接](https://nubjs.com/blog/introducing-nub)
- **Playwright v1.61** — WebAuthn passkey、Web Storage API
  来源: JSer.info #774 | [链接](https://github.com/microsoft/playwright/releases/tag/v1.61.0)

### 🎨 CSS/样式

- **自定义 select 高度** — Jake Archibald calc-size()
  来源: Frontend Focus #748 | [链接](https://frontendfoc.us/link/187308/rss)
- **Modern CSS 主题** — light-dark()+contrast-color()+Style Queries
  来源: Frontend Focus #747 | [链接](https://una.im/modern-css-theming/)
- **Chrome 150** — text-fit、渐变边框、polygon() 圆角
  来源: JSer.info #773 | [链接](https://developer.chrome.com/blog/chrome-150-beta?hl=en)
- **Safari 27 beta** — base-select、Scroll Anchoring
  来源: JSer.info #774 | [链接](https://webkit.org/blog/17967/news-from-wwdc26-webkit-in-safari-27-beta/)
- **Container Queries + Subgrid** — 全浏览器支持
  来源: Frontender #472 | [链接](https://www.sitepoint.com/css-container-queries-subgrid-the-layout-trilogy-thats-now-in-every-browser/)

### 🛠 工具/构建

- **Vite 8.1** — bundled dev mode，大应用 15x 提速
  来源: React Status #480 | [链接](https://react.statuscode.com/link/187136/rss)
- **WASI 0.3** — 原生异步，host 共享事件循环
  来源: JSer.info #774 | [链接](https://bytecodealliance.org/articles/WASI-0.3)
- **gh-stack** — GitHub 官方堆叠 PR
  来源: FE News 2026-06 | [链接](https://github.com/github/gh-stack)
- **MarkItDown (Microsoft)** — 文件→Markdown，135k★
  来源: FE News 2026-06 | [链接](https://github.com/microsoft/markitdown)

### ⚡ 性能优化

- **Hydration 不匹配的 LCP 代价**
  来源: React Status #481 | [链接](https://react.statuscode.com/link/187443/rss)
- **Container Timing API** — 组件级渲染时间测量
  来源: FE News 2026-06 | [链接](https://developer.chrome.com/blog/container-timing-origin-trial)
- **Declarative Partial Updates** — Chrome 148 实验性
  来源: FE News 2026-06 | [链接](https://developer.chrome.com/blog/declarative-partial-updates)

### 🤖 AI/机器学习

- **State of AI 2026** — TypeScript 首超 JS，AI 代码 54%
  来源: FE News 2026-06 | [链接](https://2026.stateofai.dev/en-US)
- **Vercel Eve** — Next.js 式 Agent 框架
  来源: React Status #480 | [链接](https://vercel.com/blog/introducing-eve)
- **MDN MCP Server** — 文档接入 AI/IDE
  来源: MDN Blog | [链接](https://developer.mozilla.org/en-US/blog/introducing-mdn-mcp-server/)
- **Uber uSpec** — 2分钟 AI 生成设计规范
  来源: FE News 2026-06 | [链接](https://www.uber.com/ca/en/blog/automate-design-specs/)
- **A2UI** — Google AI Agent UI 协议
  来源: FE News 2026-06 | [链接](https://a2ui.org/)
- **Rapid-MLX** — Apple Silicon 本地推理 4.2x Ollama
  来源: FE News 2026-06 | [链接](https://github.com/raullenchai/Rapid-MLX)

### 📚 周刊摘要

#### 阮一峰科技爱好者周刊 #402 (7月3日)

**封面：我在智念 AI 的日子（小说）** — 关于 AI 时代程序员异化的反思小说：Token 排行榜、AI 代码零审查、同事用表情符号交流。同时讨论了美光5年内存合同、特斯拉200美元AI预算上限、AI种子骗局等。工具推荐：软件源 CDN 镜像网关、抖音批量下载、前端文件预览。学习：Jest/Vitest 测试入门
来源: 阮一峰博客 | [链接](https://www.ruanyifeng.com/blog/2026/07/weekly-issue-402.html)

#### FE News 2026年6月刊

Naver FE 团队策划。核心内容：State of AI 2026 调查（TypeScript首超JS，AI代码占比54%）、Declarative Partial Updates API、TanStack 供应链攻击复盘、Container Timing API 起源试验、Uber uSpec 设计规范自动化。工具推荐：Wave Terminal、tegaki 手写动画字体、A2UI 协议、gh-stack 堆叠PR、MarkItDown、Rapid-MLX 本地推理、Multica 多Agent管理
来源: FE News | [链接](https://fenews.substack.com/p/fe-news-2026-06)

#### JSer.info #774 (6月22日)

TypeScript 7.0 RC（Go编译器）、Babel 8.0.0（ESM-only）、React Router v8（ESM-only EOL）、Biome v2.5（500 Lint规则）、pnpm 11.7（Pacquet Rust解析）、Playwright v1.61（passkey + Web Storage）、Safari 27 beta（base-select）、WASI 0.3（原生异步）、Vercel Eve Agent框架、MDN MCP、Nub 工具箱、Webwright 浏览器Agent、Wakaru JS反编译
来源: JSer.info #774 | [链接](https://jser.info/2026/06/22/typescript-7.0-rc-babel-8.0.0-react-router-v8/)

### 🌟 GitHub 热门

- ai-berkshire — 价值投资 AI 研究框架（Claude Code/Codex）
- Webwright (Microsoft) — SWE 风格浏览器 Agent 框架
- Nub — Node.js 全能工具包（Zod作者）
- Wakaru — JS 反编译器和 Bundle 拆分
- MarkItDown (Microsoft) — 135k★ 文件转 Markdown
- Rapid-MLX — Apple Silicon 本地推理 4.2x Ollama

### 📋 其他动态

- Vercel Services — 多框架同项目运行
- WASI 0.3 — 异步处理原生集成
- VoidZero 加入 Cloudflare（Vite/Oxc）
- pnpm Rust 重写计划（Pacquet）
- Git 2.55 — git history fixup
- PostgreSQL 19 Beta 1 发布
- Pointer Events Level 3 成为 W3C 推荐标准
- CSS Day 2026 — Una Kravets 展示最新 CSS UI 进展
- Google JSIR — JavaScript 高级 IR 提案

---
📅 抓取: 2026-07-05 | 📡 数据源: 9/10 成功（HN Show 502）
