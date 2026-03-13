# Scrapling

**GitHub**: https://github.com/D4Vinci/Scrapling

**Stars**: 29212 ⭐ | **Forks**: 2204

## 项目简介
Scrapling 是一个自适应的网页抓取框架，能够处理从单个请求到大规模爬虫的各种任务。它具有极快的速度，能自动学习网站结构变化并在页面更新时重新定位元素，同时它的提取器（fetchers）天然可以绕过如 Cloudflare Turnstile 等反爬虫系统。

## 核心特性
- **自适应解析 (Adaptive Parsing)**: 学习网站更改，在页面更新时自动重新定位元素，确保爬虫不会因简单的 UI 改变而失效。
- **无感抓取 (Stealth Mode)**: 提取器内置高级隐身功能和指纹伪装，开箱即可轻松绕过各种反爬虫系统（如 Cloudflare 的 Turnstile 和 Interstitial）。
- **完整爬虫框架**: 提供类似 Scrapy 的 Spider API，支持并发抓取、跨域限制、暂停/恢复、流式传输（Streaming Mode）以及多会话类型的路由。
- **动态加载支持**: 可以通过 Playwright的 Chromium 或 Google Chrome 执行全浏览器自动化，适用于动态渲染内容的网站。
- **AI 辅助 (MCP Server)**: 内置 MCP Server，利用 Scrapling 先提取目标内容再传给 AI（如 Claude/Cursor），加速操作并降低 Token 消耗。

## 使用场景 (或 核心概念 / 架构)
Scrapling 适用于从简单页面数据提取到复杂的企业级并发网络爬虫的构建。可以在不写一行代码的情况下通过命令行使用，也可在代码里处理从静态请求到自动化无头浏览器的需求。

例如简单的自适应解析：
```python
from scrapling.fetchers import StealthyFetcher

StealthyFetcher.adaptive = True
p = StealthyFetcher.fetch('https://example.com', headless=True)
# 收集在网站结构改变下仍能存活的数据
products = p.css('.product', adaptive=True)
```

## 适用人群
数据工程师、网页抓取开发者、AI Agent 开发者。

## 相关资源
- [官方文档](https://scrapling.readthedocs.io)
- [GitHub 仓库](https://github.com/D4Vinci/Scrapling)