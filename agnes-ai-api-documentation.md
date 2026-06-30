# Agnes AI API 完整文档

> **文档版本：** v1.2.14
> **来源：** https://agnes-ai.com/doc/overview 及其子页面
> **整理时间：** 2026-06-06
> **GitHub 仓库：** https://github.com/lj1270998580-crypto/Agnes-help-skill
> **本文档整合了 Agnes AI API 官方在线文档的全部内容，方便 Agent 快速获取信息**

> 📢 **更新检查：** 建议定期从 GitHub 仓库获取最新版文档，确保信息准确。
> 仓库地址：https://github.com/lj1270998580-crypto/Agnes-help-skill

---

## 目录

1. [概述](#一概述)
2. [Agnes 1.5 Flash](#二agnes-15-flash)
3. [Agnes 2.0 Flash](#三agnes-20-flash)
4. [Agnes Image 2.0 Flash](#四agnes-image-20-flash)
5. [Agnes Image 2.1 Flash](#五agnes-image-21-flash)
6. [Agnes Video V2.0](#六agnes-video-v20)
7. [隐私政策](#七隐私政策)
8. [服务条款](#八服务条款)

---

Sapiens AI 是 Agnes AI 的母公司，专注于研发先进的多模态 AI 模型与基础设施，致力于为下一代智
能应用、创意应用和消费产品提供强大的 AI 能力支持。
我们的使命是：
让世界级AI属于每一个人。
通过Agnes AI，我们希望提高高质量AI技术的使用效率，让开发者、创作者、创业团队和企业都能够以
更简单、更稳定、更经济的方式，将先进的AI能力接入自己的产品与业务中。
我们相信，世界级人工智能不应该只属于少数大型机构，而应该成为每一个开发者使用、每一个产品实
现集成、每一个用户实现受益的基础能力。
Agnes AI，让世界级AI属于每一个人。
Agnes AI API为开发者提供统一、稳定、易接入的多模态AI模型服务，支持文本、图像、视频等多种生
成与理解能力。
开发者可以通过 Agnes AI API 快速构建 AI 原生应用，包括但不限于：
AI对话与文本生成
逻辑推理与内容理解
文生图与图像编辑
图生视频与视频生成
音视频同步生成

## 一、关于 Sapiens AI
## 二、Agnes AI API 简介

Agent工具与自动化工作流程
创意内容生成与多模态互动应用
Agnes AI API 兼容 OpenAI 风格接口，方便开发者基于现有代码快速迁移和接入，减少开发成本，提
高集成效率。
Agnes AI API 目前主要支持以下核心能力：
支持高质量的文本生成、内容续写、摘要提取、逻辑推理、问答对话、代码辅助和Agent任务处理等场
景。
适用场景包括：
AI聊天助手
内容创作
文档总结
智能问答
代码生成
代理自动化任务
支持根据文本提示词生成高清图像，也支持对现有图片进行修改、优化和风格化处理。
适用场景包括：
文生图
图像编辑
商品图生成
## 三、核心能力
### 1. 内容生成与推理
### 2. 生成图像与编辑
/ /

创意海报生成
角色形象生成
社交媒体素材制作
支持生成高质量视频内容，并可支持音频与画面同步生成，降低视频制作流程，提升内容生产效率。
适用场景包括：
AI视频生成
图生视频
短视频创作
创意广告素材
角色动画
音视频同步内容生成
支持文本、图像、视频等多种模态能力组合，帮助开发者构建更智能、更自然的交互体验。
适用场景包括：
多模态 AI 助手
图像理解
视频理解
创意工作流
AI社交互动
教育、娱乐与生产力工具
### 3. 视频与音视频同步生成
### 4. 多模态理解与创作
/ /

Agnes AI 提供多类型模型能力，包括文本模型、图像模型、视频模型和多模态模型。
其中，Sapiens AI的模型包括自研的 Claw 系列模型，以及为创意生成场景的图像、视频和音视频模型。
这些模型可以帮助开发者快速完成从理解内容、文本生成，到图像生成、图像编辑、视频生成的完整AI
能力接入。
Agnes AI API 兼容 OpenAI 风格接口。
如果您已经使用过OpenAI-Compatible API，通常只需要修改以下配置即可完成接入：
基本 URL
API密钥
模型名称
兼容的方式可以帮助开发者快速迁移现有项目，降低接入成本，并减少重复开发工作。
所有API请求均应基于以下Base URL发起：
请确保请求路径基于该地址拼接，避免因路径错误导致接口请求失败。
所有API请求都需要通过API Key进行身份认证。
请在请求头中填写以下参数， YOUR_API_KEY 替换为你自己的有效 API Key：
## 四、模型能力### 概述
## 五、接口兼容性
## 六、基本网址
https://apihub.agnes-ai.com/v1
## 七、身份认证
Authorization: Bearer YOUR_API_KEY
/ /

API Key属于敏感信息，请妥善保管。
请勿将 API Key暴露在以下位置：
公开代码仓库
前端客户端代码
截图或录屏内容
公开文档
可被别人访问的配置文件
如果发现API密钥泄露，建议立即在控制台删除或重置该密钥，防止产生非授权调用。
您可以按照以下步骤快速开始使用Agnes AI API：
登录 Agnes AI 控制台，进入 API Key 管理页面，创建并复制您的 API Key。
根据你的使用场景选择对应模型，例如文本模型、图像模型、视频模型、多模态模型。
将 API Base URL 配置为：
在请求 Header 中加入 API Key，并按照 OpenAI-Compatible API 格式发起请求。
## 八、安全提醒
## 九、快速开始
### 第一步：创建 API Key
### 第二步：选择模型
### 第三步：配置请求地址
https://apihub.agnes-ai.com/v1
### 第四步：发起 API 请求
/ /

Agnes AI API 适用于以下产品和业务场景：
AI聊天应用
人工智能搜索与研究工具
人工智能编程与办公工具
AI图片生成工具
AI视频生成工具
AI角色与互动应用
AI社交产品
代理自动化平台
创意内容制作平台
教育、娱乐、电商与营销工具
本文档用于帮助开发者快速了解Agnes AI API的基础能力、接入方式和使用规范。
如需查看具体模型参数、请求示例、### 返回格式和### 错误码说明，请继续阅读对应模型的详细接入文档。
## 十、适用场景开发
## 十一、文档说明
/ /

---

Agnes 1.5 Flash 是一款轻量、大的语言模型，针对高效低延迟、高并发和占用部署场景进行了优化。
Agnes 1.5 Flash具备以下特点：
采用先进的量化技术，显着降低计算资源需求
在模型性能与推理速度之间取得良好的平衡，适合生产环境中的实时应用场景
支持文本+图像的多模态输入
Agnes 1.5 Flash适用于以下场景：
实时交互类应用
高并发服务系统
成本敏感型业务负载
轻量化智能接口
项目 说明
### API 端点 https://apihub.agnes-ai.com/v1/chat/completions
Agnes 1.5 Flash
模型### 概述
适用场景
接口信息

请求方法 POST
内容类型 application/json
身份验证方法 Bearer Token
身份验证头 Authorization: Bearer YOUR_API_KEY
Content-Type 头 Content-Type: application/json
参数 类型 是否必填 说明
model string 是
模型名称，固定
为 agnes-1.5-
flash
messages array 是 对话消息数组
temperature number 否
采样温度，用于
控制生成内容的
随机性
top_p number 否 核采样概率
max_tokens integer 否 最大生成token数
量
frequency_penalty number 否 频率惩罚，用于
减少重复内容
presence_penalty number 否
存在惩罚，用于
激励模型引入新
话题
repetition_penalty number 否 重复控制系数
stop string/array 否 停止序列
seed integer 否 随机种子，为保
证结果可恢复
### 请求参数

调用示例
1.纯文本对话请求
curl https://apihub.agnes-ai.com/v1/chat/completions \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-1.5-flash",
    "messages": [
      {
        "role": "user",
        "content": "what'\''s this?"
      }
    ],
    "temperature": 0.5,
    "max_tokens": 1024
  }'
2. 多模态请求（文本+图像）
curl https://apihub.agnes-ai.com/v1/chat/completions \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-1.5-flash",
    "messages": [
      {
        "role": "user",
        "content": [
          {
            "type": "text",
            "text": "Describe this image"
          },
          {
            "type": "image_url",
            "image_url": {
              "url": "https://example.com/image.jpg"
            }
          }

字段 说明
id 本次对话请求的唯一 ID
created 请求时间戳
choices[0].message.content 模型返回的内容
        ]
      }
    ]
  }'
### 响应格式
{
  "id": "chatcmpl-xxx",
  "object": "chat.completion",
  "created": 1773803415,
  "model": "agnes-1.5-flash",
  "choices": [
    {
      "index": 0,
      "finish_reason": "stop",
      "message": {
        "role": "assistant",
        "content": "This image shows..."
      }
    }
  ],
  "usage": {
    "prompt_tokens": 120,
    "completion_tokens": 300,
    "total_tokens": 420
  }
}
### 响应字段说明

finish_reason 生成结束原因，例如 stop、length 等
usage token消耗统计
项目 数值
Context 512K
Max Output 64K
类型 ### ### 价格 现价
Input Tokens $0.07 / 1M tokens $0 / 1M 
tokens
Output Tokens $0.15 / 1M tokens $0 / 1M 
tokens
支持文本+图像多模态输入
针对低延迟和高吞吐场景优化
兼容 OpenAI 聊天完成 API
兼容 OpenAI Responses API
适合生产环境布置
### 模型限制
### ### 价格
### 功能与兼容性

---

Agnes 2.0 Flash 是由 Sapiens AI 开发的一款快速、高效的语言模型，面向智能体工作流、工具调
用、编程任务、推理、多轮对话、图片理解以及高频生产环境应用场景设计。
Agnes 2.0 Flash 在 Claw-Eval 基准测试中取得了强劲表现，在 General Leaderboard 中排名第 9，
Pass^3 分数为 60.9%，展现出在主流语言模型中较强的自主智能体能力。
Agnes 2.0 Flash 针对快速、可靠、低成本的语言生成、智能体任务执行和图片理解进行了优化。
该模型支持以下能力：
能力 说明
Chat 
Completion 为对话和应用生成高质量回复
多轮对话 在多轮交互中保持上下文连续性
### 图片 URL 输入支持通过公网图片 URL 传入图片内容
图片理解 支持基于图片的内容理解、截图分析和信息提取
工具调用 调用外部工具和函数，支持智能体工作流
智能体工作流 支持规划、执行和多步骤任务完成
编程任务 辅助代码生成、调试、解释和重构
推理 处理结构化推理、任务拆解和决策
流式输出 实时返回响应，提升用户体验
OpenAI 兼容 
API 使用兼容 OpenAI Chat Completions API 的结构
Agnes 2.0 Flash
模型### 概述

Agnes 2.0 Flash 适用于以下场景：
场景 示例用例
AI 助手 通用问答、日常助手、效率支持
自主智能体 多步骤任务执行、规划和工具使用
编程助手 代码生成、调试、重构和解释
工作流自动化任务拆解、流程自动化和执行规划
客户支持 FAQ 问答、客服聊天机器人、服务自动化
搜索与问答 基于搜索的回答、摘要生成、信息提取
内容生成 营销文案、文章、产品描述、脚本
开发者工具 API 助手、文档助手、编程 Copilot
AI 原生应用 消费级应用、效率工具、智能体应用
图片理解 图片描述、截图分析、视觉问答、信息提取
项目 说明
API Endpoint https://apihub.agnes-ai.com/v1/chat/completions
Request 
Method POST
Content-Type application/json
AuthenticationBearer Token
Authentication 
Header Authorization: Bearer YOUR_API_KEY
适用场景
API 信息
Endpoint

参数 类型 是否必填 说明
model string 是 模型名称，固定为 agnes-2.0-flash
messages array 是 对话消息数组，包括 system、user 和 
assistant 消息
messages[].content string / array是 消息内容。可为纯文本字符串，也可为包含 
text 、image_url  的内容数组
temperature number 否 控制输出随机性。较低值会生成更确定性的结
果
top_p number 否 控制核采样。较低值会使输出更加聚焦
max_tokens number 否 响应中最多生成的 token 数
stream boolean 否 是否启用流式响应输出
tools array 否 用于工具调用工作流的工具定义
tool_choice string / object否 控制模型是否以及如何使用工具
chat_template_kwargs object 否 #### OpenAI 兼容请求中用于开启 Thinking 等扩
展能力
thinking object 否 #### Anthropic 兼容请求中用于开启 Thinking 模
式
Agnes 2.0 Flash 支持通过图片 URL 输入图片内容。开发者可以在同一个 messages 请求中同时传入
文本指令和图片 URL，让模型基于图片进行理解、分析、问答或信息提取。
支持的输入类型包括：
输入类型 支持方式 说明
文本 text 普通文本指令或问题
图片 URL image_url 通过公网可访问的图片链接传入图片
### 请求参数
### 图片 URL 输入支持

当使用图片 URL 输入时，messages[].content 应使用数组结构，每个内容块代表一种输入内容。
用于生成普通的聊天补全响应。
### 图片内容结构
{
  "role": "user",
  "content": [
    {
      "type": "text",
      "text": "Describe the content of this image."
    },
    {
      "type": "image_url",
      "image_url": {
        "url": "https://example.com/image.jpg"
      }
    }
  ]
}
调用示例
1. 基础 Chat Completion 请求
curl https://apihub.agnes-ai.com/v1/chat/completions \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-2.0-flash",
    "messages": [
      {
        "role": "system",
        "content": "You are a helpful AI assistant."
      },
      {
        "role": "user",
        "content": "Explain how autonomous agents use tools to complete tasks."
      }

用于启用流式输出。
用于需要外部工具调用的智能体工作流。
    ],
    "temperature": 0.7,
    "max_tokens": 1024
  }'
2. 流式输出请求
curl https://apihub.agnes-ai.com/v1/chat/completions \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-2.0-flash",
    "messages": [
      {
        "role": "user",
        "content": "Write a short product introduction for an AI assistant app."
      }
    ],
    "stream": true
  }'
3. 工具调用请求
curl https://apihub.agnes-ai.com/v1/chat/completions \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-2.0-flash",
    "messages": [
      {
        "role": "user",
        "content": "What is the weather like in Singapore today?"
      }
    ],
    "tools": [
      {

用于通过图片链接传入图片，并让模型理解或分析图片内容。
        "type": "function",
        "function": {
          "name": "get_weather",
          "description": "Get the current weather for a location",
          "parameters": {
            "type": "object",
            "properties": {
              "location": {
                "type": "string",
                "description": "The city and country"
              }
            },
            "required": ["location"]
          }
        }
      }
    ]
  }'
4. 图片 URL 输入请求
curl https://apihub.agnes-ai.com/v1/chat/completions \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-2.0-flash",
    "messages": [
      {
        "role": "user",
        "content": [
          {
            "type": "text",
            "text": "Describe the content of this image."
          },
          {
            "type": "image_url",
            "image_url": {
              "url": "https://example.com/image.jpg"
            }
          }

字段 类型 说明
id string 本次补全请求的唯一 ID
object string 对象类型，通常为 chat.completion
created integer 请求时间戳
        ]
      }
    ]
  }'
### 响应格式

{
  "id": "chatcmpl_xxx",
  "object": "chat.completion",
  "created": 1774432125,
  "model": "agnes-2.0-flash",
  "choices": [
    {
      "index": 0,
      "message": {
        "role": "assistant",
        "content": "Autonomous agents use tools by understanding the user's goal, breaking it in
      },
      "finish_reason": "stop"
    }
  ],
  "usage": {
    "prompt_tokens": 35,
    "completion_tokens": 58,
    "total_tokens": 93
  }
}
### 响应字段说明

model string 本次请求使用的模型
choices array 生成的响应结果列表
choices[].index integer 响应结果的索引
choices[].message object Assistant 消息对象
choices[].message.role string 消息发送者角色
choices[].message.content string 模型生成的响应内容
choices[].finish_reason string 生成停止原因
usage object Token 使用信息
usage.prompt_tokens integer 输入 token 数量
usage.completion_tokens integer 输出 token 数量
usage.total_tokens integer 使用的 token 总数
对于代码编写、调试、推理和 Agent 工作流，建议开启 Thinking 模式，以提升代码质量、任务拆解能
力和问题解决效果。
使用 OpenAI 兼容 API 格式时，在请求体中添加 chat_template_kwargs.enable_thinking：
### 为编码任务启用 Thinking
#### OpenAI 兼容请求
{
  "model": "agnes-2.0-flash",
  "messages": [
    {
      "role": "user",
      "content": "Help me write a Python script to process a CSV file."
    }
  ],
  "chat_template_kwargs": {
    "enable_thinking": true

使用 Anthropic 兼容 API 格式时，在请求体中添加 thinking 字段：
budget_tokens 用于控制最大 Thinking token 预算。对于常见编码任务，建议从 2048 开始设置。对
于更复杂的调试、重构或多步骤 Agent 任务，可以根据需要适当提高该值。
Agnes 2.0 Flash 支持以下能力：
Chat Completion
多轮对话
System Prompt
图片 URL 输入
图片理解
流式输出
工具调用
  }
}
#### Anthropic 兼容请求
{
  "model": "agnes-2.0-flash",
  "messages": [
    {
      "role": "user",
      "content": "Help me refactor this TypeScript function and explain the changes."
    }
  ],
  "thinking": {
    "type": "enabled",
    "budget_tokens": 2048
  }
}
### 功能与兼容性

智能体工作流
编程任务
推理任务
JSON 风格输出
兼容 OpenAI Chat Completions API 的请求结构
为了获得更好的结果，建议提供清晰的指令、上下文和期望的输出格式。
对于编程任务，建议提供编程语言、框架、错误信息和期望行为。
对于智能体工作流，建议清晰描述目标、可用工具和任务约束。
### 最佳实践
### Prompt 编写建议
#### 示例：产品文案生成

You are a product marketing expert. Write a concise App Store description for an AI assistant ap
#### 示例：编程任务

Help me debug this React component. The issue is that the button state does not update after cl
#### 示例：智能体工作流

You are an autonomous research agent. Search for relevant information, summarize the key finding
#### 示例：图片理解任务

对于图片理解任务，建议明确说明希望模型关注的内容，例如整体描述、文字提取、界面分析、物体识
别或结构化输出。
建议使用以下结构组织 Prompt：
图片 URL 必须可公网访问。
如果图片 URL 需要登录、鉴权或存在防盗链，模型可能无法读取。
建议使用标准图片格式，例如 JPG、JPEG、PNG 或 WebP。
对于截图、报错图、产品界面图，建议在文本中补充你希望模型重点关注的问题。
图片 URL 输入可以与工具调用、流式输出和 Agent 工作流结合使用。

Analyze this screenshot. Identify the main UI elements, explain the possible issue, and provide 
### 推荐 Prompt 结构
[Role] + [Task] + [Context] + [Requirements] + [Output Format]
示例

You are a senior product manager. Analyze this feature idea for an AI assistant app. Consider u
### 图片理解 Prompt 示例

You are an image analysis assistant. Analyze the provided image URL, summarize the key informat
### 图片 URL 使用建议

项目 数值
Context 512K
Max Output 64K
类型 ### ### 价格 现价
Input Tokens $0.1 / 1M 
tokens
$0 / 1M 
tokens
Output Tokens $0.2 / 1M 
tokens
$0 / 1M 
tokens
使用 agnes-2.0-flash  作为模型名称。
基础 Chat Completion 请求必须包含 model  和 messages 。
messages[].content  可使用纯文本字符串，也可使用包含文本和图片 URL 的内容数组。
如需输入图片，请使用 image_url  并提供公网可访问的图片 URL。
如需启用流式响应，请将 stream  设置为 true 。
对于工具调用工作流，请提供 tools ，并可按需提供 tool_choice 。
temperature  用于控制随机性。较低值更适合确定性任务，较高值更适合创意生成。
Agnes 2.0 Flash 适合需要快速响应、强任务完成能力、图片理解能力和可靠智能体表现的生
产级应用。
### 模型限制
### ### 价格
说明

---

Agnes Image 2.0 Flash 是由 Sapiens AI 开发的一款高性能图像生成与图像编辑模型。
该模型支持 文生图、图生图 和 多图合成 工作流程，适用于快速创意制作、图像优化、营销视觉设计、
电商产品图、社交内容生成以及专业视觉内容制作等场景。
Agnes Image 2.0 Flash已登上 人工分析图像编辑排行榜，取得 ELO 1,184【动态调整】的成绩，并
进入 Top 20 区间，表现出在主流图像模型中导入的图像编辑能力。
Agnes Image 2.0 Flash针对快速、高质量的图像生成与图像编辑任务进行了优化。
该模型支持以下能力：
能力 说明
文本转图像 根据文本提示生成图像
图像到图像 基于图像输入进行编辑、转换或增强
多图像输入 支持输入多张参考图并合成为一张新图像
图像编辑 修改构图、风格、对象、背景、场景和景观细节
样式控制 调整艺术风格、天线、布局和视觉方向
快速世代 针对快速、突出的生产工作流程进行优化
兼容 OpenAI 的 
API 使用兼容 OpenAI Images API 的请求结构
Agnes Image 2.0 Flash接入文档
### 一、模型简介
二、模型### 概述

场景 示例用例
创意设计 海报、概念艺术、社交媒体视觉图
营销内容 产品广告、活动创意、Banner
文生图 通过提示生成产品图、插画、场景图、概念图
图像编辑 对象替换、背景更换、风格转换、局部改图
角色合成 将多个角色或参考图组合到相同场景中
视觉生产 为App、网站、游戏和视频生成素材
电商 产品图优化、场景化产品图、营销主图
社交内容 Meme、人物、人生图
### 三、适用场景
### 四、API 基础信息
基本 URL
https://apihub.agnes-ai.com
端点
POST https://apihub.agnes-ai.com/v1/images/generations
标题
-H "Authorization: Bearer YOUR_API_KEY"
-H "Content-Type: application/json"
### 五、模型名称

模型 用途
agnes-image-2.0-flash 文生图、图生图、多图合成、图像编辑
参数 类型 是否必填 说明
model string 是
模型名称，固定
为 agnes-image-
2.0-flash
prompt string 是
描述目标或图像
编辑需求的文本
提示词
size string 是
图像输出尺寸，
例如 1024x768
、1024x1024 、
768x1024、4096x4096（4K 已全面支持）
image string[] 图生图必填
输入图片数组，
支持公网 URL 
或 Data URI 
Base64
return_base64 boolean 否 文生图返回 
Base64 时使用
extra_body.response_format string 否
输出格式，常
用 url
 或 b64_json
文生图只需要确定：
agnes-image-2.0-flash
六、### 请求参数
### 七、重要说明
1. 文生图需传 image

图生图父母图合成时，需要在大量 image 架构：
多图合成时可以确定多张图片网址：
当前接入方式中，图生图请求不需要传输：
必须排序 model、prompt、size 和 image。

{
  "model": "agnes-image-2.0-flash",
  "prompt": "A clean product photo of a glass cube on a white studio background, soft shadows, h
  "size": "1024x768"
}
2.图生图需传 image

**⚠️ 重要：image 参数必须放在 `extra_body` 中，不能放在请求体顶层！**

- ❌ 错误（顶层）：`"image": ["url"]` → 实际执行 text-to-image，image_tokens: 0
- ✅ 正确（extra_body）：`"extra_body": {"image": ["url"]}` → 实际执行 i2i-general

```json
{
  "extra_body": {
    "image": [
      "https://example.com/input.png"
    ]
  }
}
```

多图合成时同样放在 extra_body 中：
```json
{
  "extra_body": {
    "image": [
      "https://example.com/character-1.png",
      "https://example.com/character-2.png"
    ]
  }
}
```
3.图生图不需要传 tags
{
  "tags": ["img2img"]
}
4. response_format  不要放在一起

不要这样写：
推荐写法：
如果将 response_format 放在其中，可能会返回 400 错误。
生成图片网址位于：
{
  "response_format": "url"
}
{
  "extra_body": {
    "response_format": "url"
  }
}
### 八、调用示例
1. 文生图：URL输出

curl https://apihub.agnes-ai.com/v1/images/generations \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-image-2.0-flash",
    "prompt": "A clean product photo of a glass cube on a white studio background, soft shadows,
    "size": "1024x768",
    "extra_body": {
      "response_format": "url"
    }
  }'
data[0].url

生成图片Base64 位于：
用于编辑或转换现有图像。
生成图片网址位于：
2. 文生图：Base64输出

curl https://apihub.agnes-ai.com/v1/images/generations \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-image-2.0-flash",
    "prompt": "A clean product photo of a glass cube on a white studio background, soft shadows,
    "size": "1024x768",
    "return_base64": true
  }'
data[0].b64_json
3.图生图：URL输入，URL输出

curl https://apihub.agnes-ai.com/v1/images/generations \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-image-2.0-flash",
    "prompt": "Transform this image into a cinematic cyberpunk style while preserving the main 
    "size": "1024x768",
    "extra_body": {
    "image": [
      "https://example.com/input-image.png"
    ],
      "response_format": "url"
    }
  }'

生成图片Base64 位于：
如果输入图片不是公网URL，也可以使用Data URI Base64作为输入。
数据URI格式：
请求示例：
data[0].url
4.图生图：URL输入，Base64输出
curl https://apihub.agnes-ai.com/v1/images/generations \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-image-2.0-flash",
    "prompt": "Make the object orange while preserving the original composition",
    "size": "1024x768"
    "extra_body": {
    
      "response_format": "b64_json"
    }
  }'
data[0].b64_json
5. 图生图：Data URI Base64 输入

data:image/png;base64,BASE64_HERE

curl https://apihub.agnes-ai.com/v1/images/generations \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-image-2.0-flash",
    "prompt": "Make the object matte black while preserving the original composition",
    "size": "1024x768",
    "extra_body": {
      "image": [
        "data:image/png;base64,BASE64_HERE"
      ],
      "response_format": "b64_json"
    }
  }'
6.多图合成请求

curl https://apihub.agnes-ai.com/v1/images/generations \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-image-2.0-flash",
    "prompt": "Combine the two characters into an intense fantasy battle scene, dynamic lighting",
    "size": "1024x768",
    "extra_body": {
      "image": [
        "https://example.com/character-1.png",
        "https://example.com/character-2.png"
      ],
      "response_format": "url"
    }
  }'
九、### 响应格式
1. URL输出
{
  "created": 1780000000,
  "data": [
    {
      "url": "https://storage.googleapis.com/agnes-aigc/xxx.png",

字段 类型 说明
created integer 请求创建时间戳
data array 生成图片结果列表
data[].url string/null 生成图片URL，Base64输出时通常为 null
data[].b64_json string/null Base64图片数据，URL输出时通常为 null
data[].revised_prompt string/null 修改后的提示，如无则为 null
类型 原价 当前### ### 价格
生成的图像 $0.003 / image $0 / image
      "b64_json": null,
      "revised_prompt": null
    }
  ]
}
2.Base64输出
{
  "created": 1780000000,
  "data": [
    {
      "url": null,
      "b64_json": "iVBORw0KGgoAAAANSUhEUgAA...",
      "revised_prompt": null
    }
  ]
}
十、### 响应字段说明
十一、### ### 价格

Agnes Image 2.0 Flash 支持以下能力：
文生图生成
图生图编辑
多图输入与合成
基于Prompt的图像转换
稳定的风格与结构控制
支持公网 URL 图片输入
支持Data URI Base64 图片输入
支持URL或Base64输出
面向生产工作流的快速生成
兼容 OpenAI Images API 的请求结构
为了获得更好的生成效果，建议在提示中提供清晰的屏幕指令，包括主体、场景、风格、灯光、结构图
和质量要求。
译文：
对于编辑任务，明确描述需要改变的内容，以及需要保持不变的内容。
十二、### 功能与兼容性
十三、### 最佳实践
1. 文生图提示编写建议

A professional product photo of a wireless headphone on a clean white background, soft studio l
2. 编辑图像提示编写建议

译文：
对于多图合成任务，建议描述不同输入图像之间的关系。
译文：
译文：
译文：

Change the background to a futuristic city at night while keeping the person’s face, outfit, an
3.多图合成提示编写建议

Place the person from the first image beside the robot from the second image in a cinematic sci-
### 十四、推荐提示结构
文生图提示结构

[Main subject] + [Scene / background] + [Style] + [Lighting] + [Composition] + [Quality requirem

A young explorer standing in an ancient temple, cinematic fantasy style, warm dramatic lighting,
图生图 提示结构

[Editing instruction] + [Elements to preserve] + [Target style / scene] + [Lighting] + [Composit

Change the background into a cinematic fantasy temple while preserving the person’s face, outf

支持。
文生图请求不需要命名 image，只需要命名 model、prompt 和 size。
支持。
图生图请求需要大量 image 库存。
不需要。
当前图生图请求只需要确定 model、prompt、size 和 image。
当前接口中，response_format 不宜放在请求中。
推荐放置：
如果输入图片URL无法被服务端访问，可能导致请求失败。
建议使用：
### 十五、常见问题
1. Agnes Image 2.0 Flash是否支持文生图？
2. Agnes Image 2.0 Flash是否支持图生图？
3.图生图是否需要 tags: ["img2img"] ？
4.为什么 response_format  放出会报错？
{
  "extra_body": {
    "response_format": "url"
  }
}
5.输入图片网址不可访问怎么办？

公网可访问的HTTPS图片地址
数据 URI Base64 输入
图片生成可能需要数秒到几十秒。
客户端设置建议超时时间，例如：
接入前建议确认：
已获得有效的API Key
请求地址为 https://apihub.agnes-ai.com/v1/images/generations
标题中已添加 Authorization: Bearer YOUR_API_KEY
标题中已添加 Content-Type: application/json
模型名称为 agnes-image-2.0-flash
文生图请求不传 image
图生图请求 image  架构
图生图请求需要传 tags: ["img2img"]
response_format  放在 extra_body  中
输入图片URL可被公网访问，或使用Data URI Base64
客户端超时时间建议设置为60s到360s
6.请求超时怎么办？
60s - 360s
### 十六、接入检查清单

---

Agnes Image 2.1 Flash 是Sapiens AI升级推出的图像生成模型，支持 文生图 和 图生图 两种工作流
程。
相比之前的版本，Agnes Image 2.1 Flash在 高信息密度 生成图像方面进行了优化，更适合复杂的视觉
细节、丰富的结构图、密集的元素和清晰的图像像素等场景。
Agnes Image 2.1 Flash可用于根据文本提示词生成图像，也可基于图片进行风格转换、局部优化、场
景落地或视觉增强，并支持以图片URL或Base64数据形式返回生成结果。
能力 说明
文生图 根据自然语言提示词生成高质量图片
图生图 根据提示词对现有图片进行转换、编辑或优化
高信息密度图像
优化 更好地处理复杂的布局、丰富的细节和密集的城市元素
结构保持 图生图时可尽量保持原图结构、主体结构和视角
灵活的尺寸控制支持自定义输出尺寸，例如 1024x768
网址返回 支持将生成结果以可访问图片URL返回
Base64返回 支持将以Base64数据返回生成结果
URL 或数据 URI 
输入 图生图支持公网图片URL 或 Data URI Base64 输入
Agnes Image 2.1 Flash
模型### 概述
核心能力

Agnes Image 2.1 Flash 适用于以下场景：
场景 示例用途
创意设计 概念图、视觉探索、海报草图
营销内容 活动图、产品、社交媒体视觉素材
高密度景观生成场景复杂、结构图丰富、密集元素画面
图片转换 风格迁移、场景重打、背景转换
内容制作 App素材、视觉、Banner、叙述视觉
产品外观 产品图、展示图、商业景观
社交媒体素材 封面图、横幅图、帖子配图
项目 说明
### API 端点 https://apihub.agnes-ai.com/v1/images/generations
请求方法 POST
内容类型 application/json
认证方式 Bearer Token
认证头 Authorization: Bearer YOUR_API_KEY
适用场景
接口信息
基本 URL
https://apihub.agnes-ai.com
接口地址

文生图和图生图均使用以下模型名称：
请使用 agnes-image-2.1-flash  作为模型名称。
文生图请求中，model 、prompt 、size  为必填参数。
图生图请求中，需要输入图片放在 `extra_body.image` 数组中。

**⚠️ 重要：image 参数必须放在 `extra_body` 中，不能放在请求体顶层！**

- ❌ 错误（顶层）：`"image": ["url"]` → 实际执行 text-to-image，image_tokens: 0
- ✅ 正确（extra_body）：`"extra_body": {"image": ["url"]}` → 实际执行 i2i-general

image 支持公网图片URL，也支持Data URI Base64。
不要将 response_format  请求体放在一起，否则可能返回 400 错误。
URL 写作，满足 "response_format": "url"  放在 extra_body  中。
有了文生图Base64输出，可使用大量参数 "return_base64": true 。
相当于图生图Base64输出，请在 extra_body  中设置 "response_format": "b64_json" 。
图生图不需要传 tags: ["img2img"] 。
公开文档中不要暴露临时API Key，请统一使用 YOUR_API_KEY 。
参数 类型 是否必填 说明
model string 是
模型名称，固定
用
途 agnes-image-
2.1-flash
prompt string 是 图片生成或图片
编辑提示词
模型名称
agnes-image-2.1-flash
重要说明
### 请求参数

size string 是 输出图片尺寸，
例如 1024x768
image string[] 图生图必填
输入图片数组，
支持公网 URL 
或 Data URI 
Base64
return_base64 boolean 否 文生图需要返回 
Base64 时使用
extra_body object 否 高级工作流扩展
参数
extra_body.response_format string 否
输出格式，常用
值为 url
 或 b64_json
用于根据文本提示词生成图片，并以图片URL形式返回结果。
生成图片网址位于：
调用示例
1. 文生图：URL输出
curl https://apihub.agnes-ai.com/v1/images/generations \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-image-2.1-flash",
    "prompt": "A luminous floating city above a misty canyon at sunrise, cinematic realism",
    "size": "1024x768",
    "extra_body": {
      "response_format": "url"
    }
  }'
data[0].url

用于将生成图片以Base64数据形式返回。
生成图片Base64 位于：
为了基于已有图像进行转换，并尽量保持原图结构。
生成图片网址位于：
2. 文生图：Base64输出

curl https://apihub.agnes-ai.com/v1/images/generations \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-image-2.1-flash",
    "prompt": "A clean product photo of a glass cube on a white studio background, soft shadows,
    "size": "1024x768",
    "return_base64": true
  }'
data[0].b64_json
3.图生图：URL输入，URL输出

curl https://apihub.agnes-ai.com/v1/images/generations \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-image-2.1-flash",
    "prompt": "Transform the scene into a rain-soaked cyberpunk night with neon reflections whi
    "size": "1024x768",
    "extra_body": {
     "image": [
      "https://example.com/input-image.png"
    ],
      "response_format": "url"
    }
  }'

用于输入图片为公网URL，输出结果为Base64数据的场景。
生成图片Base64 位于：
图生图也支持使用Data URI Base64作为输入图片。
数据URI格式：
请求示例：
data[0].url
4.图生图：URL输入，Base64输出
curl https://apihub.agnes-ai.com/v1/images/generations \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-image-2.1-flash",
    "prompt": "Make the object orange while preserving the original composition",
    "size": "1024x768"
    "extra_body": {
    "image": [
      "https://example.com/input-image.png"
    ],
      "response_format": "b64_json"
    }
  }'
data[0].b64_json
5. 图生图：Data URI Base64 输入
data:image/png;base64,BASE64_HERE
curl https://apihub.agnes-ai.com/v1/images/generations \
  -H "Authorization: Bearer YOUR_API_KEY" \

当 extra_body.response_format 设置 url 为时，### 返回格式如下：
生成图片网址：
当启用Base64输出时，### 返回格式如下：
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-image-2.1-flash",
    "prompt": "Make the object matte black while preserving the original composition",
    "size": "1024x768",
    "extra_body": {
     "image": [
      "data:image/png;base64,BASE64_HERE"
    ],
      "response_format": "b64_json"
    }
  }'
### 返回格式
URL 输出
{
  "created": 1780000000,
  "data": [
    {
      "url": "https://storage.googleapis.com/agnes-aigc/xxx.png",
      "b64_json": null,
      "revised_prompt": null
    }
  ]
}
data[0].url
#### Base64 输出

生成图片Base64：
为了获得更好的图像生成效果，建议使用语音的提示词结构：
对于图生图任务，需要明确说明“要改变什么”和“要保留什么”。
{
  "created": 1780000000,
  "data": [
    {
      "url": null,
      "b64_json": "iVBORw0KGgoAAAANSUhEUgAA...",
      "revised_prompt": null
    }
  ]
}
data[0].b64_json
### 推荐提示词结构
[主体] + [场景 / 环境] + [风格] + [光照] + [构图] + [质量要求]
效果

A luminous floating city above a misty canyon at sunrise, cinematic realism, wide-angle composit

Transform the scene into a rain-soaked cyberpunk night with neon reflections while preserving th
### 最佳实践
#### 文生图建议

生成复杂图片时，建议使用更具体的提示词，包含主体、环境、风格、灯光、镜头角度和细节要求。
更好的示例：
推荐包含以下要素：
主体
场景或环境
景观风格
嗡
镜头角度
构图
细节密度
质量要求
编辑现有图片时，建议同时说明转换要求和保留要求。
更好的示例：
推荐结构：
译文：

A futuristic city marketplace filled with flying vehicles, holographic signs, dense crowds, neon
#### 图生图建议

Convert the image into a fantasy winter landscape, add snow, warm window lights, and a magical a
[修改要求] + [新风格 / 新场景] + [需要添加或移除的元素] + [需要保留的元素]

Agnes Image 2.1 Flash 针对复杂、细节丰富的景观画面进行了优化。为了获得更好的结果，明确描述
了景观体系。
推荐包含：
主体
背景环境
重要次要元素
风格和音响
构图约束
图生图时需要保留的内容
更好的示例：
不要将 response_format 请求体放在一起。
错误示例：

Change the daytime street scene into a cinematic cyberpunk night scene, add neon signs and wet r
#### 高信息密度图像建议

A large fantasy harbor city built on cliffs, hundreds of small boats, layered stone bridges, glo
### 常见错误与排查
1. response_format  在此导致报错
{
  "model": "agnes-image-2.1-flash",
  "prompt": "A futuristic city",
  "size": "1024x768",

正确示例：
不要传：
图生图只需要在 image 阵列中提供输入图片。
正确示例：
  "response_format": "url"
}
{
  "model": "agnes-image-2.1-flash",
  "prompt": "A futuristic city",
  "size": "1024x768",
  "extra_body": {
    "response_format": "url"
  }
}
2.图生图不需要 tags
{
  "tags": ["img2img"]
}
{
  "model": "agnes-image-2.1-flash",
  "prompt": "Make the object blue while preserving the original composition",
  "size": "1024x768",
  "extra_body": {
    "image": [
      "https://example.com/input.png"
    ],
    "response_format": "url"
  }
}

如果输入图片URL无法被服务端访问，请求可能失败。
建议：
使用公网可访问的HTTPS图片地址。
确保图片 URL 不需要登录、Cookie 或笔记本标头。
如果图片无法公开访问，建议使用Data URI Base64 输入。
图片生成可能需要数秒到几十秒，具体取决于提示词复杂度、图片大小和服务负载。
建议客户端超时时间设置为：
图生图请求中，image 备份为必填。
错误示例：
正确示例：
3.输入图片URL不可访问
4.请求超时
60s 到 360s
5.图生图请求需要 image（必须放在 extra_body 中）

**⚠️ 重要：image 参数必须放在 `extra_body` 中，不能放在请求体顶层！**

```json
{
  "model": "agnes-image-2.1-flash",
  "prompt": "Make the image cyberpunk style while preserving the original composition",
  "size": "1024x768",
  "extra_body": {
    "image": [
      "https://example.com/input.png"
    ],
    "response_format": "url"
  }
}
```

类型 ### ### 价格
生成图片 0  $0.003  / 张
模型名称固定使用 agnes-image-2.1-flash 。
API端点使用 https://apihub.agnes-ai.com/v1/images/generations 。
文生图请求中，、、model 为prompt 必填size  。
图生图请求中，需要输入图片 URL 或 Data URI Base64 放在 `extra_body.image` 数组中。
需要图片URL输出时，使用 extra_body.response_format: "url" 。
文生图需要Base64输出时，使用 return_base64: true 。
图生图需要Base64输出时，使用 extra_body.response_format: "b64_json" 。
不要将 response_format  请求体放在一起。
不需要传 tags: ["img2img"] 。
公开文档中不要暴露临时 API Key，请使用 YOUR_API_KEY 。
    "https://example.com/input.png"
  ],
  "extra_body": {
    "response_format": "url"
  }
}
### ### 价格
### 备注

---

Agnes Video V2.0 是面向生产环境的视频生成模型，支持 文生视频、图生视频、多图视频生成 和 关
键帧动画 工作流。
开发者可以通过文本提示词、图片 URL 以及多张参考图片生成高质量视频。该模型适用于故事创作、营
销视频、产品演示、社交媒体内容、App 动态素材以及 AI 创意工作流。
Agnes Video V2.0采用异步任务式API。您需要先创建视频生成任务，然后使用返回的 video_id
 或 task_id 查询视频结果。
能力 说明
文生视频 根据文本提示词直接生成视频
图生视频 将静态图片动画化为动态视频
多图视频生成 使用多张参考图片指导视频生成
关键帧动画 在多个关键帧之间生成平滑过渡
场景运动控制 通过提示词控制主体动作、镜头运动和场景动态
视觉一致性 在多帧之间保持主体、风格和场景一致
电影级输出 生成高质量电影级视频
异步API 先提交任务，再查询生成结果
Agnes Video V2.0 API接入指南
### 概述
### 支持能力

场景 效果
故事创作 短片、角色场景、叙述片段
营销视频 产品广告、活动视频、推广内容
社交媒体内容 卷轴、短裤、TikTok 风格视频
图像动画化 动画化人像、产品、角色或场景
产品演示 根据文本或图像生成产品展示视频
关键帧过渡 在不同的视觉状态之间生成平滑转场
游戏 / App 素材为number产品生成动态素材
沉浸式内容 生成电影级AI场景和动态视频
开始接入前，请确保您已具备以下条件：
1. 已获得有效的Agnes AI API Key。
2. 当前网络环境可以访问Agnes AI API Gateway。
3. 已确认模型名称：agnes-video-v2.0 。
4. 已准备好视频生成所需的文本提示词。
5. 若使用图生视频、多图视频或关键帧动画，请准备好可公网访问的图片URL。
项目 说明
端点 https://apihub.agnes-ai.com/v1/videos
适用场景
准备工作
### API 端点
### 创建视频任务

方法 POST
内容类型 application/json
验证 Bearer Token
标题 Authorization: Bearer YOUR_API_KEY
### 创建视频任务后，响应中会返回 video_id。
使用推荐 video_id 查询视频结果。
项目 说明
端点 https://apihub.agnes-ai.com/agnesapi?video_id=<VIDEO_ID>
方法 GET
验证 Bearer Token
标题 Authorization: Bearer YOUR_API_KEY
旧版本任务查询接口仍然支持，用于兼容现有接入逻辑。
项目 说明
端点 https://apihub.agnes-ai.com/v1/videos/{task_id}
方法 GET
验证 Bearer Token
标题 Authorization: Bearer YOUR_API_KEY
### 查询视频结果：推荐方式
### 查询视频结果：兼容旧方式
### 请求参数
### 创建视频任务参数

参数 类型 是否必填 说明
model string 是
模型名称、用
途 agnes-video-
v2.0
prompt string 是 视频内容的文本
描述
image string/array 否 图片URL 或图片
URL 存储
mode string 否
生成模式，例
如 ti2vid
 或 keyframes
height integer 否 视频高度，默认
值 768
width integer 否 视频宽度，默认
值 1152
num_frames integer 否
视频帧数，必
须 ≤ 441 ，且
满足 8n + 1
frame_rate number 否 视频FPS，支持
范围为 1–60
num_inference_steps integer 否 推理步数
seed integer 否 随机种子，为保
证结果可恢复
negative_prompt string 否
负向提示词，用
于描述需要避免
的内容
extra_body.image array 否
多图视频或关键
帧模式中的输入
图片URL
extra_body.mode string 否 额外模式设置，
例如 keyframes

用于直接根据文本提示词生成视频。
用于将单张图片动画化。
用于通过多张输入图片指导视频生成。
### 创建视频任务
示例 1：文生视频

curl -X POST https://apihub.agnes-ai.com/v1/videos \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-video-v2.0",
    "prompt": "A cinematic shot of a cat walking on the beach at sunset, soft ocean waves, warm 
    "height": 768,
    "width": 1152,
    "num_frames": 121,
    "frame_rate": 24
  }'
示例2：图生视频

curl -X POST https://apihub.agnes-ai.com/v1/videos \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-video-v2.0",
    "prompt": "The woman slowly turns around and looks back at the camera, natural facial expre
    "image": "https://example.com/image.png",
    "num_frames": 121,
    "frame_rate": 24
  }'
示例3：多图视频生成

用于在多个关键帧之间生成平滑动画。

curl -X POST https://apihub.agnes-ai.com/v1/videos \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-video-v2.0",
    "prompt": "Create a smooth transformation scene between the two reference images, cinematic 
    "extra_body": {
      "image": [
        "https://example.com/image1.png",
        "https://example.com/image2.png"
      ]
    },
    "num_frames": 121,
    "frame_rate": 24
  }'
示例 4：关键帧动画

curl -X POST https://apihub.agnes-ai.com/v1/videos \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agnes-video-v2.0",
    "prompt": "Generate a smooth cinematic transition between the keyframes, maintaining visual 
    "extra_body": {
      "image": [
        "https://example.com/keyframe1.png",
        "https://example.com/keyframe2.png"
      ],
      "mode": "keyframes"
    },
    "num_frames": 121,
    "frame_rate": 24
  }'

视频任务创建成功后，API 会返回任务信息。
响应中会同时包含 task_id 和 video_id。
其中，video_id 是推荐用于查询视频结果的ID。
字段 类型 说明
id string 任务ID，可用于旧版本查询接口
task_id string 任务ID，作用 id  相同
video_id string 视频ID，推荐用于查询视频结果
object string 对象类型，通常为 video
model string 当前任务使用的模型
status string 当前任务状态
progress integer 当前任务进度
created_at integer 任务创建时间戳
seconds string 视频时长（秒）
size string 视频分辨率
### 创建任务响应
{
  "id": "task_YOUR_TASK_ID",
  "task_id": "task_YOUR_TASK_ID",
  "video_id": "video_YOUR_VIDEO_ID",
  "object": "video",
  "model": "agnes-video-v2.0",
  "status": "queued",
  "progress": 0,
  "created_at": 1780457477,
  "seconds": "10.0",
  "size": "1280x768"
}
### 响应字段说明

### 创建视频任务后，使用返回的 video_id 查询视频结果。建议轮询间隔5s。
译文：
查询视频结果时，也可以确定 model_name 显式模型指定名。
译文：
 
为了兼容旧版本，仍然可以使用 task_id 查询视频结果。
查询视频结果
推荐方式：使用 video_id  查询
curl --location --request GET 'https://apihub.agnes-ai.com/agnesapi?video_id=<VIDEO_ID>' \
  --header 'Authorization: Bearer <API_KEY>'
curl --location --request GET 'https://apihub.agnes-ai.com/agnesapi?video_id=video_xxxxxx' \
  --header 'Authorization: Bearer <API_KEY>'
可选参数：model_name

curl --location --request GET 'https://apihub.agnes-ai.com/agnesapi?video_id=<VIDEO_ID>&model_na
  --header 'Authorization: Bearer <API_KEY>'

curl --location --request GET 'https://apihub.agnes-ai.com/agnesapi?video_id=video_xxxxxx&model_
  --header 'Authorization: Bearer <API_KEY>'
兼容方式：使用 task_id  查询
curl --location --request GET 'https://apihub.agnes-ai.com/v1/videos/<TASK_ID>' \
  --header 'Authorization: Bearer <API_KEY>'

译文：
该方式仍然支持，但新的接入建议使用 video_id 查询方式。
当任务完成后，API会返回最终视频结果。
字段 类型 说明
id string 任务编号
video_id string 视频ID
model string 当前任务使用的模型
object string 对象类型
status string 任务状态
progress integer 任务进度
curl --location --request GET 'https://apihub.agnes-ai.com/v1/videos/task_xxxxxx' \
  --header 'Authorization: Bearer <API_KEY>'
查询结果响应

{
  "id": "task_YOUR_TASK_ID",
  "video_id": "video_YOUR_VIDEO_ID",
  "model": "agnes-video-v2.0",
  "object": "video",
  "status": "completed",
  "progress": 100,
  "seconds": "10.0",
  "size": "1280x768",
  "remixed_from_video_id": "https://storage.googleapis.com/agnes-aigc/aigc/videos/2026/06/03/vid
  "error": null
}
结果字段说明

seconds string 视频时长（秒）
size string 视频分辨率
remixed_from_video_id string 本字段为最终生成的视频URL，仅在 status  为时 completed
 可用
error object/null 错误信息，任务失败时返回
状态 说明
queued 任务正在队列中等待
in_progress 视频正在生成中
completed 视频已生成完成
failed 视频生成失败
Agnes Video V2.0 支持通过 num_frames 和 frame_rate 控制视频时长。
计算公式：
其中：
num_frames  表示生成的视频总帧数；
frame_rate  表示视频帧率，即每秒播放多少帧；
num_frames  必须小于或等于 441 ；
num_frames  必须满足 8n + 1 ；
frame_rate  支持范围为 1–60 。
### 任务状态说明
### 视频时长控制
seconds = num_frames / frame_rate

目标时长 ### 参数推荐
约3秒 num_frames: 81 ， frame_rate: 24
约5秒 num_frames: 121 ， frame_rate: 24
约10秒 num_frames: 241 ， frame_rate: 24
约18秒 num_frames: 441 ， frame_rate: 24
如果希望生成更长的视频，可以增加 num_frames 或减少 frame_rate。
如果希望画面更流畅，可以使用更高的 frame_rate，例如 24 或 30。但在相同的 num_frames 下，
frame_rate 如图，视频时长越短。
使用场景 推荐设置
标准视频生成 width: 1152 ，，， height: 768   num_frames: 121   frame_rate: 24
短视频社交内容num_frames: 81  或 121 , frame_rate: 24
更长的视频 增加 num_frames  或减少 frame_rate
更平滑的运动 使用 frame_rate: 24  或 30
可复现结果 固定 seed
关键帧过渡 使用 extra_body.mode: "keyframes"
避免不需要的内
容 使用 negative_prompt
文生视频任务建议描述主体、动作、环境、镜头运动、灯光和风格。
### 常用时长参数
### 参数推荐
提示### 最佳实践
#### 文生视频提示

推荐结构：
译文：
图生视频任务建议描述哪些内容需要运动，同时说明哪些主体元素需要保持稳定。
译文：
多图视频任务建议描述输入图片之间的关系，以及画面如何过渡。
译文：
关键帧动画任务提示清晰描述关键帧之间的过渡关系。
译文：
[主体] + [动作] + [场景] + [镜头运动] + [光照] + [风格]

A young astronaut walking across a red desert planet, dust blowing in the wind, slow cinematic t
#### 图生视频提示

Animate the character with subtle breathing motion, hair moving gently in the wind, background 
#### 多图视频提示

Use the first image as the starting scene and the second image as the target scene. Create a smo
#### 关键帧动画提示

Create a smooth transition from the first keyframe to the second keyframe, maintaining character

状态码 说明
400 请求无效，请检查### 请求参数
401 未授权，请检查 API Key
404 任务或视频不存在
500 服务器错误
503 服务繁忙，请稍后重试
类型 标准### ### 价格 当前### ### 价格
视频时长 $0.005 / 
second $0 / second
使用 agnes-video-v2.0  作为模型名称；
视频生成是异步任务；
需要先### 创建视频任务，再查询视频结果；
### 创建任务响应中会同时返回 task_id  和 video_id ；
新接入点使用建议 video_id  查询视频结果；
旧版本 task_id  查询接口仍然支持；
video_url  仅在 status  为时 completed  可用；
num_frames  必须小于或等于 441 ；
num_frames  必须满足 8n + 1 ，例如 81 、121 、161 、241  或 441 ；
### 错误码
### ### 价格
### 注意事项

文生视频任务仅要求确定 model  和 prompt ；
图生视频任务需要通过 image  提供图片URL；
多图视频任务中需要 extra_body.image  提供多个图片URL；
关键帧动画需要设置 extra_body.mode  为 keyframes 。

---

生效日期：[2026年4月1日]
本隐私政策（“政策”）详细解释了Sapiens AI（“Agnes AI”、“我们”、“我们”或“我们的”）在您访问或
使用我们的平台、应用程序编程接口（API）、人工智能（AI）模型、软件应用程序和相关服务（统称
为“服务”）时如何收集、使用、存储、传输和保护您的个人和非个人信息。本政策还### 概述了您对您的信
息的权利以及您如何获得这些权利。
通过以任何方式访问、浏览或使用本服务（包括但不限于注册帐户、提交数据或使用我们的人工智能工
具），您承认您已阅读、理解并同意本隐私政策的条款。如果您不同意政策本，请不要使用本服务。
本政策适用于访问或使用服务的所有个人和实体（包括用户、开发者、客户和访客），以及 Agnes AI 
收集的与此类访问或使用相关的所有信息。具体来说，本政策主题：
Agnes AI官方平台及网站（包括所有子域名及相关网页）；
Agnes AI 提供所有API、软件开发套件（SDK）和开发人员工具；
Agnes AI 开发、拥有或运营的所有应用程序、插件和服务（无论是通过网络、移动设备还是
其他设备访问）；
您与 Agnes AI 之间的所有通信（包括但不限于支持请求、反馈、电子邮件和应用内消息）；
您或代表您在使用服务时提交的任何数据（包括客户数据和用户生成的内容）。
本政策不适用于：
与本服务集成或链接的第三方服务、产品或平台（包括但不限于第三方支付处理商、云存储和
社交媒体登录服务）；您对此类第三方服务的使用受其各自隐私政策的约束，而不是本政策；
链接到服务或从服务链接的外部网站、平台或应用程序；我们确定此类外部网站的隐私内容或
负责；
Agnes AI 隐私政策
## 1. 本政策的范围

第三方收集的信息，独立于其与服务的集成；
无法识别您或任何个人身份的匿名或汇总数据。
个人信息：可单独或与其他信息结合使用来识别、联系或定位特定个人的任何信息。这包括但
不限于全名、电子邮件地址、电话号码、公司名称、职位、邮政地址和唯一标识符（例如用户 
ID）。
敏感个人信息：个人信息的子集，由于其倾向而受到更严格的法律保护。这包括但不限于财务
信息（如信用卡号）、健康信息、生物识别数据、种族或民族、宗教信仰、政治观点以及与怠
人相关的数据。
客户数据：您、您的用户或您的组织在使用服务时提交的所有数据、内容和信息，包括但不限
于提示、输入、文件、文档、图像、文本以及通过服务上传或传输的任何其他内容。
使用数据：您使用服务时自动收集的非个人或假名数据，包括但不限于API调用日志、交互记
录、会话数据、设备信息以及与您使用服务相关的指标。
数据匿名：经过处理后，无论是单独还是与其他数据结合，都无法重新识别个人身份，并且无
法合理地重新识别个人身份。
聚合数据：与用户其他的数据相结合并以无法识别任何个人用户的方式聚合的数据。
Cookie：当您访问服务时存储在您的设备（计算机、手机、平板电脑）上的小文本文件，有
助于我们识别您的设备并记住有关您使用服务的某些信息。
我们主要通过清晰的方式向您收集信息：您自愿提供的信息、您使用服务时自动收集的信息以及从第三
方收集的信息。我们仅收集提供、改进和保护服务所需的信息。
您在使用服务时可以选择向我们提供某些信息。这包括：
账户信息：当您在 Agnes AI 注册账户时，系统会要求您提供个人和/或商业信息，例如您的
全名、电子邮件地址、公司名称、职位和密码。该信息用于创建和管理您的账户、验证您的身
份以及与您的沟通。
## 2. 定义
## 3. 我们收集的信息
### 3.1 您提供的信息
/ /

您的付款和付款详细信息：如果订阅付费计划或从 Agnes AI 购买任何服务，您将需要提供付
款信息（例如发票号、付款地址）。我们不会直接存储您的完整付款详细信息；相反，这些信
息由我们的第三方支付处理商（例如 Stripe、PayPal）根据其隐私政策和行业标准进行处理和
存储。
通讯：当您我们的支持团队（通过电子邮件联系、应用内聊天或其他渠道）、提供反馈或参与
调查时，我们可能会收集您的通讯内容以及您的联系信息，以回应您的请求、解决您的疑虑并
改进并服务。
您提交的内容：您在使用服务时提交的任何内容，包括但不限于提示、输入、文件（例如文
档、图像、音频）和其他用户生成的内容。该内容用于提供您请求的 AI 功能（例如，生成响
应、分析数据），并可用于改进我们的 AI 模型（除非您在适用的情况下选择退出）。
可选信息：您还可以选择提供其他信息（例如个人资料图片、偏好设置）以增强您对服务的使
用。此信息为可选的，您可以选择保留它，而不会影响您使用服务核心功能的能力。
当您访问或使用服务时，我们会自动收集某些使用数据和设备信息，以确保服务正常运行、改进我们的
产品并增强您的用户体验。这包括：
设备信息：有关您用于访问服务的设备的信息，例如您的设备类型（例如计算机、手机）、操
作系统版本、浏览设备类型和版本、IP地址、MAC地址和设备标识符。这些信息有助于我们针
对不同的设备优化服务并解决技术问题。
使用数据：您与服务交互的日志，包括但不限于 API 调用（例如，调用次数、调用时间、响应
时间）、会话持续时间、访问的页面、使用的功能和采取的操作（例如，提交提示、下载文
件）。该用于数据分析使用模式、确定需要改进的领域并确保服务运行。
Cookie 和跟踪技术：我们使用 Cookie 和类似的跟踪技术（例如网络信标、像素标签、本地
返回存储）来收集有关您使用服务的信息。当您使用服务时，Cookie 帮助我们识别您的设
备、记住您的偏好（例如语言设置）并跟踪您与服务的交互。您可以通过浏览器设置禁用 
cookie，但请注意，如果禁用 cookie，服务的某些功能可能无法正常运行。
如果您选择使用第三方帐户（例如 Google、Apple）登录服务，我们可能会根据该第三方企业的隐私政
策和您从第三方企业处接收的权限接收某些信息。这通常包括：
您与第三方帐户关联的电子邮件地址；
第三方账户中显示您的全名；
### 3.2 自动收集信息
### 3.3 第三方数据
/ /

第三方首先提供唯一标识符（用于将您的第三方帐户链接到您的 Agnes AI 帐户）；
如果您授予，则其他有限信息（例如个人资料图片）。
除了验证您的帐户和提供服务所需的信息之外，我们不会从第三方收集任何其他信息。在您明确同意的
情况下，我们不会出于本政策所述目的以外的任何目的访问或使用您的第三方帐户数据。
我们仅将收集的信息用于合法商业目的，并遵守适用的法律和法规。您的信息的具体用途如下：
我们使用您的信息来运营、维护和提供服务的核心功能，包括：
创建和管理您的账户，包括验证您的身份并确保账户安全；
提供人工智能功能（例如，根据您的提示生成响应、分析您提交的内容、处理您的请求）；
处理付费计划或服务付款，包括开具发票、商品和预防欺诈；
提供与服务相关的通信（例如账户更新、服务公告、密码重置说明）；
提供客户支持并回复您的询问、反馈或反馈。
我们使用您的信息来保护服务、您的账户和我们的用户进行安全威胁、诈骗和诈骗，包括：
检测和预防欺诈活动（例如未经授权的账户访问、支付欺诈）；
识别并解决破坏服务问题（例如垃圾邮件、有害内容、违反我们的服务条款）；
监控服务是否存在安全漏洞、恶意软件和其他威胁；
实施安全措施来保护您的信息（例如加密、访问控制）；
调查安全事件并采取适当的行动来降低风险。
我们使用您的信息来改进服务、开发新功能并优化用户体验，包括：
4.我们如何使用您的信息
4.1 服务操作
4.2 安全性和缺陷
4.3 改进与分析
/ /

分析使用模式以确定需要改进的领域（例如，提高人工智能响应准确性、改进用户界面）；
使用匿名或聚合的用户输入和输出来训练和改进我们的人工智能模型（除非您在适用的情况下
选择退出）；
根据用户需求和反馈开发新功能、工具和服务；
进行内部研究和分析，以更好地了解用户如何与服务互动；
测试和优化服务的性能、可靠性和速度。
我们根据法律、法律程序或监管义务的要求使用和披露您的信息，包括：
执行我们的服务条款、隐私政策和其他适用政策；
响应政府当局、执法机构或其他第三方的法律请求（例如传票、法院命令、搜查令）；
遵守适用的法律和法规（例如数据保护法、税法、反欺诈法）；
保护我们的合法权益和资产，以及我们的用户和公众的权益和安全。
作为一项人工智能驱动的服务，Agnes AI 依靠用户的输入和输出来提高人工智能模型的准确性、功能和
性能。关于人工智能数据使用，请注意以下要点：
您提交的任何输入（例如提示、文件、文本）和服务生成的输出（例如 AI 响应、分析）可能
会被处理、存储并用于训练和改进我们的 AI 模型，除非您选择退出此类使用（在提供退出功
能的情况下）。
当使用用户数据进行模型改进时，我们将采取措施对数据进行匿名化或聚合，以确保其无法链
接到您或任何个人用户。这可能包括删除个人标识符、扰乱数据或将其与其他用户的数据相结
合。
您不得向服务提交任何敏感个人信息（例如健康数据、财务数据、生物识别数据）或机密信息
（例如商业秘密、专有信息），除非您已获得明确授权并已采取适当措施保护此类信息。
您全权负责：(a) 确保您向服务提交的任何数据合法、准确且符合适用的法律和法规； (b) 获
得您向服务提交数据的第三方（例如您的用户）的任何必要同意； (c) 确保您对服务的使用和
您提交的数据不侵犯任何第三方权利（例如版权、隐私权）。
4.4 法律合规性
5. AI数据使用（重要）
/ /

如果您希望选择不将您的输入和输出用于 AI 模型改进（如果有），请通过 
[support@yourdomain.com] 与我们联系，并提供您的帐户详细信息和选择退出请求。
我们使用 cookie 和类似的跟踪技术来增强您的用户体验、改进服务并确保安全。以下是我们使用的 
cookie 类型及其用途的详细说明：
基本 Cookie：这些 Cookie 是服务正常运行所必需的。它们支持帐户身份验证、会话管理和
访问服务安全区域等核心功能。您无法在不影响您使用服务的能力的情况下禁用这些 
cookie。
性能 Cookie：这些 Cookie 收集有关您如何使用服务的信息（例如，您访问了哪些页面、您
在每个页面上花费的时间、您遇到的任何错误）。这些数据用于提高服务的性能和可靠性，以
及识别和解决技术问题。
功能 Cookie：这些 Cookie 会记住您的偏好和设置（例如语言、区域、主题），以提供更加
个性化的用户体验。它们还可以用于记住您的登录状态，这样您就不必每次访问服务时都登
录。
分析 Cookie：这些 Cookie 用于分析用户行为和使用模式，以帮助我们了解服务的使用方式
并确定需要改进的领域。我们可能会使用使用这些 cookie 的第三方分析工具（例如 Google 
Analytics）来收集和处理这些数据。
您可以通过浏览器设置来控制和管理 cookie。大多数浏览器允许您查看、删除或阻止 cookie。但请注
意，禁用某些 cookie 可能会影响服务的功能。有关如何管理 cookie 的更多信息，请参阅浏览器的帮助
文档。
我们不会使用 cookie 进行定向广告或为第三方广告目的收集信息。
Agnes AI 认真对待您的隐私，在任何情况下都不会将您的个人信息出售给任何第三方。我们可能会与以
下类型的第三方共享您的信息，但仅限于下述目的并遵守适用法律：
6. Cookie 和跟踪技术
6.1 Cookie 类型
6.2 管理 Cookie
7. 信息共享
/ /

我们可能会与帮助我们运营、维护和改进服务的第三方服务提供商共享您的信息。这些服务提供商有合
同义务保护您的信息，并且仅将其用于执行我们要求的服务。示例包括：
支付处理商（例如 Stripe、PayPal）处理支付和管理账单；
云存储提供商（例如 AWS、Google Cloud）安全地存储您的数据；
分析服务，帮助我们分析使用数据并改进服务；
客户支持工具可帮助我们回复您的询问和反馈；
安全提供商帮助检测和防止欺诈和安全威胁。
如果我们有关联公司（例如母公司、子公司、姊妹公司），我们可能会出于运营目的与他们共享您的信
息，例如提供服务、改进我们的产品或遵守法律义务。我们的附属公司必须遵守本隐私政策并保护您的
信息。
如果法律、法律程序或监管义务要求，我们可能会向政府当局、执法机构或其他第三方披露您的信息。
这包括回应传票、法院命令、搜查令或其他法律请求，以及配合调查或执法行动。
如果发生业务转让（例如合并、收购、资产出售、破产），您的信息可能会作为交易的一部分转移给收
购方或继承实体。我们将提前通知您任何此类转让（如果法律要求），并确保收购实体遵守本隐私政
策。
只有在获得您明确同意的情况下，我们才可能出于其他目的与第三方共享您的信息。您可以随时通过 
[support@yourdomain.com] 联系我们撤回您的同意。
您的信息可能会被处理、存储并传输到您居住国以外的国家/地区，包括但不限于新加坡、美国以及我们
或我们的服务提供商运营的其他司法管辖区。我们确保所有跨境数据传输均遵守适用的数据保护法律和
7.1 服务提供商
7.2 附属公司
7.3 法律权限
7.4 业务转让
7.5 基于同意的共享
8. 数据传输
/ /

法规，并实施适当的保护措施以在传输和存储过程中保护您的信息。
我们用于跨境数据传输的保障措施包括：
欧盟委员会批准的标准合同条款 (SCC)（适用于传输至欧洲经济区/英国以外的国家/地区）；
与我们的服务提供商签订的数据保护协议 (DPA)，其中包括符合适用法律的隐私保护；
遵守欧盟-美国标准数据隐私框架 (DPF) 和其他适用框架（如适用）；
确保我们在其他司法管辖区的服务提供商维持足够的数据保护标准。
如果您位于欧洲经济区、英国或其他具有严格跨境数据传输要求的司法管辖区，您可以通过 
[support@yourdomain.com] 与我们联系，索取 SCC 或我们使用的其他保护措施的副本。
Agnes AI 致力于保护您的信息免遭未经授权的访问、使用、披露、更改或破坏。我们实施行业标准的安
全措施来确保您的数据安全，包括：
加密：我们使用 HTTPS 和 SSL/TLS 加密来保护您的设备和我们的服务器之间传输的数据。我
们还使用强大的加密算法对静态敏感数据（例如个人信息、客户数据）进行加密。
访问控制：我们实施严格的访问控制，以确保只有授权人员才能访问您的信息。访问权限是在
“需要知道”的基础上授予的，我们会定期审查和更新访问权限。
监控系统：我们使用先进的监控系统来检测和响应安全威胁、异常活动和潜在违规行为。我们
定期审核我们的系统和流程，以识别和修复安全漏洞。
员工培训：我们的员工定期接受有关数据保护、隐私和安全### 最佳实践的培训，以确保他们了解
自己的责任并遵守适用的法律。
定期安全审计：我们定期进行安全审计和渗透测试，以评估我们安全措施的有效性并确定需要
改进的领域。
虽然我们采取一切合理措施来保护您的信息，但没有任何系统或安全措施是 100% 安全的。我们无法保
证您的信息的绝对安全，并且您承认，尽管我们尽了最大努力，但仍存在未经授权访问您的信息的风
险。如果我们发现影响您个人信息的数据泄露，我们将根据适用法律通知您和相关当局。
## 9. 数据安全
10. 数据保留
/ /

我们仅在实现收集信息的目的所必需的期限内或根据法律要求保留您的信息。每种类型信息的保留期限
根据以下因素确定：
收集信息的目的（例如，只要您的帐户处于活动状态，帐户信息就会被保留）；
法律和监管要求（例如，我们可能出于税务或审计目的保留财务记录）；
业务需求（例如，保留使用数据以改进服务）；
解决争议、执行我们的条款或保护我们的合法权利的需要。
保留期到期后，我们将采取合理措施删除您的信息或对其进行匿名化处理，使其无法再用于识别您的身
份。例如：
帐户信息：只要您的帐户处于活动状态，就会保留。如果您删除帐户，我们将在合理的时间内
删除您的帐户信息，法律要求我们保留的信息除外。
客户数据：根据向您提供服务所需的时间或根据您的要求保留。您可以随时联系我们请求删除
您的客户数据。
使用数据：保留一段合理的时间（例如 12-24 个月），以分析使用模式并改进服务，之后将
其匿名或删除。
付款信息：仅在处理付款以及遵守税务和法律要求所需的时间内保留，此后将被删除（或根据
法律要求以加密形式存储）。
根据您所居住的国家或地区，根据适用的数据保护法（例如，欧洲经济区/英国的 GDPR、加利福尼亚州
的 CCPA、新加坡的 PDPA），您可能拥有与您的信息相关的某些权利。这些权利可能包括：
访问权：您有权请求访问我们持有的有关您的个人信息，包括有关我们如何收集、使用和共享
您的信息的详细信息。
更正权：您有权要求我们更正我们持有的有关您的任何不准确或不完整的个人信息。
删除权：您有权要求我们删除您的个人信息，但有某些例外情况（例如，如果法律要求我们保
留信息）。
数据可移植性权利：您有权索取结构化、机器可读格式的个人信息副本，以便您可以将其传输
给其他服务提供商（如适用）。
11. 您的权利
/ /

反对处理的权利：您有权反对出于某些目的（例如，直接营销、模型改进）处理您的个人信
息，并且我们将停止处理您的信息，除非我们有令人信服的合法理由继续处理。
撤回同意的权利：如果我们根据您的同意处理您的信息，您有权随时撤回您的同意。撤回同意
不会影响撤回前基于同意进行的处理的合法性。
要行使任何这些权利，请通过电子邮件 [support@yourdomain.com] 向我们提交请求。我们可能会要
求您提供身份证明以验证您的请求（以确保您的信息不会透露给未经授权的个人）。我们将在适用法律
要求的期限内回复您的请求（例如，CCPA 规定为 30 天，GDPR 规定为 45 天）。
如果您对我们对您请求的答复不满意，您可能有权向您所在司法管辖区的数据保护机构提出投诉。
本服务不适合 16 岁以下的个人（“儿童”）使用。我们不会故意收集、使用或披露儿童的个人信息。如果
我们发现我们在未经父母或法定监护人同意的情况下收集了儿童的个人信息，我们将立即采取措施删除
该信息并终止该儿童的帐户。
如果您是父母或法定监护人，并认为您的孩子已向我们提供了个人信息，请通过 
[support@yourdomain.com] 与我们联系，并提供您孩子的姓名和任何相关详细信息，我们将采取适
当的行动。
服务可能包含第三方服务、产品或平台（例如第三方 API、社交媒体网站、支付处理器）的链接。当您
使用这些第三方服务时，您将直接向第三方提供信息，他们的隐私政策将管辖您信息的收集、使用和披
露。
Agnes AI 对任何第三方服务的隐私惯例、内容或安全性不承担任何责任。我们鼓励您在向您使用的任何
第三方服务提供您的信息之前查看其隐私政策。
您提交到服务公共区域（例如公共论坛、共享工作区或可公开访问的人工智能输出）的任何内容可能对
服务的其他用户或公众可见。该内容可能会被第三方重复使用、共享或索引，我们无法控制其他用户或
第三方如何使用此类内容。
您应避免向服务的公共区域上传或提交任何敏感个人信息、机密信息或其他敏感内容。 Agnes AI 对因
您提交公共内容而造成的任何损失或损害不承担任何责任。
12. 儿童隐私
13. 第三方服务
14. 公共内容警告
/ /

我们可能会不时更新本隐私政策，以反映我们的做法、适用法律或服务的变化。当我们更新政策时，我
们将修改本页顶部的“生效日期”。
次要更新（例如澄清、技术变更）将在服务上发布后生效。重大更新（例如，我们收集或使用您的信息
的方式发生变更）将提前通知您（例如，通过电子邮件、应用内通知或服务上的显着通知），以便您有
机会查看这些变更。
您在更新的政策生效后继续使用服务即表示您接受更新的条款。如果您不同意更新后的政策，请停止使
用本服务。
如果您对本隐私政策、您的信息或我们的隐私惯例有任何问题、疑虑或请求，请通过以下方式与我们联
系：
公司：Sapiens AI
电子邮件：[support@agnes-ai.com]
我们将尽快回复您的询问，通常在 5-10 个工作日内。
本节根据当地数据保护法规定了适用于位于特定司法管辖区的用户的附加条款。
对于位于欧洲经济区 (EEA)、英国 (UK) 或瑞士的用户，您的个人信息的处理受通用数据保护条例 
(GDPR) 和适用的国家法律管辖。处理您的个人信息的法律依据如下：
合同履行：处理对于履行您与 Agnes AI 之间的合同是必要的（例如，提供服务、处理付
款）。
合法利益：为了我们的合法商业利益，处理是必要的，前提是此类利益不会凌驾于您的隐私权
之上。合法利益包括改进服务、确保安全和防止欺诈。
同意：处理基于您的明确同意（例如，使用您的数据改进 AI 模型、与第三方共享您的信
息）。
15. 本政策的更新
16. 联系我们
17. 司法管辖区特定规定
17.1 欧洲经济区/英国/瑞士 (GDPR)
/ /

法律义务：为了履行我们的法律义务（例如，响应法律要求、维护财务记录），必须进行处
理。
除了第 11 条中### 概述的权利外，您还有权： (a) 请求限制处理您的个人信息； (b) 向您所在司法管辖区的
数据保护机构提出投诉； (c) 接收有关跨境数据传输保障措施的信息。
对于位于美国加利福尼亚州的用户，您的个人信息的处理受加利福尼亚州消费者隐私法 (CCPA) 和加利
福尼亚州隐私权法 (CPRA) 的管辖。 CCPA/CPRA 赋予您的权利包括：
访问权：您有权请求访问我们在过去 12 个月中收集的有关您的个人信息的类别和特定部分。
删除权：您有权要求删除您的个人信息，但有某些例外情况（例如，如果我们需要保留信息以
提供服务）。
不受歧视的权利：我们不会因您行使 CCPA/CPRA 规定的权利而歧视您（例如，向您收取更高
的费用、提供较低质量的服务）。
我们不会将您的个人信息泄露给任何第三方，除非您明确同意，我们也不会因有价值的而披露您的个人
信息。您可以通过 [support@yourdomain.com] 联系我们，提交无偿 CCPA/CPRA 权利的请求。我们
将使用备案的信息验证您的请求，请在收到您的请求后 45 天回复（如有必要，可能会延长 45 天）。
对于位于新加坡的用户，您的个人信息的处理受《个人数据保护法》(PDPA) 的管辖。适用于我们服务的 
PDPA 的主要条款包括：
同意：我们仅在您同意的情况下收集和使用您的个人信息（除非 PDPA 规定有例外情况）。
撤回同意：您可以随时撤回对处理您的个人信息的同意，我们将采取合理措施来满足您的请
求。
数据传输保护：我们确保您的个人信息的跨境传输符合PDPA，包括使用适当的保护措施（例
如DPA、SCC）。
安全措施：我们实施合理的安全措施来保护您的个人信息免遭未经授权的访问、使用或披露。
您有权要求访问和更正您的个人信息，如果您对我们对您的请求不满意，您有权向个人数据保护委员会 
(PDPC) 提出投诉。
17.2 加利福尼亚州 (CCPA/CPRA)
17.3 新加坡（PDPA）
17.4 加拿大/澳大利亚/马来西亚
/ /

对于位于加拿大、澳大利亚或马来西亚的用户，您的个人信息的处理受当地数据保护法管辖，包括：
加拿大：个人信息保护和电子文件法 (PIPEDA)。您有权访问和更正您的个人信息，只有在确
保接收方提供充分保护的情况下，我们才可能跨境传输您的信息。
澳大利亚：《1988年隐私法》。您有权访问和更正您的个人信息，如果您认为您的隐私权受
到侵犯，您有权向澳大利亚信息专员办公室（OAIC）提出投诉。
马来西亚：2010 年个人数据保护法 (PDPA)。您有权访问和更正您的个人信息，我们在收集、
使用或披露您的信息之前必须征得您的同意（除非适用的例外情况）。
Agnes AI 根据算法、机器学习模型和用户输入提供人工智能生成的内容和功能。请注意以下重要免责声
明：
人工智能生成的内容可能不准确、不完整、存在偏见或具有不正确性。它不能替代专业建议
（例如法律、医疗、财务建议）。
您不必依赖人工智能生成的内容来做出任何关键决策。在使用任何人工智能生成的内容之前，
您全权负责验证其准确性、局限性和适当性。
Agnes AI 不保证人工智能模型生成的内容的准确性、可靠性或适用性。对于因使用人工智能
生成的内容而造成的任何损失或损害，我们不承担任何责任。
您有责任确保您使用的任何人工智能生成的内容均符合适用的法律、法规和第三方权利（例如
版权法、商标法）。
本隐私政策构成我们的服务条款的一部分。使用服务即表示您同意本政策和我们的服务条款。
如果根据适用法律发现本政策的任何条款无效或无法执行，则其余条款仍将具有完全效力。
我们可能会因业务转让并将本政策项下的权利和义务转让给第三方，但我们会提前通知您任何
此类转让（如果法律要求）。
本政策受[司法管辖区，例如新加坡]的法律管辖，不包括其法律冲突原则。
18.AI免责声明（强烈建议保留）
十九、附加规定
/ /

---

生效日期：[2026年4月1日]
提供者 Sapiens AI / 阿格尼
斯人工智能
文件类型 服务条款
联系方式 support@agnes-
ai.com
这些服务条款（“条款”或“协议”）在您对 Agnes AI 平台的访问和使用，包括所有应用程序编程接口 
(API)、人工智能 (AI) 模型、基于 Web 的应用程序、桌面或移动软件、开发人员工具以及 Sapiens AI
（以下简称“Agnes AI”、“我们”、“我们”或“我们的”）。
通过访问、浏览或使用服务的任何部分（包括但不限于注册帐户、提交数据或拨打 API 电话），您（“客
户”、“您”或“您的”）同意接受本协议的法律约束，包括本文引用的所有其他政策、指南或更新（统称为
“政策”）。如果您不同意本协议的所有条款和条件，您必须立即停止访问或使用服务。
就本协议而言，除非上下文没有明确规定，下列术语应具有以下含义：
服务：Agnes AI提供的所有产品、服务和技术的总称，包括但不限于大型语言模型（LLM）、
修改多模式生成工具（图像、视频、音频、文本）、API、软件开发工具包（SDK）、门户网
站、开发仪表板、文档、支持人员服务以及对所有内容的任何更新或。
客户/“您”：访问或使用任何个人、公司、合伙企业、有限责任公司或其他实体实体的服务，无
论是代表自己还是代表第三方（如果您代表某个实体实体，您声明并保证您能够使该实体遵守
本协议）。
最终：用户使用您使用的服务构建、部署或操作的任何应用程序（定义如下）、吸引任何个人
或实体的交互或结算受益。
Agnes AI 服务条款
## 1. 定义

客户数据：您、您的最终用户或您的授权代表向服务提交、上传、传输或提供的与您使用服务
相关的所有数据、信息、内容或材料（包括文本、图像、视频、音频、个人数据和业务数
据）。
输出：服务响应客户数据或用户输入而生成的所有内容、结果、响应、建议或其他材料，包括
但不限于文本、图像、视频、音频、代码或预测。
应用程序：您使用本服务开发、构建、部署或运营的任何网站、Web应用程序、移动应用程
序、软件程序、产品或服务（包括但不限于将服务的API或模型集成到您自己的产品中）。
API密钥：由Agnes AI提供的唯一标识符，用于验证您对服务的API的访问权限，用于跟踪您
对服务的使用情况并对其进行操作。
机密信息：任何一方披露的与本协议相关的任何非公开信息，包括但不限于技术规范、模型架
构、API文档、定价信息、客户数据、业务计划和商业秘密。
通过访问或使用服务，您向Agnes AI声明并保证：
如果您是个人，您已年满18周岁（或您所在司法管辖区的法定年龄），并且具有签订本协议并
受本协议约束的法律能力；
如果您是实体，则您是根据您所在司法管辖区的法律合法组织和有效存在的实体，您有权遵守
本协议规定您的实体遵守其条款；
您对服务的访问和使用遵守所有适用的地方、州、国家和国际法律、法规和条约（包括但不限
于数据保护法、隐私法、出口管制法和反洗钱法）；
您和您的最终用户不位于任何受联合国、美国、欧盟或其他适用司法管辖区（统称为“受司法
司法管辖区”）实施全面经济制裁的国家或地区，也不是该等国家或地区的公民或居民；
您没有被列入联合国、美国外国资产控制办公室 (OFAC)、欧盟或其他适用机构制定的任何制
裁名单中；
您不得使用本服务为位于受司法管辖区或列入制裁名单的任何个人或实体谋取利益。
Agnes AI 保留随时使用服务的资格的权利，并且如果我们确定您不符合资格或违反本第 2 条中规定的
任何声明和保证，则可以暂停或终止您的访问。
## 2. 资格和接受
## 3. 服务范围
/ /

Agnes AI 同意根据本协议的条款和您选择任何适用的定价计划向您提供服务的访问权限。服务的具体特
性和功能可能会有所不同，具体取决于您的定价计划，Agnes AI 保留随时向服务添加、修改或删除功能
的权利，进而向您发出合理的通知（紧急情况或安全问题类似）。
该服务包括但不限于以下核心产品：
大型语言模型（LLMs）：预先训练的人工智能模型，能够理解和生成类似人类的文本，包括
但不限于文本完成、摘要、翻译、问答和对话生成；
多模态生成：用于生成或处理图像、视频、音频和文本内容的工具和模型（例如，根据文本提
示生成图像、视频编辑、音频解析和跨模态转换）；
API基础设施：安全、可扩展的API，允许您将服务集成到您的应用程序中，包括文档、速率限
制和监控工具；
开发人员工具：支持您使用服务的资源，包括 SDK、示例、测试环境、调试代码工具以及用于
跟踪使用情况、计费和性能的开发人员仪表板。
Agnes AI 仅作为服务的技术而成功。我们不控制也不对以下内容负责：
您的业  务逻辑：您的应用程序的设计、功能或操作，包括但不限于您的业务模型、用户体验或
决策流程；
最终用户行为：最终用户对应用程序的操作、行为或使用，包括最终用户对服务的任何误用或
打扰；
内容使用：您或您的最终用户如何使用、分发或修改服务生成的输出，或类使用而产生的任何
后果。
Agnes AI 不通过服务提供法律、财务、医疗或其他专业建议。本服务生成的任何产出参考，不应被视为
专业建议。
### 3.1 服务规定
### 3.2 服务范围限制
## 4. 账户注册及安全
### 4.1 账户注册
/ /

要访问服务的某些功能（包括 API 访问和付费计划），您必须在 Agnes AI 注册帐户。注册帐户时，您
同意：
提供准确、完整和最新的信息（包括您的姓名、电子邮件地址、公司名称和付款详细信息（如
果适用））；
如果有任何详细信息发生变化，请及时更新您的账户信息；
为您的帐户使用强而独特的密码和保密；
为您的账户实施适当的访问控制（例如，对团队成员进行基于角色的访问），以防止未经授权
的访问；
不与任何第三方共享您的账户帐户（包括API密钥），受授权员工或承包商合同的保密义务。
您对您的账户下发生的所有活动承担全部责任，包括但不限于所有 API 呼叫、数据作业以及任何个人或
实体使用您的账户账户采取的操作。您同意：
定期监控您的账户活动以检测任何未授权的使用；
如果您的账户或API涉及任何未经授权的访问，或与您的账户相关的任何其他安全漏洞，请立
即通知Agnes AI；
采取合理的一切措施，请务必授权使用您的剂量并造成任何损害。
如果我们怀疑或确定以下情况，Agnes AI 可能会暂停或限制您的账户（包括取消 API 访问权限），恕
不另行通知：
您在帐号注册期间或与使用服务相关的过程中提供了欺骗性、误导性或不准确的信息；
您的帐户已被盗用或面临被盗用的风险（例如，未授权访问您的API密钥）；
您违反本协议（包括第 5 条规定的危险使用政策）；
您对 Agnes AI 的服务、服务或服务的其他用户的使用造成安全风险；
法律或法院命令要求我们这样做。
如果您的帐户被暂停，您可以联系 Agnes AI 的支持团队来解决问题，如果我们确定问题已解决并且您
### 4.2 账户责任
### 4.3 账户暂停
/ /

遵守本协议，我们将恢复您帐户的访问权限。
您同意、也不会允许您的最终用户将服务用于任何非法、有害或违反本协议的目的。 严格禁止将本服务
用于以下用途（“禁止用途”）：
使用本服务从事或协助任何非法活动，包括但不限于：
违反任何地方、州、国家或国际法律、法规或条约（例如侵犯版权、侵犯商标、侵犯隐私和盗
窃数据）；
实施欺诈、诈骗或失实陈述（例如，生成虚假文件、冒充个人或实体或欺骗消费者）；
参与洗钱、恐怖融资或其他金融犯罪；
拥有、分发或生成适用法律规定的非法内容（例如非法药品、假冒商品或被盗财产）。
使用本服务生成、分发或宣传有害、暴力或歧视性内容，包括但不限于：
煽动或宣扬恐怖主义、暴力或极端主义的内容（例如制造武器的说明、恐怖主义宣传或号召对
个人或团体使用暴力）；
基于种族、民族、性别、性取向、宗教、残疾或任何其他受保护特征的仇恨言论或歧视；
涉及剥削或虐待儿童的内容（例如儿童性虐待材料、诱骗未成年人或危及儿童的内容）；
宣扬自残、自杀或饮食失调的内容；
骚扰、欺凌或跟踪任何个人（例如，生成威胁消息或人肉搜索个人信息）。
以欺骗性、误导性或对个人或社会构成风险的方式使用本服务，包括但不限于：
生成误导性或欺骗性内容（例如，为了政治操纵而深度伪造公众人物、虚假新闻或虚假产品评
论），而没有明确且显着地披露该内容是人工智能生成的；
5. 常用政策
5.1 非法活动
5.2 有害内容
5.3 不安全的人工智能使用
/ /

滥用深度伪造技术未经个人同意冒充个人，或创建可能损害个人声誉或安全的内容；
参与自动滥用（例如，生成垃圾邮件、短信或社交媒体帖子；操纵在线民意调查或评论；或发
起网络钓鱼攻击）；
使用服务生成可用于实施网络攻击的内容（例如恶意软件、勒索软件或网络钓鱼脚本）。
试图损害服务的安全性或完整性，包括但不限于：
逆向工程、反编译、反汇编或以其他方式尝试提取服务的人工智能模型或软件的源代码、模型
权重或算法；
未经 Agnes AI 明确书面许可，从服务中抓取、爬行或提取数据（包括但不限于训练数据、模
型输出或 API 文档）；
发起或协助对服务基础设施的攻击（例如，DDoS 攻击、暴力攻击或未经授权访问 Agnes AI 
的服务器）；
规避 Agnes AI 实施的速率限制、访问控制或其他安全措施；
将恶意软件、病毒或其他有害代码引入服务中。
Agnes AI 保留监控您对服务的使用的权利，以确保遵守本可接受的使用政策。如果我们确定您或您的最
终用户正在从事任何禁止使用的行为，我们可能会采取我们认为适当的任何行动，包括但不限于：
删除或禁止访问由服务生成的任何违反本政策的内容；
暂停或终止您的帐户以及对服务的访问；
向执法部门或相关监管机构报告您的活动；
对于因您的违规行为造成的任何损失，对您采取法律行动。
如果您部署或提供任何使用本服务的应用程序（包括但不限于向最终用户提供应用程序），您同意遵守
以下 AI 特定责任：
5.4 安全违规
5.5 可接受使用政策的执行
6. AI 特定职责
/ /

当服务生成或处理内容（即人工智能生成的内容）时，您必须以易于理解和访问的方式向最终
用户清楚、显着地披露。此披露必须在最终用户与人工智能生成的内容交互之前或同时进行，
并且不得隐藏或误导。
如果适用法律或法规（例如欧盟的人工智能法案、美国的联邦贸易委员会指南）要求，您必须
提供有关在您的应用程序中使用人工智能的其他信息，包括但不限于人工智能的目的、人工智
能的限制以及人工智能如何做出决策。
您必须实施合理的审核机制，以防止您的最终用户将您的应用程序（以及服务）用于禁止用
途。这可能包括但不限于内容过滤、用户报告工具以及对高风险内容的人工审核。
您必须监控最终用户对应用程序和服务的使用情况，以检测并解决任何误用或滥用行为。如果
您发现最终用户有任何禁止使用的行为，您必须立即采取行动停止此类使用并通知 Agnes 
AI。
如果适用法律或法规要求，您必须将标识符（例如水印、元数据或日志记录）添加到 AI 生成
的内容中，以便可以将内容追溯到您的应用程序和服务。
您必须按照适用法律的要求保存您使用服务的记录（包括 API 呼叫、客户数据和输出），并根
据要求向 Agnes AI 或监管机构提供此类记录。
您承认并同意服务按“原样”提供，并且服务生成的输出可能包含错误、不准确或偏见。您全权负责：
对服务生成的输出的所有用途，包括但不限于将输出分发给最终用户、在业务决策中使用输出
或将输出集成到您的应用程序中；
基于服务生成的输出做出的任何决定（例如，雇用决定、财务决定或医疗建议）；
输出或您对输出的使用造成的任何损害或损害，包括但不限于对个人、企业或声誉的损害。
Agnes AI 对输出中的任何错误、不准确或偏差不承担任何责任，并且您同意赔偿 Agnes AI 因您使用输
出而引起的任何索赔（详情请参阅第 15 节）。
6.1 披露和透明度
6.2 审核和监控
6.3 标识符和责任
6.4 输出和决策的责任
/ /

您对服务的使用须遵守您选择的定价计划（如 Agnes AI 网站或单独的订单中所述）。服务的定价基于
以下一种或多种模式：
基于使用的定价：根据您对服务的实际使用情况付费，例如处理的令牌数量、进行的 API 调用
数量、使用的计算资源量或生成的内容量（例如图像、视频）。
基于订阅的定价：您需要支付固定的月费或年费才能访问一组特定的功能或使用限制。如果您
超出订阅计划的使用限制，则可能会根据定价计划中规定的超额条款向您收取额外费用。
所有定价均以您的定价计划中指定的货币（例如美元、欧元）为单位，不包括您负责支付的税费、关税
或其他政府费用（除非您提供有效的免税证明）。
当您使用服务时，服务费用会自动累积，并根据您的定价计划定期（例如每月、每年）向您收
取费用。
您同意提供准确、完整的付款信息（例如信用卡详细信息、银行账户信息）并保持该信息最
新。 Agnes AI 可能会使用第三方支付处理商来处理付款，您的支付信息将受支付处理商的隐
私政策的约束。
除非您根据第 14 条（终止）或定价计划的条款终止您的帐户或定价计划，否则我们将继续向
您收取服务费用。您负责承担截至终止之日所产生的所有费用。
Agnes AI 保留随时更新或更改服务定价的权利。对于任何### ### 价格变更，我们将至少提前 30 天向您提供书
面通知（例如，通过电子邮件发送至与您的帐户关联的地址，或通过服务的开发者仪表板）。如果您在
### ### 价格变更生效后继续使用服务，即表示您同意新的定价。
如果您未能在到期日之前支付任何发票，Agnes AI 可能会采取以下措施：
暂停您对服务的访问（包括 API 访问），直到支付所有未付款项；
对所有未清金额按每月 [X]% 的费率（或适用法律允许的最高费率）收取滞纳金；
## 7. 账单、定价和付款
### 7.1 定价模型
### 7.2 计费规则
7.3 ### ### 价格变化
### 7.4 不付款
/ /

根据第 14 条终止您的帐户和本协议；
采取法律行动收取任何未付款项，包括但不限于律师费和法庭费用。
客户数据：您保留提交给服务的所有客户数据的完全所有权。 Agnes AI 不主张对客户数据的
任何所有权，除非本协议明确规定。
输出：您可以拥有服务生成的输出，前提是此类所有权受到适用法律的允许，并且不侵犯 
Agnes AI 或任何第三方的知识产权。 Agnes AI 保留使用输出来改进服务的权利（除非您选
择退出此类使用（如果有））。
通过向服务提交客户数据，您授予 Agnes AI 有限的、非独占的、不可转让的许可：
仅出于向您提供服务的目的处理、存储和传输客户数据（例如，生成输出、维护服务和提供支
持）；
使用客户数据来改进服务的人工智能模型、算法和功能（包括但不限于训练和微调模型），除
非您通过服务的设置（如果有）选择退出此类使用。如果您选择退出，Agnes AI 将不会使用
您的客户数据来改进服务，但仍可能处理您的客户数据以向您提供服务。
本许可将在本协议终止时终止，但 Agnes AI 可以根据第 8.4 条（数据保留）和适用法律保留和使用客
户数据。
您向 Agnes AI 保证：
您拥有收集、使用和向服务提交所有客户数据的合法权利，并且此类提交不违反任何适用的法
律、法规或第三方权利（包括但不限于隐私权、版权和商标）；
您已获得最终用户或其数据包含在客户数据中的其他第三方的所有必要同意（例如，同意根据
数据保护法处理个人数据）；
客户数据不包含任何非法、有害或不当内容（如第 5 节中定义）；
## 8. 数据使用和隐私
### 8.1 数据的所有权
### 8.2 Agnes AI 的许可
### 8.3 您对数据的责任
/ /

您将遵守与收集、使用和提交客户数据以及使用输出相关的所有适用的数据保护法（例如 
GDPR、CCPA、HIPAA）。
Agnes AI 将在向您提供服务所需的时间内或根据适用法律的要求保留您的客户数据。在您的帐户或本协
议终止后，Agnes AI 可以删除您的客户数据，但可以在合理的时间内保留您的客户数据的副本，以遵守
法律义务、解决争议或执行本协议。您可以随时联系 Agnes AI 的支持团队请求删除您的客户数据，我
们将尽合理努力在合理的时间内删除您的客户数据，并遵守任何法律义务。
Agnes AI 实施合理的技术、管理和物理保障措施，以保护客户数据和服务的安全性、机密性和完整性。
这些保障措施包括但不限于：
对传输中的客户数据（使用 TLS/SSL）和静态进行加密；
访问控制，以限制授权的 Agnes AI 员工和承包商对客户数据的访问；
定期安全审计和漏洞评估；
对员工进行数据安全和隐私### 最佳实践培训；
业务连续性和灾难恢复计划可最大限度地减少安全漏洞或系统故障时的数据丢失。
然而，没有任何安全措施是完全万无一失的，Agnes AI 不能保证客户数据永远不会被未经授权的第三方
访问、披露或修改。
您对用于访问本服务的自己的系统、设备和网络的安全承担全部责任，包括但不限于：
实施适当的安全措施来保护您的帐户凭据（包括 API Key）和客户数据；
为与服务交互的系统配置额外的保护（例如防火墙、加密）；
确保访问服务的员工和承包商接受安全### 最佳实践培训并遵守本协议。
### 8.4 数据保留
## 9. 数据安全
### 9.1 Agnes AI 的安全义务
### 9.2 您的安全责任
/ /

Agnes AI 对以下原因造成的任何数据丢失、泄露或损坏不承担责任：
您的行为或不作为（例如，共享帐户凭据、未能实施适当的安全措施）；
您的系统或服务配置错误；
第三方（例如黑客、恶意软件）未经授权访问您的系统或客户数据；
超出 Agnes AI 合理控制范围的事件（例如自然灾害、对第三方提供商的网络攻击）。
如果由于 Agnes AI 的疏忽而导致涉及您的客户数据的安全漏洞，Agnes AI 将立即通知您（根据适用法
律）并采取合理措施来缓解漏洞。
Agnes AI 保留服务的所有权利、所有权和利益，包括但不限于所有人工智能模型、API、算法、软件、
代码、文档、商标、徽标和其他知识产权。本协议不授予您对服务的任何所有权，但本协议规定的使用
服务的有限许可除外。
您同意不主张本服务或其任何部分的任何所有权，也不对本服务进行修改、反向工程或创建衍生作品
（本协议明确允许的除外）。
您保留您的客户数据、您的应用程序以及与之相关的任何知识产权（例如版权、商标、专利）的所有权
利、所有权和利益。除第 8.2 条规定的有限许可外，本协议不授予 Agnes AI 您的客户数据、应用程序
或相关知识产权的任何所有权。
您同意不会：
逆向工程、反编译、反汇编或以其他方式尝试提取服务的人工智能模型或软件的源代码、模型
权重或算法；
提取、抓取或复制用于训练服务人工智能模型的任何训练数据；
使用服务的技术或知识产权重建、复制或创建竞争性人工智能模型或服务；
### 9.3 数据安全责任限制
## 10. 知识产权
### 10.1 Agnes AI 的知识产权
### 10.2 客户的知识产权
### 10.3 知识产权限制
/ /

未经 Agnes AI 明确书面许可，使用服务的商标、徽标或其他品牌；
侵犯 Agnes AI 的任何知识产权。
该服务可能与第三方服务、产品或网站（例如云存储提供商、支付处理器或分析工具）集成或链接。这
些第三方服务不受 Agnes AI 控制，并且 Agnes AI 不负责：
第三方服务的可用性、功能或性能；
第三方服务的任何中断、错误或故障；
第三方服务的隐私惯例或内容；
由于您使用第三方服务而造成的任何伤害或损害。
您对第三方服务的使用须遵守这些第三方的条款和条件，并且您同意查看并遵守这些条款。 Agnes AI 
不认可任何第三方服务，您使用第三方服务的风险由您自行承担。
Agnes AI 旨在提供服务的高可用性，但我们不保证服务 100% 可用。由于以下原因，该服务有时可能
不可用：
定期维护（我们将提供定期维护的合理通知，紧急情况除外）；
计划外维护或技术问题（例如服务器故障、软件错误）；
超出 Agnes AI 合理控制范围的事件（例如自然灾害、网络攻击或互联网中断）。
对于付费定价计划，Agnes AI 可能会提供服务级别协议 (SLA)，其中规定了服务的最低正常运行时间百
分比以及正常运行时间低于商定百分比时您可以采取的任何补救措施（例如服务积分）。 SLA 的具体条
款将在您的定价计划或单独的订单中列出。对于免费定价计划，不提供 SLA，并且 Agnes AI 不保证任
何级别的服务可用性。
11. 第三方服务
12. 服务可用性和 SLA
12.1 服务可用性
12.2 服务水平协议（SLA）
/ /

Agnes AI 保留随时修改、更新或终止服务的任何特性或功能的权利，并向您发出合理通知（紧急情况或
安全问题除外）。我们还可能弃用服务的 API 或模型的旧版本，并将向您提供迁移到新版本的合理通
知。
如果我们合理确定以下情况，Agnes AI 可以暂停或限制您对服务的访问（包括 API 访问）：
您违反了本协议的任何条款或条件（包括可接受的使用政策）；
您对服务的使用会对 Agnes AI、服务或服务的其他用户造成安全风险；
法律、法院命令或监管机构要求我们这样做；
您未能支付任何未付发票（如第4 条所述）；
您的帐户已被盗用或面临被盗用的风险。
如果出现严重安全风险（例如，严重违反服务安全或利用服务实施严重犯罪），Agnes AI 可能会立即暂
停您对服务的访问，恕不另行通知。暂停后，我们将通知您暂停的原因，并为您提供解决问题的机会
（如果适用）。
您：您可以随时联系 Agnes AI 的支持团队或按照服务开发人员仪表板中的终止说明来终止本
协议和您的帐户。终止后，您将无法再访问服务，并且您负责承担截至终止之日所产生的所有
费用。
通过 Agnes AI：在以下情况下，Agnes AI 可以终止本协议和您的帐户：
您违反了本协议的任何条款或条件，并且在收到 Agnes AI 的书面通知后 30 天内未纠正此类
违反行为；
您在收到未付款通知后未能支付任何未付发票；
您失去使用服务的资格（例如，您搬到受制裁的司法管辖区）；
12.3 服务的修改
13. 暂停和执行
## 14. 终止
14.1 任何一方终止
/ /

Agnes AI 确定您对服务的使用构成重大法律或安全风险；
Agnes AI 终止服务或您正在使用的特定功能。
本协议终止后：
根据本协议，您的所有许可将立即终止；
您将无法再次访问您的帐户或服务；
您必须支付截至终止之日产生的所有未付费用；
Agnes AI 可以在合理的保留期间（如第 8.4 节）规定后删除您的客户数据，除非法律要求保
留；
您必须停止使用服务生成的任何受 Agnes AI 知识产权保护的输出；
本协议中根据其性质应在终止后继续有效的部分（包括但不限于第8、10、15、16、17和20
节）将继续对双方具有约束力。
您同意Agnes AI、其关联公司、管理人员、、和承包商（统称为“受赔偿方”）进行赔偿，并作出赔偿，
并裁定因以下原因引起或伤害相关的任何及所有索赔、损失、损害、责任、费用和开支（包括但不限于
律师费、法庭费用和员工解救费用）：
您对服务的使用，包括但不限于任何禁止的使用；
您的应用程序，包括但不限于侵犯第三方知识产权或对任何个人造成损害或实质造成损害的任
何损害；
您的客户数据，包括但不限于您的客户数据违反任何合理的法律或第三方权利；
您未遵守本协议或任何适用法律；
您的最终用户对服务或您的应用程序的使用。
Agnes AI 将通知您任何需要赔偿的指控，并且您同意支持 Agnes AI 对此类指控进行辩护。如果您未能
这样做，Agnes AI 保留对任何被告进行辩护和控制的权利，并且您同意辩护 Agnes AI 因此进行类辩护
而产生的任何费用。
14.2 终止的影响
15. 赔偿
/ /

在适用法律允许的最大范围内，AGNES AI 及其受赔偿方对任何间接、偶然、后果性、特殊、惩罚性或
惩罚性损害（包括但不限于收入、利润、数据或业务损失）承担责任。 因本协议或您对服务的使用而产
生或相关损害的机会，即使 AGNES AI 已被告知发生此类损害的可能性。
在适用法律允许的最大范围内，AGNES AI 及其受偿方对本协议或您对服务的使用引起的或相关损坏的
任何指控的全部责任不应超过您在签署协议之前六 (6) 个月内向 AGNES AI 支付的费用。
无论法律责任限制理论如何（如合同、目标、疏忽、严格责任），即使服务未能按要求或预期执行，此
责任均适用。
某些司法限制曼哈顿区不允许排除或限制疾病某些，因此上述可能对您不适用。在这种情况下，Agnes 
AI 及其受赔偿方的责任应限于适用法律允许的最大范围。
双方同意维护对方机密信息的机密性，并使用保护与自己类似机密的机密信息的一致程度（但明显于合
理范围）来保护此类机密信息。双方均未披露方事先书面同意，任何一方均不得向任何第三方披露对方
的机密信息，但以下情况是：
需要访问机密信息以履行职责并受授权的员工、承包商或顾问的保密义务；
监管机构或法院命令，前提是接收方向披露方合理发布通知（如果法律允许）以允许披露方对
披露方提出质疑；
与接收方有业务关系的第三方，前提是此类第三方受保密义务的约束。
机密信息不包括以下信息：
并非因接收方的过错而公开可用；
在披露方之前披露的内容与接收方相同，无任何保密义务；
由接收方独立开发，未使用披露方的机密信息；
来自第三方，该第三方有权披露该信息，且不承担任何保密义务。
此保密义务将在本协议终止后继续有效[X]年（或根据适用法律的要求）。
16. 责任限制
17. 保密
18. 合规和出口管制
/ /

您同意遵守所有适用的出口管制法律、制裁法规和贸易法（包括但不限于美国出口管理条例（EAR）、
欧盟双重用途条例以及联合国、美国和欧盟实施的制裁）。您同意不会：
将服务或任何相关技术出口、再出口或转让给予任何受司法管辖的管辖区或所列人员；
将服务用于出口管制法律或制裁禁止的任何目的；
向位于受制裁区域或制裁名单上的任何个人或切实提供对服务的访问权限。
如果我们确定您违反任何出口管制法律或制裁规定，或者您对服务的使用构成合规风险，Agnes AI 保留
终止您访问服务的权利。
Agnes AI 保留随时服务（包括添加、删除或更改功能）和更新这些条款的权利。我们将向您提供有关条
款的任何重大变更的合理通知（例如，通过电子邮件发送到与您的帐户关联的地址，或通过服务的开发
者仪表板）。您如果在更新后的条款生效后继续使用本服务，即表示您同意接受更新后的条款的约束。
如果您不同意更新后的条款，您必须立即停止使用服务并终止您的帐户。
本协议应受新加坡法律管辖并根据新加坡法律解释，不考虑其法律冲突原则。
因本协议或您使用服务而引起或损害的任何争议、争议或指控（包括但不限于有关违约金、知识产权和
疏忽的争议）均应由新加坡国际仲裁中心（SIAC）根据仲裁时有效的SIAC规则通过仲裁解决。仲裁应在
新加坡进行，仲裁为语言英语。仲裁庭应根据SIAC规则裁决的[一/三]仲裁庭的裁决为终局裁决，对双方
均具有约束力的，并可在任何有管辖权的法院强制执行。
在提起仲裁之前，双方应尝试通过善意谈判解决争议。如果双方在第一次书面通知争议后 30 天内无法
通过协商解决争议，则双方应共同建立仲裁。
Agnes AI 可能会在我们的营销材料（包括但不限于我们的网站、社交媒体和销售练习）中使用您的公司
名称、本质和您使用服务的简要说明客户参考。如果您没有被用作客户参考，您可以通过向 Agnes AI 
19. 服务和条款的更新
20.适用法律及争议解决
20.1 适用法律
20.2 争议解决
21. 营销和宣传
/ /

的支持团队发送书面请求来选择退出。选择退出将在收到您希望的请求后 30 天内生效。
完整协议：本协议（包括任何适用的政策和定价计划）构成您与 Agnes AI 之间关于您使用服
务的完整协议，并取代双方之间所有先前或类似的协议、陈述或谅解（无论是口头还是口
头）。
可分割性：如果有曼哈顿权的法院发现本协议的任何条款无效、无效或无法执行，则该条款应
从本协议中分割，其余条款仍具有完全效力。
无第三方受益人：本协议由您和 Agnes AI 承担，任何第三方均不享有本协议项下的任何权利
或利益（第 15 条明确规定的条款）。
转让：未经Agnes AI事先书面同意，您不得转让本协议或本协议项下您的任何权利或义务。
Agnes AI可以在您同意的情况下将本协议转让给任何关联公司或利益继承者（例如，在合并、
收购或出售资产的情况下）。
弃权：Agnes AI 未能执行本协议的任何条款或条件不应被视为该条款或条件的放弃，并且不
得阻止 Agnes AI 今后执行该条款或条件。
通知：本协议条款下的所有通知均应采用书面形式，并应发送至与您的帐户关联的电子邮件地
址（对于向您发出的通知）或第23条中规定的联系信息（对于向Agnes AI发出的通知）。通
知在发送（如果通过电子邮件发送）或送达（如果通过挂号信发送）时即视为已收到。
如果您对本协议或服务有任何问题、疑虑或请求，请通过以下方式联系我们：
公司：Sapiens AI
电子邮件：support@agnes-ai.com
22. 杂项
23. 联系方式
/ /


---

> 本文档由 Agnes AI API 官方在线文档整理生成，仅供学习和参考使用。如有疑问，请联系 support@agnes-ai.com。
