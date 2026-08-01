---
layout: default
title: 前端技术周报 (2026-08-02)
date: 2026-08-02
category: RSS 周报
---

## 📰 前端技术周报 (2026-08-02)

### 📝 本周要点

1. **TypeScript 7.0 正式发布** - Go 移植版 tsc 带来 10x 速度提升，--checkers/--builders 并行控制、全新 --watch、LSP 支持。但编译器 API 暂未公开，Vue 等工具暂时无法使用。
   来源: JavaScript Weekly #796 | [链接](https://javascriptweekly.com/issues/796)

2. **Octane: 编译型 React 替代框架** - Inferno 作者 Dominic Gannaway 推出的编译型框架，无需 VDOM，支持 TSX/JSX。已有人创建 Nextane 实验项目。
   来源: React Status #485 | [链接](https://octanejs.dev/)

3. **npm 12 发布，安全大升级** - allowScripts 默认禁用，--allow-git/--allow-remote 默认 none。2FA 绕过令牌即将淘汰。
   来源: JSer.info #776 | [链接](https://github.com/npm/cli/releases/tag/v12.0.0)

4. **ECMAScript 2026 正式获批** - 新增 Array.fromAsync、Uint8Array.toBase64/fromBase64、Iterator.concat()、Math.sumPrecise()、Error.isError()、Map.getOrInsert() 等。
   来源: JSer.info #775 | [链接](https://github.com/tc39/ecma262/releases/tag/es2026)

5. **Vite 8.1 发布** - 实验性 --experimental-bundle 支持开发时也打包分发、Chunk Import Map 解决哈希链式变更、Wasm ESM 集成。
   来源: JSer.info #775 | [链接](https://vite.dev/blog/announcing-vite8-1)

6. **React 19.2.8/19.1.9/19.0.8 安全修复** - 修复 Server Function 端点 DoS 漏洞。
   来源: JavaScript Weekly #796 | [链接](https://javascriptweekly.com/link/188530/rss)

7. **TanStack 停止使用 RSC，全面改版** - 升级后仅 27KB 的 markdown + 高亮栈，纯 SSR 更小更快。同时发布 TanStack Markdown、Highlight、Charts 新库。
   来源: React Status #485 | [链接](https://tanstack.com/blog/we-stopped-using-rsc-on-tanstack-com)

8. **MDN 推出 MCP 服务器** - 将 MDN 文档和浏览器兼容性数据直接接入 AI 编辑器和 IDE，支持 VS Code、Zed、Cursor、Claude Code 等。
   来源: MDN Blog | [链接](https://developer.mozilla.org/en-US/blog/introducing-mdn-mcp-server/)

---

### ⚛️ React/前端框架

- **Octane: React 编程模型，但编译** - Inferno 作者推出的编译型框架，无 VDOM，提前生成响应式代码。有人创建了 Nextane（基于 Vinext）实验项目。
  来源: React Status #485 | [链接](https://octanejs.dev/)

- **TanStack 停止使用 RSC** - Tanner Linsley 用数据证明，纯 SSR 比 RSC 更小更快，代码更易维护。同时发布全品牌改版和新的 landing page。
  来源: React Status #485 | [链接](https://tanstack.com/blog/we-stopped-using-rsc-on-tanstack-com)

- **React 19.2.8/19.1.9/19.0.8 安全更新** - 修复 Server Function 端点的 DoS 漏洞。
  来源: JavaScript Weekly #796 | [链接](https://javascriptweekly.com/link/188530/rss)

- **React Router 8.3 发布** - 持续迭代。
  来源: JavaScript Weekly #796

- **Nuxt 4.5.1 和 3.21.10** - 上周 Nuxt 4.5 大版本后的安全补丁。Nuxt 3 将在 7月31日结束生命周期。
  来源: JavaScript Weekly #796 / #795 | [链接](https://nuxt.com/)

- **Vue 3.6 RC2** - Vapor Mode 功能已完整，即将正式发布。
  来源: JavaScript Weekly #795 | [链接](https://javascriptweekly.com/link/188487/rss)

- **Preact 11.0 Beta 2** - 维护者称这是 Preact 11 的最后一个 Beta 之一。
  来源: JavaScript Weekly #795

- **Ember 7.1** - 新增多种 Helper 和操作符，文档现代化。
  来源: JavaScript Weekly #796

- **MobX 7.0** - 瘦身，移除废弃 API，始终使用 Proxy 支持的可观察对象和数组。
  来源: React Status #485 | [链接](https://github.com/mobxjs/mobx/releases/tag/mobx%407.0.0)

- **Mantine 9.5** - 日期选择器新增原生年月选择，新增 SunburstChart 组件。
  来源: React Status #485 | [链接](https://mantine.dev/changelog/9-5-0)

---

### 📦 JavaScript/TypeScript

- **TypeScript 7.0 正式发布** - Go 移植版 tsc 作为 npm 的 typescript 包发布。--checkers/--builders/--singleThreaded 并行控制，--watch 基于 Parcel 重写，LSP 支持。但程序 API 尚未公开。
  来源: JSer.info #776 | [链接](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/)

- **Anders Hejlsberg 演示 TypeScript 7 的 10x 加速** - 在 VS Code 130 万行代码库上演示。同时介绍了新 LSP 语言服务器，以及为何编译器 API 用户（Vue、Astro、Svelte）需继续使用 TypeScript 6。
  来源: JavaScript Weekly #796 | [链接](https://javascriptweekly.com/link/188488/rss)

- **ECMAScript 2026 正式发布** - 新增 Array.fromAsync、Uint8Array.toBase64/fromBase64、Iterator.concat()、Math.sumPrecise()、Error.isError()、Map.getOrInsert() 等。
  来源: JSer.info #775 | [链接](https://github.com/tc39/ecma262/releases/tag/es2026)

- **Await Dictionary (Promise.allKeyed) 进入 Stage 3** - TC39 会议最新进展。
  来源: JavaScript Weekly #796 | [链接](https://javascriptweekly.com/link/188472/rss)

- **import defer — 延迟模块求值** - 进入 Stage 3 提案。
  来源: JavaScript Weekly #796 | [链接](https://javascriptweekly.com/link/188495/rss)

- **Deno 2.9.4 发布** - 持续迭代。
  来源: JavaScript Weekly #796

- **Deno compile 将支持 QuickJS 替代 V8** - Ryan Dahl 表示可生成更小的二进制文件。
  来源: JavaScript Weekly #796 | [链接](https://javascriptweekly.com/link/188473/rss)

- **Babel 8.0.0 发布** - ESM only，Node.js 24+ 必需，@babel/preset-env 默认不再编译到 ES5。
  来源: JSer.info #774 | [链接](https://babeljs.io/blog/2026/06/16/8.0.0/)

- **Flow 已从 OCaml 移植到 Rust** - 使用 AI 逐行移植，无代码冻结的迁移过程。
  来源: JSer.info #775 | [链接](https://medium.com/flow-type/flows-ocaml-to-rust-port-78b95bcf49e9)

- **Node.js 26.5.0 发布** - 新增 Blob.prototype.textStream()、--experimental-import-text、ReadableStreamTee 等。
  来源: JSer.info #776 | [链接](https://nodejs.org/en/blog/release/v26.5.0)

- **Node.js 新 API 文档站点预览** - 新增搜索功能。
  来源: JavaScript Weekly #796 | [链接](https://javascriptweekly.com/link/188474/rss)

- **Oxlint 类型感知 Lint 功能稳定** - 基于 Rust 的快速 Lint 工具。
  来源: JavaScript Weekly #796 | [链接](https://javascriptweekly.com/link/188475/rss)

- **Prisma 7.9 发布** - 持续迭代。
  来源: JavaScript Weekly #796

---

### 🎨 CSS/样式

- **Chrome 150 发布** - 支持 CSS AccentColor/AccentColorText、polygon() 圆角、text-fit、cross-origin()/integrity()/referrer-policy() 修饰符。DOM 新增 focusgroup 属性、popover=hint 行为变更。
  来源: JSer.info #776 | [链接](https://developer.chrome.com/release-notes/150)

- **Frontend Focus #752: conic-gradient() 的多功能用法** - 本期还涵盖 CSS Subgrid 重建世界杯表格等。
  来源: Frontend Focus | [链接](https://frontendfoc.us/issues/752)

- **Frontend Focus #751: 用 CSS Subgrid 重建世界杯表** - 深入探讨 Subgrid 的实际应用场景。
  来源: Frontend Focus | [链接](https://frontendfoc.us/issues/751)

- **CSS 中测量组件性能的 Container Timing API** - 现已在 Chrome 中开启 Origin Trial。
  来源: JavaScript Weekly #796 | [链接](https://javascriptweekly.com/link/188496/rss)

- **Prettier 3.9 发布** - Markdown 解析器更新为 micromark v4，YAML 解析器更新为 yaml v2，支持 GraphQL.js v17 语法，移除 import...assert 支持。
  来源: JSer.info #775 | [链接](https://prettier.io/blog/2026/06/27/3.9.0)

---

### 🛠 工具/构建

- **Vite 8.1 发布** - 实验性 --experimental-bundle 使开发时也打包分发。Chunk Import Map 解决哈希链式变更问题。Wasm ESM 集成、import.meta.glob 的 caseSensitive 选项。
  来源: JSer.info #775 | [链接](https://vite.dev/blog/announcing-vite8-1)

- **Rspack 2.1 发布** - builtin:swc-loader 支持 React Compiler，import.meta.glob 支持，TypeScript 7 类型检查支持，CircularCheckRspackPlugin，持久缓存自动清理，production mode 默认启用纯函数优化。
  来源: JSer.info #775 | [链接](https://rspack.rs/blog/announcing-2-1)

- **pnpm 11.10 发布** - 新增 pnpm issues/prefix 命令，支持 pnpm_config__auth 环境变量，pnpm self-update 的 v12 兼容。
  来源: JSer.info #776 | [链接](https://github.com/pnpm/pnpm/releases/tag/v11.10.0)

- **ESLint 10.8 发布** - 持续迭代。
  来源: JavaScript Weekly #796

- **ESLint 官方 Codemods 发布** - 自动化 ESLint 版本迁移（v8→v9、v9→v10）。
  来源: JavaScript Weekly #795

- **eslint-package-json** - Sindre Sorhus 出品，捕捉 package.json 中的各种错误。
  来源: JavaScript Weekly #796 | [链接](https://javascriptweekly.com/link/188507/rss)

- **Bruno 4.0** - 开源 HTTP API 客户端，Postman 的 JavaScript 轻量替代品。
  来源: JavaScript Weekly #796 | [链接](https://javascriptweekly.com/link/188504/rss)

- **tslog 5** - 零依赖日志库，重写后 ESM only，支持 Worker、React Native，Pretty 输出，JSON 可选，Middleware 支持。
  来源: JavaScript Weekly #796 | [链接](https://javascriptweekly.com/link/188505/rss)

- **MapLibre GL JS 6.0** - WebGL 驱动的交互式矢量地图库，ESM only，需 WebGL 2，性能大幅提升。
  来源: JavaScript Weekly #796 | [链接](https://maplibre.org/)

- **Satori 0.29** - 将 HTML 和 CSS（JSX 语法）转换为 SVG 的库。
  来源: JavaScript Weekly #796

- **httpxy (unjs)** - Node.js 全功能 HTTP/WebSocket 代理库，Fetch API 兼容。
  来源: JSer.info #776 | [链接](https://github.com/unjs/httpxy)

---

### ⚡ 性能优化

- **TanStack 网站移除 RSC 后性能提升** - 纯 SSR 页面更小，阻塞时间更低，代码更易维护。
  来源: React Status #485 | [链接](https://tanstack.com/blog/we-stopped-using-rsc-on-tanstack-com)

- **Container Timing API 衡量组件性能** - Chrome Origin Trial 中的新 API，用于测量前端组件性能。
  来源: JavaScript Weekly #796 | [链接](https://javascriptweekly.com/link/188496/rss)

- **Cloudflare Workers Cache 发布** - Worker 前段可配置缓存，支持 Cache-Control/Vary，ctx.cache.purge() 按标签或路径删除。
  来源: JSer.info #776 | [链接](https://blog.cloudflare.com/workers-cache/)

---

### 🧪 测试/质量

- **Shadscan: shadcn 应用的确定性 UI 审计** - 约 60 个确定性检查（无需 AI 或 API 密钥），覆盖可访问性、状态、组合最佳实践。
  来源: JavaScript Weekly #796 | [链接](https://www.shadscan.com/)

- **Oxlint 类型感知 Lint 功能稳定** - 快速、类型感知的 Lint 工具。
  来源: JavaScript Weekly #796

- **rev-dep: JS/TS 依赖分析工具** - 检查依赖循环引用和死代码，CLI 快速。
  来源: JSer.info #775 | [链接](https://github.com/jayu/rev-dep)

---

### 🤖 AI/机器学习

- **MDN 推出 MCP 服务器** - 将 MDN 文档和浏览器兼容性数据接入 AI 编辑器，支持 Claude Code、VS Code、Cursor、Zed 等工具。测试显示带 MCP 的回答准确率大幅提升。
  来源: MDN Blog | [链接](https://developer.mozilla.org/en-US/blog/introducing-mdn-mcp-server/)

- **Safari MCP 服务器发布** - Safari Technology Preview 247 新增，AI Agent 可操控 Safari 标签页，访问 DOM、网络、控制台、截图。
  来源: JSer.info #775 | [链接](https://webkit.org/blog/18136/introducing-the-safari-mcp-server-for-web-developers/)

- **Better Auth 加入 Vercel** - Vercel 收购 TypeScript 认证库 Better Auth，保持 MIT 许可，将继续开发 Agent Auth Protocol。
  来源: JSer.info #776 | [链接](https://better-auth.com/blog/better-auth-joins-vercel)

- **Vite+ Beta 发布** - VoidZero 推出，改进 vp run 缓存、vp migrate 覆盖范围，支持代理和自定义 CA。
  来源: JSer.info #775 | [链接](https://voidzero.dev/posts/announcing-vite-plus-beta)

- **Blume: Markdown 优先的文档生成工具** - 基于 Astro + Vite，支持搜索、OpenAPI 生成 API 参考、MCP 服务、Ask AI。
  来源: JSer.info #776 | [链接](https://useblume.dev/)

- **Facebook Astryx 开源设计系统** - 基于 React + StyleX，完全可定制，Agent Ready。
  来源: JSer.info #775 | [链接](https://github.com/facebook/astryx)

---

### 📚 周刊摘要

#### 阮一峰科技爱好者周刊 #406 — 道可，道非，常道

**核心话题**：华为任正非引用老子《道德经》"道可，道非，常道"，为华为半导体突围之路定性——走对走错都是路，不走只有等死。

**科技动态**：
- **长征三号乙火箭遭雷击** - 7月23日发射后47秒被闪电击中，因法拉第笼设计未受影响，卫星顺利入轨
- **特斯拉童车** - 官网推出225美元儿童平衡车，无踏板设计独特
- **树的生长实验** - 意大利艺术家将青铜手模型握在树上，14年后手已陷入树干

**工具推荐**：Orion 浏览器、Chirp 声音传输工具、Bento Slides PPT 编辑器、FluxDown 多协议下载器、StaticShield 网页密码保护、Figwright（Figma MCP 服务器）

来源: 阮一峰博客 #406 | [链接](https://www.ruanyifeng.com/blog/2026/07/weekly-issue-406.html)

#### JSer.info #776 — TypeScript 7.0、npm 12、Next.js 安全策略

**TypeScript 7.0 发布**：Go 移植版 tsc，--checkers/--builders/--singleThreaded 并行控制，--watch 重写，LSP 支持。但程序 API 尚未公开。
**npm 12 发布**：allowScripts 默认禁用，--allow-git/--allow-remote 默认 none。2FA 绕过令牌 2026年8月起失效。
**Next.js 安全策略**：每月一次预公告安全发布，紧急漏洞随时修复。

来源: JSer.info #776 | [链接](https://jser.info/2026/07/17/typescript-7.0-npm-12-next.js/)

#### JavaScript Weekly #796 — Rust 正在吞噬 JavaScript（2026 版）

**头条**：Lee Robinson 更新热门文章，Rspack、Biome、Turbopack、Bun 持续印证 Rust 趋势。Anders Hejlsberg 演示 TS7 10x 加速。Octane 编译型框架发布。

**代码与工具**：MapLibre GL JS 6.0、Bruno 4.0、tslog 5、eslint-package-json、Shadscan、isomorphic-git 1.40

来源: JavaScript Weekly #796 | [链接](https://javascriptweekly.com/issues/796)

---

### 🔥 Hacker News 热门

1. **TurboFieldfare: 2GB RAM Mac 上运行 Gemma 4 26B** - 流式路由专家到 SSD，M2 MBA 上 5-6 tok/s。904 points
2. **HNewhere: HN 链接评论同屏显示** - 用户脚本，点击链接同时显示文章和评论。430 points
3. **CheapFoodMap: 10 美元以下美食地图** - 众包 15 城市 1200+ 餐厅。283 points
4. **Distilling DeepSeek 不传递审查** - 蒸馏 DeepSeek 到 GPT-OSS，审查特性未传递。165 points
5. **Kedge: 全栈云平台** - 3ms 创建 VM，CRDT 复制 SQLite。135 points
6. **Gander: Android 零权限文件查看器** - 无 INTERNET 权限，本地渲染。202 points
7. **MarbleOS: AI Agent GUI 接口** - 像桌面 GUI 一样操作 AI 代理。130 points

---

### 🌟 GitHub 热门

| 项目 | 本周 Stars | 描述 |
|------|-----------|------|
| block/buzz | +10,558 | 蜂群思维通信平台 (Rust) |
| diegosouzapw/OmniRoute | +7,701 | 免费 AI 网关，290+ 提供商 |
| permissionlesstech/bitchat | +6,761 | 蓝牙 Mesh 聊天 |
| citrolabs/ego-lite | +4,741 | AI Agent 浏览器自动化 |
| alibaba/open-code-review | +4,746 | 阿里巴巴代码审查工具 (Go) |
| ayghri/i-have-adhd | +5,133 | ADHD 友好 Agent 输出 |
| virgiliojr94/book-to-skill | +4,603 | 技术书 PDF 转 Claude Skill |
| 1jehuang/jcode | +3,351 | 最高 RAM 效率的工具 |
| pascalorg/editor | +2,863 | 3D 建筑设计编辑器 |
| CoreBunch/Instatic | +2,866 | Webflow/Framer 开源替代 |
| different-ai/openwork | +2,213 | Claude Cowork 开源替代 |
| earthtojake/text-to-cad | +1,901 | CAD/CAE/CAM Agent 技能库 |

---

### 📡 其他动态

- **Electron 43 发布** - Chromium 150、Node.js v24.17.0、V8 15.0
- **Wordgard 0.1** - ProseMirror/CodeMirror 作者开发的富文本编辑器库
- **Basecoat 1.0** - Tailwind CSS 实现的 shadcn/ui 兼容组件库
- **js1024 代码高尔夫竞赛** - 已截稿，获胜者下周公布
- **OpenJS Foundation 贡献者排名** - Node、Express、Electron 年度 Top 贡献者
- **Medium 构建新目录功能** - 从第三方 Chrome 扩展获得灵感

---

📅 抓取时间: 2026-08-02 16:00
📡 数据源: 8/10 成功（React Status ✓、JavaScript Weekly ✓、JSer.info ✓、Hacker News ✓、GitHub Trending ✓、阮一峰 ✓、Frontend Focus ✓、MDN ✓；Frontender Medium ❌、FE News Substack ❌）