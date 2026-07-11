---
layout: default
title: 前端技术周报 (2026-07-12)
date: 2026-07-12
category: RSS 周报
---

## 📰 前端技术周报 (2026-07-12)

### 📝 本周要点

1. **TypeScript 7.0 正式发布** - 微软正式发布 TypeScript 7.0，语言引擎从 JS 改为 Go实现，速度提升10倍。
   来源: React Status, JavaScript Weekly, 阮一峰 | [链接](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/)

2. **ECMAScript 2026 规范正式获批** - 新增 Array.fromAsync、Uint8Array Base64/Hex转换、Math.sumPrecise()等。
   来源: JavaScript Weekly, JSer.info | [链接](https://pawelgrzybek.com/whats-new-in-ecmascript-2026/)

3. **Vite+ Beta发布：统一JS工具链** - Vite团队将Vite/Vitest/Oxlint整合到单个vp命令，MIT开源。
   来源: JavaScript Weekly, React Status | [链接](https://voidzero.dev/posts/announcing-vite-plus-beta)

4. **shadcn/ui 将 Base UI 设为默认组件库** - 新项目使用Base UI而非Radix。
   来源: React Status, JavaScript Weekly | [链接](https://ui.shadcn.com/docs/changelog/2026-07-base-ui-default)

5. **CSS Mixins 在 Chromium 中开始实现** - Edge团队实现浏览器原生CSS mixins。
   来源: Frontend Focus #749

6. **Safari引入MCP服务器** - TP 247支持Agent连接Safari窗口调试。
   来源: Frontend Focus, JavaScript Weekly | [链接](https://webkit.org/blog/18136/introducing-the-safari-mcp-server-for-web-developers/)

7. **MDN发布官方MCP服务器** - 将MDN文档带入AI工具和IDE。
   来源: MDN Blog | [链接](https://developer.mozilla.org/en-US/blog/introducing-mdn-mcp-server/)

8. **npm v12发布** - 生命周期脚本默认不再运行。
   来源: React Status #482

---

### React/前端框架

- **逆向工程ChatGPT Web** - React Router 7、TanStack Query、Radix、ProseMirror均在其中。
  来源: React Status #482 | [链接](https://performance.dev/chatgpt)

- **Vercel收购Better Auth** - 认证库团队加入Vercel。
  来源: React Status #482 | [链接](https://vercel.com/blog/vercel-acquires-better-auth)

- **Next.js WebSocket支持RFC** - Route Handlers中引入WebSocket。
  来源: React Status #482

- **vinext 1.0 Beta** - Cloudflare的Next.js替代，支持App Router、RSC、ISR。
  来源: React Status | [链接](https://github.com/cloudflare/vinext)

- **Meta开源Astryx设计系统** - 150+ React组件。
  来源: JavaScript Weekly | [链接](https://astryx.atmeta.com/)

- **Bun用Rust重写** - AI辅助移植，驱动Bun 1.4+。
  来源: React Status #482 | [链接](https://bun.com/blog/bun-in-rust)

### JavaScript/TypeScript

- **Vite 8.1发布** - 实验性开发时打包、Chunk Import Map。
  来源: JSer.info #775 | [链接](https://vite.dev/blog/announcing-vite8-1)

- **Deno 2.9发布** - 实验性desktop应用、跨包管理器lockfile。
  来源: JSer.info #775 | [链接](https://deno.com/blog/v2.9)

- **Medal将Electron bundle从40MB削减到2.7MB** - 代码分割和死代码消除。
  来源: JavaScript Weekly #793

- **Wordgard** - ProseMirror作者新富文本编辑器，支持协编。
  来源: JavaScript Weekly, Frontend Focus | [链接](https://wordgard.net/)

### CSS/样式

- **CSS锚点定位API全面支持** - 所有主流浏览器已支持。
  来源: Frontend Focus, 阮一峰 | [链接](https://www.joshwcomeau.com/css/anchor-positioning/)

- **CSS border-shape属性就绪** - Chromium独占，实现装饰效果。
  来源: Frontend Focus #749

### 工具/构建

- **Vite+ Beta** - 统一JS工具链。 | [链接](https://voidzero.dev/posts/announcing-vite-plus-beta)
- **Elm时隔6年发布新版本** - 前端编译语言。 | [链接](https://elm-lang.org/news/faster-builds)
- **webpack-dev-server 6.0** - Express 5 + ESM。
- **OverflowGuard** - 不依赖断点的自适应组件。 | [链接](https://overflowguard.dev/)

### AI/机器学习

- **AI成本已超工程师工资** - Anthropic AI支出是工资2.3倍。
  来源: 阮一峰 #403 | [链接](https://tomtunguz.com/ai-spend-breakeven-2029/)

- **MDN MCP服务器发布** - 文档直接注入IDE。
  来源: MDN Blog | [链接](https://developer.mozilla.org/en-US/blog/introducing-mdn-mcp-server/)

- **Safari MCP服务器** - Agent驱动浏览器调试。
  来源: Frontend Focus | [链接](https://webkit.org/blog/18136/introducing-the-safari-mcp-server-for-web-developers/)

### 周刊摘要

#### 阮一峰 #403

核心话题：**为什么Dropbox不成功** - 定位C端而非B端是根本原因。消费者只愿消磨时间不願为效率付费。市值60亿美元 vs Airbnb 850亿美元。

AI成本超过工程师、TypeScript 7.0发布、Elm时隔6年发布新版本。

工具：Davit、Flint、Vite+、FlareStarter

来源: 阮一峰 | [链接](https://www.ruanyifeng.com/blog/2026/07/weekly-issue-403.html)

#### JSer.info #775

Deno 2.9、Vite 8.1、ES2026正式批准、Node.js 24.18.0 LTS

### Hacker News热门

1. Fable: reMarkable变哈利波特日记 - 504分 | [链接](https://github.com/MaximeRivest/Riddle)
2. Anthropic: 语言模型全局工作空间 - 392分
3. Ternlight: 7MB浏览器嵌入模型 - 260分
4. Show HN: 原生Mac文件管理器 - 9MB无Electron | [链接](https://whimfiles.com/)

### GitHub热门

1. MadsLorentzen/ai-job-search - AI求职框架
2. facebook/astryx - Meta开源设计系统
3. browser-use/video-use - Agent编辑视频
4. usestrix/strix - AI安全测试代理
5. Zackriya-Solutions/meetily - 会议记录

### 深度阅读

1. The Descent: 前端20年技术演进 | [链接](https://davidpoblador.com/descent-frontend-evolution/)
2. Working with AI: htmx作者实践 | [链接](https://htmx.org/essays/working-with-ai/)

---
抓取时间: 2026-07-12 | 数据源: 9/10成功
