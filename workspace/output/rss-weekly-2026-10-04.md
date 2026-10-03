---
layout: default
title: 前端技术周报 (2026-10-04)
date: 2026-10-04
category: RSS 周报
---

## 📰 前端技术周报 (2026-10-04)

### 📝 本周要点

- **Shopify 放弃 React Native，转用 Swift/Kotlin 原生开发移动端** — 六年前高调转向 RN 的 Shopify 如今走回原生；阮一峰认为 AI 作为"无所不能的翻译器"宣判了 RN 这类中间层的死刑。中秋/十一假期周刊休刊一周。
  来源: 阮一峰 #413 | [链接](http://www.ruanyifeng.com/blog/2026/09/weekly-issue-413.html)
- **React 19.3 发布，Fragment Refs 稳定** — 新增 `use(browser())` 实现浏览器专属渲染，支持 Trusted Types API。
  来源: JSer.info / react.dev | [React 19.3](https://react.dev/blog/2026/09/09/react-19-3)
- **lovable.dev（月 4200 万访问）从 Next.js 迁移到 TanStack Start（Cloudflare workerd）** — 6 个月双栈并行、按路由组切流，中位 TTFB 快 49%，dev 内存 8GB→1.5GB，全程无中断。
  来源: FE News 2026-09 | [lovable.dev](https://lovable.dev/blog/how-we-migrated-lovable-dev-away-from-nextjs)
- **Bun 1.4：核心从 Zig 重写为 Rust** — Linux 启动快 2 倍、Windows 快 2.5 倍，HTTP 内存降 13–48%；内置 Bun.WebView 无头浏览器自动化，并原生支持 React Compiler（860 组件 465ms vs Babel 9.15s，约 20 倍差）。
  来源: FE News | [Bun 1.4](https://bun.com/blog/bun-v1.4)
- **pnpm 12（Rust 重写版）正式发布，12.4/12.6 持续迭代** — 新增 `python.enabled`/`cargo.enabled` 多生态依赖管理；字节级稳定 lockfile，大规模 workspace peer 解析快 2–3 倍。
  来源: FE News / JSer.info | [pnpm 12](https://pnpm.io/blog/whats-different-in-pnpm-12)
- **Next.js 16.3：Turbopack 磁盘缓存默认开启，dev 内存最多降 90%** — CI 重复构建最快 5.5 倍；新增 Instant Navigations 与 Rust 版 React Compiler（实验性）。
  来源: FE News | [Next.js 16.3](https://nextjs.org/blog/next-16-3)
- **PortSwigger：CSS 是"你邮箱里的炸弹"** — 纯 CSS 即可在 Gmail/Outlook 等客户端窃取认证 token、构建键盘记录器，还能向 AI 浏览器植入间接提示词注入。
  来源: FE News / Frontender | [portswigger.net](https://portswigger.net/research/css-the-bomb-inside-your-inbox)
- **联合国投票废除墨卡托投影** — 建议改用 Equal Earth 等积投影（"格陵兰不再和非洲一样大"）。
  来源: 阮一峰 #413 | [链接](http://www.ruanyifeng.com/blog/2026/09/weekly-issue-413.html)

### ⚛️ React/前端框架

- **Signals 进入 React-Redux（React Status #492 头条）**；同期收录 Redact（React 兼容同步运行时 v0.1，含 Vite 插件）、Lovable 自研 Rust dev server、GitHub Copilot 桌面端渲染 2000+ 文件大 PR 的工程复盘（把代码行渲染放在 React 之外）。
  来源: React Status | [#492](https://react.statuscode.com/issues/492) / [#490 Shopify 移动战略](https://react.statuscode.com/issues/490)
- **React Three Fiber 9.8** — 兼容 React 19.3。来源: React Status #492
- **Preact 11 RC** — compat 层新增 `use()`/`useEffectEvent()`，`createPortal()` 进核心，用最长递增子序列最小化子节点移动；报 React 19.0.0 兼容版本。来源: FE News | [releases](https://github.com/preactjs/preact/releases/tag/11.0.0-rc.0)
- **Solid 2.0 RC** — async 成为响应图一等公民，编译器换成 Oxc Rust（基准比 Solid 1 快 23–355 倍），SolidStart 并入 Vite 插件 "start mode"。来源: FE News | [solidjs.com](https://www.solidjs.com/blog/solid-2-0-rc-the-big-reveal)
- **SvelteKit 3.0 RC** — 配置并入 `vite.config.ts`、`$lib`→`#lib`、错误统一走 `handleError`、Vite 8/Rolldown 必选。来源: FE News | [svelte.dev](https://svelte.dev/blog/sveltekit-3-release-candidate)
- **TanStack Form v2 Alpha** — 验证管道化、字段类型 branding（编译期拦截错配）、SSR 共享 formOptions；后续移植 Vue/Solid/Angular/Lit。来源: FE News | [tanstack.com](https://tanstack.com/blog/announcing-tanstack-form-v2-alpha)
- **React 可访问性常见错误清单** — 11 项审计 checklist：按钮语义、路由切换焦点管理、动态通知 `role="alert"`/`"status"`。来源: FE News 2026-09
- **Vue 开发者转 React（Part 1）**— 组件、Props 与心智模型重置。来源: Frontender #485 | [telerik.com](https://www.telerik.com/blogs/react-vue-developers-part-1-components-props-mental-reset)
- **Angular 22 三篇系列** — Signal Forms 迁移、Zoneless 变更检测、NgRx SignalStore 状态管理。来源: Frontender #484/#485

### 📦 JavaScript/TypeScript

- **Anthropic 两周让 Claude App 快 3 倍（JS Weekly #804 头条）** — p75 "time-to-typeable" 从 3.1s 降到 0.55s；一个 em dash 把 V8 正则打进慢路径，加上杂散 locale 配置等"杂项课"。来源: JavaScript Weekly | [#804](https://javascriptweekly.com/issues/804)
- **V8 破坏了我的常量时间 JS 库** — 引擎对 `xor` 等"常数时间"代码的优化会泄漏时序信息。来源: Frontender #485 | [soatok.blog](https://soatok.blog/2026/09/12/the-v8-javascript-runtime-undermined-my-constant-time-javascript-library/)
- **Yelp 3 年 7 个月把 570 包 / 140 万行 Flow 迁到 TypeScript** — 类型覆盖率 83.15%→96.44%，渐进式 + 双类型系统边界共存（flowts / flow-to-typescript-codemod）。来源: FE News | [engineeringblog.yelp.com](https://engineeringblog.yelp.com/2026/08/migrating-a-large-flow-monorepo-to-typescript.html)
- **What async promised** — Josh Segall 复盘 callback→Promise→async/await 每代兑现与未兑现的承诺。来源: FE News
- **嵌套 Promise 的正当用途** — James Coglan（EscoDB）：flatten 意味着时间串行化，显式包一层 `promise` 可表达"调用但不等待"的并发。来源: FE News
- **Hanging Promises 控制流** — Inngest TS SDK 用永不 resolve 的 Promise 让函数永久挂起、GC 回收调用栈，实现 step 级 workflow。来源: FE News
- **JavaScript Temporal API 达到 Stage 4** — 生产环境替代 `Date` 的实用指南（Frontender #485）。
- **AbortController 防止陈旧 API 响应**（Frontender #485 | sitepoint.com）

### 🎨 CSS/样式

- **12 个能帮你"退休"依赖的 CSS 新特性（Frontend Focus #759）**；**GitHub 为何现在装更多 CSS（#760）** — 花 3 年从 github.com 移除 styled-components/CSS-in-JS，改用 CSS Modules。来源: Frontend Focus | [#760](https://frontendfoc.us/issues/760) / [#759](https://frontendfoc.us/issues/759)
- **Dart Sass 2 之路** — 把一批弃用项升级为破坏性变更。来源: Frontender #485 | [sass-lang.com](https://sass-lang.com/blog/the-road-to-dart-sass-2/)
- **用 CSS 检测元素重叠**（ishadeed.com）；**PostCSS Smooth Corners**（squircle 圆角插件，github.com）。来源: Frontender #485
- **响应式 iframe（Chrome 154）**；**一个 SVG 九张海报：CSS linked parameters**（pepelsbey.dev）。来源: Frontender #485
- **Design Tokens、Web Components 与 CSS @layer** — 自定义属性值与级联上下文是不同概念；用 `$extensions` 标记生成 `:host` 默认值与 `:defined` 重定义。来源: FE News | [alwaystwisted.com](https://www.alwaystwisted.com/articles/design-tokens-and-web-components)
- **暗色模式切换：两态就够了** — Lea Verou 批评 Light/Dark/System 三态暴露内部数据模型；建议首点击切换并保存显式覆盖，二次点击回系统默认。来源: FE News | [lea.verou.me](https://lea.verou.me/blog/2026/dark-mode-toggles/)

### 🛠 工具/构建

- **Bun 1.4**（见要点）；**pnpm 12 Rust 重写版**（见要点）。
- **Next.js 16.3** — Turbopack 磁盘缓存 + 内存驱逐默认开启（内存最多降 90%），`typescript@^7` 可用 TS7 做类型检查，`catchError` 错误边界、`experimental.useOffline`。来源: FE News
- **Vite+ 1.0** — GitLab CI 的 setup-vp、Homebrew/Docker 镜像；`vp test` 迁移到 Vitest 5.0.1，oxlint/oxfmt 改用 `--lsp` 形式。来源: JSer.info / VoidZero
- **Oxlint 1.79 支持 React Compiler** — Oxc AST 上直接跑编译器，"100ms 的文件现在 10ms"，约 Babel 10 倍；Vite 用 @vitejs/plugin-react v6.1.0 集成（实验性）。来源: FE News | [oxc.rs](https://oxc.rs/blog/2026-08-18-react-compiler-support)
- **Rslib 1.0** — 基于 Rsbuild 的库开发工具。来源: Frontender #483
- **Cursor TypeScript SDK（公开 Beta）** — 以"Cursor 相同的运行时/模型"编程式调用编码 agent，用于 CI/CD 与产品内嵌。来源: FE News
- **TSRX** — Dominic Gannaway 的 TS 语言扩展，同一源码编译到 React/Preact/Solid/Ripple/Vue。来源: FE News

### 🚀 性能优化

- **Baseline 帮你少发 JS** — 以 web.dev/Baseline 为基准系统清理 npm 依赖，gzip 可回收 60–90KB：国际化族（约 14KB 换 Intl API）、HTTP 客户端（约 17KB 换 fetch + AbortSignal）、UI 原语（约 24KB 换 Popover API）、lodash 族（约 8KB）。来源: FE News | [smashingmagazine.com](https://www.smashingmagazine.com/2026/08/how-baseline-can-help-ship-less-javascript/)
- **从 1256ms 到 96ms：修复巨型 React 下拉的 INP**（Frontender #484 | dev.to/subito）。
- **Your SPA is leaking memory — 做浸泡测试**（Frontender 早期 | denodell.com）。
- **Hermes 看不见的内存：React Native 中陈旧 Shadow Node** — Fabric 的 Shadow Node Wrapper 抓住死树的 shared pointer，JS 堆外 C++ 内存累积，GC 无法感知。来源: FE News | [swmansion.com](https://swmansion.com/blog/the-memory-hermes-cant-see-stale-shadow-nodes-in-react-native/)

### 🧪 测试/质量

- **Vitest 5.0 RC** — `clearMocks` 默认改 `true`；fake timer 也 mock `Temporal`；`vi.mock`/`vi.hoisted` 必须在文件顶层，否则报错；JSON/JUnit reporter 默认写文件。来源: FE News | [releases](https://github.com/vitest-dev/vitest/releases/tag/v5.0.0-rc.3)
- **Shopify 把移动端 E2E 稳定性提到 98%** — 弃用 Appium + Test ID，改用计算机视觉（PaddleOCR 识别文字、OpenCV 匹配图标），严格 builder API"每步都带断言"。来源: FE News | [shopify.engineering](https://shopify.engineering/mobile-e2e-testing)
- **Oxlint 1.79 的 React Compiler 规则** — 22 条 Rules of React 校验（见工具/构建）。
- **fallow audit** — 检测循环依赖、重复代码、复杂度、架构边界违规与 CSS 样式差异，可做 PR 门禁。来源: JSer.info

### 🤖 AI/机器学习

- **The AI Engineering Skills Map（Andrew Ng）** — 分析 1 万+招聘 JD，归纳四大能力：构建/部署 AI 应用（核心是 eval 与错误分析闭环）、软件工程基本功（成本/扩展/可靠/速度权衡）、编码 agent 运用、"塑造要做什么"（shaping the build）。来源: FE News | [x.com](https://x.com/AndrewYNg/status/2088302050706686198)
- **Kitesurf（Cloudflare）** — agent 专用浏览器引擎，跑在 Workers V8 isolate；"浏览器是为人的，agent 不需要 tab/扩展/像素级渲染"。来源: FE News | [blog.cloudflare.com](https://blog.cloudflare.com/kitesurf/)
- **Chrome Prompt API（内置 AI）** — 自然语言请求发往 Gemini Nano 等 on-device 模型；Mozilla 标准立场投 negative（跨浏览器输出质量不可控）。来源: FE News
- **AI 文本水印原理图解** — declaude 项目：水印藏在"词与词之间的选择"，检测只能由持钥方验证，改写即稀释。来源: FE News | [declaude.org](https://declaude.org/watermarking/)
- **Addy Osmani：AEO（Agentic Engine Optimization）** — 把编码 agent 当第一读者的文档优化；AGENTS.md 成仓库根标准入口。来源: FE News
- **AI 驱动设计违反 UX 定律**（Frontender #484 | hackernoon.com）；**10 个反 AI 垃圾的前端动作**（Frontender #483 | evilmartians.com）
- **Pac-Bench** — 衡量模型一次提示能否做出 Pac-Man 游戏（Hacker News）。

### 🔒 安全

- **CSS 是"你邮箱里的炸弹"（PortSwigger）** — 见 CSS/要点。
- **最简单的供应链防御** — 包管理器"最小发布年龄"（minimum release age）策略：只装上市 7 天以上的版本；作者 21 起供应链攻击中 11 起可被该单策略拦截，pnpm 11 已默认 1 天。来源: FE News
- **Google Search 新垃圾政策"back button hijacking"** — 用 history.pushState/JS 拦截返回键跳转到非预期站点，非法流媒体常用，将限制搜索曝光。来源: FE News

### 📚 周刊摘要

#### 阮一峰 科技爱好者周刊 #413：再见了，React Native

本期封面：**Shopify 宣布放弃 React Native，改用 Swift/Kotlin 原生开发移动端**——六年前它高调转 RN（真理由是"省钱"），如今有了 AI 作为"无所不能的自动翻译器"，中间语言/翻译层（RN）被判死刑。作者认为 React Native 十年未解决基本技术问题、上手不便，"被替代一点都不冤"。

其他话题：联合国投票废除墨卡托投影、改用 **Equal Earth 等积投影**（"赤道的非洲面积是格陵兰 14 倍"）；中秋/十一假期周刊休刊。

**技术文章**：用 JS 取消网页 CSS 样式表；容器管理与反向代理工具；JavaScript 的怪异之处；Google 搜索的 `udm` 参数（如 `udm=2` 返回图像）；通俗解释"熵"。

**工具推荐**：Great Tables（Python 复杂表格库）；ghostty-web（Ghostty 编译成 WASM 的网页全功能终端）；Infat（Mac 按后缀设默认打开方式）；mini-img-editor（WebGL 在线图片编辑器）；CryptPad（端对端加密的在线 Office）；Lyrimuse（macOS 桌面歌词）；capcut-cli（剪映非官方 CLI）；mailez（Go 单文件自托管邮件系统）；Status Trio（Mac 三合一状态栏图标）；Polycompiler（JS/Python 双环境单脚本）。

**资源**：gpcb.net（网络设备拓扑图工具）；视觉风格图鉴（一颗苹果 100+ 风格）；AI IP 检测（看你连 Claude/ChatGPT/Grok 时真实连接的 IP）；引力 Gravity（万有引力网页多媒体教程）。

**图片**：F-35 飞行员头盔（约 40 万美元/顶）；苏联 Mi-6 巨型直升机（曾载 80 人，仅造一架）。
来源: 阮一峰 | [weekly-issue-413](http://www.ruanyifeng.com/blog/2026/09/weekly-issue-413.html)

#### FE News 2026-09（月刊）

**深度阅读**：
- **CSS 是"你邮箱里的炸弹"**（PortSwigger Gareth Heyes）— 纯 CSS 在 Gmail/Outlook/Fastmail/ProtonMail/Yahoo/AOL 中窃取 token 与击键，含多种 sanitizer 绕过（CSSOM 解析不一致的 "CSS mutation"、URL 逃逸、Outlook 媒体查询干扰）；应对：沙箱 iframe、`select`/`:has`/`:checked`/`:focus` 拦截、图像请求限流。
- **Baseline 帮你少发 JS**（见性能优化）。
- **Yelp 大规模 Flow→TypeScript 迁移**（见 JavaScript）。
- **Shopify 移动端 E2E 稳定性 98%**（见测试）。
- **Hermes 看不见的 C++ 内存泄漏**（见性能）。
- **设计令牌 + Web Components + @layer**（见 CSS）。
- **Oxc Minifier 变量 mangling 原理** — 按 liveness 分槽 + chordal graph 完美消去序逆序，字符按出现频率排序以提升 gzip 率。
- **lovable.dev 离开 Next.js**（见要点）。

**教程**：
- **Progressive Enhancement 用在 JavaScript 内部**（Remy Sharp）— 先内联最小代码绑事件 + 视觉反馈，重依赖加载完再把队列里的交互任务交给真实渲染逻辑。
- **TanStack Router 可靠的 query 预取** — 把 queryOptions 提升到路由 context，loader 与组件共用同一对象，避免"两处不同步"。
- **AI 文本水印原理**（见 AI）。

**代码与工具**：
- **Next.js 16.3**（见工具/构建）
- **Bun 1.4**（见要点）
- **pnpm 12**（见要点）
- **Vitest 5.0 RC**（见测试）
- **Oxlint 1.79 React Compiler 支持**（见工具）
- **React Native 0.87** — Strict TS API 默认、Metro 0.87（sourcemap 快 2 倍/内存降 50%）、iOS 实验性 Swift Package Manager、AGP v9；需 Node 22.13+/Kotlin 2.0+。来源: [reactnative.dev](https://reactnative.dev/blog/2026/08/11/react-native-0.87)
- **SvelteKit 3.0 RC / Solid 2.0 RC / Preact 11 RC / TanStack Form v2 / Astro 7.2**（见框架/工具）
- **Cursor TypeScript SDK / TSRX**（见工具）
- **Kitesurf（agent 浏览器引擎）**（见 AI）

来源: FE News | [2026-09 期](https://fenews.substack.com/p/fe-news-2026-09) / [GitHub 原文](https://github.com/naver/fe-news/blob/master/issues/2026-09.md)

#### JSer.info（#780，2026-09-29）

- **React 19.3** — Fragment Refs 稳定，`use(browser())` 浏览器专属渲染，Trusted Types，Server Components 直渲 Fragment，`onFullscreenChange`/`maskType`。来源: [react.dev](https://react.dev/blog/2026/09/09/react-19-3)
- **pnpm 12.4 / 12.6** — `python.enabled`/`cargo.enabled` 多生态依赖管理；12.6 增 `autoDedupe`、`pnpm add --save-types`、Catalogs 的 file:/link: 支持。来源: [pnpm.io](https://pnpm.io/blog/releases/12.4)
- **Vite+ 1.0** — 见工具/构建。
- **Zod 4.6** — `validate()`/`validateAsync()`、`z.instanceof().properties()`、`z.fromJSONSchema()` 支持更多 JSON Schema 关键字、`z.iban()`/`z.withParser()`。来源: [zod.dev](https://zod.dev/blog/zod-4-6)
- **Webpack 5.111** — ESM 输出 Stable（无需 `experiments.outputModule` 即可用 `output.module`）。来源: [webpack.js.org](https://webpack.js.org/blog/2026-09-14-webpack-5-111/)
- **项目**：`lovablelabs/oj`（面向 React 的 Rust 原生构建工具，内嵌 V8、Vite/Rollup 兼容插件 + SSR + TanStack Start）；`shadcn-ui/lint`（面向 agent 的 Tailwind 设计系统 linter）；`unjs/upm`（TS 写的极小 npm registry 包管理器）。
来源: JSer.info | [RSS](https://jser.info/rss/)

### 🔥 Hacker News 热门（Show HN，points≥50）

- **Offrun** — 一个工作台并行管理所有编码 agent（Claude Code、Codex、AGY、Grok Build）。[offrun.dev](https://offrun.dev/)
- **Giving Opus 5.5 a simulated paint canvas**（367 分）— [stillwet.art](https://stillwet.art/)
- **Real-time Solar System with 526k asteroids + 全部在轨卫星**（406 分）— [space.bl2.net](https://space.bl2.net/)
- **Rhun** — 用汇编写的开源代码编辑器 — [rhun.app](https://rhun.app/)
- **Open-source model routing for coding agents（Astra 级性能）** — [HN 讨论](https://news.ycombinator.com/item?id=49911500)
- **Ledge.sh** — 可在笔记里跑 shell/SQL/代码的 Markdown notebook — [ledge.sh](https://ledge.sh/)
- **Pac-Bench** — 衡量模型一次提示做 Pac-Man 的基准 — [jonclegg.github.io](https://jonclegg.github.io/pacman-bakeoff/)
- **NSL — WSL for Linux**；**Dental Scope**（3D 牙科解剖）；**JBR-001**（Arduino UNO Q 桌面机器人）；**Hn.watch**（所有 HN 帖子的视频版）；**Hntui**（HN 终端 UI）。

### 🐙 GitHub 本周热门

- **paperclipai/paperclip** — 大家用来"管理工作中的 agent"的开源应用。
- **vectorize-io/hindsight** — "会学习的 agent 记忆"。
- **debpalash/VoiceStudio** — 开源、全本地化的 ElevenLabs 替代（语音克隆）。
- **rohitg00/ai-engineering-from-scratch** — AI 工程从零学起。
- **pbakaus/impeccable** — 让 AI harness 更会做设计的"设计语言"。
- **heygen-com/hyperframes** — "写 HTML，渲染视频，为 agent 而生"。
- **TencentCloud/Octop** — 自托管多用户/多 agent 智能助手。
- **google/ax** — Google 的开源 agentic 编排运行时（agentexecutor.io）。
- **anthropics/financial-services** — Claude for Financial Services 参考 agent/技能/数据连接器。
- **tile-ai/tilelang** — 面向高性能 GPU/CPU 的领域专用语言。
- **anthropics/claude-code-action** — 面向 GitHub PR/issue 的通用 Claude Code action。
- **alirezarezvani/claude-skills**（380+ 技能）、**flutter/flutter**、**vercel/next.js**、**pytorch/pytorch**、**harry0703/MoneyPrinterTurbo**（AI 一键生成短视频）、**pablostanley/yoinks**（终端抓任意视频）。

### 💬 其他动态

- **MDN MCP Server 介绍**（6 月）— 官方把 MDN 内容以 MCP 形式提供给 agent。来源: MDN | [链接](https://developer.mozilla.org/en-US/blog/introducing-mdn-mcp-server/)（注：MDN 博客近期无新增文章，最新为此篇）
- **Frontend Focus #758：当 CSS 可以运行 JavaScript**（9/16）— [链接](https://frontendfoc.us/issues/758)
- **Frontend Focus #757：2026 年 HTML 新特性**（9/9）— [链接](https://frontendfoc.us/issues/757)
- **JS Weekly #803：JavaScript 桌面应用 < 10MB**（9/22）— [链接](https://javascriptweekly.com/issues/803)
- **JS Weekly #802：函数式编程术语图谱**（9/15）— [链接](https://javascriptweekly.com/issues/802)

---

📅 抓取时间: 2026-10-04 (Asia/Shanghai, UTC+8)
📡 数据源: 10/10 成功（React Status、JS Weekly、Frontender、FE News、JSer.info、Hacker News Show、GitHub Trending、阮一峰、Frontend Focus、MDN Blog；其中 Medium/Substack 因网络直连超时改由 web_extract 抓取成功，MDN 最新内容为 6 月旧文）
