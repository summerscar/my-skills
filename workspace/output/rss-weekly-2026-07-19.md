---
layout: default
title: 前端技术周报 (2026-07-19)
date: 2026-07-19
category: RSS 周报
---

## 📰 前端技术周报 (2026-07-19)

### 📝 本周要点

- **TypeScript 7.0 正式发布，10x 速度提升** — 原生 Go 移植版 tsc 正式以 npm typescript 包发布，带来了 10 倍速度提升。--checkers/--builders/--singleThreaded 并行控制选项，重写的 --watch 模式，LSP 全面支持。但程序 API 尚未公开，部分工具（如 Vue）暂不兼容。来源: JSer.info | [链接](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/)

- **npm 12 发布，默认禁用生命周期脚本** — npm 12 带来了重大安全变更：allowScripts 默认禁用，--allow-git/--allow-remote 默认设为 none。2FA 绕过漏洞修复，Granular Access Token 逐步淘汰。来源: JSer.info | [链接](https://github.com/npm/cli/releases/tag/v12.0.0)

- **Bun 用 Rust 重写，Zig 社区震惊** — Bun 的创建者 Jarred Sumner 分享了将 JavaScript 运行时从 Zig 移植到 Rust 的完整故事，借助 Claude Code 实例耗费约 $165k API 费用。Bun 1.4 将基于 Rust 版本。来源: JavaScript Weekly #794 | [链接](https://bun.sh/blog)

- **Vercel 收购 Better Auth** — 开源 TypeScript 认证库 Better Auth 被 Vercel 收购，将保持 MIT 许可，继续开发 Agent Auth Protocol，并融入 Vercel Connect 和 Eve 的 Agent 身份管理。来源: JSer.info | [链接](https://better-auth.com/blog/better-auth-joins-vercel)

- **Pete Hunt 回归领导 Next.js 项目** — Guillermo Rauch 宣布 Vercel 聘请了 Pete Hunt（早期 React 核心成员）和 Nick Schrock（GraphQL 联合创建者），Pete 将领导 Next.js 项目。来源: React Status #483 | [链接](https://react.statuscode.com/issues/483)

- **Chrome 150 发布** — CSS 新增 AccentColor/AccentColorText、polygon() 圆角支持、text-fit 属性；url() 支持 cross-origin()/integrity() 修饰符；focusgroup 属性、popover=hint 行为变更；WebGPU 新增 setImmediateData()。来源: JSer.info | [链接](https://developer.chrome.com/release-notes/150)

- **Next.js 宣布安全发布新策略** — 每月一次预公告安全发布，首批计划 2026 年 7 月 20 日发布 Next.js 16.2 和 15.5 的补丁。来源: JSer.info | [链接](https://nextjs.org/blog/next-security-release-program)

### ⚛️ React/前端框架

- **ReactBench：评估编码 Agent 写 React 的能力** — React Scan 和 Million.js 团队推出的基准测试，评估 AI 编码 Agent 在"真实 React 工作"中的表现。GPT 5.6 Sol 目前领先。来源: React Status #483 | [链接](https://react.statuscode.com/issues/483)

- **React 团队页面重构** — 围绕 Leadership Council 和工作组结构重组了官方团队页面。来源: React Status #483 | [链接](https://react.statuscode.com/issues/483)

- **shadcn/typeset: 全新排版系统** — 即插即用的 HTML 排版 CSS 系统，通过单个 CSS 文件和少量 CSS 变量驱动。来源: React Status #483 | [链接](https://ui.shadcn.com)

- **Jack Herrington 认为不再有理由选择 Next.js** — 45 分钟访谈中解释了为何全面转向 TanStack 方案。来源: React Status #483 | [链接](https://react.statuscode.com/issues/483)

- **Kent C. Dodds: 框架战争已结束** — 11 分钟视频解释了为何 React 未被替代。来源: React Status #483 | [链接](https://react.statuscode.com/issues/483)

- **Linaria 维护者构建新零运行时 CSS-in-JS 方案** — 维护 6 年 Linaria 后构建了 dx-styles，一个零运行时编译时替代方案。来源: React Status #483 | [链接](https://react.statuscode.com/issues/483)

- **Preact 11.0 Beta 2 发布** — 迁移指南已就绪，即将正式发布。来源: React Status #483 | [链接](https://react.statuscode.com/issues/483)

- **React Mosaic 7.0 发布** — 组件平铺"窗口管理器"，布局引擎大改。来源: React Status #483 | [链接](https://react.statuscode.com/issues/483)

### 📦 JavaScript/TypeScript

- **TypeScript 7.0 正式发布** — Go 原生移植，10x 速度提升。并行控制，重写 --watch，LSP 全面支持。但程序 API 尚未公开。来源: JSer.info | [链接](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/)

- **npm 12 发布** — 安全重大更新：allowScripts 默认禁用，--allow-git/--allow-remote 默认 none。来源: JSer.info | [链接](https://github.com/npm/cli/releases/tag/v12.0.0)

- **Bun 用 Rust 重写** — 借助 Claude Code 实例完成从 Zig 到 Rust 的移植，耗费约 $165k API 费用。来源: JavaScript Weekly #794 | [链接](https://bun.sh/blog)

- **Node.js v26.5.0 发布** — 新增 Blob.prototype.textStream()、--experimental-import-text、ReadableStreamTee 等。来源: JSer.info | [链接](https://nodejs.org/en/blog/release/v26.5.0)

- **Electron 43 发布** — Chromium 150、Node.js v24.17.0、V8 15.0 更新。启动性能优化。来源: JSer.info | [链接](https://www.electronjs.org/blog/electron-43-0)

- **pnpm 11.10 发布** — 新增 pnpm issues/pnpm prefix 命令，pnpm v12 兼容。来源: JSer.info | [链接](https://github.com/pnpm/pnpm/releases/tag/v11.10.0)

- **Fuse.js 7.3 发布** — 轻量级模糊搜索库，新增逐词模糊匹配和 Web Worker 分布式搜索。来源: JavaScript Weekly #780 | [链接](https://fusejs.io/)

- **Babylon.js 9.0 发布** — Microsoft 的 3D 渲染引擎，新增节点粒子编辑器、体积光照、高级高斯泼溅等。来源: JavaScript Weekly #780 | [链接](https://blogs.windows.com/windowsdeveloper/2026/03/26/announcing-babylon-js-9-0/)

### 🎨 CSS/样式

- **Chrome 150 CSS 新特性** — AccentColor/AccentColorText 系统色彩、polygon() 圆角支持、text-fit 属性等。来源: JSer.info | [链接](https://developer.chrome.com/release-notes/150)

- **MDN 推出 MCP 服务器** — 将 MDN 文档和浏览器兼容性数据直接带入编辑器/IDE。同时 light-dark() CSS 函数现在支持图片值。来源: MDN Blog | [链接](https://developer.mozilla.org/en-US/blog)

- **CSS is DOOMed: 用纯 CSS 渲染毁灭战士** — 用纯 CSS 渲染实现 1993 年《毁灭战士》的版本，游戏逻辑用 JavaScript。来源: JavaScript Weekly #780 | [链接](https://nielsleenheer.com/articles/2026/css-is-doomed-rendering-doom-in-3d-with-css/)

### 🔧 工具/构建

- **Cloudflare Workers Cache 发布** — Worker 前段可放置缓存，支持 Cache-Control/Vary，ctx.cache.purge() 支持标签/路径删除。来源: JSer.info | [链接](https://blog.cloudflare.com/workers-cache/)

- **Cloudflare 发布 EmDash** — Astro 驱动的"WordPress 精神继承者"，已重建 Cloudflare 博客。来源: React Status #483 | [链接](https://react.statuscode.com/issues/483)

- **Vite+ Beta 发布** — 统一 Vite、Vitest、Oxlint 等工具的 CLI，vp 单命令即可使用。来源: React Status #482 | [链接](https://react.statuscode.com/issues/482)

- **vinext 1.0 Beta: 在 Vite 上运行 Next.js 应用** — Cloudflare 用 AI 一周构建的 Next.js 克隆，经 1600+ PR 后达到 1.0 beta。来源: React Status #482 | [链接](https://react.statuscode.com/issues/482)

- **Blume: Markdown-first 文档站点生成器** — 基于 Astro 和 Vite，支持搜索、OpenAPI/AsyncAPI API 参考、MCP 服务器。来源: JSer.info | [链接](https://useblume.dev/)

- **unjs/httpxy: Node.js HTTP/WebSocket 代理库** — Fetch API 兼容的 proxyFetch、proxyUpgrade、createProxyServer。来源: JSer.info | [链接](https://github.com/unjs/httpxy)

### 🧪 测试/质量

- **ReactBench: React 编码 Agent 基准测试** — 评估 AI 模型在真实 React 场景中的编码能力，GPT 5.6 Sol 领先。来源: React Status #483 | [链接](https://react.statuscode.com/issues/483)

- **JetStream 3 基准测试发布** — WebKit、Google 和 Mozilla 联合推出最新版浏览器 JS/WASM 性能基准测试套件。来源: JavaScript Weekly #780 | [链接](https://webkit.org/blog/17899/introducing-the-jetstream-3-benchmark-suite/)

### 🤖 AI/机器学习

- **Vercel 收购 Better Auth** — 开源 TypeScript 认证库，将被整合到 Vercel 的 Agent 生态系统中。来源: JSer.info | [链接](https://better-auth.com/blog/better-auth-joins-vercel)

- **Hallmark: 反 AI 味的设计 Skill** — Together AI 出品，57 道反模板检测、20 个主题。来源: GitHub Trending | [链接](https://github.com/Nutlope/hallmark)

- **Safari 引入 MCP 服务器** — 最新预览版中，Safari 引入了 MCP 服务器，让 Agent 在调试期间控制 Safari 窗口。来源: React Status #482 | [链接](https://react.statuscode.com/issues/482)

- **MDN MCP 服务器发布** — 将 MDN 文档/浏览器兼容性数据直接带入 AI 编码工具。来源: MDN Blog | [链接](https://developer.mozilla.org/en-US/blog)

### 📚 周刊摘要

#### 阮一峰科技爱好者周刊 #404 - 你需要知道的 AI 内存知识

本期深入探讨了运行 AI 模型的内存硬件知识：RTX 5090（32GB 显存，104.8 TFLOPS）vs AMD Strix Halo（128GB 统一内存，14.8 TFLOPS）。独显算力是板载方案的 7 倍，但显存小。内存带宽是关键：RTX 5090 带宽 1792GB/s，AMD 仅 256GB/s。还讨论了命名规范建议（采用 has-/can-/should- 前缀）、OpenAI 推出便捷键盘、AI 倦怠的四个阶段等话题。

**工具推荐**：WhatCable（macOS USB-C 电缆检测）、GPU OCR（高速文字识别）
来源: 阮一峰博客 | [链接](https://www.ruanyifeng.com/blog/2026/07/weekly-issue-404.html)

#### JavaScript Weekly #794 - npm 12、TypeScript 7 和 Bun in Rust

Bun 从 Zig 到 Rust 移植完整故事（$165k API 费用）、npm 12 生命周期脚本默认禁用、TypeScript 7 的 10x 速度提升、Better Auth 加入 Vercel、JetStream 3 浏览器基准测试、ECMAScript 2026 新特性、Svelte 月度更新、Cloudflare EmDash。
来源: JavaScript Weekly | [链接](https://javascriptweekly.com/latest)

#### JSer.info #776 - TypeScript 7.0、npm 12、Next.js 安全策略

TypeScript 7.0 Go 原生移植、npm 12 安全重大变更、Next.js 安全发布策略（每月一次预公告）、Chrome 150 CSS 新特性、Electron 43、Node.js v26.5、Cloudflare Workers Cache、Better Auth 加入 Vercel。工具推荐：Blume、ttsc、ant、Wordgard、virtua、httpxy。
来源: JSer.info | [链接](https://jser.info/2026/07/17/typescript-7.0-npm-12-next.js/)

#### Frontend Focus #750 - 前端还需要构建工具吗？

对 2026 年构建工具的功能逐一审计：Vendor prefixing 和 ES5 转译正在过时，Sass 功能也在减少。
来源: Frontend Focus | [链接](https://frontendfoc.us/latest)

### 🚀 Hacker News 热门

- **Super Dario** (393 pts) — 超级马里奥风格游戏 [链接](https://superdario.pawb.de)
- **Opening lines of famous literary works** (179 pts) — 著名文学作品开场白 [链接](https://www.verbaprima.com/)
- **SSH Honeypot live** (172 pts) — 实时观看机器人与 SSH 蜜罐交互 [链接](https://honeypotlive.cc/)
- **misa77 编解码器** (164 pts) — 比 LZ4 快 2 倍的解压缩，5219 MB/s [链接](https://github.com/welcome-to-the-sunny-side/misa77)
- **IKEA Complexity Index** (137 pts) — IKEA 产品复杂度指数 [链接](https://ikea.greg.technology/)
- **C++26 Reflection Type Erasure** (117 pts) — C++26 反射实现类型擦除 [链接](https://ryanjk5.github.io/posts/rjk-duck/)
- **4M Wikipedia events timeline** (108 pts) — 400 万维基百科事件可缩放时间线 [链接](https://app.everything.diena.co/)
- **YouTube Guitar Tab Parser** (108 pts) — 视频转 PDF 吉他谱 CLI [链接](https://github.com/marcelpanse/youtube-guitar-tab-parser)
- **RL agent trains models** (107 pts) — 强化学习训练 Agent 训练模型，$1.3k [链接](https://github.com/Danau5tin/ai-trains-ai)
- **Jacquard 编程语言** (102 pts) — 为 AI 而生的新语言 [链接](https://github.com/jbwinters/jacquard-lang)
- **Nobie** (96 pts) — Excel 兼容运行时 [链接](https://nobie.com)
- **Leaves** (90 pts) — 文本界面磁盘 Treemap 可视化 [链接](https://github.com/patonw/leaves)
- **Hackney** (96 pts) — 比较 Uber/Lyft/Waymo/Robotaxi 价格 [链接](https://hackney.app)

### ⭐ GitHub 热门

- **Nutlope/hallmark** — 反 AI 味设计 Skill，Together AI 出品 [链接](https://github.com/Nutlope/hallmark)
- **samchon/ttsc** — TypeScript Go 工具链，500x 更快 Lint [链接](https://github.com/samchon/ttsc)
- **theMackabu/ant** — C 实现的小型 JavaScript Runtime [链接](https://github.com/theMackabu/ant)
- **inokawa/virtua** — ~3kB 虚拟列表/网格组件，支持 React/Vue/Solid/Svelte [链接](https://github.com/inokawa/virtua/)
- **unjs/httpxy** — Node.js 全功能 HTTP/WebSocket 代理库 [链接](https://github.com/unjs/httpxy)

### 📌 其他动态

- **react-dropzone 17.0** — 基于 Hook 的文件拖放区域库 [链接](https://react-dropzone.js.org/)
- **react-fontawesome 3.4** — 支持 Font Awesome 7.3 新动画 [链接](https://react.statuscode.com/issues/483)
- **React Hook Form 7.81.0** — 新增 FieldArray 组件 [链接](https://react.statuscode.com/issues/482)
- **React Router 8.2.0** — 最新版本发布 [链接](https://react.statuscode.com/issues/482)
- **React Native 0.87 RC** — 候选版本发布 [链接](https://react.statuscode.com/issues/482)
- **Neutralinojs 6.7** — 跨平台桌面应用框架 [链接](https://github.com/neutralinojs/neutralinojs)
- **TinyBase v8.1** — 响应式数据存储，新增原生 Svelte 5 支持 [链接](https://tinybase.org/)
- **Verdaccio 6.4** — 自托管私有 npm 注册表 [链接](https://github.com/verdaccio/verdaccio)

---

📅 抓取时间: 2026-07-19 22:00
📡 数据源: 10/10 成功
