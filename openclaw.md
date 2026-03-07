# OpenClaw

**GitHub**: https://github.com/openclaw/openclaw

**Stars**: 271,027 ⭐ | **Forks**: 51,789

## 项目简介

OpenClaw 是一个开源的个人 AI 助手项目，名为"🦞 Kapybara 水豚"。它的设计理念是构建一个**在任何操作系统、任何平台上运行的通用 AI 助手**，采用"龙虾之道"（The Lobster Way）的开发哲学。

## 核心特性

### 1. 跨平台支持
- Linux (主要开发环境)
- macOS
- Windows (WSL)
- ARM64 (Raspberry Pi)
- iOS/Android (即将支持)

### 2. 多模型支持
- **大语言模型**: OpenAI, Anthropic, Google, DeepSeek, MiniMax 等
- **图像模型**: 支持多种视觉模型
- **本地部署**: 支持 Ollama, LM Studio 等本地模型

### 3. 多渠道接入
- **Telegram**: 主要即时通讯渠道
- **WhatsApp**: 实时通讯支持
- **Discord**: 社区平台集成
- **Signal**: 隐私通讯
- **Slack**: 企业协作
- **IRC**: 传统协议

### 4. 智能体编排
- **Sub-agent**: 支持创建子智能体处理复杂任务
- **Session Management**: 多会话管理
- **Context Isolation**: 上下文隔离，保护隐私

### 5. 技能系统 (Skills)
- 可插拔的技能架构
- 预置大量实用技能
- 支持自定义技能开发
- **MCP 集成**: 支持 Model Context Protocol

### 6. 记忆系统
- **短期记忆**: 当前会话上下文
- **长期记忆**: 持久化存储，跨会话学习
- **向量搜索**: 语义检索

### 7. 自动化
- **Cron Jobs**: 定时任务调度
- **Heartbeat**: 心跳检查与健康监控
- **Workflows**: 自定义工作流

## 技术架构

```
┌─────────────────────────────────────────────┐
│              OpenClaw Core                  │
├─────────────────────────────────────────────┤
│  Channels  │  Skills  │  Memory  │  Agents │
├─────────────────────────────────────────────┤
│           LLM Providers (OpenAI, Claude...) │
├─────────────────────────────────────────────┤
│         Platform Layer (Linux, Mac, Pi...)  │
└─────────────────────────────────────────────┘
```

## 核心概念

### Kapybara (水豚)
OpenClaw 的官方 AI 助手形象，一个性格鲜明、适应性强的人工智能助手。

### Skills (技能)
可重用的自动化模块，例如：
- `polymarket-cli`: 预测市场交易
- `gh-issues`: GitHub Issues 管理
- `weather`: 天气查询
- `project-pm`: 项目管理

### Channels (渠道)
支持多种通讯平台的统一接口。

### Memory (记忆)
分层记忆系统，支持上下文持久化。

## 部署方式

### Docker (推荐)
```bash
# 快速启动
docker run -d --name openclaw \
  -v ~/.openclaw:/home/node/.openclaw \
  -p 8080:8080 \
  openclaw/openclaw
```

### 手动部署
```bash
# 克隆仓库
git clone https://github.com/openclaw/openclaw.git
cd openclaw

# 安装依赖
pip install -e .

# 配置
cp .env.example .env
# 编辑 .env 添加 API keys

# 运行
python -m openclaw
```

## 社区

- **Discord**: https://discord.com/invite/clawd
- **文档**: https://docs.openclaw.ai
- **技能市场**: https://clawhub.com

## 相关资源

- [官方文档](https://docs.openclaw.ai)
- [GitHub](https://github.com/openclaw/openclaw)
- [Discord 社区](https://discord.com/invite/clawd)
- [技能市场](https://clawhub.com)
- [Docker Hub](https://hub.docker.com/r/openclaw/openclaw)
