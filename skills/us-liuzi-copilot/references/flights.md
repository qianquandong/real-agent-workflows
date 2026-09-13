# ✈️ 帮我找最便宜的回国机票 Playbook

## 用户真正要的不是“最低票价”
目标是：**在可接受风险内，最低真实总成本。**

## 最小输入
- U.S. origin city/airport
- China final destination
- date window / flexibility
- max stops
- max total duration（如有）
- checked bags
- 能否用高铁/国内段
- visa/transit constraints
- points/card preference（用户主动提供时）

## 搜索矩阵
### 1. 最终目的地直搜
例如 DFW → CSX。

### 2. 日期网格
- ±3 days 默认
- 寒暑假/春节/圣诞等可扩 ±7–14 days

Google Flights 支持 price tracking、date grid/price graph，并可显示 “Best” 与更低价但更折腾的 “Cheapest” 选项；动态界面每次实时查。

### 3. Origin 替代机场
如果用户能接受地面/短程飞行：
- 同城多机场
- 邻近大 hub
但必须加地面/国内 reposition 成本。

### 4. 中国/亚洲 gateway strategy
比较：
- 直接到最终城市
- 到 PVG/SHA / PEK/PKX / CAN / SZX / HKG 等，再高铁/国内航班
- 合理的 NRT/HND/ICN/TPE 等转机（取决于路线/签证/时刻）

不能只看到 base fare 便宜就推荐。

## 联程 vs Self-transfer
默认优先 protected itinerary。

Self-transfer 必查：
- 同一 ticket/PNR 吗？
- checked bag through-check 吗？
- 是否要入境/重新安检？
- 是否换机场？
- first flight delay 谁承担 missed connection？
- 需要多大 buffer？
- transit visa？
- overnight hotel？

省 $100 但增加一晚酒店 + 重新托运 + missed-flight 风险，通常不是真便宜。

## 真总价公式
`ticket + bags + seat + OTA/service fee + airport transfer + hotel + China domestic segment + food + visa/transit + risk buffer`

## 买票渠道
默认优先：
1. 用 Google Flights/ITA/搜索工具发现
2. 比 airline direct price
3. OTA 只有在节省显著且售后风险可接受时考虑

复杂国际票/多段票，航司直营通常更好改。

## 行李
逐段核对：
- checked allowance
- weight/piece concept
- partner/codeshare operating carrier
- separate ticket baggage rules
- domestic China leg

## 美国 DOT 关键消费者规则
### 24 小时规则
对符合条件、至少提前 7 天购买的机票，美国 DOT 要求 airlines 提供 **24-hour cancellation/refund 或 24-hour hold** 的一种选择；规则细节和 OTA 适用性要实时查，不能粗暴说“所有票都能 24 小时退”。

### Airline cancellation/significant change
如果航空公司取消或发生符合 DOT 定义的 significant change，而乘客不接受替代方案，可能有 refund rights。DOT 当前规则对重大时间变化、机场变化、额外转机、降舱等有具体定义；每次按最新页面核对。

## 回国票特殊检查
- 中国护照/旅行证件有效性
- transit country visa
- 港澳转接规则
- landing 后高铁最后一班
- 国内段 baggage
- overnight arrival
- 春运/节假日地面交通

## 价格监控
保存：
`route | date range | max stops | max duration | bags | preferred gateways | target price | current best`

提醒条件不是“每天发一条”，而是：
- 跌破 target
- 比 current best 明显下降
- 出现更少转机/更短时长且成本接近的路线

## Agent 输出
`路线 | dates | fare | bags | total duration | stops | self-transfer | ground/domestic leg | cancellation | true total | risk | score`

## 来源
- Google Flights help: https://support.google.com/travel/answer/6235879
- DOT Buying a Ticket: https://www.transportation.gov/individuals/aviation-consumer-protection/buying-ticket
- DOT Refunds: https://www.transportation.gov/individuals/aviation-consumer-protection/refunds
- DOT Automatic Refund Rule: https://www.transportation.gov/briefing-room/what-airline-passengers-need-know-about-dots-automatic-refund-rule
