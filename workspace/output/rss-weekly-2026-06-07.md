---
layout: default
title: 前端技术周报 (2026-06-07)
date: 2026-06-07
category: RSS 周报
---

## 📰 前端技术周报 (2026-06-07)

### 📝 本周要点

- **React Compiler Rust 端即将合并** - Meta 内部测试效果良好，预计下周合并主分支
  来源: React Status #477 | [链接](https://github.com/facebook/react/pull/36173#issuecomment-4608356402)

- **VoidZero（Vite/Vitest 母公司）加入 Cloudflare** - 核心构建工具链团队并入 Cloudflare
  来源: React Status #477 | [链接](https://blog.cloudflare.com/voidzero-joins-cloudflare/)

- **Chrome 149 正式支持 DevTools MCP Server** - AI 工具可编程驱动调试和性能审计
  来源: Frontend Focus #744 | [链接](https://developer.chrome.com/blog/new-in-devtools-149)

- **HTML-in-Canvas API 开启 Origin Trial** - 可在 Canvas 中渲染交互式 HTML/CSS
  来源: Frontend Focus #744 | [链接](https://developer.chrome.com/blog/html-in-canvas-origin-trial)

- **State of AI 2026 调查结果发布** - TypeScript 首次超过 JavaScript，AI 生成代码占比达 54%
  来源: FE News / JavaScript Weekly | [链接](https://2026.stateofai.dev/en-US)

- **TanStack npm 供应链攻击安全事件** - 42 个包 84 个恶意版本，6 分钟内完成攻击
  来源: FE News | [链接](https://tanstack.com/blog/npm-supply-chain-compromise-postmortem)

- **Declarative Partial Updates API** - Chrome 148 实验性推出 HTML 流式部分更新
  来源: FE News | [链接](https://developer.chrome.com/blog/declarative-partial-updates)

### ⚛️ React/前端框架

- **React Compiler Rust Port 即将合并** - React 核心团队的 Hanlon 和 Savona 表示 Meta 内部测试效果出色，预计下周合并。现在可以提前测试 Rust 版本的 React Compiler。
  来源: React Status #477 | [链接](https://github.com/facebook/react/pull/36173#issuecomment-4608356402)

- **React Spectrum 1.4 发布** - Adobe 的完整 React 设计系统发布 v1.4，新增集合组件拖放支持、`TableView` 高亮选择和 `TableFooter` 等。
  来源: React Status #477 | [链接](https://react-spectrum.adobe.com/releases/v1-4-0)

- **React 19.2.7 / 19.1.8 / 19.0.7 修复 Server Actions 回归问题** - 小版本补丁修复了 Server Actions 的回归 bug。
  来源: React Status #477 | [链接](https://github.com/facebook/react/releases/tag/v19.2.7)

- **React Router 安全更新** - v7.16.0、v6.30.4 和 Remix 2.17.5 修复了 7 个安全漏洞。
  来源: React Status #477 | [链接](https://github.com/remix-run/react-router/security/advisories)

- **shadcn/ui 新增 eject 命令和 GitHub 注册表支持** - `eject` 可将 shadcn 的 Tailwind 代码内联到你的 CSS 中，GitHub 公共仓库可作为组件注册表。
  来源: React Status #477 | [链接](https://ui.shadcn.com/docs/cli#eject)

- **Lovable 切换到 TanStack Start** - 流行的 AI 建站工具 Lovable 默认使用 TanStack Start 构建 AI 生成的应用。
  来源: React Status #477 | [链接](https://lovable.dev/blog/building-apps-using-tanstack-start)

- **react-call 2.0：将组件变成可 await 的异步函数** - 适用于选择器、确认框、对话框等需要返回值的场景，v2 新增 HMR 持久化。
  来源: React Status #477 | [链接](https://github.com/desko27/react-call)

- **ESLint "You Might Not Need An Effect" 1.0** - 检测 React 中不必要使用 Effect 的 ESLint/Oxlint 插件。
  来源: React Status #477 | [链接](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect)

- **Component Architecture for React Server Components** - 探讨 RSC 如何优化页面架构的深度文章。
  来源: React Status #477 | [链接](https://aurorascharff.no/posts/component-architecture-for-react-server-components/)

- **The Conductor Rewrite：React 性能优化实战** - 深入剖析 Mac 应用 Conductor 如何通过重渲染优化、路由选择和虚拟化实现 2 倍性能提升。
  来源: React Status #477 | [链接](https://performance.dev/the-conductor-rewrite)

- **Mantine 9.3** - 大型 React 组件库发布新版本，新增响应式分页、文本换行控制、可调整大小的分隔面板等。
  来源: React Status #477 | [链接](https://mantine.dev/changelog/9-3-0/)

### 📦 JavaScript/TypeScript

- **TypeScript 在 State of AI 2026 中首次超过 JavaScript** - TypeScript（5,360人）超越 JavaScript（4,831人）成为开发者最常用的语言。
  来源: FE News / JavaScript Weekly | [链接](https://2026.stateofai.dev/en-US)

- **Node.js 26.3.0 发布** - npm 升级到 11.16.0，macOS x64 降级为 Tier 2 平台，QUIC 大量改进。
  来源: JavaScript Weekly #788 | [链接](https://javascriptweekly.com/link/185967/web)

- **Ember 7.0 发布** - 长期框架的重大版本更新，移除废弃功能。
  来源: JavaScript Weekly #788 | [链接](https://javascriptweekly.com/link/185966/web)

- **Astro 6.4 发布** - 新增可插拔 Markdown 流水线、基于 Rust 的 Markdown 处理器、Cloudflare 高级路由辅助。
  来源: JavaScript Weekly #788 | [链接](https://javascriptweekly.com/link/185969/web)

- **date-fns v4.4 发布，v5.0 进入 Alpha** - 为未来 TC39 Temporal API 做准备，成为"Temporal-first"库。
  来源: JavaScript Weekly #788 | [链接](https://javascriptweekly.com/link/186009/web)

- **Anders Hejlsberg 在 The Pragmatic Engineer 播客** - TypeScript 之父畅谈 TypeScript、JavaScript 的优缺点以及他如何使用 AI。
  来源: JavaScript Weekly #788 | [链接](https://javascriptweekly.com/link/186012/web)

- **Hocuspocus 4：为任何应用添加实时协作** - 基于 Yjs 的实时协作后端，支持 Node、Bun、Deno 和 Cloudflare Workers。
  来源: JavaScript Weekly #788 | [链接](https://javascriptweekly.com/link/185959/web)

- **PGlite 0.5：浏览器中运行 Postgres** - WASM 中运行 Postgres 数据库，升级到 Postgres 18.3，支持响应式和实时同步。
  来源: JavaScript Weekly #788 | [链接](https://javascriptweekly.com/link/185996/web)

- **npm 11.16.0 引入 opt-in 安装脚本策略** - 使用 `allowScripts` 支持可选安装脚本策略（目前仅警告）。
  来源: JavaScript Weekly #788 | [链接](https://javascriptweekly.com/link/185962/web)

- **Red Hat npm 包被后门攻击** - 数十个 Red Hat npm 包被发现被植入后门。
  来源: JavaScript Weekly #788 | [链接](https://javascriptweekly.com/link/186017/web)

- **Using AI to Write Better Code More Slowly** - Nolan Lawson 的文章指出 LLM 不仅可以快速生成代码，更可以帮助开发者更"慢"地写出更高质量的代码。
  来源: JavaScript Weekly #788 | [链接](https://javascriptweekly.com/link/185974/web)

- **How to Evaluate an npm Package: 2026 Edition** - 2026 年评估 npm 包的实用清单，涵盖来源证明、安装脚本、CI 质量等。
  来源: JavaScript Weekly #788 | [链接](https://javascriptweekly.com/link/185961/web)

### 🎨 CSS/样式

- **Chrome 149 支持 CSS gap decorations** - 可对 flex 和 grid 项目之间的空白区域进行样式修饰。
  来源: Frontend Focus #744 | [链接](https://developer.chrome.com/blog/new-in-chrome-149)

- **PolyCSS：用 CSS 在 DOM 中渲染 3D 网格** - 使用 CSS `matrix3d()` 变换渲染纹理 3D，无需 WebGL 或 Canvas。
  来源: Frontend Focus #744 | [链接](https://polycss.com/)

- **Revealing Text with CSS `letter-spacing`** - CSS-Tricks 文章探讨利用 `letter-spacing` 实现文本动画效果。
  来源: Frontend Focus #744 | [链接](https://css-tricks.com/revealing-text-with-css-letter-spacing/)

- **Algorithmic Theming Engines 与 `contrast-color()`** - 构建自校正色彩系统的方案。
  来源: Frontend Focus #744 | [链接](https://www.smashingmagazine.com/2026/05/building-self-correcting-color-systems-contrast-color/)

- **Curlwind：无需构建的 Tailwind 工具类生成器** - 通过查询参数按需生成所需类，无需构建步骤。
  来源: Frontend Focus #744 | [链接](https://curlwind.com/)

- **Fontastic Space：寻找数学最优的字体配对** - 基于大写高度、上升部差异等多维度匹配的字体搭配工具。
  来源: Frontend Focus #744 | [链接](https://fontastic.space/)

### 🔧 工具/构建

- **VoidZero 加入 Cloudflare** - Vite、Vitest、Rolldown、Oxc 的母公司 VoidZero 正式加入 Cloudflare，将构建工具链带入 Cloudflare 生态。
  来源: React Status #477 | [链接](https://blog.cloudflare.com/voidzero-joins-cloudflare/)

- **ESLint 10.4.1 发布** - JavaScript 生态系统中最流行的 linter 更新。
  来源: JavaScript Weekly #788 | [链接](https://javascriptweekly.com/link/185972/web)

- **Expo UI 正式版发布** - 从 JavaScript 使用原生 SwiftUI 和 Jetpack Compose，一个 import 即可跨平台。
  来源: JavaScript Weekly #788 | [链接](https://javascriptweekly.com/link/185985/web)

- **Component Party：UI 框架对比大全** - 流行框架代码片段对比，新增 Ripple、Ember Polaris 支持。
  来源: JavaScript Weekly #788 | [链接](https://component-party.dev/)

- **tsParticles 4：粒子引擎** - 支持所有主流框架和原生 JS，实现五彩纸屑、烟花、萤火虫等特效。
  来源: JavaScript Weekly #788 | [链接](https://javascriptweekly.com/link/185987/web)

- **TinyBase 8.4** - 响应式数据存储和同步引擎，本地优先应用。新增完整 SolidJS 支持。
  来源: JavaScript Weekly #788 | [链接](https://javascriptweekly.com/link/185997/web)

- **Fuse.js 7.4** - JavaScript 模糊搜索库，v7.4 新增 Web Workers 驱动的并行搜索。
  来源: JavaScript Weekly #788 | [链接](https://javascriptweekly.com/link/185992/web)

- **MarkItDown：微软开源文件转 Markdown 工具** - PDF、Office、图片等格式转 Markdown，LLM 处理管道优化。GitHub 135k stars。
  来源: FE News | [链接](https://github.com/microsoft/markitdown)

- **Wave Terminal：AI 开源终端** - 支持 SSH、远程文件编辑、内嵌 VSCode 编辑器、Dashboards。
  来源: FE News | [链接](https://www.waveterm.dev/)

### ⚡ 性能优化

- **Frontend's Missing Metric: The TBT Window** - Harry Roberts 提出追踪 FCP 到 TTI 之间的"TBT Window"，因为 TBT 指标的变化可能来自 FCP/TTI 移动而非实际阻塞工作变化。
  来源: Frontend Focus #744 | [链接](https://csswizardry.com/2026/06/front-ends-missing-metric-the-tbt-window/)

- **Container Timing API 开启 Origin Trial** - Chrome 148 起，Widget、卡片等组件级别的渲染完成时间测量，比 LCP 更精细化。
  来源: FE News | [链接](https://developer.chrome.com/blog/container-timing-origin-trial)

- **Intentionally Blocking Rendering with JavaScript** - 有时故意使用 `blocking="render"` 阻止渲染，可以避免 JavaScript 测量前的布局闪烁。
  来源: Frontend Focus #744 / JavaScript Weekly | [链接](https://www.jayfreestone.com/writing/intentional-render-blocking-javascript/)

- **Source Maps 完全指南** - 源码映射的工作原理及安全注意事项，避免暴露代码库。
  来源: React Status #477 | [链接](https://neciudan.dev/everything-you-need-to-know-about-sourcemaps)

### 🤖 AI/机器学习

- **State of AI 2026 调查结果** - 7,258 名开发者参与。AI 生成代码占比平均 54%（去年 28%），其中 47% 会被重构。代码编辑器排名：VS Code(4,667)、Cursor(1,770)、Zed(964)。编码 Agent：GitHub Copilot(67.9%)、Claude Code(62.9%)、OpenAI Codex(34.5%)。模型使用率：ChatGPT(88.4%)、Claude(82.1%)、Gemini(72.6%)。
  来源: FE News / JavaScript Weekly | [链接](https://2026.stateofai.dev/en-US)

- **Chrome 149 DevTools MCP Server 正式版** - AI 编码工具可编程驱动 Chrome DevTools 进行调试和性能审计。
  来源: Frontend Focus #744 | [链接](https://developer.chrome.com/blog/new-in-devtools-149)

- **Redesigning Workflows for AI** - Jakob Nielsen 基于 515 家初创公司研究，指出 AI 不应只嵌入现有流程而应重新设计整个工作流，可带来营收 90% 增长。
  来源: FE News | [链接](https://www.uxtigers.com/post/workflow-redesign)

- **Uber uSpec：AI Agent 自动化设计规范** - 利用 Cursor IDE + Figma MCP，数周的工作缩短到 2 分钟内完成，并开源给社区。
  来源: FE News | [链接](https://www.uber.com/ca/en/blog/automate-design-specs/)

- **AI Has Created a Code Overload（纽约时报）** - AI 工具使月代码产出增长 10 倍，但审查队列超 100 万行，代码瓶颈问题严重。
  来源: FE News | [链接](https://www.nytimes.com/2026/04/06/technology/ai-code-overload.html)

- **A2UI：Google 开源的 AI Agent UI 协议** - 安全声明式 UI 格式，AI Agent 只能使用批准组件，跨框架渲染。
  来源: FE News | [链接](https://a2ui.org/)

- **Rapid-MLX：Apple Silicon 本地 AI 推理工具** - 比 Ollama 快 4.2 倍，Qwen3.5-4B 达 160 tokens/s。
  来源: FE News | [链接](https://github.com/raullenchai/Rapid-MLX)

- **Multica：开源 AI Agent 管理平台** - 像管理团队成员一样管理 AI 编码 Agent，支持 Claude Code、Copilot、Codex、Gemini。
  来源: FE News | [链接](https://github.com/multica-ai/multica)

- **하네스 엔지니어링 백과사전（Harness Engineering 百科）** - 关于如何设计 AI Agent 工作环境的韩文在线书籍。
  来源: FE News | [链接](https://wikidocs.net/book/19689)

- **Code Wiki：Gemini 驱动的仓库文档生成** - 自动生成自然语言摘要和架构图，随时保持最新的仓库文档。
  来源: Frontend Focus #744 | [链接](https://codewiki.google/)

- **Microsoft Edge 扩展设备端 AI 能力** - 新的浏览器端模型和 API。
  来源: Frontend Focus #744 | [链接](https://blogs.windows.com/msedgedev/2026/06/02/expanding-on-device-ai-in-microsoft-edge-new-models-and-apis-for-the-web/)

### 🔒 安全

- **TanStack npm 供应链攻击安全事件** - 2026 年 5 月 11 日，42 个 npm 包 84 个恶意版本在 6 分钟内被发布。恶意代码窃取 AWS、GCP、GitHub 凭据并自我传播。根本原因是 `pull_request_target` 权限提升 + GitHub Actions 缓存投毒 + OIDC 令牌提取。1 小时 43 分钟内所有恶意版本被下架。
  来源: FE News | [链接](https://tanstack.com/blog/npm-supply-chain-compromise-postmortem)

- **React Router 安全漏洞修复** - v7.16.0、v6.30.4 和 Remix 2.17.5 修复了 7 个安全漏洞。
  来源: React Status #477 | [链接](https://github.com/remix-run/react-router/security/advisories)

- **Red Hat npm 包被后门植入** - 数十个 Red Hat npm 包被发现恶意代码。
  来源: JavaScript Weekly #788 | [链接](https://javascriptweekly.com/link/186017/web)

- **新型用户追踪技术：利用 OPFS 分析 SSD 使用** - 利用 Origin Private File System 功能实现的绕过式用户追踪方法。
  来源: JavaScript Weekly #788 | [链接](https://javascriptweekly.com/link/185965/web)

### 🎯 GitHub/开源

- **GitHub CLI 扩展 gh-stack：官方支持 Stacked PR** - GitHub 官方 CLI 扩展，管理分支链和堆叠 PR。目前 Private Beta。
  来源: FE News | [链接](https://github.com/github/gh-stack)

- **ccstatusline：Claude Code 状态行格式化工具** - 实时显示模型名、分支、Token 用量、会话费用等信息。
  来源: FE News | [链接](https://github.com/sirmalloc/ccstatusline)

- **Clawd on Desk：AI 编码 Agent 桌面宠物** - 像素动画显示 Agent 状态（空闲、思考、构建等），支持 Allow/Deny 弹窗。
  来源: FE News | [链接](https://github.com/rullerzhou-afk/clawd-on-desk)

- **Microsoft MarkItDown** - 文件转 Markdown 工具，GitHub 135k stars。
  来源: FE News | [链接](https://github.com/microsoft/markitdown)

- **Vim Hero：交互式 Vim 学习平台** - 无需安装直接在浏览器中学习 Vim，50+ 课程。
  来源: FE News | [链接](https://www.vim-hero.com/)

### 🌐 浏览器/Web 标准

- **Declarative Partial Updates API** - Chrome 148 实验性功能：`<template for>` + `<?marker>` 实现 HTML 流式非顺序更新；新的 `setHTML()`、`streamHTML()`、`appendHTML()` API。npm 上已有 polyfill。
  来源: FE News | [链接](https://developer.chrome.com/blog/declarative-partial-updates)

- **HTML-in-Canvas API Origin Trial** - Chrome 中可在 Canvas 中渲染交互式 HTML/CSS，结合 DOM 和 Canvas 优势。
  来源: Frontend Focus #744 | [链接](https://developer.chrome.com/blog/html-in-canvas-origin-trial)

- **What's New in Web UI（Google I/O 2026）** - Una Kravets 和 Bramus 展示滚动驱动动画、元素级 View Transitions、CSS `@function`、`contrast-color()`、Style Queries、HTML-in-Canvas 等。
  来源: FE News | [链接](https://www.youtube.com/watch?v=uT7MVcCQ4rw)

- **Chrome 149 新功能** - CSS gap decorations、DevTools MCP Server 正式版、浏览器内置 AI API 扩展。
  来源: Frontend Focus #744 | [链接](https://developer.chrome.com/blog/new-in-chrome-149)

- **VS Code 1.123 改进内置浏览器** - 新增书签功能和更多截图方式。
  来源: Frontend Focus #744 | [链接](https://code.visualstudio.com/updates/v1_123#_integrated-browser)

- **Accessible Split-Cell Table Headers** - Eric Meyer 讲解如何实现可访问的分割单元格表头。
  来源: Frontend Focus #744 | [链接](https://meyerweb.com/eric/thoughts/2026/05/28/accessible-i-think-split-cell-table-headers/)

### 📚 周刊摘要

#### FE News 2026-06（6月4日发布）

本期 FE News 涵盖大量 Web 平台新特性、AI 生态调查和安全事件。主要内容：

**核心文章**：

- **Declarative Partial Updates** - Chrome 148 实验性 API，实现 HTML 流式部分更新，包括 Out-of-Order Streaming（`<template for>` + `<?marker>`）和 HTML Insertion Methods（`setHTML()`、`streamHTML()`、`appendHTML()`）。npm 已有 polyfill。
  [链接](https://developer.chrome.com/blog/declarative-partial-updates)

- **State of AI 2026** - Devographics 年度调查，7,258 人参与。TypeScript 首超 JavaScript，AI 生成代码占比 54%。Cursor 跃升至编辑器第二。Claude Code 满意度最高。
  [链接](https://2026.stateofai.dev/en-US)

- **TanStack 供应链攻击事后分析** - 42 个包被篡改，攻击仅 6 分钟完成，窃取云凭据。原因是 GitHub Actions 工作流配置漏洞。
  [链接](https://tanstack.com/blog/npm-supply-chain-compromise-postmortem)

- **Container Timing API Origin Trial** - Chrome 148 起，组件级性能测量，超越 LCP 的限制。
  [链接](https://developer.chrome.com/blog/container-timing-origin-trial)

- **What's New in Web UI (Google I/O 2026)** - 滚动驱动动画、CSS `@function`、`contrast-color()`、View Transitions 等新特性。
  [链接](https://www.youtube.com/watch?v=uT7MVcCQ4rw)

**代码与工具**：
- **Wave Terminal** - AI 开源终端，SSH、远程编辑、Dashboards [链接](https://www.waveterm.dev/)
- **tegaki** - 所有字体转为动画手写体的库，支持 React/Vue/Svelte/SolidJS/Astro [链接](https://github.com/KurtGokhan/tegaki)
- **A2UI** - Google 开源 AI Agent UI 协议，声明式安全 UI 生成 [链接](https://a2ui.org/)
- **ccstatusline** - Claude Code 状态行工具 [链接](https://github.com/sirmalloc/ccstatusline)
- **Clawd on Desk** - AI 编码 Agent 桌面宠物 [链接](https://github.com/rullerzhou-afk/clawd-on-desk)
- **gh-stack** - GitHub CLI Stacked PR 扩展 [链接](https://github.com/github/gh-stack)
- **Meetily** - 本地 AI 会议助手，隐私优先 [链接](https://github.com/Zackriya-Solutions/meetily)
- **whatcani.run** - Apple Silicon AI 模型基准平台 [链接](https://www.whatcani.run/)
- **Mesurer** - React 测量覆盖工具 [链接](https://mesurer.ibelick.com/)
- **MarkItDown** - 微软文件转 Markdown [链接](https://github.com/microsoft/markitdown)
- **Rapid-MLX** - Apple Silicon 快速本地 AI 推理 [链接](https://github.com/raullenchai/Rapid-MLX)
- **Multica** - AI Agent 管理平台 [链接](https://github.com/multica-ai/multica)

#### 阮一峰科技爱好者周刊（第 399 期）：中国 AI 大厂访问记

本期以"中国 AI 大厂访问记"为主题，详细记录了美国访问团对中国 14 家 AI 和机器人公司的访问观感。

**核心内容摘要**：

- **算力差距** - 中国 AI 算力约为美国的 1/8，相当于美国 2023 年水平。华为 Ascend 950PR 性能仅与 2022 年 H100 相当。英伟达已出货 700 万颗 Hopper/Blackwell GPU，华为今年计划仅 75 万颗。
  [链接](https://www.ruanyifeng.com/blog/2026/06/weekly-issue-399.html)

- **计算效率逆袭** - 芯片管制倒逼中国公司提高效率，单位算力支持的 AI 智能是简单扩展下的 4-7 倍，弥补了算力差距。

- **开源分歧** - 万亿参数模型是否开源成为分水岭。一些公司认为万亿参数模型开源是资源浪费，另一些公司把开源视为信仰。

- **字节跳动 Seed 部门最受敬畏** - 国内唯一闭源 AI 前沿团队，豆包几乎垄断 AI 用户流量。

- **AI 行业年轻化** - 中国 AI 公司大量使用 25-26 岁的博士生"实习生"，可享有完整权限和工作实验自由。

- **数据产业缺失** - 中国几乎没有 AI 训练数据产业，公司自行准备数据或使用内部标注团队。

- **政府推动** - 上海、北京、杭州市政府是 AI 领域的真正推动者，被"错失恐惧"驱动。

**文章精选**：
- **I Can't Afford My AI** - 作者用 AI 找编译器 Bug，发现 AI 费用比工资高一个数量级 [链接](https://newsletter.semianalysis.com/p/finding-miscompiles-for-fun-not-profit)
- **HTML 替代 JS 的四种场景** - 弹框和浮层等场景可纯用 HTML 实现 [链接](https://www.htmhell.dev/adventcalendar/2025/27/)
- **负载均衡节点健康检查** - 客户端 vs 服务端负载均衡的区别 [链接](https://singh-sanjay.com/2026/01/12/health-checks-client-vs-server-side-lb.html)

**工具推荐**：
- **Penpot** - 开源 Figma 替代，可视化布局转 CSS/HTML [链接](https://github.com/penpot/penpot)
- **readNeo** - 微信读书数据面板 [链接](https://github.com/extrastu/readneo)
- **AppPorts** - macOS 应用迁移到外置存储 [链接](https://github.com/wzh4869/AppPorts)
- **pixtuoid** - 像素小人展示 AI Agent 终端动画 [链接](https://github.com/IvanWng97/pixtuoid)
- **Nginx Proxy Manager** - Web 管理 Nginx 反向代理和 SSL [链接](https://github.com/NginxProxyManager/nginx-proxy-manager)

---

📅 抓取时间: 2026-06-07 17:00
📡 数据源: 10/10 成功
