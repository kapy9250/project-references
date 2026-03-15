# agency-agents

**GitHub**: https://github.com/msitarzewski/agency-agents

**Stars**: 45480 ⭐ | **Forks**: 6789

## 项目简介
`agency-agents` 是一个提供“一整套 AI Agent 专家团队”的提示词与角色预设集合。每个 Agent 都被精心设计为具有独特的身份、沟通风格、工作流和可交付成果的特定领域专家，而不是泛泛的提示词模板。

从前端开发、安全工程师到 UI 设计师、UX 研究员，甚至包含营销和运营领域的细分角色，该项目旨在让你能够在各种 AI 编程助手（如 Claude Code, Cursor, Aider, Windsurf 等）中快速“雇佣”专属专家来辅助完成任务。

## 核心特性
- **专业化预设 (Specialized)**：每个 Agent 在特定领域具有深度专业知识（如：Autonomous Optimization Architect、Solidity Smart Contract Engineer 等）。
- **个性化驱动 (Personality-Driven)**：具有独特的语气、沟通风格和解决问题的方法。
- **目标与交付物导向 (Deliverable-Focused)**：不仅提供指导，还注重提供真实的代码、严谨的流程和可衡量的结果。
- **多工具兼容 (Multi-Tool Integrations)**：提供脚本一键将预设转换为适用于 Claude Code、Cursor、Copilot、Aider 和 Windsurf 的格式。

## 使用场景 (或 核心概念 / 架构)
当你面对一个需要特定领域专家（如进行安全代码审查、数据库调优或 UI 设计验证）的任务，但团队内缺乏相应人手时，可以加载对应 Agent 的 `.md` 规则文件到你的 AI 工具中。

**典型用法 (Claude Code 示例)**:
```bash
# 将 agents 复制到 Claude Code 目录
cp -r agency-agents/* ~/.claude/agents/
```
随后在对话中激活："Hey Claude, activate Frontend Developer mode and help me build a React component"。

项目结构按领域划分，如：
- `engineering/`（涵盖前端、后端、DevOps、数据工程等）
- `design/`（涵盖 UI、UX、品牌等）
- `paid-media/`（涵盖 PPC 策略等）

## 适用人群
- 使用 AI 代码助手（Claude Code, Cursor 等）的独立开发者与小型团队。
- 希望提升 AI 对话输出专业度和一致性的 Prompt 工程师与架构师。
- 需要临时“聘用”虚拟专家来补齐团队技能短板的项目经理。

## 相关资源
- [GitHub 仓库](https://github.com/msitarzewski/agency-agents)
