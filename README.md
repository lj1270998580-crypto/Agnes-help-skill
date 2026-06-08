# Agnes AI 帮助中心

> Agnes AI，让世界级 AI 属于每一个人。

本仓库是 Agnes AI API 的**非官方帮助资源集合**，包含交互式接入助手、完整 API 文档、以及通用支持 Skill，帮助开发者快速接入 Agnes AI 全模态 API（文本、图像、视频）。

---

## 📢 重要公告

**Agnes 2.0 全模态模型 API 正式开放全球免费调用！**

- ✅ 不限期、全模态、API 调用完全免费（RPM 20 以内）
- ✅ 注册官网 → 生成 KEY → 直接调用
- ✅ 文本、图像、视频全能适配
- ✅ 模型持续升级并保持免费

**官方平台：** https://platform.agnes-ai.com

---

## 📦 仓库内容

| 文件 | 说明 | 用途 |
|------|------|------|
| `agnes-ai-assistant.html` | 交互式接入助手 | 浏览器打开，自助完成接入、排查问题（**自动检查 GitHub 更新**） |
| `agnes-ai-api-documentation.md` | 完整 API 文档 | 整合官方全部接口信息，供 Agent 读取（**带版本号**） |
| `SKILL.md` | 通用支持 Skill | 兼容 OpenClaw / Claude Code / Claude Desktop / Hermes / Codex / WorkBuddy / Cherry Studio / Opencode / Kimi Work（**加载时检查更新**） |

---

## 🚀 快速开始

### 方式一：交互式 HTML 助手（推荐新手）

1. 下载 `agnes-ai-assistant.html`
2. 用浏览器直接打开（无需服务器）
3. 跟随 4 步向导完成接入
4. 遇到问题用左侧「问题排查」工具自助诊断

**HTML 助手包含：**
- ⚡ 快速接入向导（4 步）
- 🤖 模型速查与选择
- 🛠️ 交互式代码生成器
- 💡 Thinking 模式详解
- 🎬 视频参数调节指南
- ❓ 可搜索 FAQ（20+ 常见问题）
- 🚨 错误码速查表
- 🔍 8 类问题智能诊断
- 📡 接口端点汇总
- ✅ 接入检查清单

### 方式二：API 文档（推荐 Agent / 开发者）

`agnes-ai-api-documentation.md` 整合了 Agnes AI 官方文档的全部内容：

- 概述与核心能力
- Agnes 1.5 Flash / 2.0 Flash 完整参数与示例
- Agnes Image 2.0 / 2.1 Flash 完整参数与示例
- Agnes Video V2.0 完整参数与示例（含异步轮询）
- 隐私政策与服务条款

### 方式三：Skill（推荐 AI 工具链集成）

将 `SKILL.md` 放入你的 AI 工具 Skill 目录，即可让 Agent 自动：

- 指导新用户完成 Agnes AI 接入
- 诊断 401/400/429/500/503 等错误
- 排查视频排队过长、图像生成失败等问题
- 指导 Thinking 模式、流式输出、工具调用等高级功能
- 指导 Codex、OpenClaw、Hermes、Claude CLI/Desktop、WorkBuddy、Cherry Studio、Opencode 等工具集成
- 指导社区 Skill 安装与使用

**兼容工具：** OpenClaw、Claude Code、Claude Desktop、Hermes、Codex、WorkBuddy、Cherry Studio、Opencode、Kimi Work

**📋 一键安装（复制发给 Agent）：**
```
请读取并安装 Agnes AI 支持 Skill：https://raw.githubusercontent.com/lj1270998580-crypto/Agnes-help-skill/main/SKILL.md
```

### 自动更新提醒

本仓库的所有文件都支持**版本检查与更新提醒**：

- **HTML 助手**：每次打开页面时自动检查 GitHub 是否有新版本，有更新则显示顶部横幅提醒
- **SKILL.md**：每次被 Agent 加载时，Agent 会检查 GitHub 最新 commit，有更新则在回复开头提醒用户
- **API 文档**：文件头部标注版本号，建议定期同步最新版

**手动检查更新方式：**
1. 访问 GitHub 仓库查看最新 commit：https://github.com/lj1270998580-crypto/Agnes-help-skill
2. 或直接让 Agent 执行：`请检查 Agnes AI 支持 Skill 是否有更新`

---

### 方式四：社区 Skill（推荐进阶用户）

| 社区资源 | 适用场景 | 安装方式 |
|----------|----------|----------|
| [Yacey 生成 Skill](https://github.com/Yacey/agnes-ai-generation-skill) | Agent 用户，需要中文提示词自动翻译 | `npx skills add Yacey/agnes-ai-generation-skill` |
| [kangarooking 免费模型 Skills](https://github.com/kangarooking/agnes-free-model-skills) | Codex 用户，需要独立文本/图片/视频 Skill | 复制到 `~/.codex/skills/` |
| [16nic ComfyUI 节点](https://github.com/16nic/comfyui-agnes-ai) | ComfyUI 用户，需要可视化节点工作流 | `git clone` 到 `ComfyUI/custom_nodes` |

详见 `SKILL.md` 第 9-18 章的完整接入指南。

---

## 🔑 接入要点速记

```
Base URL: https://apihub.agnes-ai.com/v1
Headers:
  Authorization: Bearer YOUR_API_KEY
  Content-Type: application/json
```

**模型名称：**
- 通用对话：`agnes-1.5-flash`
- 编程/Agent/推理：`agnes-2.0-flash`
- 图像生成（推荐）：`agnes-image-2.1-flash`
- 视频生成：`agnes-video-v2.0`

**⚠️ 视频接口重要提醒：**
- **必须用 `video_id` 查询视频结果**：`GET /agnesapi?video_id=<ID>`
- **不要用 `task_id` 查询**，会导致排队异常延长（超过 5 分钟大概率是接口搞错了）

---

## 📚 官方与社区资源

| 资源 | 链接 |
|------|------|
| 官方平台 | https://platform.agnes-ai.com |
| 官方文档 | https://agnes-ai.com/doc/overview |
| 操作手册 | https://agnes-ai.com/doc/常用接入文档 |
| 视频文档 | https://agnes-ai.com/doc/agnes-video-v20 |
| OpenClaw 接入 | https://agnes-ai.com/doc/cid1 |
| Hermes 接入 | https://agnes-ai.com/doc/cid2 |
| Claude CLI 接入 | https://agnes-ai.com/doc/cid3 |
| Claude Desktop 接入 | https://agnes-ai.com/doc/cid4 |
| WorkBuddy 接入 | https://agnes-ai.com/doc/cid5 |
| Cherry Studio 接入 | https://agnes-ai.com/doc/cid6 |
| Opencode 接入 | https://agnes-ai.com/doc/cid7 |
| Codex++ 接入 | https://agnes-ai.com/doc/cid8 |
| 常见问题 QA | https://icn1d2hdv39m.feishu.cn/wiki/R7TEwjadJibD62kWeS9cubtpnPi |
| 社区教程 | https://github.com/Yacey/agnes-ai-generation-skill |
| 社区 Skill | https://github.com/kangarooking/agnes-free-model-skills |
| ComfyUI 节点 | https://github.com/16nic/comfyui-agnes-ai |
| 支持邮箱 | support@agnes-ai.com |

---

## 🔄 更新记录

| 日期 | 更新内容 |
|------|----------|
| 2026-06-06 | 初始版本：整合官方文档、创建交互式 HTML 助手、编写通用 Skill |
| 2026-06-06 | 补充 Codex++ 官方接入指南（区分 GUI 工具与 CLI 工具） |
| 2026-06-08 | Agnes-2.0-Flash 上下文窗口回退：官方从 1M 回退至 **256K**（Context 1M → 256K，Max Output 1M → 65.5K），此前 1M 支持因稳定性问题已回退 |
| 2026-06-06 | 修复图生图 `image` 参数位置：必须放在 `extra_body` 中，不能放请求体顶层（官方文档错误修正） |

---

## ⚠️ 免责声明

本仓库为社区整理的非官方资源，内容基于 Agnes AI 官方公开文档。如有与官方文档冲突之处，请以官方文档为准。

> Agnes AI 官方公司：Sapiens AI / Agnes AI
