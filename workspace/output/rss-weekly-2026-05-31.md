---
layout: default
title: 前端技术周报 (2026-05-31)
date: 2026-05-31
category: RSS 周报
---

## 📰 前端技术周报 (2026-05-31)

### 📝 本周要点

- **npm 与 pnpm 推出分阶段发布 (Staged Publishing)** - npm CLI v11.15.0 和 pnpm 11.3 同时支持分阶段发布模型，包在正式上线 npm registry 前需经过审批步骤，有效防范供应链攻击。来源: JavaScript Weekly, JSer.info | [链接](https://docs.npmjs.com/staged-publishing)
- **React 13 岁了——社区热议"还有人喜欢 React 吗？"** - React 于 2013 年 5 月 29 日首次发布，David Bushell 长期收集开发者对 React 的怨言记录，引发 Hacker News 广泛讨论。来源: React Status, Frontend Focus | [链接](https://react.statuscode.com/issues/476)
- **Token 费用难以负担：AI 编程比人类程序员更昂贵** - OpenAI 员工月消耗 6030 亿 Token（约 130 万美元），Uber 4 个月花完全年 34 亿美元 AI 预算，微软因费用超标放弃 Claude Code。阮一峰分析认为 AI 不会大规模替代程序员。来源: 阮一峰博客 | [链接](http://www.ruanyifeng.com/blog/2026/05/weekly-issue-398.html)
- **Deno 2.8 发布："最大的一次小版本更新"** - Node.js 兼容性从 42% 跃升至 76.4%（超过 Bun），新增 `audit fix`、`pack`、`why` 等子命令，支持 `import defer`，`npm:` 前缀不再必需，性能全面大幅提升。来源: JavaScript Weekly, JSer.info | [链接](https://deno.com/blog/v2.8)
- **Yelp 从 Webpack 迁移到 Rspack，构建时间减半** - 分享迁移实践，重点讨论了 barrel files（桶文件）和 re-exports 的性能影响。来源: JavaScript Weekly | [链接](https://engineeringblog.yelp.com/2026/05/optimizing-our-build-times-by-migrating-from-webpack-to-rspack.html)

---

### ⚛️ React/前端框架

- **TanStack Router 与 TanStack Query 搭配使用** - Dominik Dorfmeister 系列文章最新篇，解释 Router 缓存是 per-route 而 Query 缓存是全局的，让 Query 管理数据层、Router 专注于路由更合适。来源: React Status | [链接](https://react.statuscode.com/issues/476)
- **TanStack Start 延迟水合 (Deferred Hydration) 解析** - Jack Herrington 分析该特性延迟首屏以下组件的水合直到需要时才执行，认为这是对 React 已有能力的语法糖封装，但值得使用。来源: React Status | [链接](https://react.statuscode.com/issues/476)
- **React Router 7.16.0 发布** - 作为 v8 的过渡版本，稳定了 `trailing-slash data-request` 标志，并对未启用的 v8 标志发出警告。来源: React Status | [链接](https://react.statuscode.com/issues/476)
- **Expo UI 进入稳定版** - 一个 import 即可在 iOS 上使用 SwiftUI、Android 上使用 Jetpack Compose 渲染原生组件。SDK 56 同步发布，Expo UI 已可投入生产。来源: React Status, JavaScript Weekly | [链接](https://react.statuscode.com/issues/476)
- **React Native Reanimated 4.4** - 新增 iOS CSS 动画引擎，通过 Core Animation 而非 JS 驱动的更新循环运行动画。React Native Gesture Handler 3.0 也同步发布，专为新架构重建。来源: React Status | [链接](https://react.statuscode.com/issues/476)
- **Fate 1.0：前 Jest 负责人打造的 React 数据框架** - Christoph Nakazawa（前 Meta 工程师）出品，基于 tRPC 或 HTTP 提供标准化缓存、视图协同定位和单根请求组合，1.0 新增 SSE 实时视图和 Vite 插件。来源: React Status, JavaScript Weekly, JSer.info | [链接](https://fate.technology)
- **Angular 22 RC** - 最终版预计 6 月初发布，亮点包括基于 signal 的表单和 OnPush 变更检测策略成为默认。来源: JavaScript Weekly | [链接](https://javascriptweekly.com/issues/787)
- **Apollo Client 4.2.0** - 新增 `RefetchEventManager` 类，支持在窗口聚焦或网络重连时自动重新获取查询；hook 和方法签名改进以反映 `defaultOptions`。来源: JSer.info | [链接](https://github.com/apollographql/apollo-client/releases/tag/%40apollo%2Fclient%404.2.0)
- **React Data Table v8.3** - 简洁灵活的表格组件，内置列排序和分页，v8.3 聚焦本地化支持。来源: React Status | [链接](https://reactdatatable.com)
- **pip-it-up：将任意组件弹入 PiP 浮动窗口** - 利用 Document Picture-in-Picture API 将 React 组件弹入画中画窗口。来源: React Status | [链接](https://pip-it-up.vercel.app)
- **Spoiled 0.5：React 剧透组件** - 在内容上显示粒子云遮挡，点击后揭示的动画效果组件。来源: React Status | [链接](https://spoiled.vercel.app)

---

### 📦 JavaScript/TypeScript

- **npm & pnpm 分阶段发布正式上线** - npm 11.15.0 和 pnpm 11.3 均支持 `stage` 命令，包发布前需维护者 2FA 审批。npm 还新增 `--allow-git`/`--allow-file`/`--allow-directory`/`--allow-remote` 控制安装来源。来源: JavaScript Weekly, JSer.info | [链接](https://javascriptweekly.com/issues/787)
- **pnpm 11.1~11.3 系列安全增强** - 新增 `pnpm audit signatures` 验证注册表签名，安装时按 `minimumReleaseAge` 重新验证 lockfile 条目，`minimumReleaseAgeStrict` 严格模式，以及 `trustLockfile` 免验证受信任文件。来源: JSer.info | [链接](https://pnpm.io/blog/releases/11.3)
- **Deno 2.8 全面升级** - Node.js 兼容性 76.4%、`deno audit fix` 自动修复漏洞、`deno pack` 构建 npm 包、`deno why` 查看依赖原因、Chrome DevTools 可检查网络流量和 CPU 分析、`catalog:` 协议统一管理 monorepo 依赖版本。来源: JavaScript Weekly, JSer.info | [链接](https://deno.com/blog/v2.8)
- **Chrome 推出声明式部分更新 (Declarative Partial Updates)** - `<template for>` 实现无 JS 的模板渲染，`setHTML()` 和 `streamHTML()` 安全地将 HTML 块乱序流式写入 DOM。Chrome 148 实验性支持，已有 polyfill。来源: JavaScript Weekly, Frontend Focus | [链接](https://developer.chrome.com/blog/declarative-partial-updates)
- **Node.js 26.2.0 (Current) 发布** - `fs.Stats` 和 `BigIntStats` 支持 `Temporal.Instant`，HTTP `writeInformation` 可发送任意 1xx 状态码，`stream.compose` 转 Stable，Web Crypto 新增 ML-DSA/ML-KEM/ChaCha20-Poly1305 算法。来源: JSer.info, JavaScript Weekly | [链接](https://nodejs.org/en/blog/release/v26.2.0)
- **Node.js 官方 Axios→fetch codemod** - 一键将使用 Axios 的代码转换为 Fetch API。来源: JavaScript Weekly, React Status | [链接](https://app.codemod.com)
- **Bun v1.3.14** - 新增 `Bun.Image` 图像处理 API（调整大小/旋转/格式转换），`Bun.serve()` 支持 HTTP/3 over QUIC，`fetch()` 实验性支持 HTTP/2 和 HTTP/3。来源: JSer.info | [链接](https://bun.com/blog/bun-v1.3.14)
- **Firefox 151 支持 Web Serial API** - JavaScript 可读写串行设备（微控制器、3D 打印机等），用户需明确授权。来源: JSer.info, JavaScript Weekly | [链接](https://hacks.mozilla.org/2026/05/web-serial-support-in-firefox/)
- **asm.js 从 Firefox 引擎中移除** - JS 引擎默认禁用 asm.js 优化，将在未来版本中彻底移除。来源: JavaScript Weekly, Frontend Focus | [链接](https://javascriptweekly.com/issues/787)
- **Alien Signals：最轻量的 Signal 库** - 融合 Vue、Preact 和 Svelte 的最佳 push-pull 响应式核心，已被合并回 Vue。来源: JavaScript Weekly | [链接](https://github.com/johnsoncodehk/alien-signals)
- **tinykeys 4.0：简约键盘快捷键库** - Jamie Kyle 出品，API 极简，页面提供实时演示。来源: JavaScript Weekly | [链接](https://jamiebuilds.github.io/tinykeys/)
- **what async promised——Promise 演进的成本分析** - callback→Promise→async/await 的演进历程，分析 async/await 隐藏并行化机会的问题。来源: FE News | [链接](https://fe.news)

---

### 🎨 CSS/样式

- **2026 State of CSS 调查问卷已开放** - 今年聚焦"最重要的特性"，认为在 AI 辅助编程时代"做少但做好"是手写 CSS 开发者的竞争力所在。来源: Frontend Focus | [链接](https://survey.devographics.com)
- **2026 年 CSS 居中技术全景** - Temani Afif 重新梳理 CSS 居中话题，涵盖 `place-content`、CSS anchor positioning 等现代技术。来源: Frontend Focus | [链接](https://css-tricks.com/the-state-of-css-centering-in-2026/)
- **CSS 布局还缺什么？** - Patrick Brosset 基于去年 State of CSS 调查结果，探讨现代 Web 设计和布局中的摩擦点，分析 CSS 尚需填补的空白。来源: Frontend Focus | [链接](https://patrickbrosset.com/articles/whats-missing-in-css-layout/)
- **CSS vs. JavaScript 动画性能** - Josh W. Comeau 深入分析 CSS 动画和 JS 动画的性能差异，探讨不同动画策略的性能影响。来源: Frontend Focus | [链接](https://www.joshwcomeau.com/animation/css-vs-javascript/)
- **从 Tailwind 迁移：学习结构化 CSS** - Julia Evans 在使用 Tailwind 八年后，将两个站点迁回语义化 HTML 和原生 CSS，分享她学到的 CSS 结构知识。来源: Frontend Focus | [链接](https://jvns.ca/blog/2026/05/19/moving-away-from-tailwind-css/)
- **CSS gap decorations 登陆 Chromium** - 无需伪元素或边框即可为 Grid、Flexbox 和多列布局的间隙设置样式。来源: Frontend Focus | [链接](https://developer.chrome.com/blog/gap-decorations-stable)
- **`sibling-index()` 和 `sibling-count()` 高级树计数** - 利用这两个 CSS 函数实现数学化布局的高级技巧。来源: Frontend Focus, Frontender Medium | [链接](https://www.smashingmagazine.com/2026/05/mathematical-layouts-sibling-index-sibling-count/)
- **框架无关的设计系统：Web Components 实践指南** - 涵盖跨框架管理、构建和打包设计系统组件的可操作指南。来源: Frontend Focus | [链接](https://piccalil.li/blog/framework-agnostic-design-systems/)
- **不要在通用元素上使用 `aria-label`** - Manuel Matuzovic 解释为什么在 `<div>` 或 `<span>` 上加 `aria-label` 违反规范且在屏幕阅读器中表现不一致。来源: Frontend Focus | [链接](https://www.matuzo.at/blog/dont-put-aria-label-on-generic-elements/)
- **Tegaki：将任意字体转为动画手写效果** - 支持任何字体和文本（含非英语），兼容所有主流框架，内置多种手写字体。来源: Frontend Focus | [链接](https://github.com/kurtextrem/tegaki)

---

### 🔧 工具/构建

- **Yelp 从 Webpack 迁移到 Rspack 的实践经验** - 构建时间减半，分享了 barrel files 和 re-exports 的性能陷阱及解决方案。来源: JavaScript Weekly | [链接](https://engineeringblog.yelp.com/2026/05/optimizing-our-build-times-by-migrating-from-webpack-to-rspack.html)
- **Playwright v1.60.0** - 支持 HAR 记录、`locator.drop()` 模拟外部拖放、`test.abort()` 中断测试、`expect(page).toMatchAriaSnapshot()` 支持 Page 级别使用。移除了多个已弃用 API。来源: JSer.info | [链接](https://github.com/microsoft/playwright/releases/tag/v1.60.0)
- **vite-plus v0.1.21** - VoidZero 出品的一站式 Vite 工具链增强 CLI，`vp create` 支持 scoped 模板，`vp migrate` 支持 named catalogs 重写和 `tsdown/client` 迁移。来源: JSer.info | [链接](https://github.com/voidzero-dev/vite-plus/releases/tag/v0.1.21)
- **MDXEditor 4.0：React 富文本 Markdown 编辑器** - 基于 Lexical，支持代码编辑、链接/图片插入、表格等。来源: React Status | [链接](https://mdxeditor.dev)
- **hermes-node：基于 Hermes 引擎的 Node.js 兼容运行时** - 可直接执行 TypeScript 文件，内置 Chrome DevTools 协议调试器，Node.js 核心模块复用 Node.js 内部 JS 实现。来源: JSer.info | [链接](https://github.com/tmikov/hermes-node)
- **sqlfu：SQL 文件优先的 TypeScript SQLite 工具包** - 从 SQL 查询生成类型安全 TypeScript 包装器，支持 Durable Object/D1/Node.js/Bun，内置 Admin UI 和 OpenTelemetry 追踪。来源: JSer.info | [链接](https://sqlfu.dev)
- **DOCX 9.7：JS 生成 Word 文档** - 成熟全面的客户端/服务端 `.docx` 生成库，提供 100+ 示例脚本。来源: JavaScript Weekly | [链接](https://docx.js.org)
- **Tailwind CSSTree** - Nicholas C. Zakas 出品，让 Tailwind 项目使用 CSSTree 语法进行 CSS 解析、遍历和生成。来源: Frontend Focus | [链接](https://github.com/nzakas/tailwind-csstree)
- **font-size-adjust-calculator** - 上传字体文件（TTF/OTF/WOFF/WOFF2），自动计算 `font-size-adjust` 属性的合适值。来源: Frontend Focus | [链接](https://clagnut.com/tools/font-size-adjust-calculator)
- **SVG Studio：浏览器端 SVG 动画工具** - 基于图层的时间轴动画编辑器，支持缓动函数、循环控制、撤销/重做，可导出干净的 SVG。来源: Frontend Focus, Frontender Medium | [链接](https://www.svgstudio.org)
- **Node.js v26.2.0 & v24.16.0 (LTS)** - Temporal API 默认启用，V8 14.6，Web Crypto 增强。来源: JavaScript Weekly | [链接](https://nodejs.org/en/blog/release/v26.2.0)

---

### ⚡ 性能优化

- **GitHub PR Files changed 性能优化** - 每行组件从 8+ 个降至 2 个，INP 从 450ms 降至 100ms（78% 提升），使用 TanStack Virtual 做窗口虚拟化。来源: FE News | [链接](https://fe.news)
- **GitHub Issues 导航性能：从延迟到即时** - GitHub 重构 issue 导航为 local-first、stale-while-revalidate 模型，基于 IndexedDB 缓存渲染并在后台重新验证，约 70% React 导航实现即时响应，P10 从 600ms 降至 70ms。来源: React Status | [链接](https://github.blog/engineering/architecture-optimization/from-latency-to-instant-modernizing-github-issues-navigation-performance/)
- **Yelp 构建优化：Webpack→Rspack** - 构建时间减半，深入分析 barrel files 带来的性能隐患。来源: JavaScript Weekly | [链接](https://engineeringblog.yelp.com/2026/05/optimizing-our-build-times-by-migrating-from-webpack-to-rspack.html)
- **MDN 从 React SPA 迁移到 Web Components+Lit+Rspack** - 使用 Declarative Shadow DOM 消除布局偏移，构建时间从 2 分钟降至 2 秒。来源: FE News | [链接](https://fe.news)
- **React at 60 FPS** - Rachel Kaufman 的幻灯片，分享无需动画库、依靠 Canvas、`requestAnimationFrame`、WebSockets 和 `React.memo` 实现高性能动画数据的技巧。来源: React Status | [链接](https://react.statuscode.com/issues/476)

---

### 🧪 测试/质量

- **Playwright v1.60.0 重大更新** - 新增 `test.abort()` 中断测试、`expect(page).toMatchAriaSnapshot()` 用于无障碍快照匹配、HAR 记录支持、`locator.drop()` 外部拖放模拟。来源: JSer.info | [链接](https://github.com/microsoft/playwright/releases/tag/v1.60.0)
- **AVA 8.0.0** - 最低要求 Node.js v22.20/v24.12，内部实现 ESM 化，新增 `test.skipIf()`/`test.runIf()` 按运行条件跳过或执行测试。来源: JSer.info | [链接](https://github.com/avajs/ava/releases/tag/v8.0.0)
- **Jest v30.4.0** - 支持 Node v26 Temporal API 的 fake timers、`jest.config.mts` 配置、ES Modules `require()` 支持（Node v24.9+）。来源: JSer.info | [链接](https://github.com/jestjs/jest/releases/tag/v30.4.0)

---

### 🤖 AI/机器学习

- **为何 AI 搞不定前端？——Adam Argyle 分析四大结构性限制** - ①训练数据偏旧，最新 CSS 能力缺失；②LLM 不是渲染引擎，无法视觉验证空间推理；③不理解状态机/SDD/BDD 等设计决策背景；④无法控制浏览器版本/视口等环境变量。来源: FE News | [链接](https://fe.news)
- **Agentic Engine Optimization (AEO)：面向 AI Agent 优化文档** - Addy Osmani 提出 6 步 AEO 栈：robots.txt→llms.txt→skill.md→Markdown→Token 计数→Copy for AI。来源: FE News | [链接](https://fe.news)
- **AI 在制造前端的"失落的十年"吗？** - Mauro Bieg 探讨 AI 辅助开发是否会导致前端质量退化，重演历史上过度依赖工具的教训。来源: Frontend Focus | [链接](https://frontendfoc.us/issues/743)
- **漏洞赏金计划的终结：Turso 因 AI 泛滥关闭** - AI 生成的假漏洞和垃圾 PR 泛滥成灾，开发者精疲力竭。即使关掉 PR，提交者还会用 AI 生成的长文争论。来源: 阮一峰博客 | [链接](http://www.ruanyifeng.com/blog/2026/05/weekly-issue-398.html)
- **Google Modern Web Guidance：也许不该依赖它** - Adrian Roselli 对 Google 新推出的 LLM 技能提出批评，建议开发者"最好忽略"，因为其中包含有问题的可访问性建议。来源: Frontend Focus | [链接](https://adrianroselli.com/2026/05/maybe-dont-rely-on-googles-modern-web-guidance.html)
- **AI 辅助工程师正在 burnout** - Ivan Chepurin 分析 AI 辅助编码的负面影响及如何避免职业倦怠。来源: JavaScript Weekly | [链接](https://javascriptweekly.com/issues/787)
- **Cursor TypeScript SDK 公测** - 编程式调用 AI 编码 Agent，将 AI 编码能力嵌入自动化工作流。来源: FE News | [链接](https://fe.news)
- **Bun 的 Rust 重写已合并** - AI 移植代码的质量受到质疑，Hacker News 上有大量讨论。来源: JavaScript Weekly | [链接](https://github.com/oven-sh/bun/pull/15609)

---

### 🔒 安全

- **npm 分阶段发布：供应链安全的重大升级** - 包在正式发布前需经审批步骤，npm 11.15.0 和 pnpm 11.3 均已支持。pnpm 11.1+ 还新增 `audit signatures` 命令和 `minimumReleaseAge` 严格模式。来源: JavaScript Weekly, JSer.info | [链接](https://docs.npmjs.com/staged-publishing)
- **最简单的供应链防线：minimumReleaseAge** - 设置 7 天冷却期可阻断 21 起 npm 攻击中的 11 起。pnpm 11.0 起将 `minimumReleaseAge` 默认设为 1 天。来源: FE News | [链接](https://fe.news)
- **Microsoft 发布 Mini Shai-Hulud 攻击详细事后分析** - 深入剖析上周 npm 供应链攻击的技术细节，该攻击影响了 170+ 个包。来源: JavaScript Weekly | [链接](https://javascriptweekly.com/issues/787)
- **StepSecurity Secure Registry：npm 安装时防御代理** - 代理型注册表服务，提供冷却期、危险包拦截和拼写混淆检测等安装时安全防护。来源: JSer.info | [链接](https://www.stepsecurity.io/blog/introducing-secure-registry-install-time-defense-for-the-npm-supply-chain)
- **TanStack 事后剖析与加固** - 2026 年 5 月 11 日 TanStack 遭供应链攻击的详细分析：攻击者利用 `pull_request_target` 配置缺陷 + GitHub Actions 缓存投毒，从 `/proc/` 提取 OIDC token 用于 npm publish。来源: JSer.info | [链接](https://tanstack.com/blog/npm-supply-chain-compromise-postmortem)
- **Google Search 将 back button hijacking 定为垃圾策略** - 劫持浏览器后退按钮将被搜索引擎惩罚。来源: FE News | [链接](https://fe.news)

---

### 🌐 其他

- **Token 费用困境** - OpenAI 员工月消耗 6030 亿 Token（约 130 万美元），Uber 4 个月花完全年 34 亿美元 AI 预算。阮一峰分析：AI 编程成本远超人类程序员，公司必然限制 Token 使用。来源: 阮一峰博客 | [链接](http://www.ruanyifeng.com/blog/2026/05/weekly-issue-398.html)
- **"The Vertical Codebase"——按领域垂直组织代码** - TkDodo 建议按领域/功能 (domain/feature) 垂直结构替代按技术类型 (components/hooks/utils) 水平结构。来源: FE News | [链接](https://fe.news)
- **Web 平台受库影响的 9 个案例** - 回顾 jQuery→`querySelector`、Bootstrap→`popovertarget`、Moment.js→`Temporal` 等库如何塑造了 Web 平台 API。来源: JSer.info | [链接](https://jadjoubran.io/blog/web-platform-influenced-by-libraries)
- **React 在 React 之外：Raycast v2.0 技术深度解析** - 热门 macOS 启动器应用 Raycast 新版全面采用 React 前端，技术细节首次公开。来源: React Status, Frontender Medium | [链接](https://www.raycast.com/blog/a-technical-deep-dive-into-the-new-raycast)
- **Google "可能已经杀死网站"** - Kevin Powell 分析 AI 爬虫和摘要如何使网站的流量价值下降，探讨这对 Web 生态的长期影响。来源: Frontend Focus | [链接](https://www.youtube.com/watch?v=frontendfoc.us/link/185742)
- **记忆体涨价：HBM 挤占 DDR 产能** - AI 机房对 HBM 的激增需求推高内存价格，消费电子产品面临内存短缺。来源: 阮一峰博客 | [链接](http://www.ruanyifeng.com/blog/2026/05/weekly-issue-398.html)
- **Hindsight：GitHub 风格个人提交热力图** - 命令行工具，扫描本地 git 仓库生成类似 GitHub 贡献图的热力图。来源: 阮一峰博客 | [链接](https://github.com/chaosprint/hindsight)
- **JSON For You：JSON 可视化处理工具** - 支持图和表视图、嵌套解析、jq 支持、CSV 导入导出，界面设计精美。来源: Frontend Focus | [链接](https://github.com/loggerhead/json-for-you)
- **dev.css：让纯 HTML 变得现代和响应式** - 受 new.css 启发的默认样式集，适用于简单博客或个人网站。来源: Frontend Focus | [链接](https://tangled.org/dev.css)

---

### 📚 周刊摘要

#### 阮一峰科技爱好者周刊 #398

**本期主题：Token 费用难以负担**

- **主题文章：Token 费用难以负担** - OpenAI 员工月消耗 6030 亿 Token（约 130 万美元），Uber 4 个月花完全年 34 亿美元 AI 预算，微软因费用超标放弃 Claude Code。阮一峰认为 AI 不会大规模替代有大型软件项目的程序员，因为成本太高。最便宜的开源模型成本约为旗舰模型的 1/30~1/50，但一个程序员每年至少消耗两三百万人民币 Token 费用。
- **漏洞赏金计划的终结** - Turso 因 AI 生成的假漏洞和垃圾 PR 泛滥、开发者精疲力竭，宣布关闭赏金计划。提交者甚至用 AI 生成长篇争论，声称"我没错"。
- **科技动态**：气温上升让猴子变胖（全球变暖理论也适用于人类）、Colossal 公司成功用人工蛋壳孵化小鸡（为复活渡渡鸟铺路）、保加利亚艺术家用路面涂鸦抗议推动坑洞修补。
- **文章推荐**：内存涨价原因（HBM 挤占 DDR 产能）、Reticulum 自组网项目、布尔逻辑批判（二元思维的局限）、中心极限定理科普（样本平均值满足正态分布但异常值可能更重要）。
- **工具推荐**：DOCX Editor（开源 docx 网页编辑器）、DvnIP（免费动态 IP 服务）、Graphite（矢量作图 Web 应用）、Hindsight（git 提交热力图）、NyaTerm（跨平台 SSH 终端）、diving-rs（Docker 镜像层分析）、CanvasCast（白板录制 Web 应用）、Vue TUI（终端组件库）。
- **AI 相关**：DeepSeek Reasonix（专为 DeepSeek 设计的终端编程 Agent，利用缓存降低费用）、FunASR（阿里通义实验室开源语音识别）、Codex Mate（一站式本地 Agent 管理面板）。

来源: 阮一峰 | [链接](http://www.ruanyifeng.com/blog/2026/05/weekly-issue-398.html)

---

📅 数据收集时间: 2026-05-31
📡 数据源: React Status / JavaScript Weekly / Frontend Focus / JSer.info / Frontender Medium / GitHub Trending / 阮一峰博客 / FE News (8/8 成功)
