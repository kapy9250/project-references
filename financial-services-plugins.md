# Claude for Financial Services Plugins

**GitHub**: https://github.com/anthropics/financial-services-plugins

**Stars**: 5974 ⭐ | **Forks**: 661

## 项目简介
`financial-services-plugins` 是由 Anthropic 官方推出的开源插件集合，旨在将 Claude（包括 Claude Cowork 和 Claude Code）转变为金融服务领域的专家。这些插件为投资银行、股票研究、私募股权和财富管理等特定金融角色提供了预配置的技能、数据连接器、斜杠命令和子智能体。

通过集成 Model Context Protocol (MCP)，这些插件能够直接连接到如 S&P Global、Morningstar、FactSet、PitchBook 等主流金融数据终端，消除手动搜集数据的繁琐，从而实现从数据获取、财务分析到报告生成的端到端自动化工作流。

## 核心特性
- **领域特定插件 (Domain-Specific Plugins)**：按不同业务职能拆分，包括基础财务分析（Core）、投资银行、股票研究、私募股权和财富管理。
- **丰富的内置技能与命令**：包含 41 个技能和 38 个快捷命令（如 `/comps` 进行可比公司分析，`/dcf` 生成现金流折现模型，`/earnings` 生成盘后财报更新等）。
- **无缝的数据源连接 (MCP Integrations)**：内置了 11 个顶级金融数据提供商的 MCP 接口，可实时提取财报、定价、宏观数据和公司资料。
- **端到端工作流 (End-to-End Workflows)**：不仅限于问答，插件支持生成可以直接用于业务的输出文件，如填入 SEC 数据的 Excel 3 表模型、基于公司模板生成的 PowerPoint 融资演示文稿（Pitch Decks）以及 Word 格式的投资备忘录（IC Memos）。
- **高度可定制性**：基于简单的 Markdown 和 JSON 文件构建（无代码），机构可以轻松插入自有的术语库、内部估值模板和专有数据连接器。

## 使用场景 (或 核心概念 / 架构)
针对金融从业人员的日常深度分析与材料准备。

**典型用例**：
- **投资银行**：起草保密信息备忘录（CIM）、建立买家名单、运行并购模型、生成公司介绍。
- **股票研究**：撰写财报更新报告、追踪催化剂、起草晨会纪要。
- **私募股权**：进行项目筛选、执行尽职调查清单、撰写投资委员会（IC）备忘录、监控投资组合的 KPI。
- **财富管理**：准备客户会议材料、进行投资组合再平衡分析、挖掘税收亏损收割（Tax-loss harvesting）机会。

**架构**：
每个插件目录包含：
- `.claude-plugin/plugin.json`: 插件声明文件。
- `.mcp.json`: MCP 服务器连接配置。
- `commands/`: 用户可主动调用的斜杠命令。
- `skills/`: Claude 在相关场景下自动调用的领域知识与工作流指令。

## 适用人群
- **金融行业专业人士**（投行分析师、研究员、投资经理、财富顾问等）。
- 探索如何将大模型（LLM）深度集成到专业金融系统和工作流中的**企业 IT 与 AI 架构师**。
- 有意利用 MCP 协议对接私有数据源的**金融科技开发者**。

## 相关资源
- [GitHub 仓库](https://github.com/anthropics/financial-services-plugins)
- [Claude Cowork 产品页](https://claude.com/product/cowork)