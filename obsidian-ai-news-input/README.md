# Obsidian · AI 新闻输入

> 每天醒来之前，过去 24 小时的 AI 圈动态已经变成一份分好类的中文简报，躺在你的 Obsidian 库里。

## 这条工作流长什么样

| | |
|---|---|
| **触发** | 每天早上定时（作者设在 05:34），电脑开着就自己跑 |
| **步骤** | 拉取 AI 热点 API → 生成分类中文简报 → 提炼 3-5 个内容选题建议 |
| **产出** | `dailies/YYYY-MM-DD.md`，每条资讯带来源链接，选题附角度、受众、形式 |
| **人工** | 0 分钟 |

## 怎么装

1. Claude Code 用户：把 [`SKILL.md`](./SKILL.md) 复制到 `~/.claude/skills/obsidian-ai-news-input/SKILL.md`；其他 agent 工具见[根 README 的通用说明](../README.md#怎么用)
2. 替换文件里的两个占位符：`<你的库路径>`、`<简报文件夹>`
3. 手动跑一次确认产出符合预期，再挂成定时任务

## 依赖

- 任何能执行 markdown 指令的 agent 工具（作者用 Claude Code；Codex / OpenCode / OpenClaw / Hermes 同理）
- 一个 Obsidian 库（其实任何 markdown 文件夹都行）
- [aihot.virxact.com](https://aihot.virxact.com) 公开 API（无需注册；接口不可用时自动降级为 WebSearch）

## 常见问题

- **API 返回 403**：curl 没带浏览器 User-Agent，SKILL.md 里的命令已包含，别删。
- **想换数据源**：把第 1 步换成你自己的 RSS / API，其余步骤不用动——这条工作流的价值在「资讯 → 结构化简报 → 选题」这个结构，数据源随便换。

---

这条工作流的完整背景见 [我真实在跑的 22 条 AI 工作流](https://realagentusecases.com/agent-101/03-ai-tools-workflows/)（定时 · 01）。
