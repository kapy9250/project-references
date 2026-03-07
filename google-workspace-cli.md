# Google Workspace CLI

**GitHub**: https://github.com/googleworkspace/cli

**Stars**: 14,229 ⭐ | **Forks**: 488

## 项目简介

Google Workspace CLI 是一个命令行工具，旨在为人类用户和 AI 智能体提供对所有 Google Workspace 应用的直接程序化访问能力。

## 支持的应用

- **Gmail**: 邮件管理、过滤、标签、自动回复
- **Google Drive**: 文件管理、共享、权限控制
- **Google Calendar**: 事件创建、会议安排、空闲检测
- **Google Sheets**: 数据读写、公式操作
- **Google Docs**: 文档创建、编辑、共享
- **Google Meet**: 会议创建与管理
- **Google Chat**: 消息发送、空间管理
- **Google Tasks**: 任务管理
- **Google Slides**: 演示文稿创建
- **Google Forms**: 表单创建与响应收集

## 核心特性

### 1. 即装即用
```bash
npm install -g @googleworkspace/cli
gws auth setup
```

### 2. 50+ 预构建智能体技能
CLI 附带 50 多个预构建的 Agent Skills，覆盖了常见的办公自动化场景：
- 自动归类邮件并归档
- 从 Sheet 读取数据发送个性化邮件
- 批量创建日历事件
- 生成财务报告
- 管理 Drive 文件权限

### 3. AI Agent 深度集成
- 支持与 Claude、ChatGPT、Cursor 等主流 AI 智能体无缝配合
- 可通过自然语言指令让 AI 完成复杂的 Workspace 任务

### 4. 动态生成
工具通过 Google Discovery Service 动态构建，确保与 Google API 保持同步。

## 与 OpenClaw 集成

如果使用 OpenClaw，可以快速链接技能：
```bash
ln -s $(pwd)/skills/gws-* ~/.openclaw/skills/
```

## 使用示例

```bash
# 检查 Drive 中外部共享的文件
gws drive check-external-sharing

# 查找下周与客户的1小时空闲时间
gws calendar find-free-time --duration 60 --participants client@example.com

# 导出本月所有客户邮件并保存到 Doc
gws gmail export --query "from:@client.com --month this" --output doc
```

## 相关资源

- [官方文档](https://github.com/googleworkspace/cli)
- [NPM 包](https://www.npmjs.com/package/@googleworkspace/cli)
- [技能市场](https://github.com/googleworkspace/cli/tree/main/skills)
