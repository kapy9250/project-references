# agent-cli

**GitHub**: https://github.com/Nunchi-trade/agent-cli

**Stars**: 240 ⭐ | **Forks**: 86

## 项目简介
`agent-cli` 是一个面向 Hyperliquid 的自主交易 Agent 框架，内置 14 种策略（做市、套利、趋势/信号、风险管理等），并提供从策略执行到风控与复盘的完整闭环。

项目不仅可作为独立 CLI 使用，也可作为 Claude Code Skill、OpenClaw AgentSkill 或 MCP Server 运行，适合把“交易策略 + Agent 自动化工作流”整合到同一套可部署系统中。

## 核心特性
- **14 个内置策略**：覆盖做市、资金费率套利、基差套利、动量突破、均值回归、对冲与 RFQ 等主流策略类型。
- **APEX 多槽位编排**：支持多策略组合与自动化调度，便于构建无人值守的交易流水线。
- **Guard 动态止损 + REFLECT 夜间复盘**：将风险控制与策略复盘模块化，形成可持续优化的运行闭环。
- **多形态集成**：同一代码库可作为 CLI、Skill、MCP Server 运行，便于接入不同 Agent 生态。
- **面向 Agent 的上手流程**：README 提供“零提示”命令路径，降低部署与验证门槛。

## 使用场景 (或 核心概念 / 架构)
适用于希望在 Hyperliquid 上快速搭建自动化交易系统的开发者/研究者，尤其是需要“策略执行 + 风控 + 编排 + 复盘”一体化能力的团队。

典型使用流程：

```bash
git clone https://github.com/Nunchi-trade/agent-cli.git && cd agent-cli
bash scripts/bootstrap.sh
hl wallet auto --save-env
hl setup claim-usdyp
hl builder approve
hl apex run --mock --max-ticks 5
```

架构层面可理解为：
- **策略层**：多类交易策略（MM/Arb/Signal/Risk）
- **执行层**：统一 CLI 执行与参数管理
- **编排层**：APEX 进行多策略调度
- **评估层**：REFLECT 复盘并输出优化建议

## 适用人群
- 想在 Hyperliquid 上做自动化交易实验的量化开发者
- 需要 Agent-native 交易基础设施的 AI/交易系统工程师
- 想把 Claude/OpenClaw/MCP 与真实策略执行连接起来的技术团队

## 相关资源
- [官方文档](https://docs.nunchi.trade)
- [GitHub 仓库](https://github.com/Nunchi-trade/agent-cli)
- [Research](https://research.nunchi.trade)
- [Discord](https://discord.gg/nunchi)
