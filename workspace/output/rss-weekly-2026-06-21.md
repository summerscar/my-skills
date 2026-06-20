---
layout: default
title: 前端技术周报 (2026-06-21)
date: 2026-06-21
category: RSS 周报
---

## 📰 前端技术周报 (2026-06-21)

### 📝 本周要点

- **React Router v8 is boring but good** — 第 479 期 React Status 封面文章，讨论 React Router v8 的"无聊但好"设计哲学
  来源: React Status | [链接](https://react.statuscode.com/issues/479)
- **JavaScript Weekly #790: Flow for TypeScript Users** — Meta 的 Flow 类型系统与 TypeScript 的对比
  来源: JavaScript Weekly | [链接](https://javascriptweekly.com/issues/790)
- **Cloudflare 收购 VoidZero** — Vite/Oxc 背后的公司被 Cloudflare 收购，JSer.info 头条
  来源: JSer.info | [链接](https://jser.info/)
- **Declarative Partial Updates API** — Chrome 148 实验性功能，无需 JS 的 HTML 部分更新
  来源: FE News | [链接](https://developer.chrome.com/blog/declarative-partial-updates)
- **阮一峰周刊 #400: rsync 的争论** — rsync 最新版由 Claude 生成引发轩然大波
  来源: 阮一峰博客 | [链接](https://www.ruanyifeng.com/blog/2026/06/weekly-issue-400.html)
- **TanStack npm 供应链攻击复盘** — 42 个包、84 个恶意版本、6 分钟完成攻击
  来源: FE News | [链接](https://tanstack.com/blog/npm-supply-chain-compromise-postmortem)
- **MDN MCP Server 发布** — 允许 AI 工具直接查询 MDN 文档
  来源: MDN Blog | [链接](https://developer.mozilla.org/en-US/blog/introducing-mdn-mcp-server/)

---

### ⚛️ React/前端框架

- **React Router v8 发布** — "boring but good" 设计哲学，稳定可靠
  来源: React Status #479 | [链接](https://react.statuscode.com/issues/479)
- **React Server Components in TanStack** — TanStack 团队实现 RSC 方案
  来源: Frontend Masters | [链接](https://frontendmasters.com/blog/react-server-components-in-tanstack/)
- **TanStack Router and Query 深度整合** — Tkdodo 博客分析两库协同
  来源: Frontend Focus | [链接](https://tkdodo.eu/blog/tan-stack-router-and-query)
- **React Server Components 与 Bundler 的集成** — 深入分析 RSC 工作原理
  来源: Frontender Digest #470 | [链接](https://reactjs-maxxing.vercel.app/blog/how-react-server-component-integrate-with-bundler)
- **Angular v22 发布** — CDK Component Portals 新指令
  来源: Frontender Digest #470 | [链接](https://blog.angular.dev/announcing-angular-v22-c52bb83a4664)
- **Solid 2.0 Beta 支持 TanStack** — TanStack Router/Start/Query 新增 Solid 支持
  来源: Frontender Digest #470 | [链接](https://tanstack.com/blog/tanstack-start-solid-v2)
- **TanStack Start 认证指南** — 2026 年开发者指南
  来源: Frontender Digest #470 | [链接](https://workos.com/blog/tanstack-start-authentication-guide)
- **Next.js App Router 缓存解析** — 深入理解 React 缓存机制
  来源: Frontender Digest #470 | [链接](https://jsdev.space/nextjs-app-cache/)
- **React 19 升级在 WordPress 中临时回退** — Gutenberg 编辑器兼容性问题
  来源: Frontender Digest #470 | [链接](https://make.wordpress.org/core/2026/06/05/react-19-upgrade-temporarily-reverted-in-gutenberg/)
- **Ember 7.0 发布**
  来源: Frontender Digest #470 | [链接](https://blog.emberjs.com/ember-released-7-0/)

---

### 📦 JavaScript/TypeScript

- **Flow for TypeScript Users in 2026** — Meta 的 Flow 与 TypeScript 差异对比，Flow 更严格
  来源: JavaScript Weekly #790
- **TypeScript 7.0 Beta 发布** — 重大版本更新
  来源: Frontender Digest #470 | [链接](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0-beta/)
- **TypeScript 6.0 迁移指南** — tsconfig 变更和适配
  来源: Frontender Digest #470 | [链接](https://www.sitepoint.com/typescript-60-migration-what-changed-and-how-to-adapt-your-tsconfig/)
- **pnpm 11.5 发布** — hoistingLimits 配置、交互式提示改进、Staged publishing 支持
  来源: JSer.info | [链接](https://github.com/pnpm/pnpm/releases/tag/v11.5.0)
- **Node.js 26.3.0 发布** — Buffer.poolSize 默认值改为 64 KiB、`permission.drop` 等
  来源: JSer.info | [链接](https://nodejs.org/en/blog/release/v26.3.0)
- **npm v12 停止运行安装脚本** — 安全大改进
  来源: Frontender Digest #470
- **ES2026 新特性** — 真正改变代码写法的新功能
  来源: Frontender Digest #470 | [链接](https://www.alexcloudstar.com/blog/es2026-javascript-features-guide/)
- **The quiet problem with unnecessary async** — 滥用 async 的问题分析
  来源: Frontender Digest #470 | [链接](https://allthingssmitty.com/2026/06/08/the-quiet-problem-with-unnecessary-async/)
- **TSRX — TypeScript 语言扩展** — 面向 AI Agent 时代的声明式 UI
  来源: Frontender Digest #470 | [链接](https://tsrx.dev/)
- **TypeScript Tips Everyone Should Know** — GitHub 热门资源
  来源: Frontender Digest #470 | [链接](https://github.com/AllThingsSmitty/typescript-tips-everyone-should-know)

---

### 🎨 CSS/样式

- **CSS @function 的作用域能力** — @function 的超能力
  来源: Frontend Focus #746 | [链接](https://frontendfoc.us/issues/746)
- **CSS @function 基础和开发体验** — 详细介绍
  来源: Frontender Digest #470 | [链接](https://frontendmasters.com/blog/the-fundamentals-and-dev-experience-of-css-function/)
- **The Field Guide to Grid Lanes** — WebKit 团队发布的网格车道指南
  来源: Frontender Digest #470 | [链接](https://gridlanes.webkit.org/)
- **Scroll-Driven, Scroll-Triggered, Scroll States and View Transitions** — CSS-Tricks 综合指南
  来源: Frontender Digest #470 | [链接](https://css-tricks.com/scroll-driven-scroll-triggered-scroll-states-and-view-transitions/)
- **Building Glass for the Web** — Aave 设计团队的玻璃效果实现
  来源: Frontender Digest #470 | [链接](https://aave.com/design/building-glass-for-the-web)
- **transitions.dev** — View Transitions 演示
  来源: Frontender Digest #470 | [链接](https://transitions.dev/)
- **Building a UI Without Breakpoints** — 无断点 UI 设计
  来源: Frontender Digest #470 | [链接](https://frontendmasters.com/blog/building-a-ui-without-breakpoints/)
- **In-N-Out Animations: Dialogs (Part 1)** — 弹窗入场/出场动画系列
  来源: Frontender Digest #470 | [链接](https://frontendmasters.com/blog/in-n-out-animations-dialogs-part-1-3/)
- **Container Timing API Origin Trial** — Chrome 148 开始 Origin Trial，可精细测量组件级别渲染性能
  来源: FE News | [链接](https://developer.chrome.com/blog/container-timing-origin-trial)
- **Theme Toggle Effect** — View Transitions API 实现深色/浅色模式切换动画
  来源: FE News | [链接](https://theme-toggle.rdsx.dev/)

---

### 🛠 工具/构建

- **Declarative Partial Updates** — Chrome 148 实验功能: Out-of-Order Streaming + HTML Streaming Methods，无需 JS 框架即可实现 HTML 局部更新
  来源: FE News | [链接](https://developer.chrome.com/blog/declarative-partial-updates)
- **VoidZero 被 Cloudflare 收购** — VoidZero (Vite/Oxc/Rolldown) 团队加入 Cloudflare
  来源: JSer.info | [链接](https://blog.cloudflare.com/voidzero-joins-cloudflare/)
- **Rolldown 1.0 发布** — VoidZero 团队的新打包工具
  来源: Frontender Digest #470 | [链接](https://voidzero.dev/posts/announcing-rolldown-1-0)
- **Yelp 从 Webpack 迁移到 Rspack** — 构建时间优化经验
  来源: Frontender Digest #470 | [链接](https://engineeringblog.yelp.com/2026/05/optimizing-our-build-times-by-migrating-from-webpack-to-rspack.html)
- **Wave Terminal** — AI 功能内置的开源终端，支持 SSH 切换、远程文件编辑
  来源: FE News | [链接](https://www.waveterm.dev/)
- **gh-stack — GitHub CLI 官方栈式 PR 工具** — 将大 PR 拆分为小 PR 链
  来源: FE News | [链接](https://github.com/github/gh-stack)
- **Mesurer — React 测量工具** — 快捷键切换元素测量和间距对齐
  来源: FE News | [链接](https://mesurer.ibelick.com/)
- **MarkItDown** — Microsoft 开源的文档转 Markdown 工具 (135k stars)
  来源: FE News | [链接](https://github.com/microsoft/markitdown)

---

### ⚡ 性能优化

- **Ending Responsive Images** — 响应式图片的终结
  来源: Frontender Digest #470 | [链接](https://cloudfour.com/thinks/ending-responsive-images/)
- **Image Optimization for Core Web Vitals in 2026** — 真正有效的图片优化策略
  来源: Frontender Digest #470 | [链接](https://www.sitepoint.com/image-optimization-for-core-web-vitals-in-2026-what-actually-moves-the-needle/)
- **Container Timing API** — 组件级别性能监控，超越 LCP
  来源: FE News | [链接](https://developer.chrome.com/blog/container-timing-origin-trial)
- **Uber 设计规格自动化系统 uSpec** — AI Agent 将数百组件设计规格文档从数周缩短到 2 分钟
  来源: FE News | [链接](https://www.uber.com/ca/en/blog/automate-design-specs/)

---

### 🧪 测试/质量

- **TanStack npm 供应链攻击复盘** — 42 个包 84 个恶意版本，6 分钟内完成攻击，20 分钟内被检测
  来源: FE News | [链接](https://tanstack.com/blog/npm-supply-chain-compromise-postmortem)
- **NVIDIA SkillSpector** — AI Agent 技能安全扫描器，检测漏洞和恶意模式
  来源: GitHub Trending | [链接](https://github.com/NVIDIA/SkillSpector)
- **npm v12 安全大升级** — 阻止安装后脚本运行
  来源: Frontender Digest #470 | [链接](https://www.aikido.dev/blog/npm-v12-block-postinstall)

---

### 🤖 AI/机器学习

- **State of AI 2026 调查结果** — 7,258 名开发者参与，TypeScript 首次超越 JavaScript，AI 代码占比升至 54%
  来源: FE News | [链接](https://2026.stateofai.dev/en-US)
- **A.I. Has Created a Code Overload** — 纽约时报分析 AI 代码激增带来的代码审查瓶颈
  来源: FE News | [链接](https://www.nytimes.com/2026/04/06/technology/ai-code-overload.html)
- **Redesigning Workflows for AI** — Jakob Nielsen：将 AI 嵌入现有流程 vs. 围绕 AI 重建流程
  来源: FE News | [链接](https://www.uxtigers.com/post/workflow-redesign)
- **A2UI — Google 开源的 AI Agent UI 协议** — 声明式数据格式，安全生成多平台 UI
  来源: FE News | [链接](https://a2ui.org/)
- **阮一峰: AI 写代码 + 人类测试模式** — rsync 3.4.3 由 Claude 生成引发的思考
  来源: 阮一峰博客
- **阮一峰: Token 费用难以负担** — 一个程序员一年可能花掉两三百万人民币的 Token 费用
  来源: 阮一峰博客
- **LLM 权重是什么** — 科普：模型代码几十 KB，权重却几十 GB
  来源: 阮一峰博客 | [链接](https://mp.weixin.qq.com/s/TM9lv6b-9AH8O9ZiApgTBA)
- **DeepSeek Reasonix** — 专为 DeepSeek 设计的终端 AI 编程 Agent，充分利用缓存降低费用
  来源: 阮一峰博客 | [链接](https://github.com/esengine/DeepSeek-Reasonix)
- **FunASR + FunClip** — 阿里通义语音识别工具包和智能视频裁剪
  来源: 阮一峰博客 | [链接](https://github.com/modelscope/FunASR)

---

### 📚 周刊摘要

#### 阮一峰科技爱好者周刊 #400

**本期核心内容：**

- **rsync 的争论** — rsync 3.4.3 由 Claude 生成引发社区愤怒。维护者 Andrew Tridgell 回应：AI 发现大量漏洞，个人精力不足以应对，引入 AI 写代码 + 更严格测试是未来方向
- **今天可以放假吗？** — AI 提高效率后能否放假一天的讨论
- **防止 Siri 被唤醒** — 苹果在 WWDC 演讲中通过删除 3k/4k/5k/6kHz 频率防止听众设备被 Siri 唤醒
- **AI 客服漏洞** — Meta AI 客服可通过简单提示词篡改用户账户（包括奥巴马账户）
- **避蚊胺研究** — 蚊子可通过条件反射适应驱蚊水

**工具推荐：**
- **ffmpeg webCLI** — 基于网页的视频编辑器，离线运行 [链接](https://github.com/tejaswigowda/ffmpeg-webCLI)
- **oproxy** — 开源本地中间人代理 [链接](https://github.com/sauravrao637/oproxy)
- **ALTCHA** — 开源 Captcha 替代品 [链接](https://altcha.org/captcha/)
- **Lightpanda Browser** — AI 自动化专用无头浏览器，内存比 Chrome 小 9 倍 [链接](https://github.com/lightpanda-io/browser)
- **中文诗词 API** — Go 语言高性能古诗词 API [链接](https://github.com/palemoky/chinese-poetry-api)
- **WorldIP.io** — 免费 IP 地址查询 [链接](https://worldip.io/)

#### 阮一峰科技爱好者周刊 #399

**本期核心内容：**

- **Token 费用难以负担** — 一名程序员一年可能花掉两三百万人民币的 Token 费用。Uber 四个月花完全年 AI 预算，微软放弃 Claude Code
- **漏洞赏金计划的终结** — AI 生成的漏洞洪水让开源项目不堪重负，Turso 终止赏金计划
- **中国 AI 大厂访问记** — 美国访问团考察 DeepSeek、字节跳动等 14 家公司的详细报告

#### FE News 2026-06

**本期核心内容：**

- **Declarative Partial Updates** — Chrome 148 新增 Out-of-Order Streaming 和 HTML Streaming Methods，无需 JS 框架即可实现 HTML 流式部分更新
- **State of AI 2026** — 调查显示 TypeScript 首次超越 JS 成为最常用语言，AI 生成代码占比从 28% 升至 54%，Cursor 成为第二大编辑器
- **TanStack 供应链攻击** — 42 个 npm 包 6 分钟内被投毒，攻击链：`pull_request_target` + GitHub Actions 缓存 + OIDC 令牌提取
- **Container Timing API** — 组件级性能监控 Chrome Origin Trial 开始
- **Uber uSpec 系统** — AI Agent + MCP 将设计文档从数周缩短到 2 分钟
- **A2UI 协议** — Google 开源，AI Agent 安全生成跨平台 UI
- **AI 代码过载** — 月代码量增长 10 倍，审查瓶颈严重

**代码与工具：**
- **Wave Terminal** — AI 内置开源终端，支持 SSH/远程文件/内嵌浏览器 [链接](https://www.waveterm.dev/)
- **tegaki** — 任何字体转动画手写体 [链接](https://github.com/KurtGokhan/tegaki)
- **gh-stack** — GitHub 官方栈式 PR CLI [链接](https://github.com/github/gh-stack)
- **MarkItDown** — Microsoft 文档转 Markdown 工具 [链接](https://github.com/microsoft/markitdown)
- **Rapid-MLX** — Apple Silicon 上运行本地 AI 模型，比 Ollama 快 4.2 倍 [链接](https://github.com/raullenchai/Rapid-MLX)
- **Multica** — 开源管理型 AI Agent 平台 [链接](https://github.com/multica-ai/multica)
- **Meetily** — 本地 AI 会议助手，所有数据本地处理 [链接](https://github.com/Zackriya-Solutions/meetily)
- **Clawd on Desk** — AI 编程 Agent 桌面像素宠物 [链接](https://github.com/rullerzhou-afk/clawd-on-desk)
- **whatcani.run** — Apple Silicon Mac 本地 AI 模型性能对比 [链接](https://www.whatcani.run/)

---

### 🔥 Hacker News 热门

- **Are You in the Weights?** — 查询 AI 模型是否"认识"你的个人识别网站 (452 pts) [链接](https://www.intheweights.com/)
- **Gerrymandle** — 每日选举区重划益智游戏 (221 pts) [链接](https://gerrymandle.cc/)
- **Talos** — Lean 形式的开源 WASM 形式验证框架 (98 pts) [链接](https://github.com/cajal-technologies/talos)
- **8-bit 棒球直播** — 实时 MLB 数据转像素艺术直播 (253 pts) [链接](https://ribbie.tv/)
- **184 个免费浏览器工具** — Brevio.pro 完全本地处理 (88 pts) [链接](https://brevio.pro)
- **High-Res Neural Cellular Automata** — 高清神经细胞自动机 (203 pts) [链接](https://cells2pixels.github.io/)
- **Metiq** — 实时 3D 地球展示 100+ 公共数据集 (137 pts) [链接](https://metiq.space/)
- **Garden of Flowers** — 2500+ 幅 17 世纪活字印刷艺术图像档案 (160 pts) [链接](https://garden-of-flowers.heikkilotvonen.com/)
- **Kage** — 将任何网站镜像为离线单二进制文件 (708 pts) [链接](https://github.com/tamnd/kage)
- **Trace** — macOS 离线会议转录 App (205 pts) [链接](https://traceapp.info/)
- **Paca** — 用 Go 写的轻量 Jira 替代品，支持人+AI 协作 (173 pts) [链接](https://github.com/Paca-AI/paca)
- **Putt.day** — 每日迷你高尔夫游戏 (318 pts) [链接](https://putt.day/)
- **Capacitor Alarm Clock** — 用炸电容来叫醒你的闹钟 (153 pts) [链接](https://github.com/ArcaEge/capacitor-alarm-clock)
- **Inkwash** — 水彩画素描 App (247 pts) [链接](https://johnowhitaker.github.io/inkwash/about)

---

### 🌟 GitHub 热门

- **NVIDIA/SkillSpector** — AI Agent 技能安全扫描器 [链接](https://github.com/NVIDIA/SkillSpector)
- **machine0** — 持久化 NixOS VM CLI (96 pts HN) [链接](https://machine0.io/)
- **ccstatusline** — Claude Code 状态行格式化工具 [链接](https://github.com/sirmalloc/ccstatusline)
- **Codex Mate** — 一站式本地 AI 编程 Agent 管理面板 [链接](https://github.com/SakuraByteCore/codexmate)
- **office-open-xml-viewer** — 前端 JS Office 文件渲染组件 [链接](https://github.com/yukiyokotani/office-open-xml-viewer)
- **SnackBase** — 通用 Python Web 管理后端 [链接](https://github.com/lalitgehani/SnackBase)
- **performative-ui** — React AI 应用组件库 [链接](https://vorpus.github.io/performativeUI/)
- **@webc.site/math** — 浏览器原生 MathML 渲染库 [链接](https://github.com/webc-site/math)

---

### 📡 其他动态

- **MDN MCP Server 发布** — AI 工具可直接查询 MDN 文档 [链接](https://developer.mozilla.org/en-US/blog/introducing-mdn-mcp-server/)
- **Google 想让 Web Agent-Ready** — 面向 AI Agent 的 Web 改造 [链接](https://thenewstack.io/google-agent-ready-web/)
- **Reticulum** — 自组网项目，在各种物理网络上搭建虚拟网络 [链接](https://www.jonaharagon.com/posts/im-getting-into-mesh-networks-meshtastic-meshcore-and-reticulum/)
- **HTML-in-Canvas 提案** — 在 Canvas 中直接渲染 HTML [链接](https://tympanus.net/codrops/2026/05/13/exploring-the-html-in-canvas-proposal/)
- **npm 12 将停止运行安装脚本** — 2026 年最大安全改进之一 [链接](https://devops-daily.com/posts/npm-v12-install-scripts-audit)

---

📅 抓取时间: 2026-06-21 00:50
📡 数据源: 9/10 成功 (JavaScript Weekly 通过搜索获取)
