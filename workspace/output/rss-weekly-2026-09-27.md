# 前端技术周报 (2026-09-27)

> 数据来源：React Status、JavaScript Weekly、Frontender、FE News、JSer.info、Hacker News、GitHub Trending、阮一峰博客、Frontend Focus、MDN Blog（共 10 个源）

## 📝 本周要点

1. **Shopify 收购 Tailwind Labs，Tailwind CSS 保持 MIT 开源** — 团队在 Shopify 支持下继续开发；Tailwind Plus 与 ui.sh 停止新注册。（[Tailwind CSS 博客](https://tailwindcss.com/blog/tailwind-is-joining-shopify)，来源：JSer.info #779 / FE News / Frontender #483）
2. **Shopify 宣布放弃 React Native，转用 Swift/Kotlin 开发移动版** — 阮一峰 #413 封面文章《再见了，React Native》解读：六年前的"全面拥抱 Web 技术"与今日的转身，核心动机都是省钱；AI 翻译能力让"中间层/中间语言"失去存在价值。Shopify 内部项目 Helix 用 LLM 辅助迁移。（[Shopify Engineering](https://shopify.engineering/back-to-native)）
3. **lovable.dev 从 Next.js 迁移到 TanStack Start（Cloudflare workerd）** — 月 4200 万访问规模，6 个月双框架并行运营、按路由分组灰度切换；中位 TTFB 快 49%，开发环境内存从 8GB 降至 1.5GB。（[lovable.dev 博客](https://lovable.dev/blog/how-we-migrated-lovable-dev-away-from-nextjs)）
4. **Anthropic 用 Claude 完成"史上最长的数学程序"：费马大定理 Lean 形式化证明** — 11 天、3 万+ 辅助定理、1300 万行代码，代码已开源。（[Anthropic Research](https://www.anthropic.com/research/formalizing-fermats-last-theorem)，来源：阮一峰 #412）
5. **Next.js 16.3.6 修复 next/og（ImageResponse）关键 RCE**，影响 v16.2+，下周的定期版本还将修复另外 9 个漏洞。（来源：React Status #492）
6. **Vitest 5.0 / Zod 4.5 / htmx 4.0 / Node.js 24.20.0 LTS / Remix 3 RC 集中发布** — 详见 JSer.info #779。（[JSer.info](https://jser.info/rss/)）
7. **GitHub Copilot 桌面应用（React + Tauri）渲染 2000+ 文件大 PR 的工程复盘** — 代码行渲染在 React 外部以保持性能。（[github.blog](https://github.blog)，来源：React Status #492 封面）
8. **GitHub 周榜被 AI Agent 生态霸榜** — cloudflare/security-audit-skill、alibaba/open-code-review、Fission-AI/OpenSpec、addyosmani/agent-skills 等 20 个仓库中过半与 agent 相关。（[GitHub Trending RSS](https://mshibanami.github.io/GitHubTrendingRSS/weekly/all.xml)）

## ⚛️ React/前端框架

- **React-Redux 9.4 Alpha：新增 opt-in 的 useSignalSelector** — 基于信号追踪每个 selector 读取的状态，dispatch 时只重跑数据真正变化的 selector。（[React Status](https://react.statuscode.com/issues/492)）
- **Redact：一个同步的 React 兼容运行时（v0.1）** — 体积是 React 的零头，支持 React 19.3 API、Vite 插件；代价是无并发渲染，Tanner Linsley 主导，暂无许可证，属实验性。（[React Status](https://react.statuscode.com/issues/492)）
- **React 19.3 发布** — React Three Fiber 9.8 已适配。（[React Blog](https://react.dev/blog/2026/09/09/react-19-3)，来源：Frontender #483）
- **Astro React 集成 v7.0** — Babel 换成 Oxc，新增 React Compiler 支持（`compiler: true`）。（[React Status](https://react.statuscode.com/issues/492)）
- **Remix 3 Release Candidate** — Remix 3.0.0-rc.1 发布。（[remix.run](https://remix.run/blog/remix-3-release-candidate)，来源：JSer.info #779）
- **React Server Functions 不只是 mutation** — 对 Server Functions 更广义用法的讨论。（[nikhilsnayak.dev](https://www.nikhilsnayak.dev/blog/react-server-functions)，来源：Frontender #484）
- **React Activity：render 不再保证 effect 的场景** — Hackernoon 深度分析。（[Hackernoon](https://hackernoon.com/react-activity-when-a-render-no-longer-guarantees-an-effect)，来源：Frontender #484）
- **Discord 迁移到 React Native 新架构的实录**。（[SWMansion](https://swmansion.com/blog/what-it-actually-takes-to-migrate-discord-to-react-native-s-new-architecture/)，来源：Frontender #483）
- **Props Are Not a Design System** — Robert Vitonsky 谈任意样式 props 为何让每个 button 都变成一次性组件。（[React Status](https://react.statuscode.com/issues/492)）
- **Vercel 公开 bug bounty 计划** — 合并私有与开源项目（含 Next.js）两个计划。（[React Status](https://react.statuscode.com/issues/492)）

## 🟨 JavaScript/TypeScript

- **Node.js 24.20.0 (LTS)** — AsyncLocalStorage 支持 `using` scope、Buffer 新增 end 参数、package maps、node:stream/iter。（[Node.js Blog](https://nodejs.org/en/blog/release/v24.20.0)，来源：JSer.info #779）
- **Node.js 26.10.0 (Current)** — 新增 util.debounce / util.throttle。（来源：JavaScript Weekly #803）
- **Zod 4.5** — z.compile() 预编译 schema、z.creditCard()、z.properties()、z.deepPartial()、字符串长度按 Code Point 计算。（[zod.dev](https://zod.dev/blog/zod-4-5)，来源：JSer.info #779）
- **htmx 4.0.0** — 属性继承改用 :inherited 显式声明、事件名改为 htmx:phase:action、XHR 换成 fetch() 实现、新增 hx-preload/hx-download。（[htmx 官方公告](https://four.htmx.org/announcements/2026-08-28-htmx-4.0.0-is-released)，来源：JSer.info #779）
- **WebKit 修复 Safari 的 Top-Level Await** — 模块加载器从 JS 实现重写为 C++ 实现，按 ECMAScript 规范支持 TLA。（[webkit.org](https://webkit.org/blog/18227/fixing-top-level-await-in-safari/)，来源：JSer.info #779）
- **V8 运行时击溃了"恒定时间" JavaScript 库** — 即使无分支代码也会因 CPU 缓存行为在布尔与 -0 的处理上泄露密钥。（[soatok.blog](https://soatok.blog)，来源：JavaScript Weekly #803）
- **jQuery 二十周年** — InfoQ 回顾这个小库如何改写 Web 开发史。（[InfoQ](https://www.infoq.com/news/2026/09/jquery-20-years/)，来源：Frontender #483）
- **Notion 如何用 CRDT 处理并发编辑**。（来源：JavaScript Weekly #803）
- **TypeScript 实战技巧：satisfies、Branded Types、穷举联合**。（[iocombats.com](https://iocombats.com/blogs/typescript-tricks-satisfies-branded-types-exhaustive-unions)，来源：Frontender #484）
- **Lovable 用 Rust 重写 Vite dev server（代号 OJ）** — 性能动机引发争议，Evan You 质疑其 benchmark，并预言 AI 时代人人维护"自己的 slop fork"。（来源：JavaScript Weekly #803）
- **minitype：以 TypeScript 库形式运行的无头排版引擎** — 支持禁则处理、竖排、注音、连字断行，输出 PDF/PNG。（[typeset.jp](https://typeset.jp/)，来源：JSer.info #779）

## 🎨 CSS/样式

- **12 个可以立即淘汰依赖的 CSS 特性** — 原生嵌套替代 Sass、:has() 替代包裹类 hack 等。（[flaviocopes.com](https://flaviocopes.com)，来源：Frontend Focus #759）
- **用 CSS anchor positioning 实现侧边注释**。（[vincent.bernat.ch](https://vincent.bernat.ch/en/blog/2026-css-sidenotes)，来源：Frontender #484）
- **margin-trim 属性移除首尾 margin** — Rachel Andrew 讲解；Chrome 155 beta 已支持。（[rachelandrew.co.uk](https://rachelandrew.co.uk/archives/2026-09-15/remove-start-and-end-margins-with-the-margin-trim-property/)）
- **比较 CSS progress() 的值** — Firefox 155 亦新增 CSS attr()/progress()/alpha()。（来源：Master.dev / JSer.info #779）
- **别再把容器查询当传统媒体查询用** — Smashing Magazine 详解。(来源：Frontender #484)
- **::checkmark 就绪前的自定义 checkbox 可靠模式** — 透明原生 input 叠加 SVG 对勾。（[piccalil.li](https://piccalil.li)，来源：Frontend Focus #759）
- **Safari "旋转抖动"修复：CSS round() 函数救场** — Cody Olsen。（来源：Frontend Focus #759）
- **设计令牌、Web Components 与 CSS @layer 的交叉点** — 自定义属性值能跨影子根继承，但文档级 @layer 顺序管不到影子根内部；用 $extensions 标记 + 双份 Style Dictionary 输出的方案。（[alwaystwisted.com](https://www.alwaystwisted.com/articles/design-tokens-and-web-components)，来源：FE News 2026-09）
- **Dark Mode 开关：两个状态就够了** — Lea Verou 论证 Light/Dark/System 三段式是暴露内部数据模型的错误设计。（[lea.verou.me](https://lea.verou.me/blog/2026/dark-mode-toggles/)，来源：FE News 2026-09）

## 🛠 工具/构建

- **tinyjs：构建 10MB 以内的 JavaScript 桌面应用** — txiki.js 后端 + 原生 webview，覆盖 macOS/Linux/Windows，附签名/公证工具；对比 Electrobun、Perry、Electron、Neutralinojs。（[tinyjs.app](https://tinyjs.app)，来源：JavaScript Weekly #803）
- **Turborepo 2.11** — 任务图实验性支持 Rust/Python/Go，启动速度较 2.9 最高提升 4 倍。（来源：JavaScript Weekly #803）
- **ESLint 10.11.0** — 性能更新，启动与 lint 更快。（来源：JavaScript Weekly #803）
- **Rspack 2.2 / Rslib 1.0** — HMR 改进、Browserslist 基线查询；Rslib 基于 Rsbuild 的库开发工具 1.0。（[rspack.rs](https://rspack.rs/blog/announcing-2-2)，来源：JSer.info #779 / Frontender #483）
- **Aube 2.0** — Rust 编写的包管理器，安装内存大幅下降、更精瘦的 resolver。（[github.com/jdx/aube](https://github.com/jdx/aube)，来源：JSer.info #779）
- **Oxc 迷你化器如何工作：变量混淆的槽位算法** — 按 liveness 分槽、弦图完美消除序、字符分配按 gzip 频率排序。（[green.sapphi.red](https://green.sapphi.red/blog/how-variable-mangling-works-in-oxc-minifier)，来源：FE News 2026-09）
- **浏览器里的持久化数据库：DuckDB-Wasm + OPFS** — 数据库文件可跨刷新保留。（[duckdb.org](https://duckdb.org)，来源：JavaScript Weekly #803）
- **Electron 44** — Chromium 152 / Node 24.18.1；clipboard API 异步化，移除 macOS 12 等旧平台支持。（[electronjs.org](https://www.electronjs.org/blog/electron-44-0)，来源：JSer.info #779）
- **Playwright v1.63.0** — 共享资源测试的 lock 排他执行、locator.visible()、frameLocator() 跨 frame 搜索、ariaSnapshotJSON()。（[GitHub Release](https://github.com/microsoft/playwright/releases/tag/v1.63.0)，来源：JSer.info #779）
- **Turbopack 如何对 JavaScript 做 chunking** — 请求数与传输量的权衡、generateComponentChunks、firstPageLoadPriority 调优。（[nextjs.org](https://nextjs.org/blog/turbopack-chunking)，来源：JSer.info #779 / Frontender #482）
- **ghostty-web：把终端模拟器 Ghostty 编译成 WASM** — 网页里跑全功能终端。（[GitHub](https://github.com/coder/ghostty-web)，来源：阮一峰 #413）
- **Pyric：面向 agent 时代的 Firebase 本地开发工具** — Vite 插件将 firebase/* import 指向本地后端。（[github.com/davideast/pyric](https://github.com/davideast/pyric)，来源：JSer.info #779）

## ⚡ 性能优化

- **用 Baseline 减少 JavaScript 体积** — 系统审计可回收 gzip 60~90KB：Intl 替代 timeago.js/pluralize、fetch+AbortSignal.timeout 替代 axios、dialog/Popover API 替代 UI 原语库；附 `npm ls` + Bundlephobia + webstatus.dev 交叉验证流程。（[Smashing Magazine](https://www.smashingmagazine.com/2026/08/how-baseline-can-help-ship-less-javascript/)，来源：FE News 2026-09）
- **从 1256ms 到 96ms：修复大型 React 下拉框的 INP**。（[dev.to](https://dev.to/subito/from-1256ms-to-96ms-fixing-inp-in-a-massive-react-dropdown-16l7)，来源：Frontender #484）
- **GitHub Copilot 桌面应用的大 PR 渲染策略** — 2000+ 文件、百万行改动的 PR 中，代码行渲染在 React 之外。（[github.blog](https://github.blog)，来源：React Status #492）
- **Stop Layout Shifts：给图片加 width/height** — 防 CLS 基础篇。（[jsdev.space](https://jsdev.space/image-width-height/)，来源：Frontender #484）
- **图片边缘团队提案 previewsrc 属性** — 浏览器原生处理"先模糊后清晰"的图片预览。（[developer.chrome.com](https://developer.chrome.com)，来源：Frontend Focus #759）

## ✅ 测试/质量

- **Vitest 5.0** — clearMocks 默认开启、locator 改为精确匹配、Benchmarking API 重写、Browser Mode 新增 browser.traceView、vi.when、vitest doctor。（[vitest.dev](https://vitest.dev/blog/vitest-5.html)，来源：JSer.info #779）
- **Shopify 把移动端 E2E 测试稳定性提到 98%** — 弃用 Appium + Test ID，改用计算机视觉：PaddleOCR 识别文本、OpenCV 匹配 Polaris 设计系统 SVG；严格 builder API 要求每步带断言，稳定性从 50% 升到 98%。（[Shopify Engineering](https://shopify.engineering/mobile-e2e-testing)，来源：FE News 2026-09）
- **Linear 为 4 倍测试量重构 CI** — 把类型感知 ESLint 规则改写为纯 AST 检查省 55% lint 时间并利于迁移 Oxlint；关闭 Vitest isolation 每月再省 17%。（[linear.app](https://linear.app)，来源：JavaScript Weekly #803）
- **供应链攻击组织 'Mini Shai-Hulud' 被卧底渗透** — Google 特工混入其群组，导致近期两人被捕。（[WIRED](https://www.wired.com)，来源：JavaScript Weekly #803）
- **CSS 邮件投毒：无 JS 窃取 token 与按键记录** — PortSwigger 在 Gmail/Outlook/Fastmail 等已做 CSS 净化的客户端中用属性选择器+嵌套 CSS 暴力破解 token、用 select/:checked 记键；AI 浏览器中 CSS 内嵌提示注入同样生效。（[portswigger.net](https://portswigger.net/research/css-the-bomb-inside-your-inbox)，来源：FE News 2026-09）

## 🤖 AI/机器学习

- **Claude 11 天完成费马大定理 Lean 形式化** — 证明 3 万+ 辅助定理、1300 万行代码，验证"AI 可校验人类数学证明"。（[Anthropic](https://www.anthropic.com/research/formalizing-fermats-last-theorem)，来源：阮一峰 #412）
- **Andrew Ng：AI 工程技能图谱** — 分析 1 万+ 招聘启事后总结四大能力：构建/部署 AI 应用（核心是 eval 与错误分析闭环）、软件基本功（成本/扩展性/可靠性权衡）、驾驭 coding agent（管理上下文、让 agent 自我闭环）、"决定做什么"（shaping the build）。（[X](https://x.com/AndrewYNg/status/2088302050706686198)，来源：FE News 2026-09）
- **前端的"Agent 层"崛起** — 框架之上出现新的 agent 层架构讨论。（[Telerik](https://www.telerik.com/blogs/beyond-frontend-backend-rise-agent-layer)，来源：Frontender #484）
- **Safari 27 内置 MCP server** — 让 agent 可以直接调试你的前端工作；Edge 同步加入 agent-ready 的 WebMCP API。（[WebKit](https://webkit.org)，来源：Frontend Focus #759）
- **Do Frameworks Matter Anymore?** — Remix 成员 Brooks Lybrand：AI 时代 agent 随时造临时框架，反而更需要好的框架。（[brookslybrand.com](https://brookslybrand.com/posts/do-frameworks-matter-anymore/)，来源：JavaScript Weekly #803 / Frontender #484）
- **AI 文本水印工作原理图解**。（[declaude.org](https://declaude.org/watermarking/)，来源：FE News 2026-09）
- **《深入理解 AI Agent：设计原理与工程实践》开源主仓库** — 全书正文、编译版 PDF 与按章配套代码。（[github.com/bojieli/ai-agent-book](https://github.com/bojieli/ai-agent-book)，来源：GitHub 周榜）
- **AI 生成设计正在破坏 UX 定律** — 生成式 UI 与经典交互原则的冲突盘点。（[Hackernoon](https://hackernoon.com/where-ai-generated-design-breaks-ux-laws)，来源：Frontender #484）

## 📚 周刊摘要

### 阮一峰《科技爱好者周刊》#413：再见了，React Native

[来源：阮一峰博客](https://www.ruanyifeng.com/blog/)（RSS）

- **封面：再见了，React Native** — Shopify 宣布放弃 React Native 改用 Swift/Kotlin。六年前的转投 RN 与今日的回归，动机都是省钱；AI 作为"自动翻译器"让中间层失去意义，React Native 这种翻译层"被替代一点都不冤"。
- **世界地图的新投影** — 联合国投票废除墨卡托投影，推荐等积的 Equal Earth 投影法。
- **科技动态** — 韩国低成本隐藏摄像头检测器；联想 830g 固态散热笔记本；成都"词元券"政府补贴 Token 消费。
- **文摘：糊状千层面（slop lasagna）** — 比起意面式缠在一起的代码，分层可整体替换的"千层面"结构更好；组件化让单层垃圾不影响全局。
- **言论** — "代码就是债务"（10 万行比 100 万行的公司更强）；"AI 出错时我们只能召唤更强大的 AI——欢迎来到魔法师时代"。
- **工具精选** — Great Tables（Python 复杂表格）、Polycompiler（JS/Python 双环境单脚本）、mailez（Go 单二进制自托管邮件系统）。
- （本期预告：下周五起中秋和十一假期周刊休息）

### FE News 2026-09（Naver FE 团队月报）

[来源：FE News Substack](https://fenews.substack.com/p/fe-news-2026-09)

12 篇文章，三大板块：

**链接 & 阅读**
- [CSS: The Bomb Inside Your Inbox](https://portswigger.net/research/css-the-bomb-in-your-inbox)：无 JS 邮件 XSS 完整利用链（见"测试/质量"分类）
- [How Baseline Can Help You Ship Less JavaScript](https://www.smashingmagazine.com/2026/08/how-baseline-can-help-ship-less-javascript/)：用 Baseline 回收 60-90KB 体积
- [The AI Engineering Skills Map](https://x.com/AndrewYNg/status/2088302050706686198)：Andrew Ng 四大 AI 工程能力
- [Dark Mode Toggles: Two States are Enough](https://lea.verou.me/blog/2026/dark-mode-toggles/)：两段式暗色切换设计
- [How We Migrated lovable.dev Away from Next.js](https://lovable.dev/blog/how-we-migrated-lovable-dev-away-from-nextjs)：4200 万月访问的框架迁移实录
- [Migrating a Large Flow Monorepo to TypeScript](https://engineeringblog.yelp.com/2026/08/migrating-a-large-flow-monorepo-to-typescript.html)：Yelp 570 包/140 万行 Flow→TS 三年半，类型覆盖率 83.15%→96.44%
- [How we raised mobile E2E test stability to 98%](https://shopify.engineering/mobile-e2e-testing)：计算机视觉替代 Test ID
- [Haptic Feedback on the Web](https://swmansion.com/blog/haptic-feedback-on-the-web-why-the-web-deliberately-refuses-to-be-as-tactile-as-native-apps/)：Web 为何"故意"没有触觉 API
- [Stale Shadow Nodes in React Native](https://swmansion.com/blog/the-memory-hermes-cant-see-stale-shadow-nodes-in-react-native/)：Hermes GC 看不见的 Fabric 内存泄漏
- [Design Tokens, Web Components, and CSS @layer](https://www.alwaystwisted.com/articles/design-tokens-and-web-components)：影子根内的 token 分层
- [How Variable Mangling Works in Oxc Minifier](https://green.sapphi.red/blog/how-variable-mangling-works-in-oxc-minifier)：混淆的图着色视角

**教程**
- [Progressive Enhancement Inside of JavaScript](https://remysharp.com/2026/08/05/progressive-enhancement-inside-of-javascript)（Remy Sharp）：JS 尚未加载区间的渐进增强——交互先内联、重依赖进队列
- [Reliable Query Prefetching with TanStack Router](https://tkdodo.eu/blog/reliable-query-prefetching-with-tanstack-router)：把 queryOptions 提升到路由上下文，单一数据源防预取漂移
- [How AI text watermarking works: a visual guide](https://declaude.org/watermarking/)

### JSer.info #779（2026-09-10）

[来源：JSer.info](https://jser.info/rss/)

- **头条**：Vitest 5.0、Zod 4.5、Shopify 收购 Tailwind Labs（MIT 保留）
- **版本发布**：plotly.js 4.0.0（移除 Mapbox 换 MapLibre、MathJax v3/v4）、htmx 4.0.0、Rspack 2.2、Node.js 24.20.0 LTS、Remix 3 RC、Electron 44（Chromium 152）、Playwright 1.63.0、Firefox 155.0（HTTP/3 QUIC v2、CSS attr()/progress()/alpha()）
- **文章**：Turbopack chunking 算法（Next.js 官方博客）；Safari TLA 修复（WebKit 模块加载器 C++ 化）
- **工具**：Aube 2.0.1（Rust 包管理器）；Pyric（Firebase agent 时代开发工具）；minitype（TS 无头排版引擎）
- **前一期 #778（08-27）**：pnpm 12（Rust 重写稳定版）、Bun 1.4、Solid 2.0 RC

## 🔥 Hacker News 热门（Show HN，近 48 小时 50+ 分）

[来源：Algolia HN API](https://hn.algolia.com/api/v1/search_by_date?tags=show_hn)

1. **[Show HN: Jev Plays Pokémon Red](https://jev-pokemon.vercel.app/)** — [256 分 / 109 评论](https://news.ycombinator.com/item?id=49845172)
2. **[Show HN: Reladraw – 自己决定布局的图表语言](https://github.com/reladraw/reladraw)** — [120 分 / 34 评论](https://news.ycombinator.com/item?id=49858513)
3. **[Show HN: Hacker Atlas – 一张 Hacker News 话题地图](https://hackeratlas.com/)** — [80 分 / 26 评论](https://news.ycombinator.com/item?id=49844497)
4. **[Show HN: 用 Claude Code skill 复盘你的象棋对局](https://github.com/brumar/chess-postmortem-skills)** — [68 分 / 51 评论](https://news.ycombinator.com/item?id=49857528)
5. **[Show HN: Doom or Bloom – 画出你的 AI 世界观](https://www.doom-or-bloom.com)** — [56 分 / 48 评论](https://news.ycombinator.com/item?id=49846953)

## 📈 GitHub 周榜（GitHub Trending Weekly）

[来源：GitHub Trending RSS](https://mshibanami.github.io/GitHubTrendingRSS/weekly/all.xml)

1. [cloudflare/security-audit-skill](https://github.com/cloudflare/security-audit-skill) — 多阶段安全审计的 coding-agent skill，带独立验证的机器可读结论
2. [anthropics/claude-code](https://github.com/anthropics/claude-code) — 终端中的 agentic 编码工具
3. [alibaba/open-code-review](https://github.com/alibaba/open-code-review) — 阿里规模验证的混合架构代码审查：确定性流水线 + LLM Agent
4. [affaan-m/ECC](https://github.com/affaan-m/ECC) — agent harness 性能优化系统：skills、instincts、memory
5. [Tencent/WeKnora](https://github.com/Tencent/WeKnora) — 开源 LLM 知识平台：文档变 RAG + 自主推理 agent
6. [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) — 生产级 AI 编码 agent 工程技能库
7. [stablyai/orca](https://github.com/stablyai/orca) — 并行 agent 集群的 ADE，用自己的订阅跑任意编码 agent
8. [vectorize-io/hindsight](https://github.com/vectorize-io/hindsight) — Hindsight：会学习的 agent 记忆
9. [anthropics/knowledge-work-plugins](https://github.com/anthropics/knowledge-work-plugins) — Claude Cowork 知识工作者插件
10. [davila7/claude-code-templates](https://github.com/davila7/claude-code-templates) — Claude Code 配置与监控 CLI
11. [paperclipai/paperclip](https://github.com/paperclipai/paperclip) — 管理办公 agent 的开源应用
12. [pytorch/pytorch](https://github.com/pytorch/pytorch) — 张量与动态神经网络，强 GPU 加速
13. [TencentCloud/Octop](https://github.com/TencentCloud/Octop) — 更聪明的自托管多用户多 agent AI 助手
14. [cloudflare/quiche](https://github.com/cloudflare/quiche) — QUIC 传输协议与 HTTP/3 实现
15. [Fission-AI/OpenSpec](https://github.com/Fission-AI/OpenSpec) — AI 编码助手的 spec-driven 开发
16. [HKUDS/CLI-Anything](https://github.com/HKUDS/CLI-Anything) — "让所有软件 agent-native"
17. [superdesigndev/treg](https://github.com/superdesigndev/treg) — agent 工具版的 OpenRouter
18. [cline/cline](https://github.com/cline/cline) — 自主编码 agent：SDK、IDE 扩展或 CLI
19. [odoo/odoo](https://github.com/odoo/odoo) — 开源企业应用套件
20. [bojieli/ai-agent-book](https://github.com/bojieli/ai-agent-book) — 《深入理解 AI Agent》开源全书（正文、PDF、配套代码）

## 🌐 其他动态

- **Frontend Focus #759 简讯** — Chrome DevTools 更新改进 MCP server 与广告脚本追踪；Chrome 155 beta 支持 CSS symbols()、JPEG XL；Edge 新增 OpaqueRange API 与组件可访问性改进；Chrome 154 落地响应式 iframe（iframe 尺寸随内容，嵌入文档需 opt-in）。（[Frontend Focus](https://frontendfoc.us/issues/759)）
- **The Root Scroller and How Not to Lose It** — Kilian Valkhof 详解视口滚动容器与常见 CSS 误用。（[polypane.app](https://polypane.app)，来源：Frontend Focus #759）
- **"AI, Make the Website Good"** — Zach Leatherman：不管用什么工具，输出质量才是关键，并犀利点评各大 AI 公司自家网站的前台质量。（[zachleat.com](https://www.zachleat.com)，来源：Frontend Focus #759）
- **19½ 条你不知道的 HTML/CSS 可访问性细节** — StripeCon Europe 演讲整理。（[noti.st](https://noti.st)，来源：Frontend Focus #759）
- **The Death of Web Development Education** — Mathias Schäfer 呼吁拯救正在消失的前端教育。（来源：Frontend Focus #759）
- **CSS 滚动触发动画已落地 Chrome（2 月起）** — 与普通/滚动驱动动画的区别、timeline-trigger 与 animation-trigger 属性。（[cydstumpel.nl](https://cydstumpel.nl)，来源：Frontend Focus #759）
- **MDN Blog** — 近期文章：[MDN MCP server 发布](https://developer.mozilla.org/en-US/blog/introducing-mdn-mcp-server/)（6 月）、[MDN 新前端内幕](https://developer.mozilla.org/en-US/blog/mdn-front-end-deep-dive/)（4 月），本周无新文。（[MDN Blog RSS](https://developer.mozilla.org/en-US/blog/rss.xml)）
- **Frontender 摘要** — #484（9/14-20）：图片宽高防 CLS、构建 10 个浏览器 API 替代库、Houdini VAT + Three.js 揉皱纸效果、Angular Zoneless 变化检测；#483（9/7-13）：Gatsby→Astro 九天迁移、Rslib 1.0、WebGPU 计算着色器语法高亮。（[Frontender](https://medium.com/feed/@frontender-ua)）
- **Playroom / pdfcn / loading-dev** — 浏览器 JSX playground（接自家组件库）、shadcn 风格 PDF 组件库（WASM 渲染）、29 个 CSS 动画 React 加载指示器。（来源：React Status #492）

---

*生成时间：2026-09-27（Asia/Shanghai）· 由 rss-reporter 工作流自动聚合*
