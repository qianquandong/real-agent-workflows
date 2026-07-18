# Real Agent Workflows

**English** | [中文](./README.zh-CN.md)

> My real, running AI workflows — open-sourced one at a time.

This is not a tool list. Every folder here is a **workflow that actually runs on my computer**: trigger, steps, and output spelled out, plus a sanitized `SKILL.md`. A SKILL.md is just a plain-markdown playbook — **this repo is a guide, not a plugin, and it is not locked to any tool**. Replace a few placeholders and feed it to whatever agent you use.

Full tour (all 22 workflows, with context): **[The 22 AI workflows I actually run](https://realagentusecases.com/agent-101/03-ai-tools-workflows/)** (in Chinese)

> Per-workflow docs and SKILL.md files are currently written in Chinese. They are plain markdown — paste one into your agent and ask it to translate or adapt; the structure carries over as-is.

## Skill vs. workflow

- A **skill** is a capability: a playbook for doing one thing well, invoked on demand.
- A **workflow** is the full chain of trigger + steps + output. It fires on a schedule or an event and runs itself.

This repo is organized by **workflow**. Each one ships as a `SKILL.md` — a step-by-step playbook any agent can execute. Put it on a schedule and it becomes a workflow.

## Available now

| Workflow | One line | Status |
|---|---|---|
| [Obsidian · AI news input](./obsidian-ai-news-input/) | Turns the last 24 hours of AI news into a categorized briefing + content topic ideas in your Obsidian vault, daily | ✅ Ready |
| [Obsidian · Morning cockpit](./obsidian-morning-cockpit/) | Pulls three news sources + triages overnight email into a one-page morning briefing; you just tick checkboxes | ✅ Ready |
| [Obsidian · Favorites harvest](./obsidian-favorites-harvest/) | Weekly: grabs new saves from Xiaohongshu/Douyin favorites, filters out pure entertainment, transcribes into knowledge cards | ✅ Ready |
| [Obsidian · Inbox ingest](./obsidian-inbox-ingest/) | Paste any link (article / video / book) onto one page; it fetches or transcribes and files a knowledge card | ✅ Ready |
| [Obsidian · Script output](./obsidian-script-output/) (optional downstream) | Picks a topic from your vault and drafts a 90-second word-for-word script daily, in both English and Chinese | ✅ Ready |
| [Email triage](./email-triage/) | One trigger word: reads 24h of email, labels (Action Required / FYI), outputs a P0/P1/P2 to-do list | ✅ Ready |

Together they form a closed loop: **news, saves, and pasted links flow in (input) → a one-page briefing you approve with checkboxes (human gate) → material becomes scripts (output)**. The human only pastes links, ticks boxes, makes calls, and records on camera.

## Roadmap (numbers match the tour page)

**Fully automatic · scheduled**

| # | Workflow | Status |
|---|---|---|
| 01 | AI news archive (daily, 05:34) | ✅ Above |
| 02 | Morning cockpit: three sources + email triage → one-page briefing (daily, 06:11) | ✅ Above |
| 03 | Daily short-video script (daily, afternoon) | ✅ Above |
| 06 | Favorites harvest: Xiaohongshu/Douyin saves → filter → transcribe (weekly) | ✅ Above |

(04 long-video scripts are too coupled to private benchmark material to open-source; the inbox-link half of 05 nightly ingest has been extracted as its own workflow — see above.)

**Manually triggered · content pipeline**

| # | Workflow | Status |
|---|---|---|
| 07 | Vault → talking-head scripts (one command, several drafts) | In progress |
| 08 | Post-shoot auto-editing (Drive watch + timestamped B-roll overlays) | In progress |
| 09 | YouTube / Xiaohongshu / Douyin video → transcript | In progress |
| 10 | Viral topic generator (give it an industry, get a batch of angles) | In progress |

**Browser control · website & leads**

| # | Workflow | Status |
|---|---|---|
| 11-16 | Site build & deploy, DNS migration, Google Business Profile setup, SEO rounds + indexing, design-system redo, SEO/GEO for a client site | In progress |

**Decisions & odd jobs**

| # | Workflow | Status |
|---|---|---|
| 17 | Email → labels (Action Required / FYI) + to-do list | ✅ Above |
| 18-22 | AI meeting notes, business diagnosis, rental application review, ebook to Kindle, session archiving | In progress |

## How to use

This repo is a **guide, not a plugin**. Any agent tool works:

- **Claude Code**: copy a `SKILL.md` to `~/.claude/skills/<name>/SKILL.md` — it is picked up automatically; add a scheduled task to make it recurring
- **Codex / OpenCode / OpenClaw / Hermes / anything else**: feed the `SKILL.md` content to your agent as task instructions and use its own scheduling mechanism
- Either way: replace the placeholders listed at the top of each file → run once manually to check the output → then put it on a schedule

Also, the specifics inside these workflows are just **what I happen to care about**: swap the news sources, platforms, and categories for your own life. The structure is universal; the content is yours.

Don't install everything at once. **Pick the one closest to your actual work, run it for two weeks, and if you're still firefighting manually, delete it and rebuild.**

## Subscribe

One fully reproducible workflow breakdown per week (trigger, tools, steps, the mistakes): [realagentusecases.com](https://realagentusecases.com)

## License

MIT © Jack Qian
