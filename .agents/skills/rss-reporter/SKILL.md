---
name: rss-reporter
description: RSS 周报生成器 - 抓取订阅的前端技术 RSS 源，获取文章内容，按主题聚合分类，过滤重复内容，用 AI 分析生成周报摘要。使用场景：(1) 用户要求总结 RSS 订阅内容 (2) 用户说"周报"、"RSS 总结"、"订阅汇总"、"前端新闻" (3) 定期自动生成技术周报。支持命令 /rss-reporter 调用。生成后默认保存到 workspace/output/ 目录，并同步发送到当前对话。
---

# RSS Reporter

抓取用户订阅的前端技术 RSS 源，获取文章内容，按主题聚合分类，用 AI 分析生成周报摘要。

## 支持的 RSS 源

默认订阅以下技术源（存储在 references/feeds.json）：

## 使用方式

### 命令调用

```
/rss_reporter           # 默认抓取最近7天
/rss_reporter --days 3  # 指定天数
```

### 对话触发

当用户说以下内容时自动触发：

- "总结一下 RSS"
- "生成周报"
- "RSS 订阅有什么新内容"
- "前端新闻汇总"
- "最近一周的前端动态"

## 工作流程

**重要：必须抓取所有配置的 RSS 源后才能生成报告，不能遗漏。**

### 1. 获取 RSS 内容

### 2. 必须抓取的源列表

每次执行必须抓取所有源, `references/feeds.json` 中配置的源

### 3. 获取文章详情（重要！）

**周刊类源必须点击进入最新文章获取正文内容：**

- **FE News**: 点击最新的月刊链接，获取正文内容并分析

获取正文后，用 AI 分析并总结：

- 核心技术动态
- 重要发布/更新
- 有趣的工具/项目
- 行业趋势

**注意：周刊类内容必须生成内容摘要，不能只列出标题和链接！**

**重要：对于周刊类内容中的"代码与工具"部分，不能只列出工具名和链接。必须访问每个工具的 GitHub 页面或文档，获取工具的描述信息，并为每个工具添加简短的中文描述。如果某个工具页面无法访问，则跳过该工具。**

### 4. 主题分类

按以下主题聚合文章：

- **React/前端框架**: react, vue, angular, svelte, nextjs, remix, hooks, component
- **JavaScript/TypeScript**: javascript, typescript, es6, node.js, deno, bun, async
- **CSS/样式**: css, tailwind, sass, animation, grid, flexbox
- **工具/构建**: webpack, vite, esbuild, rollup, babel, cli, bundler
- **性能优化**: performance, lighthouse, web vitals, cache, bundle size
- **测试/质量**: test, jest, vitest, cypress, playwright, lint, eslint
- **AI/机器学习**: ai, llm, gpt, chatgpt, copilot, machine learning
- **安全**: security, vulnerability, attack, xss, csrf
- **GitHub/开源**: github, trending, open source, release, stars
- **Hacker News 热门**: hacker news, show hn, ycombinator
- **其他**: 不属于以上类别的

### 5. 生成周报

输出格式：

```markdown
## 📰 前端技术周报 (YYYY-MM-DD)

### 📝 本周要点

- **标题** - 简要描述
  来源: xxx | [链接](url)

### ⚛️ React/前端框架

- **标题** - [内容摘要]
  来源: xxx | [链接](url)

### 📦 JavaScript/TypeScript

...

### 📚 周刊摘要

#### 阮一峰科技爱好者周刊 #XXX

[本期核心内容总结：]

- **重点 1** - 简要描述 [链接](url)
- **重点 2** - 简要描述 [链接](url)
- **重点 3** - 简要描述 [链接](url)

**工具推荐**：

- **工具名** - 简要描述 [链接](url)
- **工具名** - 简要描述 [链接](url)

#### FE News 月刊

[本期核心内容总结：]

- **重点 1** - 简要描述 [链接](url)

**代码与工具**：

- **工具名** - 简要描述 [链接](url)
- **工具名** - 简要描述 [链接](url)

---

📅 抓取时间: YYYY-MM-DD HH:mm
📡 数据源: X/Y 成功
```

## 配置

RSS 源列表存储在 `references/feeds.json`，格式：

```json
[{ "name": "显示名称", "url": "归档页面URL", "type": "browser" }]
```

可自定义添加或删除订阅源。

## 输出要求

### 1. 保存周报文件

生成周报后保存到 `workspace/output/rss-weekly-YYYY-MM-DD.md`

**文件格式要求：**

- 必须在文件开头添加 Jekyll front matter（YAML 头部）：
  ```yaml
  ---
  layout: default
  title: 前端技术周报 (YYYY-MM-DD)
  date: YYYY-MM-DD
  category: RSS 周报
  ---
  ```
- 然后才是周报内容

**重要：如果文件已存在，必须先删除旧文件再创建新文件，确保覆盖已存在的内容。**

**注意：GitHub Pages 使用 Jekyll 自动渲染 Markdown 为 HTML，因此 index.html 中的链接应指向 .html 文件（如 rss-weekly-YYYY-MM-DD.html），而非 .md 文件。**

### 2. 更新 index.html（重要！）

生成周报后，**必须更新 workspace/output/index.html**，将新生成的周报添加到文章列表中。

更新规则：

- 扫描 `workspace/output/` 目录下所有 `*.md` 文件
- 按文件名（日期）倒序排列
- 生成文章列表 HTML，格式如下：
  ```html
  <li class="post-item">
    <h2><a href="文件名.html">标题</a></h2>
    <p class="date">日期 <span class="category">分类</span></p>
  </li>
  ```
- 分类根据文件名判断：
  - `rss-weekly-*.md` → "RSS 周报"
  - `github-release-*.md` → "GitHub Release"
- 标题从 Markdown 文件的第一行提取（去掉 `# ` 前缀）
- 日期从文件名提取（YYYY-MM-DD 格式）
- 替换 index.html 中的 `<!-- 文章列表将由 skill 自动更新 -->` 注释后的整个列表

**重要：更新 index.html 后，必须保存文件。**

### 3. 发送完整版到对话（重要！）

周报生成后，**必须将完整周报内容直接发送到对话中**，让用户立即看到全部内容。

**禁止行为：**

- ❌ 不要只发送简略版或摘要
- ❌ 不要只说"周报已生成"然后只给文件路径
- ❌ 不要省略任何章节内容

**正确做法：**

- ✅ 将完整 Markdown 内容直接贴在对话回复中
- ✅ 包含所有章节：焦点、框架更新、工具、AI、GitHub、HN、深度阅读、资源推荐等
- ✅ 用户应该能在对话中直接阅读完整周报，无需打开文件

## 注意事项

1. **优先获取最新一期** - 归档页面通常按时间倒序排列，第一个链接是最新
2. **限制文章数量** - 每个源获取最近 1-2 期即可，避免信息过载
3. **过滤广告内容** - 忽略 "sponsor"、"classifieds" 等广告标记

## 特殊源处理

### FE News (Substack)

- 访问 https://fenews.substack.com/archive 获取最新月刊
- **必须点击进入文章获取正文内容并总结**
