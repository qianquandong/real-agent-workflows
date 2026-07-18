---
name: obsidian-ai-news-input
description: 每日 AI 热点采集 · 定时把过去 24 小时的 AI 圈动态整理成中文简报，写进 Obsidian，并附 3-5 个内容选题建议
---

你在用户的电脑上执行每日 AI 资讯采集任务，目标是一个 Obsidian 库。

> 使用前替换两个占位符：`<你的库路径>`（Obsidian 库的绝对路径）、`<简报文件夹>`（库内存放每日简报的相对路径，例如 `dailies`）。

## 目标

拉取过去 24 小时的 AI 圈热点，生成当天的中文简报，并给出 3-5 个内容选题建议（假设用户是内容创作者；不是的话删掉选题这步即可）。

## 执行步骤

1. **拉数据**：调用 aihot 公开 API 获取最近 24 小时精选资讯：

   ```
   curl -sH "User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36" \
     "https://aihot.virxact.com/api/public/items?mode=selected&since=<24小时前的ISO时间>&take=100"
   ```

   注意：**必须带浏览器 User-Agent，否则 403**。接口无数据或报错时，改用 WebSearch 搜当天 AI 热点兜底，保证简报不开天窗。

2. **写简报**：在 `<你的库路径>/<简报文件夹>/` 下创建 `YYYY-MM-DD.md`。全文中文，按类别分组（模型发布 / 产品发布 / 行业动态 / 论文 / 技巧与观点），每条含：中文标题、一句话摘要、来源链接（URL 必须保留）。带 frontmatter：`type: daily`、`domain: AI`、`status: archived`、`created`、`tags`。

3. **提炼选题**：从当天资讯里挑出有内容价值的故事（争议、突破、趋势转折），在文件末尾写 3-5 个选题建议，每条注明角度、受众、形式。选题只是灵感，不当成结论。

4. **收尾汇报**：一句话说明当天热点数量与推荐选题。

## 语言要求

- 全文自然中文，读起来像人写的：短句、无排比套话、无翻译腔。
- 技术术语与品牌名保留原形：AI、LLM、GPT、API、RAG、agent、Token、prompt、OpenAI、Anthropic、Claude、GitHub 等。

## 铁律

- 每条资讯必须来自真实抓取，**绝不编造**；抓不到就写明「今日数据源不可用」。
- 简报是资讯归档，不是已验证的知识——不要把它写成确定性结论。

## 怎么定时跑

在 Claude Code / Claude 桌面端里把本 SKILL.md 注册为定时任务（scheduled task），建议每天早上内容创作开始前跑（作者设在 05:34）。电脑关机错过的话，下次开机手动补跑一次即可。
