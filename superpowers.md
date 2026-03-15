# Superpowers

**GitHub**: https://github.com/obra/superpowers

**Stars**: 85552 ⭐ | **Forks**: 6722

## 项目简介
`superpowers` 是一个为各类 AI 编程助手（如 Claude Code、Cursor、Codex、Gemini CLI 等）提供的一整套**软件开发工作流与 Agentic Skills 框架**。
它通过预设一系列可组合的“技能（Skills）”，改变了 Agent 拿到需求就直接写代码的习惯，强制其遵循规范的工程流程（如 TDD 测试驱动、系统化调试、多阶段代码审查和基于 Subagent 的拆解开发），从而让 AI 能够稳定、自主地工作几个小时而不偏离目标。

## 核心特性
- **标准化的开发工作流 (The Basic Workflow)**：包含从 `brainstorming`（需求确认） -> `using-git-worktrees`（隔离开发环境） -> `writing-plans`（拆分任务） -> `subagent-driven-development`（分派子 Agent 迭代） -> `finishing-a-development-branch`（合并清理）的完整链路。
- **强制测试驱动开发 (TDD)**：严格执行 Red-Green-Refactor 循环，确保先写出失败的测试用例，再编写最小实现代码，任何未经测试验证的代码都会被删除。
- **系统化调试 (Systematic Debugging)**：提供 4 阶段的根本原因分析流程（包含追踪、深度防御、基于条件的等待等技术），并要求 `verification-before-completion`（修复前必须验证）。
- **广泛的平台兼容性**：支持作为官方插件或扩展在 Claude Code、Cursor、Codex、OpenCode 和 Gemini CLI 中安装使用。

## 使用场景 (或 核心概念 / 架构)
当你觉得现有的 AI 编程助手在处理复杂需求时缺乏计划性、容易写出不带测试的意大利面条代码、或者在遇到 Bug 时只会盲目试错时，可以使用 Superpowers。

安装后，只需像平时一样唤醒 Agent，例如输入 `"help me plan this feature"`。此时 Agent 会自动激活框架，按照以下步骤运行：
1. 和你确认设计并输出文档。
2. 制定一份初级工程师都能看懂的详尽实施计划。
3. 把任务切分成 2-5 分钟的小块。
4. 调度子 Agent 逐个任务去执行（写测试 -> 写代码 -> Code Review -> 提交），全过程高度自治。

## 适用人群
- 使用 Claude Code、Cursor 等 AI 编码工具的独立开发者及工程师。
- 希望规范 AI 助手生成代码的质量，强制执行测试驱动开发的团队。
- 研究 Agent 工作流和工程化落地的 AI 开发者。

## 相关资源
- [GitHub 仓库](https://github.com/obra/superpowers)
- [Claude Code Marketplace](https://claude.com/plugins/superpowers)
