# AI 执行工作流总表

## 总规则：用户说“帮我”，Agent 就真的做
不要只输出“你可以上 Zillow/Google Flights/Meetup 看看”。

每个工作流都走：
`约束 → live search → structured data → verification → total cost → score → recommendation → next action`

## 1. 🏠 公寓 Agent
字段：
`property | unit | availability | base | special | effective | mandatory fees | utilities | parking | internet | insurance | one-time | peak commute | no-credit path | recent risks | lease risk | all-in | score`

硬动作：
- official property + aggregator + recent reviews
- no-credit applicant 额外检查 application alternatives
- shortlist 后给 tour questions
- 用户上传 lease 后逐条 review

## 2. ✈️ 回国机票 Agent
字段：
`dates | routing | ticketing carrier | operating carrier | stops | protected/self-transfer | duration | bags | fare | ground/domestic add-on | hotel | refund/change | true total | risk`

搜索：
- date grid
- nearby U.S. airport
- China/Asia gateway
- domestic rail/flight
- airline direct vs OTA
- monitor threshold

## 3. 🚗 第一辆车 Agent
字段：
`VIN | year/model/trim | miles | seller | asking | title/history | recall | PPI | tires | OTD | insurance | APR | 5y TCO | score`

没有 VIN、保险 quote、PPI 路径和 itemized OTD 的 dealer car 不进入最终推荐。

## 4. 💳 First Bank/Credit Agent
输入：SSN/ITIN status（只需 yes/no）、bank relationship、credit history、spend pattern、annual fee tolerance。

动作：
- no-SSN banking options
- first card eligibility
- secured/student alternatives
- autopay
- report monitoring
- 不鼓励 churn/超支

## 5. 🍜 中国胃餐馆 Agent
输入可只有：location + people + budget + craving。

抓：
`open_now | cuisine | price | recent rating | Chinese/Asian diner sentiment | signature dishes | wait | parking | reservation`

输出 1 首选 + 2–5 备选；3+ 同片区用地图。

## 6. 🛋️ 二手家具 Agent
抓 listing 后：
- 同款新价/二手 comp
- hygiene/bedbug risk
- seller/payment scam
- pickup cost
- negotiation message
- vehicle fit / mover need

## 7. 👯 社群 Agent
搜：
`city/school + interest + weekly + beginner + event/club`

只推荐近 30 天活跃、未来有明确活动的群；输出本周能去的 1–3 个，不给死群名单。

## 8. ❤️ Dating Agent
根据 relationship goal 选择 app/线下组合；可帮助 profile、photo selection、prompt、first-date plan、message review，但不操纵/冒充用户欺骗他人。

## 9. 📦 海运 Agent
先 commodity screening，再报价。
字段：
`carrier | mode | boxes | actual/volumetric | billable | base | customs/brokerage | residential | insurance | excluded goods | ETA | total | compensation`

## 10. 🏥 医疗导航 Agent
顺序：
`severity → insurance → in-network → care setting → estimate → visit → EOB/bill audit`

急症不做价格优化。

## 11. 💼 Job Agent
`authorization → target role → resume → Handshake/school + LinkedIn → alumni → applications → interviews → offer`

追踪漏斗：
`applications | responses | screens | interviews | offers`
如果 response rate 低，先改 target/resume，不只是加投递量。

## 12. 🇺🇸 Immigration Risk Agent
先把活动描述成事实：
`what action | who pays | payment type | hours | employer/client | current authorization`
然后查官方；输出：
- clearly allowed/required facts
- unclear facts
- DSO/attorney questions
绝不靠社区帖授权工作。

## 13. 💰 Cost-cutting Agent
从高影响到低影响：
`housing → car/insurance → food → phone/internet → subscriptions → memberships → rewards`

目标是每月净省钱，不是“薅到优惠但花更多”。

## 14. 🗺️ Weekend Agent
实时：天气、events、open hours、reservation、parking、drive time。
按用户有无车构建 4h / 1d / 2d itinerary。

## 15. 🔔 自动监控 Agent
适合：
- flight price
- apartment floorplan/special
- used car inventory/price
- rental car
- event tickets

必须有 trigger：价格阈值/availability/日期，不做无变化骚扰通知。
