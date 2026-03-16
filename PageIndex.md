# PageIndex

**GitHub**: https://github.com/VectifyAI/PageIndex

**Stars**: 21,836 ⭐ | **Forks**: 1,724

## 项目简介
`PageIndex` 是一个由 Vectify AI 提出的 **无向量 (Vectorless)、基于推理 (Reasoning-based)** 的 RAG（检索增强生成）框架。
针对传统基于向量的 RAG 在处理专业长文档时往往由于“语义相似度 ≠ 真实相关性”而导致检索不准确的问题，PageIndex 摒弃了传统的向量数据库和文本切块（Chunking）机制。它通过将长文档转化为结构化的“树状索引（Tree Index）”，并让大语言模型（LLMs）模拟人类专家的思维过程，在树状结构中通过多步推理进行检索。

## 核心特性
- **无向量数据库 (No Vector DB)**：彻底抛弃向量相似度检索，而是使用文档结构和 LLM 的推理能力来寻找目标信息。
- **无文本切块 (No Chunking)**：文档按照其自然的章节层级进行组织，而不是被强行切割成固定长度的人工片段。
- **类人检索模式 (Human-like Retrieval)**：模拟人类阅读和提取复杂文档知识的方式，通过“目录树”一步步向下钻取。
- **高可解释性与可追溯性 (Explainability and Traceability)**：检索过程基于显式推理，不仅摆脱了传统向量检索的“黑盒”和“玄学检索（Vibe retrieval）”问题，还能精确提供页码和章节的引用来源。

## 使用场景 (或 核心概念 / 架构)
非常适合处理超过 LLM 上下文限制、且需要领域专业知识和多步推理的长篇专业文档，例如：财务报告、监管申报文件（SEC Filings）、学术教科书、法律合同和技术手册。

**检索架构（两步走）**：
1. **构建索引**：将长文档（如 PDF 或 Markdown）解析并生成类似“目录”的**树状结构索引**。树的每个节点包含层级标题、页码范围和该段落的摘要。
2. **树搜索 (Tree Search)**：在用户提问时，系统将问题和树状索引提供给 LLM，让 LLM 通过推理决定应该深入查看哪个节点，层层递进直到找到最相关的原文段落。

*注：PageIndex 在针对长篇财务文档分析的基准测试 (FinanceBench) 中，取得了 98.7% 的业内领先准确率（大幅超越传统向量 RAG）。*

## 适用人群
- **AI/LLM 工程师与研究员**：苦恼于传统 Vector RAG 在长文档问答中频繁“幻觉”或找不到核心关键信息的开发者。
- **金融/法务/医疗等专业领域从业者**：需要对研报、财报、合同等长篇复杂文档进行高精度信息提取的团队。
- **Agent 应用开发者**：希望为自己的 Agent（通过 API 或 MCP）提供“人类阅读级”文档解析外挂的开发者。

## 相关资源
- [GitHub 仓库](https://github.com/VectifyAI/PageIndex)
- [官方主页](https://vectify.ai)
- [Chat 平台体验](https://chat.pageindex.ai)
- [Cookbooks & 教程](https://docs.pageindex.ai/cookbook/vectorless-rag-pageindex)