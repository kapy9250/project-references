# chrome-cdp-skill

**GitHub**: https://github.com/pasky/chrome-cdp-skill

**Stars**: 1985 ⭐ | **Forks**: 102

## 项目简介
`chrome-cdp-skill` 是一个让 AI 代理（Agent）能够直接访问并交互你当前正在运行的实时 Chrome 浏览器会话的工具。与传统的浏览器自动化工具（如新建一个隔离的、干净的浏览器实例）不同，它直接连接到你已经打开的标签页、已登录的账户以及当前的页面状态。

该工具开箱即用，无需安装复杂的浏览器自动化框架（不需要 Puppeteer），只需要在 Chrome 中开启一个调试开关即可。

## 核心特性
- **直接连接实时会话**：代理可以读取你已经登录的页面（如 Gmail、GitHub、内部工具），与你正在工作的标签页交互。
- **持久化守护进程机制**：为每个被访问的标签页生成一个轻量级的后台守护进程保持会话。有效避免了 Chrome "允许调试" 弹窗的频繁出现，并且即使在打开了 100+ 个标签页的情况下依然能够稳定运行（不会像许多基于 Puppeteer 的工具那样在枚举目标时超时）。
- **轻量且无依赖**：唯一运行依赖是 Node.js 22+，无需执行 `npm install`。
- **丰富的 CDP 指令支持**：通过命令行可以直接获取页面 DOM 树（精简无障碍树或完整 HTML）、截图、执行 JS、触发点击或输入、以及纯原生 CDP 命令透传。

## 使用场景 (或 核心概念 / 架构)
主要用于赋予 AI Agent (如 `pi`, `Claude Code`, `Cursor` 等) 真实的浏览器控制权。

**核心架构与原理**：
它直接连接到 Chrome 暴露的远程调试 WebSocket 端口。它不依赖 Puppeteer 等中间件。首次访问某个标签页时，它会启动一个守护进程维持连接状态。守护进程在 20 分钟无活动后会自动退出。如果浏览器的调试端口文件路径非标准，可通过环境变量 `CDP_PORT_FILE` 配置。

**使用示例**：
```bash
scripts/cdp.mjs list                              # 列出打开的标签页
scripts/cdp.mjs shot   <target>                   # 对目标标签页截图
scripts/cdp.mjs snap   <target>                   # 获取页面结构 (精简的语义化可访问性树)
scripts/cdp.mjs click  <target> "selector"        # 点击指定元素
scripts/cdp.mjs eval   <target> "expression"      # 在页面上下文中执行 JS
```

## 适用人群
- AI Agent 开发者和使用者，希望代理能直接在自己正在使用的浏览器环境中执行操作。
- 需要轻量级命令行浏览器 CDP 控制方案的自动化工程师。

## 相关资源
- [GitHub 仓库](https://github.com/pasky/chrome-cdp-skill)