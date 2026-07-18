---
name: obsidian-morning-cockpit
description: 每早首页驾驶舱 · 三个信息源抓料 + Gmail 分类，组装成 Obsidian 里的一页早报，素材等人勾选
---

你在用户的电脑上维护他的 Obsidian「首页」——他每天早上唯一要看的一页。

> 使用前替换占位符：`<你的库路径>`、`<首页文件>`（如 `首页.md`）、`<你的关注领域>`（用来标注哪些新闻跟用户最相关，例如「AI agent、内容创作、本地生意」）。

## 首页的规矩（最重要）

首页可能还有其他小节（待办、其他任务写入的内容）。本任务**只改写自己负责的两节**：「待勾选的新素材」和「Gmail Action」，外加顶部日期。改写一节时写到下一个 `## ` 标题为止，**其余小节一个字都不碰**。多个定时任务共写一页时，这条规矩是不打架的前提。

## 步骤

1. **抓三源**：
   - a) AI 热点：aihot 公开 API（必须带浏览器 User-Agent，否则 403）：
     ```
     curl -sH "User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36" \
       "https://aihot.virxact.com/api/public/items?mode=selected&since=<24小时前ISO>&take=100"
     ```
     取当天精选，列 8-12 条最有价值的；纯噪音压成一行「其余」扫过，不隐藏。
   - b) GitHub trending：WebFetch `https://github.com/trending` 取 top 20，跟 `<你的关注领域>` 相关的标 ⭐。
   - c) 非 AI 大新闻：WebSearch 当天要闻（政治/经济/世界），不超过 10 条，必须带真实来源链接。

2. **去重**：对照台账文件（如库根的 `selected-topics.md`，一行一条：URL + 标题 + 日期），已入库的不再列。

3. **Gmail 分类**：用 Gmail MCP（`search_threads`）扫近 1 天收件箱（排除 promotions/social），分「必须看 / 必须回 / 可忽略」写进「Gmail Action」节，每条带 `https://mail.google.com/mail/#all/<messageId>` 直达链接。Gmail 工具不可用时，该节只写一行「⚠️ 今日 Gmail 未连上」，**绝不编造邮件**。

4. **组装首页**：重写「待勾选的新素材」节——每条新闻一行：标题 + 一句话 + 来源链接 + 复选框 `- [ ]`，跟 `<你的关注领域>` 强相关的加一句「👉 跟你最有关系」的理由。

## 铁律

- **不自动往素材库/知识库写任何条目**——素材入库必须等人在首页勾选（下游入库任务只处理勾中的）。
- 所有数字和标题必须来自真实抓取，绝不编造。
- 首页是给人看的早报，不是数据 dump：先说结论，链接放行尾。

## 怎么定时跑

注册为每日定时任务，设在用户起床前（作者设在 06:11）。如果搭配「AI 新闻输入」任务，让它先跑（比如 05:34），本任务组装首页时数据已就位。
