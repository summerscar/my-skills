---
layout: default
title: 前端技术周报 (2026-06-28)
date: 2026-06-28
category: RSS 周报
---

## 📰 前端技术周报 (2026-06-28)

### 📝 本周要点

1. **TypeScript 7.0 RC 发布** - 编译器移植到 Go 语言
2. **Babel 8.0.0 正式发布** - ESM-only, Node.js 24+ 必需
3. **Dan Abramov 加入 Next.js 团队**
4. **React Router v8 发布**
5. **MDN MCP Server 发布**
6. **CSS 自动选择可读文本颜色**
7. **VoidZero 加入 Cloudflare**

来源: JSer.info #774, React Status #480, MDN Blog, Frontend Focus #747, JavaScript Weekly, FE News 2026-06, 阮一峰周刊 #399-#401

### ⚛️ React/前端框架

- **Dan Abramov 加入 Next.js 团队** - React 核心成员加入 Vercel
  来源: React Status #480 | [链接](https://react.statuscode.com/issues/480)
- **React Router v8 发布** - Remix 新版路由 API
  来源: JSer.info #774 | [链接](https://remix.run/blog/react-router-v8)
- **VoidZero 加入 Cloudflare** - JS 工具链重大变动
  来源: JS Weekly #789 | [链接](https://javascriptweekly.com/issues/789)

### 📦 JavaScript/TypeScript

- **TypeScript 7.0 RC** - Go 移植编译器, typescript@rc 发布
  来源: JSer.info #774 | [链接](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0-rc/)
- **Babel 8.0.0** - ESM-only, Node 24+, 不再默认编译 ES5
  来源: JSer.info #774 | [链接](https://babeljs.io/blog/2026/06/16/8.0.0/)
- **JavaScript Temporal 即将到来** - 新日期时间 API
  来源: MDN Blog | [链接](https://developer.mozilla.org/en-US/blog/javascript-temporal-is-coming/)
- **Flow vs TypeScript in 2026** - Meta Flow 与 TS 语法趋近
  来源: JS Weekly #790 | [链接](https://javascriptweekly.com/issues/790)
- **Deno 2.9 支持桌面应用** - canary 版支持桌面构建
  来源: JS Weekly #791 | [链接](https://javascriptweekly.com/latest)

### 🎨 CSS/样式

- **CSS 自动选择可读文本颜色** - 根据背景自动选择前景色
  来源: Frontend Focus #747 | [链接](https://frontendfoc.us/issues/747)
- **View Transitions 入门指南** - 一行 CSS 实现页面过渡
  来源: MDN Blog | [链接](https://developer.mozilla.org/en-US/blog/view-transitions-beginner-guide/)
- **h1 默认样式即将改变** - 浏览器调整嵌套标题样式
  来源: MDN Blog | [链接](https://developer.mozilla.org/en-US/blog/h1-element-styles/)
- **Scroll Progress Animations** - 滚动驱动动画登陆 CSS
  来源: MDN Blog | [链接](https://developer.mozilla.org/en-US/blog/scroll-progress-animations-in-css/)

### 🔧 工具/构建

- **Vite 8.1 发布** - 性能改进
  来源: JS Weekly #791
- **GTmetrix MCP** - 性能测试 MCP 服务器
  来源: Frontender Digest #471 | [链接](https://gtmetrix.com/blog/gtmetrix-mcp/)
- **ALTCHA** - 开源 Captcha 替代品
  来源: 阮一峰周刊 #400 | [链接](https://altcha.org/captcha/)

### 📊 性能优化

- **优化 LCP** - 通过图片加载改善 Largest Contentful Paint
  来源: MDN Blog | [链接](https://developer.mozilla.org/en-US/blog/fix-image-lcp/)
- **JavaScript 性能修复** - 长任务/大包体积/水合问题
  来源: MDN Blog | [链接](https://developer.mozilla.org/en-US/blog/fix-javascript-performance/)

### 🤖 AI/机器学习

- **MDN MCP Server** - 为编码 AI 提供 Web 平台文档
  来源: MDN Blog | [链接](https://developer.mozilla.org/en-US/blog/introducing-mdn-mcp-server/)
- **Why AI Sucks At Front End** - LLM 前端结构性弱点
  来源: FE News 2026-06 | [链接](https://fenews.substack.com/p/fe-news-2026-06)
- **Lightpanda Browser** - AI 专用无头浏览器, 内存小 9 倍
  来源: 阮一峰周刊 #400 | [链接](https://github.com/lightpanda-io/browser)
- **OnePagent** - 单文件 AI 智能体工作台
  来源: 阮一峰周刊 #401 | [链接](https://github.com/sligter/OnePagent)

### 📚 周刊摘要

#### 阮一峰 #401: 如何赚到10亿美元

PG 牛津演讲: 创业赚10亿取决于增长率 x 持续时长。月增93%仅需9.5个月, 月增15%五年4384倍。
- Speedtest 12亿美元被收购, 靠出售网速数据盈利
- PR不是免费的: SQLite作者比喻PR像送小狗
- HTTP QUERY 方法引入
- PACT 匿名令牌协议 (替代 Captcha)
- 工具: Lore(二进制版本管理), DNS Pick, GitFolio, JSOS, AnyDrag

#### 阮一峰 #400: rsync 的争论

rsync v3.4.3 由 Claude 生成引发争议。维护者: AI漏洞大量涌现, 引入AI写代码自己写测试。
- 今天可以放假吗 - AI效率提升讨论
- WWDC防止Siri唤醒 - 扩音设备删除特定频率
- Meta AI客服漏洞 - 诱导修改用户邮箱
- 避蚊胺研究 - 蚊子可适应驱蚊水

#### FE News 2026-06

Naver FE工程师策划的韩国前端月刊:
- TanStack npm供应链攻击(42包84恶意版本)
- Why AI Sucks At Front End
- Deno 向 Node.js 靠拢争议

#### JSer.info #774 (2026-06-22)

- TypeScript 7.0 RC (Go移植)
- Babel 8.0.0 (ESM-only)
- React Router v8

### ⭐ GitHub 热门

- **OpenMontage** - 开源AI视频制作系统 [链接](https://github.com/calesthio/OpenMontage)
- **Penpot** - 开源 Figma 替代 [链接](https://github.com/penpot/penpot)
- **Nginx Proxy Manager** - Web管理Nginx [链接](https://github.com/NginxProxyManager/nginx-proxy-manager)

### 🌐 其他动态

- **HTTP QUERY 方法** [链接](https://kreya.app/blog/new-http-query-method-explained/)
- **PACT 匿名令牌协议** [链接](https://www.cloudflare.com/press/press-releases/2026/cloudflare-collaborates-with-leading-browsers-to-develop-a-privacy-first-protocol-for-the-global-internet/)
- **MDN 前端重构深度解析** [链接](https://developer.mozilla.org/en-US/blog/mdn-front-end-deep-dive/)
- **TanStack npm 供应链攻击** [链接](https://fenews.substack.com/p/fe-news-2026-06)

---

📅 抓取时间: 2026-06-28
📡 数据源: 9/10 成功 (HN Show RSS 502不可用)