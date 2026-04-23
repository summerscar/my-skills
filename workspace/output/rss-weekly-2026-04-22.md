---
layout: default
title: 前端技术周报 (2026-04-22)
date: 2026-04-22
category: RSS 周报
---

## 📰 前端技术周报 (2026-04-22)

### 📝 本周要点

- **pnpm 11 RC 0 发布** - 纯 ESM 包迁移，Node.js 18-21 支持终止，加强供应链安全
  来源: [JSer.info](https://jser.info/2026/04/15/pnpm-11-rc-0-webpack-5.106-servo-v0.1.0/) | [GitHub](https://github.com/pnpm/pnpm/releases/tag/v11.0.0-rc.0)
- **TypeScript 6.0 正式发布** - 这是基于当前 JavaScript 代码库的最后一个版本，TypeScript 7 将基于 Go 语言
  来源: [JSer.info](https://jser.info/2026/04/06/typescript-6.0-es2026-rc-axios/) | [官方公告](https://devblogs.microsoft.com/typescript/announcing-typescript-6.0/)
- **Vite 8.0 发布** - 新版本带来重要更新和性能改进
  来源: [JSer.info](https://jser.info/2026/03/22/vite-8.0-temporal-stage-4-next.js-16.2/)
- **Temporal API 达到 Stage 4** - 9 年的标准化旅程，将进入 ES2026，彻底修复 JavaScript 时间处理问题
  来源: [FE News](https://bloomberg.github.io/js-blog/post/temporal/) | [JSer.info](https://jser.info/2026/03/22/vite-8.0-temporal-stage-4-next.js-16.2/)
- **Bun v1.3.12 发布** - 新增 Bun.WebView、支持直接执行 Markdown 文件
  来源: [JSer.info](https://jser.info/2026/04/15/pnpm-11-rc-0-webpack-5.106-servo-v0.1.0/) | [Bun Blog](https://bun.com/blog/bun-v1.3.12)
- **webpack 5.106 发布** - 新增 Plugin Validation Hook、CSS Modules 运行时样式注入支持
  来源: [JSer.info](https://jser.info/2026/04/15/pnpm-11-rc-0-webpack-5.106-servo-v0.1.0/) | [webpack 博客](https://webpack.js.org/blog/2026-04-08-webpack-5-106/)
- **Servo v0.1.0 发布** - Rust 编写的嵌入式 Web 渲染引擎，提供轻量级高性能替代方案
  来源: [JSer.info](https://jser.info/2026/04/15/pnpm-11-rc-0-webpack-5.106-servo-v0.1.0/) | [Servo 博客](https://servo.org/blog/2026/04/13/servo-0.1.0-release/)
- **Node.js 将采用年度主要版本发布** - 从 Node 27 开始，每年发布一个主要版本
  来源: [FE News](https://socket.dev/blog/node-js-moves-to-annual-major-releases-starting-with-node-27)
- **Axios npm 包遭受供应链攻击** - 跨平台 RAT 恶意软件，提醒开发者注意包安全
  来源: [FE News](https://snyk.io/blog/axios-npm-package-compromised-supply-chain-attack-delivers-cross-platform/) | [JSer.info](https://jser.info/2026/04/06/typescript-6.0-es2026-rc-axios/)
- **Google 打击"劫持返回按钮"行为** - 6 月中旬开始惩罚干扰浏览器历史记录导航的网站
  来源: [Frontend Focus #737](https://frontendfoc.us/issues/737) | [Google](https://developers.google.com/search/docs/specialty/seo/back-button-hijacking)

### ⚛️ React/前端框架

- **TanStack Start 重新思考 React Server Components** - [React Status #470](https://react.statuscode.com/issues/470)
- **React 优化案例研究来自 GitHub** - [React Status #469](https://react.statuscode.com/issues/469)
- **为什么测试 ID 是无障碍代码异味** - [React Status #468](https://react.statuscode.com/issues/468)
- **如何构建自己的服务端 React 框架** - [React Status #467](https://react.statuscode.com/issues/467)
- **Vite 8.0、RedwoodSDK 1.0、shadcn/cli v4 等重磅发布** - [React Status #466](https://react.statuscode.com/issues/466)
- **React 19.2 的 Activity 组件如何保持状态活跃** - [React Status #465](https://react.statuscode.com/issues/465)
- **Cloudflare 推出 Vite 驱动的 Next.js** - [React Status #464](https://react.statuscode.com/issues/464)
- **TanStack Hotkeys - 新的跨平台键盘工具包** - [React Status #463](https://react.statuscode.com/issues/463)
- **Next.js 16.2 发布** - [JSer.info](https://jser.info/2026/03/22/vite-8.0-temporal-stage-4-next.js-16.2/)
- **Expo UI in SDK 55: Jetpack Compose 现在可用于 React Native 应用** - [FE News](https://expo.dev/blog/expo-ui-in-sdk-55-jetpack-compose-now-available-for-react-native-apps)
- **React Server Components Your Way** - [JSer.info](https://jser.info/2026/04/15/pnpm-11-rc-0-webpack-5.106-servo-v0.1.0/)
- **MDN 新前端技术深度解析** - [MDN Blog](https://developer.mozilla.org/en-US/blog/mdn-front-end-deep-dive/)

### 📦 JavaScript/TypeScript

- **TypeScript 6.0 正式发布** - 这是基于当前 JavaScript 代码库的最后一个版本，TypeScript 7 将基于 Go 语言重写
  来源: [JSer.info](https://jser.info/2026/04/06/typescript-6.0-es2026-rc-axios/) | [官方公告](https://devblogs.microsoft.com/typescript/announcing-typescript-6.0/)
- **TypeScript 6.0 RC 发布** - [JSer.info](https://jser.info/2026/03/12/typescript-6.0-rc-solid-v2.0.0-beta-node.js/)
- **jQuery 4.0.0 发布** - jQuery 20 周年纪念主要版本，移除 IE10 及以下支持
  来源: [JSer.info](https://jser.info/2026/01/26/jquery-4.0.0-rolldown-1.0-rc-styelelint-17/)
- **Temporal API 达到 Stage 4** - 9 年的标准化旅程，将进入 ES2026
  来源: [FE News](https://bloomberg.github.io/js-blog/post/temporal/) | [JSer.info](https://jser.info/2026/03/22/vite-8.0-temporal-stage-4-next.js-16.2/)
- **Node.js 安全更新** - Node.js 20.20.0/22.22.0/24.13.0/25.3.0 安全版本发布
  来源: [JSer.info](https://jser.info/2026/01/17/node.js-chrome-144-firefox-147-electron-40/)
- **Node.js 将从 27 版本开始采用年度主要版本发布** - [FE News](https://socket.dev/blog/node-js-moves-to-annual-major-releases-starting-with-node-27)
- **Node.js worker threads 的问题与解决方案** - Inngest 分享使用 Worker Threads 解决事件循环饥饿问题的经验
  来源: [FE News](https://www.inngest.com/blog/node-worker-threads)
- **Intl API: 你没有使用的最佳浏览器 API** - [JSer.info](https://jser.info/2026/04/15/pnpm-11-rc-0-webpack-5.106-servo-v0.1.0/)

### 🛠️ 工具/构建

- **pnpm 11 RC 0 发布** - 纯 ESM 包迁移，Node.js 18-21 支持终止，.npmrc 仅限认证/注册表配置，pnpm ci 命令新增，SBOM 生成支持
  来源: [JSer.info](https://jser.info/2026/04/15/pnpm-11-rc-0-webpack-5.106-servo-v0.1.0/) | [GitHub](https://github.com/pnpm/pnpm/releases/tag/v11.0.0-rc.0)
- **Vite 8.0 发布** - [JSer.info](https://jser.info/2026/03/22/vite-8.0-temporal-stage-4-next.js-16.2/)
- **Bun v1.3.12 发布** - 新增 Bun.WebView、支持直接执行 Markdown 文件 (bun ./file.md)、新增回调式 cron 调度器 Bun.cron()、支持 Explicit Resource Management (using/await using)
  来源: [JSer.info](https://jser.info/2026/04/15/pnpm-11-rc-0-webpack-5.106-servo-v0.1.0/) | [Bun Blog](https://bun.com/blog/bun-v1.3.12)
- **webpack 5.106 发布** - 新增 Plugin Validation Hook (compiler.hooks.validate)、CSS Modules 运行时样式注入支持 (exportType: "style")、CommonJS Tree Shaking 改善、新增 create-webpack-app 工具、实验性 WebAssembly 支持 (ES Stage 3 Source Phase Imports)、oxc-parser 支持
  来源: [JSer.info](https://jser.info/2026/04/15/pnpm-11-rc-0-webpack-5.106-servo-v0.1.0/) | [webpack 博客](https://webpack.js.org/blog/2026-04-08-webpack-5-106/)
- **Rolldown 1.0 RC 发布** - [JSer.info](https://jser.info/2026/01/26/jquery-4.0.0-rolldown-1.0-rc-styelelint-17/)
- **Stylelint 17 发布** - [JSer.info](https://jser.info/2026/01/26/jquery-4.0.0-rolldown-1.0-rc-styelelint-17/)
- **Yarn 6 Preview 发布** - Rust 重写，性能改善
  来源: [JSer.info](https://jser.info/2026/02/04/yarn-6-preview-webassembly-10-state-of-javascript-2025/)
- **Pagefind v1.5.0 发布** - Rust JavaScript 搜索库，新增 Web Components UI 系统、元数据字段默认索引、CJK 查询自动分词、Web Worker 搜索执行
  来源: [JSer.info](https://jser.info/2026/04/15/pnpm-11-rc-0-webpack-5.106-servo-v0.1.0/)
- **Servo v0.1.0 发布** - Rust 编写的嵌入式 Web 渲染引擎，提供轻量级高性能替代方案，Embedding API 已在 crates.io 发布
  来源: [JSer.info](https://jser.info/2026/04/15/pnpm-11-rc-0-webpack-5.106-servo-v0.1.0/) | [Servo 博客](https://servo.org/blog/2026/04/13/servo-0.1.0-release/)
- **yuku-toolchain/yuku** - 纯 Zig 编写的高性能 JavaScript/TypeScript 编译器和工具链
  来源: [JSer.info](https://jser.info/2026/04/15/pnpm-11-rc-0-webpack-5.106-servo-v0.1.0/)
- **Deno 2.7 发布** - [JSer.info](https://jser.info/2026/02/26/electrobun-v1-deno-2.7-oxfmt-beta/)
- **Electrobun v1 发布** - TypeScript 跨平台桌面应用开发框架
  来源: [JSer.info](https://jser.info/2026/02/26/electrobun-v1-deno-2.7-oxfmt-beta/)

### 🎨 CSS/样式

- **Google 打击"劫持返回按钮"行为** - 从 6 月中旬开始，Google 搜索将开始惩罚"劫持"返回按钮的网站
  来源: [Frontend Focus #737](https://frontendfoc.us/issues/737) | [Google](https://developers.google.com/search/docs/specialty/seo/back-button-hijacking)
- **CSS View Transitions 初学者指南** - 只需一行 CSS 即可为多页应用带来流畅的动画导航
  来源: [MDN Blog](https://developer.mozilla.org/en-US/blog/view-transitions-beginner-guide/)
- **图像格式：编解码器和压缩工具** - 在系列的最后一部分中，实验编解码器、指标和工具以找到平衡效率和视觉保真度的实用方法
  来源: [MDN Blog](https://developer.mozilla.org/en-US/blog/image-formats-codecs-compression-tools/)
- **图像格式：从编码器到解码器的像素数据** - 从单个像素到屏幕上完全解码的图像，原始像素数据经过转换、压缩和高效交付
  来源: [MDN Blog](https://developer.mozilla.org/en-US/blog/image-formats-pixels-graphics/)

### 🚀 性能优化

- **The 49MB Web Page** - New York Times 仅显示四个标题就需要 422 个网络请求和 49MB 数据，加载时间 2 分钟的分析结果
  来源: [FE News](https://thatshubham.com/blog/news-audit)
- **使 diff 行性能化的艰难爬坡** - [JSer.info](https://jser.info/2026/04/15/pnpm-11-rc-0-webpack-5.106-servo-v0.1.0/)

### 🧪 测试/质量

- **Summary of CVE-2026-23869** - Vercel 安全漏洞总结
  来源: [JSer.info](https://jser.info/2026/04/15/pnpm-11-rc-0-webpack-5.106-servo-v0.1.0/)

### 🤖 AI/机器学习

- **Chrome 原生支持技能** - Chrome 官方宣布支持在 Gemini 插件中使用技能（skill），即预置提示词，一键完成任务
  来源: [阮一峰周刊](https://blog.google/products-and-platforms/products/chrome/skills-in-chrome/)
- **Claude Code 源码真相** - Claude Code 源码泄漏研究发现源码全部由 AI 生成，质量不高，一个函数长达 3,167 行，包含 486 个判断分支和 12 层嵌套
  来源: [阮一峰周刊](https://techtrenches.dev/p/the-snake-that-ate-itself-what-claude)
- **Skill Issue: Andrej Karpathy on Code Agents** - Andrej Karpathy 讨论 AI 模型能力限制、编码代理熟练度、自然语言编码的二次效应等
  来源: [FE News](https://www.youtube.com/watch?v=kwSVtQ7dziU)
- **From IDEs to AI Agents with Steve Yegge** - Steve Yegge 讨论 AI 如何改变软件工程工作
  来源: [FE News](https://www.youtube.com/watch?v=aFsAOu2bgFk)
- **Agent Skills with Anthropic** - [FE News](https://www.deeplearning.ai/short-courses/agent-skills-with-anthropic/)
- **AI 工具推荐**：
  - **OmniVoice Studio** - 视频配音 AI 桌面应用，支持语音翻译和克隆，完全本地生成
  - **EVA** - 极简 AI 编程智能体，单个 Python 脚本，低配版 Claude Code
  - **claude-msync** - 导出 claude code 记忆的命令行工具
  - **TokenTracker** - 本地 Token 消耗统计报表生成工具
    来源: [阮一峰周刊](http://www.ruanyifeng.com/blog/2026/04/weekly-issue-393.html)

### 🔒 安全

- **Axios npm 包遭受供应链攻击** - 交付跨平台 RAT 恶意软件
  来源: [FE News](https://snyk.io/blog/axios-npm-package-compromised-supply-chain-attack-delivers-cross-platform/) | [JSer.info](https://jser.info/2026/04/06/typescript-6.0-es2026-rc-axios/)
- **Node.js 安全更新** - 多个版本的安全版本发布
  来源: [JSer.info](https://jser.info/2026/01/17/node.js-chrome-144-firefox-147-electron-40/)
- **Hacker News 禁止 AI 生成评论** - 明确禁止发布 AI 生成或 AI 编辑的评论
  来源: [FE News](https://news.ycombinator.com/newsguidelines.html)

### 📊 GitHub/开源

- **andrej-karpathy-skills** - 基于 Andrej Karpathy 对 LLM 编码陷阱观察的 CLAUDE.md 文件，改善 Claude Code 行为
  来源: [GitHub Trending](https://github.com/forrestchang/andrej-karpathy-skills)
- **Show HN: Daemons** - 从构建代理转向清理代理产物的产品类别，为处理代理创建输出的运营拖累而构建
  来源: [Hacker News Show](https://charlielabs.ai/)
- **Show HN: GoModel** - Go 编写的开源 AI 网关，Docker 镜像仅 17MB，比 LiteLLM 小 44 倍
  来源: [Hacker News Show](https://github.com/ENTERPILOT/GOModel/)
- **Show HN: VidStudio** - 不上传文件的浏览器视频编辑器
  来源: [Hacker News Show]

### 📚 周刊摘要

#### 阮一峰科技爱好者周刊 #393

**本期核心内容总结：**

- **脑腐状态** - 讨论"脑腐"（brain rot）现象，即思考能力下降、难以长时间集中注意力。主要原因是网络平台的夸张"标题党"文章和短视频，导致大脑被密集刺激，思维兴奋状态维持时间越来越短。应对之策可能是将学习和思考拆解成一系列短问题。[链接](https://jshamsul.com/essays/2026-04-12-brainrot-industrial-complex)
- **权重有没有版权？** - 讨论开源大模型权重的版权问题。有人认为权重是计算结果，没有版权；计算结果不过是机械过程的产物，不涉及人类创造力。[链接](https://news.ycombinator.com/item?id=47738685)
- **摄像头耳机** - 华盛顿大学开发出世界首个带有微型摄像头的无线耳机，用于与 AI 互动。[链接](https://www.washington.edu/news/2026/04/14/cameras-in-wireless-earbuds-vuebuds/)
- **AI 歌手** - AI 歌手 Eddie Dalton 在 iTunes 单曲榜前 100 名中占据 11 席。[链接](https://www.showbiz411.com/2026/04/05/itunes-takeover-by-fake-ai-singer-eddie-dalton-now-occupies-eleven-spots-on-chart-despite-not-being-human-or-real-exclusive)
- **经济舱座椅** - 美联航推出可拆卸座椅的经济舱，允许乘客躺在地上睡觉。[链接](https://www.usatoday.com/story/travel/airline-news/2026/03/24/united-couch-style-economy-seats/89306783007/)

**工具推荐**：

- **DAVINCI RESOLVE 21** - 视频编辑软件新增图像编辑功能 [链接](https://www.blackmagicdesign.com/products/davinciresolve/photo)
- **Phyphox** - 手机传感器应用 [链接](https://phyphox.org/)
- **Material You NewTab** - Chrome 新标签页定制插件 [链接](https://github.com/XengShi/materialYouNewTab)
- **ClipCascade** - 剪贴板同步工具 [链接](https://github.com/Sathvik-Rao/ClipCascade)
- **Gridea Pro** - 静态博客写作客户端 [链接](https://github.com/Gridea-Pro/gridea-pro)
- **Recordly** - 开源录屏与编辑工具 [链接](https://github.com/webadderall/Recordly)
- **Input 0** - macOS 语音输入工具 [链接](https://github.com/10xChengTu/input0)
- **OpenToggl** - 开源时间追踪工具 [链接](https://github.com/CorrectRoadH/OpenToggl)

#### JSer.info #769 (2026-04-15)

**本期核心内容总结：**

- **pnpm 11 RC 0 发布** - 纯 ESM 包迁移，Node.js 18-21 支持终止，.npmrc 仅限认证/注册表配置，pnpm ci 命令新增，SBOM 生成支持，供应链安全加强 [链接](https://github.com/pnpm/pnpm/releases/tag/v11.0.0-rc.0)
- **webpack 5.106 发布** - 新增 Plugin Validation Hook、CSS Modules 运行时样式注入支持、CommonJS Tree Shaking 改善、新增 create-webpack-app 工具、实验性 WebAssembly 支持 [链接](https://webpack.js.org/blog/2026-04-08-webpack-5-106/)
- **Bun v1.3.12 发布** - 新增 Bun.WebView、支持直接执行 Markdown 文件、新增回调式 cron 调度器、支持 Explicit Resource Management [链接](https://bun.com/blog/bun-v1.3.12)
- **Servo v0.1.0 发布** - Rust 编写的嵌入式 Web 渲染引擎，提供轻量级高性能替代方案 [链接](https://servo.org/blog/2026/04/13/servo-0.1.0-release/)
- **Pagefind v1.5.0 发布** - Rust JavaScript 搜索库，新增 Web Components UI 系统、元数据字段默认索引、CJK 查询自动分词 [链接](https://github.com/Pagefind/pagefind/releases/tag/v1.5.0)

**文章推荐**：

- **Summary of CVE-2026-23869** - Vercel 安全漏洞总结 [链接](https://vercel.com/blog/summary-of-cve-2026-23869)
- **The uphill climb of making diff lines performant** - 使 diff 行性能化的艰难爬坡 [链接](https://github.blog/2026-04-08-the-uphill-climb-of-making-diff-lines-performant/)
- **React Server Components Your Way** - TanStack Blog [链接](https://tanstack.com/blog/latest/react-server-components-your-way)
- **The Intl API: The best browser API you're not using** - 你没有使用的最佳浏览器 API [链接](https://polypane.app/blog/the-intl-api-the-best-browser-api-youre-not-using/)
- **Under the hood of MDN's new frontend** - MDN 新前端技术深度解析 [链接](https://developer.mozilla.org/en-US/blog/mdn-front-end-deep-dive/)

#### FE News 2026-04

**本期核心内容总结：**

- **The 49MB Web Page** - NYT 页面性能分析，仅显示四个标题就需要 422 个网络请求和 49MB 数据 [链接](https://thatshubham.com/blog/news-audit)
- **Node.js worker threads** - Inngest 分享使用 Worker Threads 解决事件循环饥饿问题的经验 [链接](https://www.inngest.com/blog/node-worker-threads)
- **Temporal API** - 9 年修复 JavaScript 时间问题的旅程，将进入 ES2026 [链接](https://bloomberg.github.io/js-blog/post/temporal/)
- **产品开发团队角色演变** - AI 工具对产品开发团队角色的影响分析 [链接](https://www.figma.com/ko-kr/reports/shifting-roles-product-teams-evolving)
- **Hacker News 禁止 AI 生成评论** - 明确禁止发布 AI 生成或 AI 编辑的评论 [链接](https://news.ycombinator.com/newsguidelines.html)
- **Andrej Karpathy 论代码代理** - 讨论 AI 模型能力限制、编码代理熟练度、自然语言编码的二次效应等 [链接](https://www.youtube.com/watch?v=kwSVtQ7dziU)
- **Steve Yegge 论从 IDE 到 AI 代理** - 讨论 AI 如何改变软件工程工作 [链接](https://www.youtube.com/watch?v=aFsAOu2bgFk)
- **设计系统超越代码** - 将设计系统视为产品而非简单组件库 [链接](https://so-so.dev/react/design-system-beyond-code/)
- **Node.js 年度主要版本发布** - 从 Node 27 开始采用年度主要版本发布计划 [链接](https://socket.dev/blog/node-js-moves-to-annual-major-releases-starting-with-node-27)
- **TypeScript 6.0 发布** - TypeScript 6.0 正式发布公告 [链接](https://devblogs.microsoft.com/typescript/announcing-typescript-6.0/)

**代码与工具**：

- **Pretext** - [链接](https://github.com/chenglou/pretext)
- **shadcn/cli v4** - [链接](https://ui.shadcn.com/docs/changelog/2026-03-cli-v4)
- **Gea** - [链接](https://github.com/dashersw/gea)
- **Defuddle** - [链接](https://github.com/kepano/defuddle)
- **Emulate** - [链接](https://emulate.dev/)
- **Ohm** - [链接](https://github.com/ohmjs/ohm)
- **Collaborator** - [链接](https://github.com/collaborator-ai/collab-public)
- **Agent Flow** - [链接](https://github.com/patoles/agent-flow)
- **RTK (Rust Token Killer)** - [链接](https://github.com/rtk-ai/rtk)
- **GSD (Get Shit Done)** - [链接](https://github.com/gsd-build/get-shit-done)
- **OpenSpec** - [链接](https://github.com/Fission-AI/OpenSpec/)
- **Impeccable** - [链接](https://github.com/pbakaus/impeccable)
- **UI UX Pro Max** - [链接](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill)
- **Agency Agents** - [链接](https://github.com/msitarzewski/agency-agents)
- **Promptfoo** - [链接](https://github.com/promptfoo/promptfoo)
- **Understand-Anything** - [链接](https://github.com/Lum1104/Understand-Anything)
- **Claude Health** - [链接](https://github.com/tw93/claude-health)
- **Supermemory** - [链接](https://github.com/supermemoryai/supermemory)

**安全警告**：

- **Axios npm 包供应链攻击** - 交付跨平台 RAT 恶意软件 [链接](https://snyk.io/blog/axios-npm-package-compromised-supply-chain-attack-delivers-cross-platform/)

---

📅 抓取时间: 2026-04-22
📡 数据源: 11/11 成功
