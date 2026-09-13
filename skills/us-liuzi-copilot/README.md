<div align="center">

# 🇺🇸 美国留子 AI 生存副驾驶

### 不是“美国留学百科”，而是一个会告诉你 **现在该怎么办** 的 AI Skill。

[![Version](https://img.shields.io/badge/version-v3.0-111111.svg)](./SKILL.md)
[![Playbooks](https://img.shields.io/badge/playbooks-30%2B-2563eb.svg)](./references/)
[![Files](https://img.shields.io/badge/Markdown-49-16a34a.svg)](./references/)
[![License](https://img.shields.io/badge/license-MIT-black.svg)](../../LICENSE)

**适合：中国留学生 · 刚来美国的年轻人 · F-1 / OPT 人群 · 第一次独立生活在美国的人**

[开始使用](./SKILL.md) · [真实问题地图](./references/query-map.md) · [没人告诉我的美国常识](./references/unwritten-america.md) · [来源索引](./references/sources.md)

</div>

---

## 一句话定位

> **来美国以后，所有“我现在该怎么办”，都可以问它。**

用户不需要先知道自己属于“住房”“金融”“移民”哪个分类。直接说问题：

- 🏠 帮我选公寓
- 🚗 帮我买第一辆车
- ✈️ 帮我找最便宜的回国机票
- 💳 帮我办第一张信用卡
- 🍜 告诉我附近中国人爱吃什么
- 🛋️ 帮我收一套二手家具
- 👯 帮我找附近华人群/活动
- ❤️ 帮我找对象
- 📦 帮我找靠谱海运
- 🏥 我生病了该去哪
- 💼 帮我找实习
- 🇺🇸 我这个情况会不会影响 F-1
- 💰 帮我把每个月生活费降下来
- 🗺️ 这个周末带我出去玩
- 🤝 帮我真正融入美国

---

## 它和普通“美国攻略”有什么不同

| 普通攻略 | 这个 Skill |
|---|---|
| 告诉你有哪些租房网站 | 直接按学校、通勤、预算筛公寓并算 all-in |
| 讲怎么买车 | VIN → title → recall → insurance → PPI → OTD 后再决定 |
| 列机票网站 | 比 gateway、自转机、行李、转机风险和真实总成本 |
| 解释信用分 | 根据 SSN/ITIN/信用历史告诉你第一步办什么 |
| 列餐馆 | 根据实时位置、口味、距离和最近评论找 |
| 说“去 networking” | 找学校/城市/行业入口，再给第一条 outreach |
| 给移民经验贴 | 高风险问题优先查 DHS/USCIS/学校 DSO 等官方来源 |

核心逻辑：**先知道你的情况 → 查最新信息 → 给 2–3 个方案 → 算总成本和风险 → 告诉你现在做什么。**

---

## 🧠 16 个超级问题池

`刚落地` · `租房` · `水电网` · `家具二手` · `买车/租车` · `驾照/DMV` · `银行/信用` · `省钱` · `吃饭` · `看病/保险` · `交朋友` · `谈恋爱` · `娱乐/旅行` · `国内↔美国物流` · `实习/找工作` · `身份/毕业以后`

完整真实问法见：[`references/query-map.md`](./references/query-map.md)

---

## 🔥 几个典型行动流

### 🏠 “我刚来 Dallas，预算 $1,400，没有车，怎么租？”

```text
学校/工作地点
  ↓
通勤半径
  ↓
实时公寓 inventory
  ↓
base rent + mandatory fees + utilities + parking + commute
  ↓
no-credit application packet
  ↓
最近评论 / 安全 / 管理问题
  ↓
tour shortlist
  ↓
lease review checklist
```

### 🚗 “预算 $10k，第一辆车买什么？”

```text
用途 + 年里程 + zip code
  ↓
候选车型
  ↓
VIN / title / recall / history
  ↓
先拿 insurance quote
  ↓
PPI
  ↓
written OTD
  ↓
比较未来 12–24 个月总成本
```

### 🇺🇸 “F-1 可以做自媒体赚钱吗？”

不会直接回答一个粗暴的 yes/no。Skill 会先拆：

`你做了什么活动 → 收入性质 → 当前身份阶段 → 是否有工作授权 → 官方规则 → 是否需要 DSO / 律师确认`

---

## 🧰 文件结构

```text
SKILL.md                 # 主路由 + 判断规则
references/
  query-map.md           # 中国留子真实问法 taxonomy
  unwritten-america.md   # “没人告诉我的美国常识”
  housing.md             # 找房/租房
  car.md                 # 买车/二手车
  flights.md             # 回国机票
  immigration-school.md  # F-1/CPT/OPT/STEM OPT
  healthcare.md          # 看病/保险/EOB/bill
  money-credit.md        # 银行/信用
  social-dating.md       # 社交/约会
  shipping.md            # 海运/跨境物流
  ...                    # 30+ 场景 playbook
templates/               # 可直接复制的询价/决策/检查表
examples/                # 示例对话
```

---

## 🧭 研究和回答原则

1. **身份 / 税务 / 法律 / 医疗 / 安全：官方来源优先。**
2. **餐馆 / 公寓体验 / 社群：地图平台 + 最近社区体验。**
3. **机票 / 房租 / 活动 / 政策：需要时实时搜索。**
4. **所有价格尽量算 all-in，而不是广告价。**
5. **不可逆操作前设置 human gate：付钱、签约、提交、取消、发送。**
6. **最终必须回答“你现在下一步做什么”。**

---

## 🤖 怎么接到 Agent

把 [`SKILL.md`](./SKILL.md) 作为主操作说明，把 `references/` 当按需加载的知识库。

```text
用户一句自然语言
   ↓
SKILL.md 做意图路由
   ↓
加载对应 reference playbook
   ↓
需要动态信息时实时搜索 / 地图 / 比价
   ↓
输出：推荐 + 成本 + 风险 + 下一步
```

它不绑定某个模型。Claude Code、Codex、OpenCode、Hermes、OpenClaw 或其他支持工具调用的 Agent 都可以适配。

---

## ⚠️ 重要说明

这不是律师、移民顾问、医生、税务师或保险经纪人的替代品。涉及身份、工作授权、税务、法律、医疗和安全时，Skill 的职责是 **找到当前权威规则、解释风险、整理问题，并在需要时明确升级给 DSO / 律师 / CPA / 医疗专业人员。**

规则和价格会变，所以这套 Skill 有意把很多场景设计成“运行时重新查询”，而不是把 2026 年的一次搜索永久写死。

---

<div align="center">

### 从“刚下飞机”一直带到“毕业离开美国”。

**US 留子 AI 生存副驾驶 · v3.0**

</div>
