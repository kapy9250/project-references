# Claude Code Best Practice

**GitHub**: https://github.com/shanraisshan/claude-code-best-practice

**Stars**: 12,036 ⭐ | **Forks**: 1,137

## 项目简介

"Practice made Claude perfect" (实践让 Claude 变得完美)。这是一个收集并总结使用 Anthropic 最新发布的 `Claude Code` (CLI 工具) 时的各种最佳实践、提示词技巧和工作流配置的实战参考指南。

## 核心内容

随着基于 Agent 的编程工具 (如 Claude Code) 的普及，开发者需要新的工作流范式来最大化这些工具的效能。该仓库主要提供了以下内容：

### 1. `.clauderc` 配置文件模板
如何为不同的项目类型设置理想的指令（System Prompts），例如：
- 前端项目 (React/Vue/TypeScript)
- 后端项目 (Node.js/Python/Go)
- 数据分析项目

### 2. CLAUDE.md 工程规范
在项目根目录下维护 `CLAUDE.md` 文件是目前 Agentic 编程的核心最佳实践。该项目提供了各种场景下的 `CLAUDE.md` 模板，指导 Claude：
- 理解项目的架构和目录结构
- 了解团队的编码规范和格式化要求
- 知道如何运行构建、测试和 lint 命令

### 3. 工作流 (Workflows)
指导用户如何将复杂任务拆解，以配合 Claude Code 的能力：
- 如何让它自主排查 Bug
- 如何让它进行跨文件的大型重构
- 如何让它阅读和理解尚未熟悉的第三方库代码

### 4. 常见陷阱与解决方案
- 解决 Context Window 溢出的问题
- 防止 AI "幻觉" (Hallucination) 和过度修改代码
- 解决死循环和重复尝试的问题

## 适用人群

该项目非常适合已经开始使用 `Claude Code`、`Cursor`、或 `OpenAI Agents` 等 AI 编程助手，并希望进一步提升 AI 生成代码质量和工作效率的开发者。

## 相关资源

- [Anthropic Claude Code 官方文档](https://docs.anthropic.com/claude/docs/claude-code)
- [Prompt Caching 技巧](https://docs.anthropic.com/claude/docs/prompt-caching)