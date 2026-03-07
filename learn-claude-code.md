# Learn Claude Code

**GitHub**: https://github.com/shareAI-lab/learn-claude-code

**Stars**: 22,668 ⭐ | **Forks**: 4,299

## 项目简介

"Bash is all you need - A nano Claude Code–like agent, built from 0 to 1"（Bash 就足够了 —— 从 0 到 1 构建一个微型的类似 Claude Code 的智能体）。

这是一个非常出色的开源教育项目，它通过一个极简的代码库（仅用 Bash 脚本和少量的辅助工具）从零开始重构和展示了像 `Claude Code` 这样的 AI Agent 命令行工具是如何在底层运行的。

## 核心设计与特性

这个项目剥离了复杂的生产级架构（没有 TypeScript，没有复杂的框架，甚至没有 Python），以最原生、最透明的方式展示了 Agentic 编程的核心：**模型通信 + 工具调用 (Tool Calling) + REPL (读取-求值-打印循环)**。

### 1. 核心循环 (The Core Loop)
项目展示了 Agent 的基本运行原理：
1. **User Input** (接收用户指令)
2. **LLM Reasoning** (发送给大模型进行思考)
3. **Tool Execution** (模型决定调用 Bash 命令或读取文件)
4. **Observation** (将命令结果反馈给模型)
5. **Repeat** (直到任务完成)

### 2. Bash 作为超级工具
项目证明了一个观点：对于一个存在于终端中的 Coding Agent 而言，只要赋予它强大的 `Bash` 读写执行权限和文件系统访问权限，大语言模型就能表现出令人惊讶的自主编程和排错能力。

### 3. API 与工具集成
- 实现了与各大主流模型 API (如 Claude 3.5 Sonnet / 3.7 Sonnet) 的底层通信
- 实现了原生的 `Function Calling` 机制
- 实现了 `MCP` (Model Context Protocol) 概念的极简版本

## 学习价值

该仓库被称为 "Agent 领域的 Karpathy 式教学" (参考 Andrej Karpathy 从零手搓 GPT 的教学风格)。通过阅读这个项目的源码，开发者可以深刻理解：
- 什么是 Agentic Workflow
- "让 AI 自己写代码并运行" 背后的安全性和沙盒考量
- 提示词工程 (Prompt Engineering) 在决定 Agent 行为时的决定性作用
- 上下文压缩 (Context Compaction) 为什么重要

## 适用人群

- 想要理解 Claude Code、Cursor、Devin 等工具**底层原理**的开发者
- 想要尝试自己**手写一个 AI Agent** 的工程师
- 对 LLM 工具调用和终端自动化感兴趣的黑客 (Hackers)

## 相关资源

- [Anthropic: Tool use (function calling)](https://docs.anthropic.com/claude/docs/tool-use)
- [Model Context Protocol (MCP)](https://modelcontextprotocol.io/)