---
layout: default
title: GitHub Release 周报 (2026-04-27)
date: 2026-04-27
category: GitHub Release
---

# 🚀 GitHub Release 周报 (2026-04-27)

> 共 3 个项目有更新

---

## QwenPaw - v1.1.4.post2

⏰ 发布时间：2026-04-25 15:04:16 UTC

### 🐛 Bug 修复

- 修复频道中审批功能不工作的问题

🔗 [Release Notes](https://github.com/agentscope-ai/QwenPaw/releases/tag/v1.1.4.post2)

---

## OpenClaw - v2026.4.24

⏰ 发布时间：2026-04-25 18:15:17 UTC

### ✨ 新增功能

- **Slack/HTTP**: 将 webhook 处理程序保持在进程全局注册表中，使 HTTP 模式在插件加载器/原生导入分离后仍能正常工作，`/slack/events/<account>` 不再在登录为活动状态后返回 404
- **浏览器工具**: 暴露稳定的 `tabId` 句柄（如 `t1`）以及可选的标签页标签，并在任何需要浏览器标签页目标的地方接受这些句柄
- **浏览器工具**: 返回 `suggestedTargetId` 作为标签页负载的第一个元素，使代理自然地重用标签或稳定的标签句柄，而不是原始 DevTools ID
- **浏览器工具**: 捆绑 `browser-automation` 技能，包含多步骤快照、稳定标签、过期引用和手动阻止器循环，用于代理控制的页面
- **浏览器工具**: 添加 `openclaw browser doctor`、URL 扩展快照、直接标记的屏幕截图和更清晰的标签页目标错误
- **Codex 模型**: 获取分页的 Codex 应用服务器模型目录，标记截断的 `/codex models` 输出
- **插件/CLI**: 在发现模式插件加载期间暴露通道插件 CLI 描述符，使快照注册表保持通道命令可见，而无需激活完整运行时
- **心跳**: 在心跳提示中包含异步执行完成详细信息，以便命令完成通知中继实际输出

### 🐛 Bug 修复

- **诊断**: 加强工具和模型诊断事件，防止敌对错误、阻塞监听器和不安全的稳定性原因字段
- **插件/入门**: 记录本地插件安装源元数据，而不在持久化的 `plugins.installs` 中重复原始绝对本地路径，同时保留链接的加载路径清理
- **群组聊天/静默回复**: 加强 `NO_REPLY` 提示指导，使群组保持安静，不叙述沉默或在沉默是预期结果时发出后备聊天
- **WhatsApp/群组+直接**: 在特定的 `groups.<id>` 或 `direct.<peerId>` 条目上设置 `systemPrompt: ""` 现在会抑制通配符系统提示，而不是回退到它，因此用户可以为特定群组或对等方静默全局提示
- **浏览器工具**: 告诉代理不要在现有会话类型、评估和其他 Chrome MCP 操作上传递每次调用的 `timeoutMs`，这些操作拒绝超时覆盖
- **浏览器工具**: 使用 Playwright 当前的 AI aria 快照 API 进行 `refs="aria"`，并在节点浏览器无法提供 aria 引用时回退到角色引用，以便代理仍然可以检查和点击控件（如 Google Meet 准入按钮）
- **插件/Google Meet**: 使用浏览器自动化来分类和清除 Meet 入口阻止器（如麦克风选择器间隙），并在重试时重用进行中的创建标签页，而不是打开重复项
- **Codex/GPT-5.4**: 加强原生和嵌入式运行时路径中的回退、身份验证配置文件、工具架构和重放边缘情况
- **模型/回退**: 在模型切换之前解析裸回退模型提供者 ID，因此当回退没有显式提供者前缀命名时，配置的回退链保持工作
- **语音通话/Telnyx**: 保留入站/出站回调元数据，并从 Telnyx 当前的 `transcription_data` 负载中读取转录文本
- **提供者/DeepSeek**: 连接 V4 思考控制和 OpenAI 兼容的重放策略，以便后续轮次保留 DeepSeek `reasoning_content`，而 None/关闭思考路径剥离重放推理字段
- **提供者/GitHub Copilot**: 在 Anthropic、Responses 和内置压缩摘要路径中统一 Copilot 请求头，包括工具结果和图像后续轮次，而不启用未验证的 Responses 继续
- **Codex 线束**: 将详细的工具进度发送到聊天通道，用于原生应用服务器运行，匹配 Pi 线束 `/verbose on` 和 `/verbose full` 行为
- **Codex 状态**: 将 Codex CLI OAuth 报告为原生 `codex/*` 会话的 `oauth (codex-cli)`，而不是显示未知身份验证
- **通道/CLI**: 接受显式共享密钥、基本 URL 和身份验证目录设置标志，并将遗留的 Nextcloud Talk `--url`/`--token` 添加命令映射到捆绑的插件设置输入
- **模型/CLI**: 保持 `openclaw models list` 只读，同时仍然显示符合条件的配置提供者行，因此列出模型不再重写每个代理的 `models.json`
- **代理/传输**: 将配置的尝试超时传播到受保护的每个请求调度程序，因此缓慢的本地 LLM 调用（如 Ollama）不再在 Undici 默认的 60 秒主体超时时失败
- **插件/提供者**: 在捆绑的提供者清单中镜像运行时身份验证选择，并在插件运行时加载之前检测 Moonshot/Kimi 网络搜索的 `KIMI_API_KEY`
- **网关/聊天**: 在聊天运行注册表中注册 chat.send 运行，以便生命周期错误事件到达客户端而不是被静默丢弃，修复卡住的"等待"状态和 /abort 报告没有活动运行
- **插件/QQ Bot**: 默认启用捆绑的 qqbot 插件，以便在首次启动时安装其运行时依赖 `@tencent-connect/qqbot-connector`，解除动态导入连接器之前配置任何账户的 QR 码绑定流程
- **网关/代理 RPC**: 将活动的 `agent` 运行注册到聊天中止控制器映射中，以便 `chat.abort` 和 `sessions.abort` 可以中断它们，匹配 `chat.send` 行为并解除通过公共 `agent` RPC 驱动网关的外部运行时
- **Matrix/CLI**: 将解析的运行时配置传递到验证命令，因此 `openclaw matrix verify status` 和同级验证子命令在获取 Matrix 客户端之前不再崩溃
- **网关/启动**: 在通道监视器报告就绪之前等待启动侧车，减少 Discord 和插件启动竞争，同时保持网关启动可观察性完整
- **插件/Google Meet**: 报告 Chrome 加入所需的手动操作，使用浏览器自动化进行 Meet 入口，并持久化私有 WS 节点选择加入，以便配对节点实时会话保持其预期的网络策略
- **Slack**: 通过正常的分块发送器路由原生流回退回复，因此长缓冲的 Slack Connect 响应不会被丢弃或重复
- **WhatsApp**: 在代理调度之前转录接受的语音笔记，同时保持口语转录不在命令授权中
- **WhatsApp**: 传递工具结果回复生成的媒体，同时仍然抑制仅文本工具聊天
- **配置/代理**: 在严格配置验证中接受 `agents.list[].contextTokens`，以便每个代理覆盖在热重载后存活，让 `/status` 反映配置的模型窗口而不是 200k 回退
- **内存搜索**: 将会话可见性和代理到代理策略应用于会话转录命中，并在结果限制之前保持 `corpus=sessions` 排名范围限于会话集合
- **代理/会话**: 停止会话写入锁定超时进入模型故障转移，因此本地锁定争用直接显示而不是跨提供者级联
- **自动回复**: 通过 `message_sending` 挂钩运行入站回复传递，以便插件可以在发送之前转换或取消生成的回复
- **CI/release-checks**: 通过步骤环境变量传递工作流输入和矩阵值，而不是将它们直接嵌入到 `run:` shell 命令中，减少跨操作系统 release-check 工作流中的模板注入表面

🔗 [Release Notes](https://github.com/openclaw/openclaw/releases/tag/v2026.4.24)

---

## OpenCode - v1.14.28

⏰ 发布时间：2026-2026-04-27 03:58:13 UTC

### 🐛 Bug 修复

- 修复了 `opencode upgrade` 在 bun 安装时失败的问题，除非在包含 package.json 的目录中

🔗 [Release Notes](https://github.com/anomalyco/opencode/releases/tag/v1.14.28)

---
