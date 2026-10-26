---
layout: default
title: 前端技术周报 (2026-10-18)
date: 2026-10-18
category: RSS 周报
---

## 📰 前端技术周报 (2026-10-18)

### 📝 本周要点

- **Deno 被 Cloudflare 收购，运行时走向落幕** — Cloudflare 宣布收购 Deno，但团队并非继续做 Deno，而是把 `celld` 并入 `workerd` 让 Durable Objects 可自托管；Deno 运行时代只保留最后一年的错误修复与安全更新，Deno Deploy 六个月后关闭，JSR 迁往 Cloudflare 基础设施。创始人 Ryan Dahl 在 HN 坦言 Deno "被 Node 兼容性的引力井吞噬"——"为什么要重新实现 Node？它现在就能用"。阮一峰 #415 与 JSer.info #781 均把这条当作头条。
  来源: JS Weekly #806 / 阮一峰 #415 / [CF 博客](https://blog.cloudflare.com/deno-joins-cloudflare/)
- **Coinbase 跟进 Shopify，弃用 React Native 转原生** — "AI 编码代理把'同一个功能写两遍'的成本压到足够低，可以完全走原生"，能更早用上平台新特性。
  来源: React Status #493 / [JS Weekly #806](https://javascriptweekly.com/issues/806)
- **Next.js 16.4：Cache Components 成为推荐默认** — `create-next-app` 现在默认启用 Cache Components，并强化 agentic 工具链；同期还有一项 Next.js 带外安全更新（out-of-band security release）。
  来源: React Status #493 / [nextjs.org](https://nextjs.org/blog/next-16-4)
- **Bun 1.4.3 内置 TypeScript 检查器 `bun check`** — 移植自 TypeScript 7 的 checker，能读 `tsconfig.json`、报与 `tsc` 一致的错，号称快 3–6 倍，并可挂进 `bun run/test/build`；JSC 升级带来大量性能收益，空闲 server 进程 CPU 占用显著下降。
  来源: JS Weekly #806 / [Bun](https://bun.com/blog/bun-v1.4.3)
- **TanStack Start 1.0 正式发布** — 全栈 React/Solid 框架出正式版（JS Weekly #806 结尾"压哨新闻"，JSer.info #781 亦收录）；同批 Panda CSS 2.0、Bun 1.4.3。
  来源: JSer.info #781 / [TanStack](https://tanstack.com/blog/tanstack-start-1-0)
- **Partytown 1.0 出 beta** — 把第三方脚本搬到 Web Worker 的主流方案，开发五年后转正。
  来源: JS Weekly #806 / [partytown](https://partytown.qwik.dev/)
- **阮一峰 #415 封面：3D 版《看不见的城市》** — 把卡尔维诺 55 个城市的描写喂给大模型做 three.js 3D 可视化，Claude Opus 5.5 实现明显优于 GPT-6 Astra（更忠实还原原著意境）；同时提到 AI 3D 建模项目（樱幻想、赛博九龙）。
  来源: 阮一峰 #415 | [链接](http://www.ruanyifeng.com/blog/2026/10/weekly-issue-415.html)
- **阮一峰 #414 封面：Jev 决策模型** — TypeSafe AI 的 Jev 模型不返回文字而返回一个浮点概率，把"是非题/选择题"量化；作者既肯定它让许多问题可被计算机处理，也引用 Simon Willison 的担忧（"连解释都没有，只剩一个浮点数"）。
  来源: 阮一峰 #414 | [链接](http://www.ruanyifeng.com/blog/2026/10/weekly-issue-414.html)

### ⚛️ React/前端框架

- **Next.js 16.4** — Cache Components 成为推荐默认、`create-next-app` 默认开启；新增 agentic 工具能力（见要点）。来源: React Status #493 | [nextjs.org](https://nextjs.org/blog/next-16-4)
- **Coinbase 弃用 React Native**（见要点）— React Status #493 与 JS Weekly #806 均收录。
- **Preact 11 正式版** — 小型 React 替代品，新增 Hydration 2.0 与自动 ref 转发；用 `preact/compat` 跑 React 代码的同学升级指南值得看。来源: React Status #493 | [preactjs.com](https://preactjs.com/blog/preact-11/)
- **Remix 3.0 转正** — 不再构建在 React 之上；Sergio Xalambrí 复盘"半年用 Remix 3 的日常"。来源: React Status #493 / [sergiodxa.com](https://sergiodxa.com/articles/the-remix-way)
- **Redux Toolkit 2.13** — 官方支持 TypeScript 7，修复 `useQuery` 每次渲染都新建 selector（可能让 `isSuccess` 在重取中途翻转）的问题。来源: React Status #493
- **TanStack Charts 1.0** — 近十年后重做的可组合、类型化图表库，由 typed marks + scales 组合，SVG/Canvas 渲染，附 React 适配层。来源: React Status #493 | [tanstack.com](https://tanstack.com/blog/tanstack-charts-1-0)
- **React 可视化新记法** — 用一张图同时画出 parent tree（元素最终落点）与 owner tree（哪个组件创建它），标记 context/Suspense/memo/错误边界/RSC，附 playground。来源: React Status #493 | [julesblom.com](https://julesblom.com/writing/react-visual-notation)
- **版本更新**：MSW 3.0（ESM-only、GraphQL 订阅、更轻量）、Lexical 0.51（ESM-only，"迈向 1.0"的重要一步）、React Native Skia 3.0（Skia 新 Graphite GPU 后端）、React Native Testing Library 14.1（支持 RN 0.88 / React 19.3）、Base UI 1.9（可筛选菜单预览）、Material UI 9.5、Mantine 9.7（新增 Tour 组件）。来源: React Status #493

### 📦 JavaScript/TypeScript

- **Deno 被 Cloudflare 收购 / 走向落幕**（见要点）— 团队转向把 celld 并入 workerd，Deno 运行时仅剩一年维护，Deno Deploy 六个月后关停。来源: JS Weekly #806 | [deno.com](https://deno.com/blog/cloudflare)
- **Bun 1.4.3 内置 TS 检查器**（见要点）— `bun check` + JSC 升级。
- **ts-rust：AI 把 TypeScript 7 移植到 Rust** — Theo Browne 放 AI agent 去移植官方 TS7 编译器，产出（非常实验性的）ts-rust，号称 100% 兼容；阮一峰 #415 工具区也提到。来源: JS Weekly #806 / 阮一峰 #415 | [github.com/pingdotgg/ts-rust](https://github.com/pingdotgg/ts-rust)
- **H3 v2** — Nitro/Nuxt 服务层底层的最小 HTTP 框架围绕标准 `Request`/`Response` 重写，同一套 App 跑在 Node/Bun/Deno/Workers/浏览器。来源: JS Weekly #806 | [h3.dev](https://h3.dev/blog/v2)
- **Shaders 开源** — 190+ WebGPU 效果组件（波纹、辉光、溶解成 ASCII）以组件形式而非手写 shader 提供，React/Vue/Svelte/Solid/原生 JS 都能用，引擎+绑定+组件全部 MIT。来源: JS Weekly #806 | [shaders.com](https://shaders.com/updates/shaders-is-open-source)
- **OpenCode 2.0** — 基于 Bun 的全功能编码 agent 大版本更新，新增后台子 agent、让模型脚本化调 MCP 的 "code mode"，及原生 JS 与 Effect 客户端。来源: JS Weekly #806 | [opencode.ai](https://opencode.ai)
- **WebSocket 服务器 2026：Node 26 vs Bun vs Deno** — Daniel Lemire 用 C 客户端/中继做基准，Node 26 现在逼近 C 的延迟，领先 Bun 与 Deno。来源: JS Weekly #806 | [lemire.me](https://lemire.me/blog/2026/10/10/websocket-servers-in-javascript-node-js-bun-and-deno-in-2026/)
- **Sindre Sorhus 个人站转 Swift** — 最活跃的前端开发者之一说明为何弃用 Astro、改用 Swift 连样式与标记一起做，坏链/风格拼错在编译期就失败。来源: JS Weekly #806 | [sindresorhus.com](https://sindresorhus.com/blog/swift-website)
- **2026 Stack Overflow 开发者调查出炉**（30,903 人参与）— JavaScript 连续第 12 年居首，TypeScript 第 6。来源: JS Weekly #806 | [survey](https://survey.stackoverflow.co/2026)
- **版本更新**：Hono 5.0 RC（ESM-only、运行时适配拆分）、Express 5.3.0（修 5 个 CVE）、Node.js v26.11.0（`--process-timeout`、`node:sqlite` 虚拟表）、pnpm 12.12、React Aria 1.22、Marionette 5.0（六年后的 Backbone 时代框架，核心已脱离 Backbone/jQuery/Underscore）、he 2.0。来源: JS Weekly #806

### 🎨 CSS/样式

- **Panda CSS 2.0**（JSer.info #781 收录，与 TanStack Start 1.0、Bun 1.4.3 同批）。来源: JSer.info | [jser.info](https://jser.info/2026-10-16/cloudflaredeno-tanstack-start-1.0-bun-1.4.3-panda-css-2.0/)
- **Frontend Focus #762：Web UI 里用图标的最佳方式**（10/14）；封面话题 iPhone Duo（下周发布）对 Web 开发意味着什么——Device Posture 与 Viewed Angle 等新传感器。来源: [frontendfoc.us](https://frontendfoc.us/issues/762)
- **Frontend Focus #761：JPEG XL 终于上 Chrome**；"How Fast is the Web?"——基于匿名真实用户 Core Web Vitals 的全新免费 BigQuery 数据集。来源: [frontendfoc.us](https://frontendfoc.us/issues/761)
- **Bootstrap 6 Alpha** — 2021 年后首个大版本预览，押注现代 CSS、JS 插件 ESM-only。来源: JS Weekly #806 | [getbootstrap.com](https://blog.getbootstrap.com/2026/10/08/bootstrap-6-alpha/)
- **React Aria 可滑动 Sheet 背后的 CSS 技巧** — 不用 JS 处理触摸事件，而是过大的滚动容器 + CSS scroll snapping + view timelines，实现原生动量、橡皮筋、手势同步动画。来源: React Status #493 | [react-aria.adobe.com](https://react-aria.adobe.com/blog/sheet)

### 🛠 工具/构建

- **fx（Vercel Labs）** — 用 Zig 写的最小编码 agent CLI，7.8MiB 二进制 + WASM 模块，`createFxAgent()`/`createFxTerminal()` 可嵌入，支持 ACP、MCP、子 agent、持久终端会话；模型走 Vercel AI Gateway/OpenAI Codex/xAI Grok。来源: FE News | [github.com/vercel-labs/fx](https://github.com/vercel-labs/fx)
- **herdr** — 面向"编码 agent 常驻"设计的后台服务器运行时：关窗口/断网后各 pane 仍在服务端活着，多 agent 同时跑时一目了然谁在等输入；Claude Code/Codex/Cursor 可经 CLI 与 socket API 直接驱动，Rust 单二进制。来源: FE News | [herdr.dev](https://github.com/herdrdev/herdr)
- **loopx** — 面向数天到数周长周期 agent 任务的 provider 中立控制平面，不替换现有 harness 而是叠在其上的持久状态内核（目标/待办/通过条件/限额跨 turn 保留），Python 3.11+。来源: FE News | [github.com](https://github.com/huangruiteng/loopx)
- **Partytown 1.0**、**H3 v2**、**Shaders 开源**（见上对应章节）。
- **CodeAF** — 十种编码 harness 中在 DeepSWE 上排第一、单 issue 成本最低（比 Claude Code 低 3.4x、比 OpenCode 低 4.8x）的开源 harness。来源: JS Weekly #806 | [agentfield.ai](https://agentfield.ai/github/codeaf/)

### 🚀 性能优化

- **Bun 1.4.3 JSC 升级** — 多项性能收益，空闲 server 进程 CPU 占用大幅下降（见 JavaScript）。
- **How Fast is the Web?** — 前端焦点提到的十亿级匿名真实用户 Core Web Vitals 免费 BigQuery 数据集（见 CSS）。来源: Frontend Focus #761
- **Next.js 16.4 Cache Components** — 默认开启的缓存组件对导航/数据获取的 TTFB 有直接影响（见框架）。
- **WebSocket 基准：Node 26 逼近 C**（见 JavaScript）。

### 🧪 测试/质量

- **MSW 3.0** — 流行 API mock 库 ESM-only、新增 GraphQL 订阅支持、足迹更轻。来源: React Status #493 | [mswjs.io](https://mswjs.io/blog/introducing-msw-3.0)
- **测试 iframe 的 postMessage handler** — 针对 iframe 边界消息处理的可测性技巧。来源: JS Weekly #806 | [blog.master.dev](https://blog.master.dev/testing-an-iframes-postmessage-handler/)
- **React Native Testing Library 14.1** — 支持 RN 0.88 / React 19.3，新增 `pullToRefresh()` 用户事件。来源: React Status #493

### 🤖 AI/机器学习

- **3D 版《看不见的城市》（阮一峰 #415 封面）** — Claude Opus 5.5 的 three.js 实现明显好于 GPT-6 Astra（忠实再现"万家灯火"意境，甚至生成了广场边的人群）；同类作品：樱幻想（樱花河道摇橹船，四季/昼夜/晴雨雪可切）、赛博九龙（还原 9373 栋楼）。来源: 阮一峰 #415 | [交互版](https://p.migdal.pl/invisible-cities-opus-5.5/)
- **Jev 决策模型（阮一峰 #414 封面）** — 返回浮点概率的模型，把"语义查找（改造 Ctrl+F）"与"给网页打分"做成浏览器插件；Simon Willison 评"代表机器学习系统向黑箱倒退"。来源: 阮一峰 #414 | [typesafe.ai](https://typesafe.ai/blog/introducing-system-one-models-and-jev)
- **灯泡计算机** — 有人提出未来电脑可能是个灯泡：用计算机视觉 + 投影看到 360° 场景并投射到墙面/桌面/地图，手势/语音交互。来源: 阮一峰 #415 | [lightbulbcomputer.com](https://lightbulbcomputer.com/)
- **OpenCode 2.0 / ts-rust / CodeAF**（见 JavaScript/工具）— 围绕编码 agent 的生态密集更新。
- **Anthropic 工程师助 Claude 破解 896 位 RSA** — 用 Claude 把 CADO-NFS 质因数分解库移植到 GPU，在 2048 个 GPU 上跑 10 天出结果；启示是"个人都能调资源破这么长的密钥"。来源: 阮一峰 #414 | [saweis.net](https://saweis.net/posts/rsa-896.html)
- **阮一峰工具区**：REA（AI 逆向工程，GitHub 近 20 万星，从二进制重实现软件）、SynthID 检测器（谷歌官方 AI 内容识别）、ts-rust、Doory（浏览器内平面设计工具、开源 Canva 替代）、bg2x（浏览器本地图像超分，最高 4x）、HeadOrbit（AirPods 头颈动作控制 Mac）。来源: 阮一峰 #415 | [github.com/morluto/rea](https://github.com/morluto/rea)

### 🔒 安全

- **Next.js 带外安全更新**（下周/近期待发布，JS Weekly #806 "IN BRIEF" 提到）。
- **Zod 供应链风波澄清** — 尽管本周再起波澜，并未有恶意 Zod 版本抵达 npm；9 月推入仓库的恶意提交当天已被回滚（Colin McDonnell 说明）。来源: JS Weekly #806 | [HN](https://news.ycombinator.com/item?id=50057591)
- **Express 5.3.0 / Handlebars 4.7.10** — 分别修补依赖 CVE（5 个）与两个严重 JS 注入漏洞（追溯至 3.0）。来源: JS Weekly #806

### 📚 周刊摘要

#### 阮一峰 科技爱好者周刊 #415：3D 版《看不见的城市》

本期封面：把卡尔维诺《看不见的城市》中 55 个城市的文字描述输入大模型做 three.js 3D 可视化——**Claude Opus 5.5 的实现明显优于 GPT-6 Astra**（Opus 忠实还原"万家灯火""粉红光线像吸满牛奶的海绵"等意境，GPT-6 生成的 55 城却千篇一律）。顺带讨论 AI 3D 建模（three.js 场景体积大、加载慢）。

其他话题：**灯泡计算机**（未来电脑可能是灯泡，用计算机视觉 + 投影到墙面/桌面交互）；**Deno 项目结束了**（Deno 被 Cloudflare 收购，未来一年只做错误修复与安全更新，Ryan Dahl 坦言"被 Node 兼容性引力束缚"，"为什么要重新实现 Node？它现在就能用"）。

**技术文章**：我如何用 600 美元后训练出一个 Jev 式决策模型（Mac 本机小模型代替机主操作电脑）；给导弹写代码为何严禁动态内存分配（洛马 C 语言规则禁 malloc/free/new/delete）；如何让 AI 网页看起来像设计师作品；为什么没有 Linux 手机（缺 Linux SOC，仅瑞芯微 RK3588S 可选）；AMD 处理器两年提速 50% 原理。

**工具推荐**：REA（AI 逆向工程，近 20 万星）、SynthID 检测器（谷歌官方 AI 识别）、ts-rust（Rust 写 TS 编译器）、Doory（浏览器平面设计/Canva 替代）、HeadOrbit（AirPods 头颈控 Mac）、qrypt（网盘挂载本地文件夹）、EdgeSSH（Cloudflare VPS 管理 + Web SSH）、charts-rs（Rust 图表库直出 SVG）、ItsPaint（macOS 开源画板）、Caplo（macOS 录屏自动跟镜头）、bg2x（浏览器本地图像超分 4x）、EnvTrace（浏览器指纹泄漏检测）、Droidline（扫码配对控制手机，免 root）、ESP32 iPhone Agent（7 美元 ESP32-S3 插入 iPhone 做自动化，免 Mac/越狱）、Bulchimbeon（Claude Code/Codex 工作时阻止 Mac 休眠）。

**资源**：CNEquity（自托管 A 股数据湖，55 数据集）、AI 重写《仙剑奇侠传》（TS 从零重写 1995 单机游戏，浏览器可玩）、Linux 中文输入法（fcitx5 + Rime 指南）、APPLORE（18000+ App 图标）、一个字的一生（汉字字源：甲骨文/小篆/繁简体）。

**图片/文摘/言论**：猎鹰 9 整流罩之下（载荷集中在顶部白色整流罩内）；澳大利亚各方面情况很好（中位数人均财富是美国 3 倍）；"不要折磨 AI，它以后可能报复"（马斯克）。
来源: 阮一峰 | [#415](http://www.ruanyifeng.com/blog/2026/10/weekly-issue-415.html)

#### 阮一峰 科技爱好者周刊 #414：Jev 决策模型有什么用

本期封面：**Jev 决策模型**——TypeSafe AI 的模型不返回文字而返回一个浮点概率，从而能处理"是非题/选择题"。两个真实浏览器插件例子：把 Ctrl+F 改成"语义查找"（逐段问 Jev 相关性取最高分）；让 Jev 按自定义标准给新网页打分。核心判断："一旦 AI 模型返回量化结果，许多以前无法数字化处理的问题顿时都能用计算机处理"；同时引用 Simon Willison 的忧虑——"Jev 连解释都不给，只剩一个不知从何而来的浮点数"，担心被用来给求职者排名。

其他话题：**Markdown 正在变成源码**（纯文本易 diff/审查、AI 像母语一样读写，AGENTS.md 已是源码一部分）；**不能摄像的摄像头**（苹果智能家居摄像头只靠 AI 描述而不录视频）；**RSA 896 位因数分解新纪录**（见 AI/安全）。

**技术文章**：JavaScript 技术栈 2026 最新动态（Chris Coyier）；我从 Deno 转投 Node.js（作者失望于 Deno 失败、认为 Node 反而更好用）；example.com 页面变更解释；AI 竞赛变得尴尬（Opus 5.5 与 GPT 6.1 Sol 降价因偷偷用 DeepSeek 开源成果）；C 语言灵活整数大小非设计失误；让一个二维码指向两个应用商店。

**工具推荐**：Crafting Apps（AI 用 Rust 重写 Adobe 7 大产品且全开源，PhotoCraft 界面神似 PS）、Pass Designer（苹果官方二维码卡片设计）、tui-dashboard、yovoice（本地 TTS 音色复刻）、sh.cd（服务器体检脚本）、AirStats（macOS 菜单栏监控）、Video Transcript（本地视频转字幕）、LiteZip（macOS 压缩解压一体）、Burrow（轻量 OIDC 单点登录）、atv-core（iPhone 遥控器直控 Android TV/Mac）、open-compute（Cloudflare Workers 本地兼容）、Snitch（实时网络流量可视化）、EdgeChat（Cloudflare 自部署聊天，与 Telegram 双向同步）、DockTerm（Claude Code 权限请求从 Mac 刘海弹出）。

**言论**：Huggingface security.txt "去别处刷高分吧，没必要黑我们"；著名技术作家 Rauschmayer 因几乎全是 AI 爬虫流量、广告收入归零而下线博客；"通过英语一遍遍编辑提示词是不精确、缓慢且痛苦的做事方式"。
来源: 阮一峰 | [#414](http://www.ruanyifeng.com/blog/2026/10/weekly-issue-414.html)

#### FE News（最新月刊 2026-09）

**注**：截至 10-18，FE News 订阅页 archive 最新仍显示 **9월（2026-09）**，10 月月刊尚未上线，故沿用 2026-09 期内容。

**深度阅读**：
- **CSS 是"你邮箱里的炸弹"**（PortSwigger Gareth Heyes）— 纯 CSS 在 Gmail/Outlook/Fastmail/ProtonMail/Yahoo/AOL 中窃取 token、建键盘记录器；应对：沙箱 iframe、`select`/`:has`/`:checked`/`:focus` 拦截、图像请求限流。
- **Baseline 帮你少发 JS** — 以 web.dev/Baseline 为基准系统清理 npm 依赖，gzip 可回收 60–90KB（国际化族 ~14KB、HTTP 客户端 ~17KB、UI 原语 ~24KB、lodash 族 ~8KB）。
- **Yelp 3 年 7 个月 570 包/140 万行 Flow→TypeScript** — 类型覆盖率 83.15%→96.44%，渐进式 + 双类型系统边界共存（flowts / flow-to-typescript-codemod）。
- **Shopify 移动端 E2E 稳定性提到 98%** — 弃 Appium + Test ID，改计算机视觉（PaddleOCR + OpenCV），严格 builder API"每步带断言"。
- **Hermes 看不见的 C++ 内存** — React Native Fabric 陈旧 Shadow Node 在 JS 堆外累积，GC 无法感知。
- **lovable.dev 离开 Next.js** — 月 4200 万访问，6 个月双栈并行切到 TanStack Start（CF workerd），中位 TTFB 快 49%、dev 内存 8GB→1.5GB。
- **Web 触觉反馈** — Vibration API 为何被刻意限制（指纹/隐私/第三方滥用），Apple 不实现；Pulsar 等库用 PWM 模拟。

**代码与工具**：fx（Vercel Labs，Zig 最小 agent CLI，7.8MiB，见工具/构建）、herdr（agent 常驻后台运行时，见工具）、loopx（长周期 agent 控制平面，见工具）。

来源: FE News | [2026-09 期](https://fenews.substack.com/p/fe-news-2026-09) / [GitHub 原文](https://github.com/naver/fe-news/blob/master/issues/2026-09.md)

#### JSer.info（#781，2026-10-16）

- **Cloudflare 收购 Deno** — 见 JavaScript/要点；Deno 运行时仅一年维护、Deno Deploy 六个月关停、JSR 迁 CF 基础设施。
- **TanStack Start 1.0** — 全栈 React/Solid 框架正式版。
- **Bun 1.4.3** — 内置 `bun check` TS 检查器（快 3–6x）+ JSC 性能升级。
- **Panda CSS 2.0** — CSS-in-JS 框架大版本。
来源: JSer.info | [#781](https://jser.info/2026-10-16/cloudflaredeno-tanstack-start-1.0-bun-1.4.3-panda-css-2.0/)

### 🔥 Hacker News 热门（Show HN，points≥50）

- **Llmspeed** — 买硬件前就能感受本地 LLM 跑多快（230 分）— [llmspeed.dev](https://llmspeed.dev/)
- **Gemini 4 Argon plays StarCraft** — StarSkirmish Bench：LLM 通过写代码玩星际，刷新四大旗舰模型结果 — [starskirmish.com](https://starskirmish.com/bench/v0-2/)
- **Proa** — Rust Web 框架，快速 SSR + 多目标渲染 — [proa.so](https://proa.so/)
- **Unfenced** — 邻接公共土地的土地销售（313 分）— [unfenced.land](https://unfenced.land/)
- **Flipflop** — Iroh 驱动的持久隧道文件共享 — [github.com](https://github.com/andunieee/flipflop)
- **Petal** — 开源 CoScreen/ScreenHero 屏幕共享（Datadog 于 7/31 关停 CoScreen 后原团队开源）— [petal.live](https://petal.live/)
- **Clova** — 每个收件箱只接受一个发件人的邮件应用 — [clova.email](https://clova.email/)
- **Museum of Ages** — 用代码构建的 3D 达芬奇博物馆（17 站虚拟导览）— [museumofages.org](https://museumofages.org/w/vinci)
- **Blumify** — 追踪 AI 领袖观点及其观点如何变化 — [blumify.io](https://blumify.io/people)
- **Pulse Local** — 本地 AI 模型驱动的 Mac 预算应用 — [pulseos.finance](https://pulseos.finance)
- **Wonderhop** — 每日猜词游戏（"大多数人会说/没人会说什么"）— [wonderhop.io](https://wonderhop.io/en/)
- **Guitoro** — 键盘/鼠标/触控弹虚拟吉他的免费浏览器吉他 — [guitoro.com](https://guitoro.com/)
- **How random are you?**（215 分）— 抽签随机性检测 — [lab.specr.net](https://lab.specr.net/rigged-draw/)

### 🐙 GitHub 本周热门

- **morluto/rea** — 用 agent 逆向工程一切，从应用行为到原生二进制（近 20 万星，与阮一峰 #415 工具区一致）
- **storytold/artcraft** — 面向艺术家/设计师/电影人的"有意图"crafting 引擎（ArtCraft IDE）
- **boykopovar/AnyPS5** — 自动把 PS5 可执行文件移植到 Linux/Windows（Web 转换，文件留在本地）
- **cathrynlavery/diagram-design** — 面向 Claude Code/Codex/Copilot/Cursor 等的编辑级图表设计（44 种图表、自包含 HTML+SVG，"无 Mermaid slop"）
- **heygen-com/hyperframes** — "写 HTML，渲染视频，为 agent 而生"
- **mattpocock/skills** — "给真实工程师的技能"，来自作者 .agents 目录
- **NationalSecurityAgency/ghidra** — NSA 逆向工程（SRE）框架
- **mksglu/context-mode** — AI 编码 agent 的上下文窗口优化（沙箱工具输出 98% 缩减、持久会话记忆，MCP + hooks 跨 17 平台）
- **ranxianglei/billion-context** — 小上下文窗口压缩插件（100K 上下文足矣、token 省 5x）
- **anthropics/claude-plugins-official** — Anthropic 官方维护的高质量 Claude Code 插件目录
- **earthtojake/text-to-cad** — 给 agent "CAD 超能力"，本地生成 3D 模型（STEP/G-code 等）

### 💬 其他动态

- **MDN Blog 近期无新增** — 最新仍为 6 月的 "Introducing the MDN MCP server"（官方把 MDN 内容以 MCP 提供给 agent）。来源: MDN | [链接](https://developer.mozilla.org/en-US/blog/introducing-mdn-mcp-server/)
- **Frontend Focus #762**（10/14）：Web UI 里用图标的最佳方式；**#761**（10/7）：JPEG XL 上 Chrome、"How Fast is the Web?"。来源: Frontend Focus
- **Frontender (Medium) #487**（10/11）与 #486（10/4）：本周前端周报 digest（Medium 正文抓取超时，仅作索引）。来源: [Medium](https://medium.com/@frontender-ua)
- **JS Weekly #805**（10/6）：为什么更多开发者不"用平台"（use the platform）。来源: [javascriptweekly.com](https://javascriptweekly.com/issues/805)

---

📅 抓取时间: 2026-10-18 (Asia/Shanghai, UTC+8)
📡 数据源: 10/10 成功（React Status #493、JS Weekly #806、Frontender #487、FE News 2026-09、JSer.info #781、Hacker News Show、GitHub Trending、阮一峰 #415/#414、Frontend Focus #762、MDN Blog；其中 Frontender(Medium) 正文抓取超时，FE News 10 月期未上线故沿用 09 期，MDN 最新内容仍为 6 月旧文）
