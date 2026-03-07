# OpenAI Agents Python SDK

**GitHub**: https://github.com/openai/openai-agents-python

**Stars**: 19,384 ⭐ | **Forks**: 3,216

## 项目简介

OpenAI Agents Python SDK 是一个轻量级但功能强大的框架，专门用于构建**多智能体工作流 (multi-agent workflows)**。它是在 OpenAI Agents SDK 基础上构建的 Python 版本，旨在帮助开发者创建复杂的 AI Agent 应用程序。

## 核心特性

### 1. 多智能体编排 (Multi-Agent Orchestration)
- 支持创建多个专门的 Agent 并协调它们之间的协作
- Agent 之间可以相互调用、传递信息

### 2. 工具集成 (Tool Integration)
- 内置丰富的工具支持
- 轻松扩展自定义工具
- 与外部服务无缝集成

### 3. 状态管理
- 内置对话历史管理
- 支持上下文持久化
- 会话恢复能力

### 4. 流式输出 (Streaming)
- 支持实时流式响应
- 便于构建交互式应用

### 5. 安全性
- 内置输入验证
- 敏感信息过滤
- 审计日志

## 核心概念

### Agent
```python
from agents import Agent

agent = Agent(
    name="Researcher",
    instructions="你是一个研究助手，擅长搜索和分析信息",
    tools=[search_tool, browser_tool]
)
```

### Handoff (交接)
在不同 Agent 之间传递控制权：
```python
agent = Agent(
    name="Triage",
    handoffs=[sales_agent, support_agent]
)
```

### Guardrails (护栏)
添加输入/输出验证：
```python
from agents import Guardrail

guardrail = Guardrail(
    name="Validate Input",
    validate_input=validate_function
)
```

## 使用场景

- **客户服务**: 多轮对话、自动路由
- **内容创作**: 多阶段写作流程
- **数据分析**: 并行处理、结果汇总
- **代码审查**: 多 Agent 协作审查

## 相关资源

- [官方文档](https://github.com/openai/openai-agents-python)
- [PyPI 包](https://pypi.org/project/openai-agents/)
- [示例代码](https://github.com/openai/openai-agents-python/tree/main/examples)
