---
layout: default
title: 前端技术周报 (2026-11-01)
date: 2026-11-01
category: RSS 周报
---

# 前端技术周报 (2026-11-01)

## 📝 本周要点

- **Cloudflare 收购 Deno** — Deno 宣布将被 Cloudflare 收购，运行一年后停止独立开发，JSR 将迁移至 Cloudflare
  来源: JSer.info | [链接](https://deno.com/blog/cloudflare)

- **TanStack Start 1.0 正式稳定** — 基于 TanStack Router 的全栈框架正式发布，支持 SSR、流式渲染和类型安全的服务器函数
  来源: React Status | [链接](https://tanstack.com/blog/tanstack-start-1-0)

- **TypeScript 7.1 Beta 发布** — 新增程序化 API、内容映射器（Content Mappers）、源阶段导入等特性
  来源: JavaScript Weekly | [链接](https://devblogs.microsoft.com/typescript/announcing-typescript-7-1-beta/)

- **Node.js v26 LTS 正式发布** — 安全更新修复了十个 CVE，包括严重的 Node2Shell Brotli 解码器远程代码执行漏洞
  来源: JavaScript Weekly | [链接](https://nodejs.org/en/blog/release/v26.12.1)

- **Shopify 放弃 React Native 回归原生** — 因编程 AI 代理使双平台开发成本大幅降低，Shopify 将移动端应用重写为 Swift/Kotlin 原生
  来源: FE News | [链接](https://shopify.engineering/back-to-native)

- **Bun 1.4.4 发布** — 新增 `bun fmt` 格式化器，兼容 Prettier 配置，速度极快
  来源: JavaScript Weekly | [链接](https://bun.com/blog/bun-v1.4.4)

- **Panda CSS 2.0 发布** — 仅支持 ESM，需 Node.js 22+，编译器改用 Rust/Oxc 重写
  来源: JSer.info | [链接](https://panda-css.com/blog/panda-css-v2)

- **QUnit 3.0 发布** — 原生 ESM 分发，默认测试超时改为 3 秒
  来源: JSer.info | [链接](https://github.com/qunitjs/qunit/releases/tag/3.0.0)

---

## ⚛️ React/前端框架

- **React 19.3 发布** — `<ViewTransition>` 和 Fragment Refs 稳定化，新增 `browser()` 钩子用于仅在浏览器渲染
  来源: JSer.info | [链接](https://react.dev/blog/2026/09/09/react-19-3)

- **Next.js 16.4 发布** — Cache Components 成为默认，支持 `create-next-app --agent`，Turbopack 优化
  来源: JSer.info | [链接](https://nextjs.org/blog/next-16-4)

- **TanStack Redact** — 更轻量的 React 替代品，可减少 20-70% 客户端包体积，但仅支持同步渲染
  来源: JavaScript Weekly | [链接](https://tanstack.com/blog/introducing-tanstack-redact)

- **TanStack AI 1.0 稳定** — 供应商中立的 AI 工具包，支持 23 个提供商适配器
  来源: React Status | [链接](https://tanstack.com/blog/tanstack-ai-1-0)

- **Preact 11 发布** — 仅支持 `.mjs` ESM 分发，移除 CommonJS/UMD，新增 Hydration 2.0
  来源: JSer.info | [链接](https://preactjs.com/blog/preact-11/)

- **React Native Windows 0.85** — 完成向新架构的迁移
  来源: React Status | [链接](https://react.statuscode.com/link/192231/rss)

- **React Compiler 在 Next.js 16.4 中的基准测试** — Babel vs Rust 实现对比
  来源: React Status | [链接](https://react.statuscode.com/link/192240/rss)

- **Async React and Progressive Server Actions** — 如何在 hydration 前保持服务端操作表单工作
  来源: React Status | [链接](https://react.statuscode.com/link/192239/rss)

---

## 📦 JavaScript/TypeScript

- **TypeScript 7.1 Beta** — 新增程序化 API、内容映射器、源阶段导入、`--target es2026`
  来源: JavaScript Weekly | [链接](https://devblogs.microsoft.com/typescript/announcing-typescript-7-1-beta/)

- **Node.js v26.12.1 安全更新** — 修复十个 CVE，包括 Node2Shell 远程代码执行漏洞
  来源: JavaScript Weekly | [链接](https://nodejs.org/en/blog/release/v26.12.1)

- **Node.js v24.22.1 / v22.23.4** — LTS 版本安全更新
  来源: JavaScript Weekly | [链接](https://nodejs.org/en/blog/release/v24.22.1)

- **pnpm 12.16 发布** — 包管理器更新
  来源: JavaScript Weekly | [链接](https://pnpm.io/blog/releases/12.16.0)

- **Bun 1.4.4** — 新增 `bun fmt` 格式化器，兼容 Prettier 配置
  来源: JavaScript Weekly | [链接](https://bun.com/blog/bun-v1.4.4)

- **Deno 2.9.8** — 维护更新
  来源: JavaScript Weekly | [链接](https://github.com/denoland/deno/releases/tag/v2.9.8)

- **Parser Combinators in TypeScript** — 从零构建解析组合子的分步教程
  来源: JavaScript Weekly | [链接](https://t3.at/blog/parser-combinators/)

- **Structs Proposal 实现** — TC39 共享结构提案的可用实现
  来源: JavaScript Weekly | [链接](https://structs.arv.tools/)

---

## 🎨 CSS/样式

- **Panda CSS 2.0** — 仅 ESM，需 Node.js 22+，编译器改用 Rust/Oxc，新增设计系统分发能力
  来源: JSer.info | [链接](https://panda-css.com/blog/panda-css-v2)

- **Responsive iframes in Chrome 154** — 新 iframe 尺寸调整 API
  来源: JSer.info | [链接](https://developer.chrome.com/blog/responsive-iframes?hl=en)

- **React Aria: Swipeable Sheet** — 使用 CSS Scroll Snap 和 `view-timeline` 实现滑动手势
  来源: JSer.info | [链接](https://react-aria.adobe.com/blog/sheet)

- **CSS Container Queries Polyfill** — CQFill 库实现容器查询兼容
  来源: Frontend Focus | [链接](https://github.com/jsxtools/cqfill)

---

## 🛠 工具/构建

- **Vite+ 1.0 发布** — VoidZero 推出的下一代构建工具，新增 GitLab CI/CD 支持
  来源: JSer.info | [链接](https://voidzero.dev/posts/announcing-vite-plus-1-0)

- **Vinext 1.4** — Vite 驱动的 Next.js 重新实现，性能大幅提升
  来源: React Status | [链接](https://vinext.dev)

- **Biome 2.6** — 新增 Markdown、YAML、SCSS 格式支持
  来源: JavaScript Weekly | [链接](https://biomejs.dev/blog/biome-v2-6/)

- **oxlint 1.89** — Rust 基础 Linter 更新推荐规则
  来源: JavaScript Weekly | [链接](https://github.com/oxc-project/oxc/releases/tag/oxlint_v1.89.0)

- **Verdaccio 7.0** — 自托管 npm registry，新增阶段发布和 2FA
  来源: JavaScript Weekly | [链接](https://github.com/verdaccio/verdaccio/releases/tag/v7.0.0)

- **Partytown v1.0.0** — 第三方脚本 Web Worker 执行库正式版
  来源: JSer.info | [链接](https://github.com/QwikDev/partytown/releases/tag/v1.0.0)

- **Express 5.3.0** — 服务端框架更新
  来源: JSer.info | [链接](https://github.com/expressjs/express/releases/tag/v5.3.0)

---

## ⚡ 性能优化

- **设计系统性能基准测试** — 测试 MUI、Mantine、Ant Design、React Spectrum 在真实场景下的性能表现
  来源: React Status | [链接](https://react.statuscode.com/link/192218/rss)

- **TanStack DB 1.0 RC1** — 响应式客户端数据层，API 稳定
  来源: React Status | [链接](https://tanstack.com/blog/tanstack-db-1-0-rc1)

- **Dead Code Shouldn't Exist** — Sentry 使用 Knip 删除 28,000 行死代码的经验分享
  来源: JavaScript Weekly | [链接](https://tkdodo.eu/blog/dead-code-shouldnt-exist)

- **React.lazy 和 Suspense 的 300ms 启动延迟** — 潜在性能问题排查与修复
  来源: React Status | [链接](https://react.statuscode.com/link/192234/rss)

---

## 🧪 测试/质量

- **QUnit 3.0 发布** — 原生 ESM，默认测试超时改为 3 秒
  来源: JSer.info | [链接](https://github.com/qunitjs/qunit/releases/tag/3.0.0)

- **Mutative 2.0** — Immer 风格不可变更新库，性能提升 3.6 倍
  来源: JavaScript Weekly | [链接](https://mutative.js.org/blog/releases/2.0/)

---

## 🤖 AI/机器学习

- **Claude Code 安全后门事件** — VS Code 扩展在 Cursor Marketplace 发现后门
  来源: Hacker News Front | [链接](https://phorion.io)

- **Shopify 使用 AI 代理重写移动端** — 利用 AI 代理将 React Native 迁移至原生，12 周完成 Shop app
  来源: FE News | [链接](https://shopify.engineering/back-to-native)

- **Linear 的 AI 编码 CI 瓶颈优化** — 代码生成加速后 CI 成为瓶颈，通过多项优化缩短 50% 时间
  来源: FE News | [链接](https://linear.app/now/ci-bottleneck-reworked)

- **Brownfield Agentic Engineering** — Addy Osmani 分享在遗留代码库中使用 AI 代理的原则
  来源: FE News | [链接](https://addyo.substack.com/p/brownfield-agentic-engineering)

- **TanStack AI 1.0** — 供应商中立的 AI 工具包，支持 chat/tools/media API
  来源: JavaScript Weekly | [链接](https://tanstack.com/blog/tanstack-ai-1-0)

---

## 📰 周刊摘要

### 阮一峰科技爱好者周刊 #416

**封面主题：编程已经面目全非**

阮一峰本周讨论了 AI 如何从根本上改变编程工作：

- **代码审查将消失** — AI 生成代码速度远超人工审查能力
- **Bug 性质改变** — 多数 Bug 变为需求表达问题而非代码问题
- **项目分工改变** — PM/设计师/工程师三元架构将消失
- **"好代码"概念消失** — 当不直接阅读代码时，代码风格规范意义不再
- **Token 为王** — 谁能负担更多 Token，谁就能开发出更好的软件

其他亮点：
- 印度证书颁发机构 eMudhra 私钥被破解，仅用 1 毫秒
- 陶哲轩公开反对大模型用于数学证明
- Simon Willison 总结 2026 年大模型发展：OpenClaw、Tokenmaxxing、Claude Fable 5 / Mythos

**工具推荐**：
- `sslx` — HTTPS 证书信息命令行工具
- `Mac.apk` — 让 Mac 运行安卓软件
- `siltop` — macOS 终端系统信息展示
- `silkpulse` — 前端远程页面调试工具

[完整文章](https://www.ruanyifeng.com/blog/2026/10/weekly-issue-416.html)

### 阮一峰科技爱好者周刊 #415

**封面主题：3D 版《看不见的城市》**

本周展示了 AI 3D 建模能力的突破：

- Claude Opus 5.5 成功将《看不见的城市》55 个城市可视化
- GPT-6 Astra 生成的版本与原著意境相去甚远
- 展示了 AI 在 3D 场景生成方面的进步与局限

其他亮点：
- **Deno 项目结束** — 被 Cloudflare 收购，创始人 Ryan Dahl 承认失败
- **灯泡计算机概念** — 未来电脑可能是一个投影设备
- **AI 逆向工程** — REA 项目使用 AI 从二进制文件重新实现软件

**工具推荐**：
- `REA` — AI 逆向工程项目
- `SynthID 检测器` — 谷歌 AI 内容识别工具
- `ts-rust` — Rust 实现的 TypeScript 编译器
- `Doory` — 开源平面设计工具

[完整文章](https://www.ruanyifeng.com/blog/2026/10/weekly-issue-415.html)

### FE News 2026-10 月刊

**本期核心内容**：

1. **VS Code 纪录片** — 官方发布的 98 分钟纪录片，讲述 VS Code 从 2015 年至今的发展史
   [链接](https://www.youtube.com/watch?v=kHL3XzjpT5w)

2. **Shopify 回归原生** — 因 AI 代理降低双平台开发成本，决定将移动端重写为 Swift/Kotlin
   [链接](https://shopify.engineering/back-to-native)

3. **Vercel design.md** — Vercel 如何让 AI 代理在代码库外也能生成符合品牌规范的页面
   [链接](https://vercel.com/blog/how-our-agents-build-on-brand-pages-with-design-md)

4. **Linear CI 优化** — AI 编码加速后，CI 成为瓶颈，通过多项优化缩短 50% 时间
   [链接](https://linear.app/now/ci-bottleneck-reworked)

5. **Brownfield Agentic Engineering** — Addy Osmani 分享遗留代码库中使用 AI 代理的原则
   [链接](https://addyo.substack.com/p/brownfield-agentic-engineering)

6. **Ramp CPO 访谈** — 编码问题解决后，产品团队的瓶颈转移到了前后阶段
   [链接](https://youtu.be/ZG8Mf3P9xzI)

7. **Claude Code effort 设置分析** — 不同 effort 级别对结果质量的实际影响
   [链接](https://claude.dev/blog/spending-your-effort/)

8. **Bend 语言** — 支持依赖类型的编程语言，可验证 AI 生成代码的正确性
   [链接](https://bend-lang.com/)

9. **Penpot 2.18.1** — 开源设计平台新增 MCP 服务器支持 AI 集成
   [链接](https://github.com/penpot/penpot)

10. **Agentlas-OS** — 多代理编排引擎，支持任务分解与独立验证
    [链接](https://github.com/agentlas-ai/Agentlas-OS/)

### JSer.info #781

**本期重点**：
- Cloudflare 收购 Deno
- TanStack Start 1.0 发布
- Bun 1.4.3 发布
- Panda CSS 2.0 发布

**其他动态**：
- Preact 11 发布
- Next.js 16.4 发布
- Node.js v26.11.0
- QUnit 3.0 发布
- Express 5.3.0 发布
- Partytown v1.0.0 发布

[完整内容](https://jser.info/2026/10/16/cloudflaredeno-tanstack-start-1.0-bun-1.4.3-panda-css-2.0/)

---

## 🔥 Hacker News 热门

- **Claude Code 安全后门** — VS Code 扩展在 Cursor Marketplace 被发现植入后门 (954 points)
- **Azure 跨租户漏洞** — 五个完整的跨租户入侵案例 (327 points)
- **Northflank 遭入侵** (465 points)
- **Sleep 框架** — Google 研究如何让 LLM 在持续学习中保留知识 (245 points)
- **Astroterm** — 终端星图项目 (235 points)

---

## 🐙 GitHub 热门

- **cloudflare/security-audit-skill** — 多阶段安全审计编码代理技能
- **AgriciDaniel/claude-seo** — Claude Code SEO 插件，26 个子技能
- **pingdotgg/t3code** — TypeScript 全栈框架
- **openclaw/openclaw** — 通用 AI 代理
- ** JetBrains/thinkrail** — AI 辅助 IDE
- **milind-soni/OpenMausBot** — Grok Bot 开源替代
- **Dokploy/dokploy** — 开源 Vercel/Netlify 替代品

---

## 📌 其他动态

- **CSS-Tricks 易主** — 正式成为独立媒体，由长期编辑 Geoff Graham 收购
- **Arc 浏览器停更** — The Browser Company 转向 Dia 浏览器
- **Google Docs 支持 Markdown** — 原生支持打开、编辑和协作 Markdown 文件
- **CoffeeScript 2.7.1** — 四年后的首次更新
- **React Window 2.5** — 虚拟列表库新增 scrollElement 属性
- **Puck 0.24** — React 可视化页面编辑器更新
- **React Hook Form 7.91** — useFieldArray 和异步验证修复

---

📅 抓取时间: 2026-11-01 09:00
📡 数据源: 10/10 成功
