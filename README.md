<div align="center">

# ⚡ Real Agent Workflows

### Real AI playbooks for work, life, research, and automation.

**Not a prompt dump. Not a tool directory.**  
Every folder is a reusable workflow or skill with the trigger, decision logic, steps, guardrails, and output spelled out.

[![License: MIT](https://img.shields.io/badge/License-MIT-black.svg)](./LICENSE)
[![Format: Markdown](https://img.shields.io/badge/Format-Markdown-111111.svg)](#how-to-use)
[![Built for Agents](https://img.shields.io/badge/Built%20for-AI%20Agents-6f42c1.svg)](#how-to-use)
[![Language](https://img.shields.io/badge/Docs-English%20%2B%20中文-0ea5e9.svg)](./README.zh-CN.md)

[中文](./README.zh-CN.md) · [Full workflow tour](https://realagentusecases.com/agent-101/03-ai-tools-workflows/) · [Follow list](./FOLLOW.md)

</div>

---

## 🌟 Featured: US 留子 AI 生存副驾驶

> **来美国以后，所有“我现在该怎么办”，都可以问它。**

A Chinese-first survival copilot for international students and newcomers in the U.S. It is built around real questions — not encyclopedia categories.

| Ask it like this | What it actually does |
|---|---|
| 🏠 **帮我选公寓** | commute radius → live inventory → all-in cost → no-credit packet → review risk → lease checklist |
| ✈️ **帮我找最便宜的回国机票** | gateways → connection risk → baggage → self-transfer → true trip cost |
| 🚗 **帮我买第一辆车** | VIN → title → recall → insurance quote → PPI → written OTD → decision |
| 💳 **帮我办第一张信用卡** | SSN/ITIN/credit-history routing → starter options → credit-building rules |
| 🍜 **告诉我附近中国人爱吃什么** | location-aware restaurant search → recent reviews → cuisine fit → price/distance |
| 🛋️ **帮我收一套二手家具** | Marketplace search → scam/bedbug checks → negotiation → pickup plan |
| 👯 **帮我找附近华人群/活动** | campus + city + interest → real communities/events → low-friction first step |
| ❤️ **帮我找对象** | app/channel choice → profile → first-date norms → safety → intent filtering |
| 📦 **帮我找靠谱海运** | restricted-item screening → quote normalization → volumetric weight → customs → claims |
| 🏥 **我生病了该去哪** | ER vs urgent care vs PCP → network check → EOB/bill audit |
| 💼 **帮我找实习** | Handshake + LinkedIn + alumni + outreach + CPT/OPT guardrails |
| 🇺🇸 **这会不会影响 F-1？** | classify activity → check current official rules → flag DSO/lawyer escalation |

**49 Markdown files · 30+ actionable playbooks · 16 high-frequency problem pools · templates + examples + source index**

### → [Open the full US 留子 Copilot skill](./skills/us-liuzi-copilot/)
### → [Read `SKILL.md`](./skills/us-liuzi-copilot/SKILL.md)

---

## 🧭 What this repository is

A **skill** is a reusable capability: a playbook for doing one thing well on demand.  
A **workflow** is the full chain of trigger → steps → output, often scheduled or event-driven.

This repository contains both. Each one is intentionally plain Markdown so it can be adapted to Claude Code, Codex, OpenCode, Hermes, OpenClaw, or any other agent that can follow instructions and use equivalent tools.

## 🧩 Available now

| Project | Type | What it does | Status |
|---|---|---|---|
| [🇺🇸 US 留子 AI 生存副驾驶](./skills/us-liuzi-copilot/) | Skill | Housing, cars, flights, credit, food, health, social life, F-1/OPT, shipping, jobs, and U.S. life decisions | ✅ Ready |
| [📦 Move Address Manager](./skills/move-address-manager/) | Skill | Plans and tracks address changes across accounts and services when moving | ✅ Ready |
| [🧠 Obsidian · AI news input](./obsidian-ai-news-input/) | Workflow | Turns the last 24h of AI news into categorized notes + topic ideas | ✅ Ready |
| [☀️ Obsidian · Morning cockpit](./obsidian-morning-cockpit/) | Workflow | Pulls sources + triages overnight email into a one-page morning briefing | ✅ Ready |
| [⭐ Obsidian · Favorites harvest](./obsidian-favorites-harvest/) | Workflow | Converts saved Xiaohongshu/Douyin content into filtered knowledge cards | ✅ Ready |
| [📥 Obsidian · Inbox ingest](./obsidian-inbox-ingest/) | Workflow | Turns pasted articles/videos/books into organized knowledge cards | ✅ Ready |
| [🎬 Obsidian · Script output](./obsidian-script-output/) | Workflow | Drafts short-form scripts from the knowledge vault | ✅ Ready |
| [📧 Email triage](./email-triage/) | Workflow | Labels incoming mail and produces a P0/P1/P2 action list | ✅ Ready |

---

## 🚀 How to use

```text
1. Pick one skill/workflow close to a real problem you have.
2. Open its SKILL.md.
3. Give that file to your agent as operating instructions.
4. Map capability labels (web search, email, browser, files...) to your agent's tools.
5. Replace placeholders and run once manually.
6. Only then automate or schedule it.
```

**Claude Code** — copy a skill to `~/.claude/skills/<name>/SKILL.md`.  
**Codex / OpenCode / Hermes / OpenClaw / others** — feed the `SKILL.md` to the agent and map the required capabilities to equivalent tools.

> The tool names are intentionally generic. The logic should survive even when the agent stack changes.

---

## 🧠 Design principles

- **Action over explanation** — end with what the user should do next.
- **Fresh data when it matters** — prices, rules, schedules, availability, laws, and local recommendations should be checked live.
- **Official sources for high-risk topics** — immigration, taxes, healthcare, safety, and legal rules are not guessed from Reddit.
- **Community data for lived experience** — recent reviews and discussions are useful for quality-of-life judgment, not as legal authority.
- **All-in cost over sticker price** — rent, flights, cars, shipping, and subscriptions are compared on actual total cost.
- **Human gates for irreversible actions** — paying, signing, filing, booking, cancelling, or sending should be explicit.

---

## 🗺️ Roadmap

**Fully automatic / scheduled**
- AI news archive
- Morning cockpit
- Daily short-video script
- Favorites harvest

**Content pipeline**
- Vault → talking-head scripts
- Post-shoot auto-editing
- Video → transcript
- Viral topic generator

**Browser / business operations**
- Site build + deploy
- DNS migration
- Google Business Profile setup
- SEO/GEO rounds
- Lead and local-business workflows

**Life agents**
- More location-aware newcomer skills
- Personal admin / move / travel / finance playbooks
- More bilingual Chinese ↔ U.S. workflows

---

## 📚 More

- **36 AI creators worth following:** [FOLLOW.md](./FOLLOW.md)
- **Full workflow tour:** [realagentusecases.com](https://realagentusecases.com/agent-101/03-ai-tools-workflows/)
- **Weekly reproducible workflow breakdowns:** [realagentusecases.com](https://realagentusecases.com)

---

<div align="center">

### Build agents that finish the job.

MIT © Jack Qian

</div>
