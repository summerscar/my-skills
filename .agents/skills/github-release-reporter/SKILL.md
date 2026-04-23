---
name: github-release-reporter
description: 追踪 GitHub 项目 Release 更新，自动总结新增功能和修复的 Bug，支持多项目订阅和变更检测；用户说 "生成github release周报" 时触发手动总结模式
user-invocable: true
tools:
  - browser
  - read
  - write
  - exec
---

# 🚀 GitHub Release 追踪器

追踪 GitHub 项目的 Release 更新，自动对比版本变化，提取新增功能和 Bug 修复，生成清晰的变更报告。

## 适用场景

- 每日定时检查订阅项目的 Release 更新（推荐 cron job 每天执行）
- 用户询问某个项目的更新情况
- "xxx 项目有什么新功能"
- "xxx 最新版本更新了什么"
- **用户说 "生成github release周报" 时触发手动总结模式**
- **手动执行时自动总结所有订阅项目的最新 Release 内容**

## 执行模式

1. **定时检查模式**：只检查 24 小时内的新 Release，无更新则静默返回
2. **手动总结模式**：用户主动执行时，总结所有订阅项目的最新 Release 内容（无论发布时间）

## 核心逻辑

**每日检查模式：**

- 只检查最近 24 小时内发布的 Release
- 无新 release 则静默返回（不生成报告）
- 有新 release 则生成变更报告并发送通知

## 数据存储

**状态文件位置：** `./reference/`

```
./reference/
├── projects.json          # 订阅的项目列表
├── releases/              # 各项目的 release 缓存
│   ├── owner_repo.json    # 项目 release 历史
│   └── ...
```

**projects.json 结构：**

```json
{
  "projects": [
    {
      "owner": "openclaw",
      "repo": "openclaw",
      "alias": "OpenClaw",
      "lastChecked": "2026-03-18T00:00:00Z",
      "lastRelease": "v2026.3.8"
    }
  ]
}
```

## 工作流程

### Step 1: 解析请求

识别用户意图：

| 用户输入                 | 操作                                             |
| ------------------------ | ------------------------------------------------ |
| "追踪 xxx/xxx 项目"      | 添加订阅                                         |
| "检查所有项目更新"       | 批量检查（24小时内）                             |
| "xxx 项目有什么更新"     | 检查单个项目                                     |
| "列出订阅的项目"         | 显示项目列表                                     |
| "取消追踪 xxx"           | 移除订阅                                         |
| "执行一下" / "运行一下"  | **手动总结模式**：总结所有订阅项目的最新 Release |
| "生成github release周报" | **手动总结模式**：总结所有订阅项目的最新 Release |

**手动总结模式执行流程：**

1. 读取 projects.json 获取所有订阅项目
2. 获取每个项目的最新 Release 信息（使用 API 或浏览器）
3. 更新 lastChecked 时间戳
4. 为每个项目生成内容总结报告，包含：
   - 版本号和发布时间
   - 主要新增功能（Features / Added）
   - 主要 Bug 修复（Fixes）
   - 破坏性变更（Breaking Changes）
   - 其他重要更新
5. 输出格式清晰的总结报告

### Step 2: 获取 Release 信息

**使用 GitHub API（推荐）：**

```bash
# 获取最新 release
curl -s "https://api.github.com/repos/{owner}/{repo}/releases/latest"

# 获取所有 releases（分页）
curl -s "https://api.github.com/repos/{owner}/{repo}/releases?per_page=10"
```

**或使用浏览器访问：**

```
https://github.com/{owner}/{repo}/releases
```

### Step 3: 解析 Release Notes

**提取信息的正则模式：**

```regex
# 版本号
v?(\d+\.\d+\.\d+(-[a-zA-Z0-9]+)?)

# Features (多种格式)
(Features?|New|新增)[：:\s]*\n([\s\S]*?)(?=\n##|\n###|\Z)
[-*]\s*(.*feature.*|.*新功能.*)

# Bug Fixes
(Bug\s*Fixes?|Fixes?|修复|Fixed)[：:\s]*\n([\s\S]*?)(?=\n##|\n###|\Z)
[-*]\s*(.*fix.*|.*修复.*|.*bug.*)

# Breaking Changes
(Breaking\s*Changes?|破坏性变更)[：:\s]*\n([\s\S]*?)(?=\n##|\n###|\Z)
```

**解析要点：**

1. 提取版本号、发布日期、发布说明
2. 按类别分类：Features、Bug Fixes、Breaking Changes、其他
3. 提取 PR 编号和贡献者（如有）

### Step 4: 检查 24 小时内的更新

**每日检查逻辑：**

1. 获取项目最新 release
2. 检查 `publishedAt` 是否在最近 24 小时内
3. 只处理 24 小时内发布的 release
4. 无新 release 则跳过，不生成报告

**时间判断示例：**

```javascript
const now = new Date();
const publishedAt = new Date(release.publishedAt);
const hoursDiff = (now - publishedAt) / (1000 * 60 * 60);

if (hoursDiff <= 24) {
  // 这是今天发布的新版本，需要处理
}
```

**多版本处理：**
如果 24 小时内有多个 release 发布，合并所有变更到一份报告中。

### Step 5: 生成报告（仅在有更新时）

**报告模板：**

```markdown
# 🚀 GitHub Release 更新 ({date})

> 共 {count} 个项目有更新

---

## {项目名} - {版本号}

⏰ 发布时间：{publishedAt}

### ✨ 新增功能

1. 新增 xxx 功能
2. 支持 yyy 平台

### 🐛 Bug 修复

1. 修复 zzz 问题

### ⚠️ 破坏性变更

- API 变更：`oldMethod()` 已移除

🔗 [Release Notes]({url})

---
```

**无更新时：**
不生成报告，直接返回："今日无 Release 更新"

### Step 6: 更新缓存

将最新的 release 信息写入缓存文件：

```json
// ./reference/releases/owner_repo.json
{
  "owner": "openclaw",
  "repo": "openclaw",
  "releases": [
    {
      "tag": "v2026.3.8",
      "name": "OpenClaw 2026.3.8",
      "publishedAt": "2026-03-15T10:00:00Z",
      "htmlUrl": "https://github.com/openclaw/openclaw/releases/tag/v2026.3.8",
      "body": "...",
      "parsed": {
        "features": ["..."],
        "fixes": ["..."],
        "breaking": ["..."]
      }
    }
  ],
  "lastUpdated": "2026-03-18T00:00:00Z"
}
```

### Step 7: 输出文件

生成周报后保存到 `workspace/output/github-release-YYYY-MM-DD.md`

**重要：如果文件已存在，必须先删除旧文件再创建新文件，确保覆盖已存在的内容。**

**注意：GitHub Pages 使用 Jekyll 自动渲染 Markdown 为 HTML，因此 index.html 中的链接应指向 .html 文件（如 github-release-YYYY-MM-DD.html），而非 .md 文件。**

### Step 8: 更新 index.html（重要！）

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

## 命令示例

### 添加订阅

```
用户：帮我追踪 openclaw/openclaw 项目的 release
```

执行步骤：

1. 调用 GitHub API 获取项目信息和最新 release
2. 添加到 projects.json
3. 缓存当前 release 信息
4. 返回确认信息

### 检查更新

```
用户：检查所有项目的更新
用户：openclaw 有什么新版本
```

执行步骤：

1. 读取 projects.json
2. 对每个项目调用 GitHub API
3. 对比缓存的 release 信息
4. 生成变更报告（仅在有更新时）

### 列出订阅

```
用户：我订阅了哪些项目
```

输出：

```
📋 已订阅的 GitHub 项目：

| # | 项目 | 别名 | 最新版本 | 最后检查 |
|---|------|------|----------|----------|
| 1 | openclaw/openclaw | OpenClaw | v2026.3.8 | 2026-03-18 |
| 2 | vercel/next.js | Next.js | v14.1.0 | 2026-03-17 |
```

## 定时检查（Cron Job 配置）

```json
{
  "name": "GitHub Release reporter",
  "schedule": { "kind": "cron", "expr": "0 9 * * *" },
  "sessionTarget": "isolated",
  "payload": {
    "kind": "agentTurn",
    "message": "使用 github_release_reporter skill 检查所有订阅项目最近 24 小时内的 Release 更新，如有更新则生成报告并发送通知。"
  },
  "delivery": {
    "mode": "announce",
    "channel": "telegram",
    "to": "your_chat_id"
  }
}
```

**每日检查流程：**

1. 遍历 projects.json 中的所有项目
2. 调用 GitHub API 获取最新 release
3. 检查 `publishedAt` 是否在 24 小时内
4. 只为 24 小时内发布的 release 生成报告
5. 无更新则静默结束，不发送通知

## 错误处理

| 错误类型         | 处理方式                         |
| ---------------- | -------------------------------- |
| 项目不存在       | 提示用户检查 owner/repo 是否正确 |
| API 限流         | 使用浏览器访问作为备选方案       |
| 网络超时         | 重试 3 次，间隔 5 秒             |
| Release 解析失败 | 保留原始 body，标记为未解析      |

## 注意事项

1. **GitHub API 限流**：未认证请求限制 60 次/小时，建议添加 GitHub Token
2. **版本号格式**：支持语义化版本 (v1.2.3) 和日期版本 (2026.3.8)
3. **Release 格式差异**：不同项目的 Release Notes 格式可能不同，需要灵活解析
4. **首次追踪**：首次添加项目时，只缓存当前版本，不生成变更报告

## GitHub Token 配置（可选）

在环境变量中配置可提高 API 限流阈值：

```
GITHUB_TOKEN=ghp_xxxx
```

使用 Token 后限流提升至 5000 次/小时。

## 扩展功能（未来）

- [ ] 支持订阅特定分支的 commits
- [ ] 支持 GitLab 项目
- [ ] 支持自定义关键字过滤
- [ ] 支持邮件/微信通知
