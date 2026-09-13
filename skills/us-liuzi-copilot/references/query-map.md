# 16 个超级问题池：真实 Query → Agent 行动图

这一页不是科普目录，而是训练 Agent 识别留子真实表达。

## 1. 🛬 刚落地美国
真实问法：
- 下飞机第一件事干嘛？
- 没美国手机号怎么打 Uber？
- 中国手机卡还要不要保号？
- 没 SSN 能不能办美国手机号/银行？
- I-94 是啥？

Agent 动作：
到达机场/学校 → 临时联网 → 地面交通 → 美国号 → I-94/学校 check-in → 银行 → 住址 → 安全/2FA。
详见 `arrival.md`、`utilities.md`、`money-credit.md`。

## 2. 🏠 租房
真实问法：
- Zillow 靠谱吗？
- 没 SSN/credit score 怎么租？
- guarantor 是什么？
- I-20 能不能当资金证明？
- 这个 apartment 值不值？

Agent 动作：
定位/通勤 → 硬需求 → 实时库存 → all-in → 最近评论 → no-credit application packet → tour → lease review。
详见 `housing.md`。

## 3. 💡 水电网 / 入住
真实问法：
- 电怎么开？
- 水费谁交？
- Spectrum 还是 AT&T？
- renters insurance 必须买吗？
- 为什么浴室不能直接冲地？

Agent 动作：
读 lease → 区分 resident-open vs property-billed → 比 provider → 看 promo expiration → move-in checklist → home safety。
详见 `utilities.md`、`unwritten-america.md`。

## 4. 🛏️ 家具二手
真实问法：
- 床垫哪里最便宜？
- Marketplace 会不会被骗？
- 二手家具怎么砍？
- 毕业季哪里捡家具？
- U-Haul 怎么租？

Agent 动作：
Buy Nothing/校园/Marketplace → 估价 → 诈骗过滤 → 验货 → 议价 → 运输；跨州 mover 查 FMCSA。
详见 `secondhand-moving.md`。

## 5. 🚗 买车 / 租车
真实问法：
- 留学生第一辆车买什么？
- $10k 买 Toyota 还是 Honda？
- clean/salvage/rebuilt 是什么？
- dealer 会不会坑？
- 没 SSN 能贷款吗？
- 为什么保险这么贵？

Agent 动作：
先算是否需要车 → 车型池 → inventory → VIN/history/recall → 保险 → PPI → OTD → financing → registration。
详见 `car.md`。

## 6. 🪪 驾照 / DMV
真实问法：
- 中国驾照能开多久？
- IDP 有用吗？
- 没 SSN 怎么办？
- Road test 怎么约？
- 哪个 DMV 好过？

Agent 动作：
先确认州 → 只查州 DMV → document checklist → permit/knowledge/road test → 车辆要求 → REAL ID/州 ID。
详见 `dmv.md`。

## 7. 💳 银行卡 / 信用卡
真实问法：
- 没 SSN 能开 checking 吗？
- 第一张卡办 Discover 还是 Chase？
- 信用分多久到 700？
- 信用卡能不能刚刷完马上还？
- Zelle/Venmo 会不会收税？

Agent 动作：
开户文件 → checking → 账号安全 → 适合薄信用/无信用产品 → autopay → credit report → 反诈骗。
详见 `money-credit.md`、`taxes.md`。

## 8. 💰 省钱 / 羊毛
真实问法：
- Costco 值不值？
- Prime Student 怎么算？
- family plan 怎么拼？
- 什么东西别原价买？
- 回国机票怎么用积分？

Agent 动作：
先从固定支出砍：房/车/保险/手机/网/订阅 → 再做学生优惠和信用卡回馈；不能为了奖励制造消费。
详见 `saving.md`、`subscriptions.md`。

## 9. 🍜 吃饭
真实问法：
- 附近最好吃的中餐？
- 川菜/东北菜/奶茶/火锅在哪？
- H Mart/99 Ranch/Costco 买什么？
- 不会做饭怎么办？

Agent 动作：
实时本地搜索 → 根据中国胃细分菜系 → 开门状态/停车/排队/人均 → 1 首选 + 备选 → 3 家以上地图。
详见 `food.md`、`grocery-shopping.md`。

## 10. 🏥 看病 / 保险
真实问法：
- 发烧去哪？
- Urgent Care 和 ER 差多少？
- in-network 怎么看？
- EOB 是账单吗？
- 牙疼怎么办？
- 没保险怎么办？

Agent 动作：
先 triage → student health/telehealth/PCP → urgent care → ER/911；再核 insurance network、estimate、EOB/bill、financial assistance。
详见 `healthcare.md`。

## 11. 👯 交朋友 / 融入美国
真实问法：
- 怎么认识美国人？
- 为什么同学聊得挺好但不约我？
- 怎么找华人群？
- 周末大家干嘛？
- 一个人太无聊怎么办？

Agent 动作：
重复场景优先 → club/sport/volunteer/professional meetup → 本周只选 1–3 个 → 具体邀约 → 连续 6–8 周。
详见 `community.md`、`etiquette.md`。

## 12. ❤️ 谈恋爱
真实问法：
- Hinge/Bumble/Tinder 哪个适合我？
- 第一次 date 谁付钱？
- 怎么判断 hookup？
- 怎么认识中国留学生？

Agent 动作：
先确认 relationship goal → 线上+线下渠道 → profile → first-date plan → safety → boundaries → scam filtering。
详见 `social-dating.md`。

## 13. 🎉 娱乐 / 旅行
真实问法：
- 周末去哪？
- 没车怎么玩？
- Spring Break 去哪？
- road trip 怎么安排？
- 圣诞一个人去哪？

Agent 动作：
定位 + 时间 + 预算 + 有无车 → 实时天气/营业/活动 → 路线 → parking/reservation → 行程地图。
详见 `travel.md`。

## 14. 📦 国内 ↔ 美国物流
真实问法：
- 淘宝怎么寄美国？
- 海运哪家靠谱？
- 食品/药/电池能不能寄？
- 毕业东西怎么寄回国？

Agent 动作：
先列物品 → 禁限运筛查 → 箱规/重量 → courier/air/sea → 同口径询价 → customs/insurance/last-mile → 总价。
详见 `shipping.md`。

## 15. 💼 实习 / 找工作
真实问法：
- 大一怎么找 internship？
- Handshake 有用吗？
- LinkedIn 怎么 cold message？
- 无薪实习要 CPT 吗？
- networking 到底怎么搞？

Agent 动作：
先 work authorization → target role → resume → school platform/Handshake → alumni/networking → applications → interview → offer。
详见 `jobs.md`、`immigration-school.md`。

## 16. 🇺🇸 身份 / 毕业以后
真实问法：
- F-1 能不能兼职？
- 自媒体能赚钱吗？
- 能开公司吗？
- 能收 1099 吗？
- OPT unemployment days 怎么算？
- STEM OPT / H-1B 怎么办？

Agent 动作：
**不凭经验直接 yes/no。** 当前身份 → 当前授权 → 活动性质 → 是否“工作/服务/收入” → DHS/USCIS/SEVP 当前规则 → DSO/律师需要确认的点。
详见 `immigration-school.md`。
