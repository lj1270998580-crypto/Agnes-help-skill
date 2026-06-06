---
name: agnes-ai-support
description: |
  Agnes AI API 接入支持与问题排查 Skill。帮助新用户完成 Agnes AI API 的接入配置，
  诊断和解决接入过程中遇到的认证、参数、响应、图像生成、视频生成等各类问题。
  涵盖 Thinking 模式开启、视频长度调节、流式输出、工具调用等高级功能指导。
  兼容 OpenClaw、Claude Code、Hermes、Codex 等工具链。
  触发词：Agnes AI、agnes、接入、API Key、401、400、排查、错误、视频生成、图像生成、
  thinking、stream、tool calling、模型选择、Base URL、apihub、agnes-2.0-flash、
  agnes-image、agnes-video、响应格式、timeout、超时、轮询、FAQ、问题排查、调试、
  platform.agnes-ai.com、免费调用、RPM、video_id、task_id。
---

# Agnes AI API 接入支持与问题排查

> 适用工具：OpenClaw / Claude Code / Hermes / Codex / Kimi Work
> 更新日期：2026-06-06
> 官方平台：https://platform.agnes-ai.com
> 官方文档：https://agnes-ai.com/doc/overview
> 操作手册：https://agnes-ai.com/doc/%E5%B8%B8%E7%94%A8%E6%8E%A5%E5%85%A5%E6%96%87%E6%A1%A3
> 社区教程：https://github.com/Yacey/agnes-ai-generation-skill
> 社区 Skill：https://github.com/kangarooking/agnes-free-model-skills
> ComfyUI 节点：https://github.com/16nic/comfyui-agnes-ai
> 常见问题 QA（飞书）：https://icn1d2hdv39m.feishu.cn/wiki/R7TEwjadJibD62kWeS9cubtpnPi

---

## 0. 重要公告（2026-06 更新）

### Agnes 2.0 全模态模型 API 正式开放全球免费调用

- **不限期、全模态、API 调用完全免费**（RPM 20 以内）
- 注册官网 → 生成 KEY → 直接调用
- 文本、图像、视频全能适配，高效便捷
- 模型会持续升级并保持免费
- 欢迎大家多用、多吐槽

**平台直达：** https://platform.agnes-ai.com

### 视频接口重要更新

- **必须使用 video_id 查询视频结果**，不要用 task_id 查询
- 使用 task_id 查询会导致视频排队过长（超过 5 分钟大概率是接口搞错了）
- 视频文档：https://agnes-ai.com/doc/agnes-video-v20
- 社区 Skill 中的视频接口可能未更新，请以官方文档为准

---

## 1. 快速接入流程（4 步）

### Step 1 — 创建 API Key
1. 访问 https://platform.agnes-ai.com 注册/登录
2. Settings → API Keys → Create new secret key
3. **只显示一次**，立即复制保存
4. 安全提醒：不要暴露在代码仓库、前端代码、截图、公开文档中

### Step 2 — 选择模型

| 场景 | 推荐模型 | 端点 |
|------|----------|------|
| 通用对话 / 高并发 / 低成本 | `agnes-1.5-flash` | `/v1/chat/completions` |
| 编程 / Agent / 推理 / 图片理解 | `agnes-2.0-flash` | `/v1/chat/completions` |
| 图像生成 / 编辑（推荐） | `agnes-image-2.1-flash` | `/v1/images/generations` |
| 图像快速生成 | `agnes-image-2.0-flash` | `/v1/images/generations` |
| 视频生成 | `agnes-video-v2.0` | `/v1/videos` |

### Step 3 — 配置请求

```
Base URL: https://apihub.agnes-ai.com/v1
Headers:
  Authorization: Bearer YOUR_API_KEY
  Content-Type: application/json
```

### Step 4 — 测试请求

```bash
curl https://apihub.agnes-ai.com/v1/chat/completions \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"model":"agnes-2.0-flash","messages":[{"role":"user","content":"Hello!"}]}'
```

---

## 2. 问题诊断决策树

### 2.1 认证类问题

**401 Unauthorized**
1. 检查 Header 格式：`Authorization: Bearer YOUR_KEY`（Bearer 后有空格）
2. 确认 Key 未过期/被删除（控制台 Settings → API Keys 查看）
3. 确认账户有余额（注册送 $0.1，当前所有模型免费但有 RPM 限制）
4. 检查 Key 是否有多余空格或换行符
5. 用 curl 直接测试，排除 SDK/框架问题

**API Key 泄露**
- 立即在控制台删除旧 Key，创建新 Key
- 检查代码仓库历史，用 git filter-repo / BFG 清理敏感信息
- 检查环境变量配置是否被意外提交

### 2.2 请求类问题（400 Bad Request）

**通用排查清单：**
1. JSON 格式是否合法（用 jsonlint 校验）
2. 必填参数是否缺失
3. 参数类型是否正确

**Chat 模型 400：**
- 必填：`model` + `messages`
- `messages` 必须是数组，元素含 `role` 和 `content`
- `temperature` 范围 0-2
- 图片 URL 输入时，`content` 必须是数组格式

**图像模型 400：**
- 文生图必填：`model` + `prompt` + `size`
- 图生图必填：`model` + `prompt` + `size` + `image`
- **response_format 必须放在 `extra_body` 中**，放根级会 400
- 图生图**不需要**传 `tags: ["img2img"]`
- `size` 格式：`1024x768` / `1024x1024` / `768x1024`

**视频模型 400：**
- 必填：`model` + `prompt`
- `num_frames` 必须 ≤ 441 且满足 `8n + 1`
- 有效值：81, 121, 161, 241, 441
- `frame_rate` 范围 1-60
- 图生视频：`image` 需为公网可访问 URL

### 2.3 响应类问题

**无响应 / 超时**
- Chat：超时建议 30s
- 图像：超时建议 60-360s（数秒到几十秒）
- 视频：异步任务，创建后需轮询查询，间隔 5s
- 检查网络能否访问 `apihub.agnes-ai.com`
- 检查防火墙/代理是否拦截

**503 Service Unavailable**
- 服务暂时繁忙，指数退避重试：1s → 2s → 4s → 8s
- 关注 Agnes AI 状态公告

**429 Rate Limited**
- 降低请求频率
- 免费账户 RPM 限制为 20，充值可提升
- 实现客户端队列和退避

### 2.4 视频排队过长（> 5 分钟）

**这是最重要的排查点：**
- **大概率是使用了 task_id 查询接口**
- **必须使用 video_id 查询**：`GET /agnesapi?video_id=<ID>`
- task_id 查询接口会导致排队异常延长
- 正确做法：创建任务后获取 `video_id`，用 video_id 轮询查询
- 轮询间隔建议 5 秒

### 2.5 输出质量问题

- 优化 Prompt 结构：`[Role] + [Task] + [Context] + [Requirements] + [Output Format]`
- 编程/推理任务开启 Thinking 模式
- 调整 `temperature`：确定性任务 0.1-0.3，创意任务 0.7-1.0
- 检查 `max_tokens` 是否足够，避免截断
- 图像任务：提供详细的场景、风格、光照、构图描述

---

## 3. 高级功能指南

### 3.1 Thinking 模式（agnes-2.0-flash）

**OpenAI 兼容格式：**
```json
{
  "model": "agnes-2.0-flash",
  "messages": [...],
  "chat_template_kwargs": {
    "enable_thinking": true
  }
}
```

**Anthropic 兼容格式：**
```json
{
  "model": "agnes-2.0-flash",
  "messages": [...],
  "thinking": {
    "type": "enabled",
    "budget_tokens": 2048
  }
}
```

**budget_tokens 建议：**
- 简单编码：2048
- 复杂调试/重构：4096+
- 多步骤 Agent：4096+

### 3.2 流式输出（SSE）

请求体加 `"stream": true`
- 响应逐块返回，每块以 `data:` 开头
- 最后以 `data: [DONE]` 结束
- 需正确解析 `choices[0].delta.content` 并拼接

### 3.3 工具调用

1. 请求中提供 `tools` 数组（含 function 定义）
2. 模型返回 `finish_reason: "tool_calls"`
3. 解析 `choices[0].message.tool_calls`
4. 执行函数后，以 `role: tool` 回传结果
5. 模型根据工具结果生成最终回复

### 3.4 视频长度调节

**公式：** `seconds = num_frames / frame_rate`

**约束：**
- `num_frames ≤ 441`
- `num_frames = 8n + 1`（81, 121, 161, 241, 441）
- `frame_rate`：1-60，推荐 24

**常用配置：**
| 时长 | num_frames | frame_rate |
|------|-----------|------------|
| ~3s | 81 | 24 |
| ~5s | 121 | 24 |
| ~10s | 241 | 24 |
| ~18s | 441 | 24 |

**更长视频：** 增加 num_frames 或降低 frame_rate

### 3.5 图像输出格式

**URL 输出：**
```json
{
  "extra_body": {
    "response_format": "url"
  }
}
```

**Base64 输出（文生图）：**
```json
{
  "return_base64": true
}
```

**Base64 输出（图生图）：**
```json
{
  "extra_body": {
    "response_format": "b64_json"
  }
}
```

---

## 4. 各模型参数速查

### agnes-1.5-flash
- 端点：`POST /v1/chat/completions`
- Context：256K
- Max Output：65.5K
- 参数：model, messages, temperature, top_p, max_tokens, frequency_penalty, presence_penalty, repetition_penalty, stop, seed
- 价格：Input $0.07/1M, Output $0.15/1M（**现价 $0，RPM ≤ 20**）

### agnes-2.0-flash
- 端点：`POST /v1/chat/completions`
- Context：256K
- Max Output：65.5K
- 额外参数：stream, tools, tool_choice, chat_template_kwargs, thinking
- 支持图片 URL 输入（messages[].content 数组格式）
- 价格：Input $0.1/1M, Output $0.2/1M（**现价 $0，RPM ≤ 20**）

### agnes-image-2.0/2.1-flash
- 端点：`POST /v1/images/generations`
- 必填：model, prompt, size
- 图生图必填：image（URL 数组或 Data URI Base64）
- size：1024x768 / 1024x1024 / 768x1024
- 输出：URL 或 Base64
- 价格：$0.003/image（**现价 $0，RPM ≤ 20**）

### agnes-video-v2.0
- 创建：`POST /v1/videos`
- **查询（强烈推荐）：`GET /agnesapi?video_id=<ID>`**
- 查询（兼容，不推荐）：`GET /v1/videos/{task_id}`
- 参数：model, prompt, image, mode, height(768), width(1152), num_frames, frame_rate(24), num_inference_steps, seed, negative_prompt, extra_body.image, extra_body.mode
- 价格：$0.005/second（**现价 $0，RPM ≤ 20**）
- **重要：必须用 video_id 查询，task_id 会导致排队过长**

---

## 5. 常见错误速查表

| 状态码 | 含义 | 常见原因 | 解决方案 |
|--------|------|----------|----------|
| 400 | 请求无效 | 参数错误、JSON 格式、必填缺失 | 检查格式、参数类型、必填字段 |
| 401 | 未授权 | API Key 错误/过期 | 检查 Authorization 头，确认 Key 有效 |
| 404 | 不存在 | 视频/任务 ID 错误 | 确认 ID 正确 |
| 429 | 速率限制 | 请求过于频繁（免费 RPM 20） | 降低频率，实现退避重试 |
| 500 | 服务器错误 | 服务端异常 | 稍后重试，持续出现联系支持 |
| 503 | 服务繁忙 | 负载高或维护 | 指数退避重试，关注公告 |

---

## 6. 接入检查清单

### 通用
- [ ] 已注册账户并创建 API Key（https://platform.agnes-ai.com）
- [ ] Base URL 正确：`https://apihub.agnes-ai.com/v1`
- [ ] 请求头包含 Authorization 和 Content-Type
- [ ] API Key 未暴露在公开代码中
- [ ] 已实现错误处理和重试逻辑
- [ ] 了解 RPM 限制（免费 20/min）

### Chat
- [ ] 模型名称拼写正确
- [ ] messages 数组格式正确
- [ ] 图片 URL 使用数组 content 格式
- [ ] 流式输出能正确解析 SSE
- [ ] 工具调用能处理 finish_reason: tool_calls

### 图像
- [ ] 模型名称正确（推荐 2.1）
- [ ] 文生图传 model + prompt + size
- [ ] 图生图传 image 数组
- [ ] response_format 在 extra_body 中
- [ ] 未传 tags: ["img2img"]
- [ ] 输入图片 URL 公网可访问
- [ ] 客户端超时 ≥ 60s

### 视频
- [ ] 模型名称：agnes-video-v2.0
- [ ] num_frames ≤ 441 且满足 8n+1
- [ ] frame_rate 在 1-60
- [ ] 图生视频图片 URL 公网可访问
- [ ] **已实现轮询查询（间隔 5s）**
- [ ] **使用 video_id 查询结果（不要用 task_id）**
- [ ] 视频排队超过 5 分钟时检查查询接口是否正确

---

## 7. 最佳实践

### Prompt 编写
- 使用结构化格式：`[Role] + [Task] + [Context] + [Requirements] + [Output Format]`
- 编程任务：提供语言、框架、错误信息、期望行为
- Agent 任务：清晰描述目标、可用工具、任务约束
- 图像任务：主体 + 场景 + 风格 + 光照 + 构图 + 质量要求
- 视频任务：主体 + 动作 + 场景 + 镜头运动 + 光照 + 风格

### 性能优化
- 高并发场景使用 agnes-1.5-flash
- 需要推理/编程使用 agnes-2.0-flash + Thinking
- 图像生成设置合理超时（60-360s）
- 视频生成使用异步 + 轮询模式
- 实现指数退避重试（1s → 2s → 4s → 8s）
- **视频查询必须用 video_id，避免 task_id 导致的排队**

### 安全
- API Key 存储在环境变量或密钥管理服务中
- 前端代码中绝不硬编码 Key
- 定期轮换 API Key
- 监控异常用量

---

## 8. 社区资源

- **官方平台**：https://platform.agnes-ai.com
- **官方文档**：https://agnes-ai.com/doc/overview
- **操作手册**：https://agnes-ai.com/doc/%E5%B8%B8%E7%94%A8%E6%8E%A5%E5%85%A5%E6%96%87%E6%A1%A3
- **视频文档**：https://agnes-ai.com/doc/agnes-video-v20
- **常见问题 QA**：https://icn1d2hdv39m.feishu.cn/wiki/R7TEwjadJibD62kWeS9cubtpnPi
- **社区教程**：https://github.com/Yacey/agnes-ai-generation-skill
- **社区 Skill**：https://github.com/kangarooking/agnes-free-model-skills
- **ComfyUI 节点**：https://github.com/16nic/comfyui-agnes-ai
- **支持邮箱**：support@agnes-ai.com
- **公司**：Sapiens AI / Agnes AI

---

> Agnes AI，让世界级 AI 属于每一个人。
