# 🚀 GitHub Release 周报 (2026-04-22)

> 共 3 个项目有更新

---

## QwenPaw - v1.1.3

⏰ 发布时间：2026-04-22 12:58 (UTC+8)

### ✨ 新增功能

**Agent System**
- **备份与恢复**：备份和恢复系统 — 创建 agents、skills、memory 和 sessions 的范围快照，支持按 agent 选择，导入/导出为 zip 文件
- **ACP Server**：通过 `qwenpaw acp` 将 QwenPaw agents 暴露为 ACP (Agent Communication Protocol) 端点
- **主动 Agent 消息**：Agents 可以主动发送消息，使用 session memory 和屏幕上下文提供及时信息
- **跨提供商消息规范化**：在对话中无缝切换 LLM 提供商 — 更改模型时自动清理和规范化提供商特定的消息字段

**Console & UI**
- **Console 插件系统**：Console 的可扩展插件架构 — 第三方插件可以注入侧边栏页面、注册路由和共享主机模块
- **Agent 统计页面**：新仪表板，包含会话和消息趋势图表、随时间变化的 token 使用情况以及渠道分解饼图

**Skills**
- **Skill 页面改进**：重新设计的 Skills 和 Skill Pool 页面，支持批量选择/管理，分离的搜索和过滤控件
- **内置 Skill 语言切换**：所有内置 skills 现在都提供英文和中文版本。从 Skill Pool 页面切换语言，导入 skills 到 agents 时支持默认语言

**Security**
- **Shell 规避守护**：新的 Tool Guard 守护进程，检测 shell 命令混淆模式
- **增强的 Tool Guard 响应**：Tool guard 消息现在包含风险严重性级别以及本地化解释，说明为什么工具调用被阻止或需要批准

**Providers**
- **本地模型管理**：为本地模型 (llama.cpp) 配置自定义服务器端口并实时监控服务器日志
- **OpenRouter 多模态检测**：OpenRouter 模型现在从模型注册表自动报告多模态能力（图像/视频支持）
- **Aliyun Coding Plan 国际化**：为 Aliyun Coding Plan 提供商添加国际区域支持

**Channels**
- **QQ 即时确认**：QQ 渠道的可配置即时回复 — 在 agent 处理请求时立即确认用户
- **Telegram 输入指示器**：输入指示器在工具执行期间保持活动状态，在 agent 工作时提供持续的视觉反馈
- **DingTalk 回复时 @提及**：在 DingTalk 群聊中回复时自动 @提及原始发送者
- **渠道健康检查和重启 API**：每个 agent 的 HTTP 端点，用于检查单个渠道健康状态和热重启渠道

**CLI**
- **更新提供商基础 URL**：`qwenpaw providers update` 现在支持从命令行更新提供商基础 URL

### 🔄 变更

- **调试页面重新设计**：将调试页面重新定位到设置下，改进组件结构、专用日志查看器和暗模式样式修复
- **`make_plan` Skill 更新**：清理了过时的文档引用并简化了 `make_plan` skill
- **统一渠道媒体目录**：所有渠道现在一致地从 agent 工作空间解析 `media_dir`，确保跨渠道类型的隔离文件存储

### 🐛 Bug 修复

**Console & UI**
- **预览 URL 前缀**：修复文件预览路径中重复的 URL 前缀
- **Markdown 渲染**：修复工作空间文件编辑器中的 markdown 渲染和代码块复制样式
- **表格滚动**：修复会话和定时作业页面上的表格滚动

**Channels**
- **WeCom 附件访问**：修复服务器部署中 WeCom 附件访问失败
- **WeCom 文件上传**：修复 WeCom 文件上传中的事件循环阻塞，并为 `send_file_to_user` 添加相对路径支持
- **WeCom 重复消息**：修复 WeCom 群消息的重复聊天条目
- **WeCom 截图文件名**：修复 WeCom 截图文件名中的 CJK 字符导致下载失败

### 🎉 新贡献者
- @daliu858, @xuanrui-L, @pxdawn, @mailmrcai, @linhuang0405, @imrewce, @zealonexp, @Prince-liu

🔗 [Release Notes](https://github.com/agentscope-ai/QwenPaw/releases/tag/v1.1.3)

---

## OpenClaw - v2026.4.21

⏰ 发布时间：2026-04-22 12:18 (UTC+8)

### ✨ 新增功能

- OpenAI/images：将捆绑的图像生成提供商和实时媒体烟雾测试默认为 `gpt-image-2`，并在图像生成文档和工具元数据中宣传更新的 2K/4K OpenAI 大小提示

### 🐛 Bug 修复

- **Plugins/doctor**：从 doctor 路径修复捆绑插件运行时依赖项，以便打包安装可以恢复缺失的渠道/提供商依赖项，而无需广泛的核心依赖项安装
- **图像生成**：在自动提供商回退之前以警告级别记录失败的提供商/模型候选，因此即使后续提供商成功，OpenAI 图像失败在网关日志中也可见
- **Auth/commands**：要求所有者身份（所有者候选者匹配或内部 `operator.admin`）用于所有者强制命令，而不是将通配符渠道 `allowFrom` 或空的所有者候选者列表视为足够，因此当 `enforceOwnerForCommands=true` 且 `commands.ownerAllowFrom` 未设置时，非所有者发送者无法通过宽松的回退到达仅所有者命令
- **Slack**：在运行时出站发送中保留线程别名，以便当调用者提供 `threadTs` 时，通用运行时发送保持在预期的 Slack 线程中
- **Browser**：立即拒绝操作路径中的无效 `ax<N>` 可访问性引用，而不是等待浏览器操作超时
- **npm/install**：将 `node-domexception` 别名镜像到根 `package.json` `overrides`，以便 npm 安装停止显示通过 Pi/Google 运行时依赖项拉取的已弃用 `google-auth-library -> gaxios -> node-fetch -> fetch-blob -> node-domexception` 链

🔗 [Release Notes](https://github.com/openclaw/openclaw/releases/tag/v2026.4.21)

---

## OpenCode - v1.14.20

⏰ 发布时间：2026-04-21 01:55 (UTC+8)

### ✨ 新增功能

- 添加了实验性 HTTP API 的 `GET /config` 端点

### 🔄 变更

**Desktop**
- 停止提示控件在每次渲染时重播其淡入动画
- 添加了在 agent 工作时隐藏会话进度条的设置
- 修复了选择服务器对话框布局，使服务器列表和操作大小正确
- 修复了同步项目更新，使桌面项目状态更改可靠地应用
- 修复侧边栏项目头像以在没有设置覆盖时回退到 `icon.url`

### 🐛 Bug 修复

**Core**
- 修复 TUI 中的系统主题回归
- 修复在 Node 下运行时 Windows 上的本地动态导入，改进插件和工具加载

**TUI**
- 修复权限回复使用远程工作空间，以便发送到正确的工作空间

**SDK**
- 修复 `WorkspaceAdaptor.create` 类型以包含 `env` 参数

### 🎉 社区贡献者
- @heimoshuiyu, @ysm-dev, @jamesmurdza, @OpeOginni

🔗 [Release Notes](https://github.com/anomalyco/opencode/releases/tag/v1.14.20)

---

**报告生成时间**：2026-04-22
