# 🚗 第一辆车 / 二手车 / 新车 / 租车 Playbook

## 先回答“到底要不要买”
Agent 先算 12–24 个月：

`买车总成本 = depreciation + tax/title/registration + insurance + financing interest + fuel/charging + maintenance/tires + parking/tolls`

对比：
`rideshare + transit + occasional rental + delivery + time cost`

学校附近、短期停留、保险极高时，买车未必更省。

## Step 1：建立车型池
输入：
- OTD cash budget / monthly all-in budget
- commute
- annual mileage
- snow/heat/terrain
- parking
- passengers/cargo
- expected ownership years
- insurance tolerance

第一辆车通常更看：可靠性、零件/维修网络、保险、保值，而不是“配置最多”。

## Step 2：搜本地 inventory
平台只是发现线索。每台候选抓：
`year | make/model/trim | mileage | VIN | asking | dealer/private | title | accident | owners | location`

## Step 3：VIN 三件套
1. vehicle history report（事故/title/里程线索）
2. NHTSA recall lookup
3. maintenance/service records（有则）

history report 不能替代机械检查。

## Title 基础
常见词：clean / salvage / rebuilt / flood / lemon/buyback 等，但定义和 registration/insurance consequences 按州不同。

默认新手不推荐 salvage/rebuilt，除非用户非常了解车况、保险/注册限制和 resale risk。

## Step 4：先拿保险 quote，再决定车
年轻驾驶员、无美国 insurance history、新驾照时，不同 VIN/车型保费差距可非常大。

Quote 时尽量同一 coverage 参数比较，不要只拿 liability-only 和 full coverage 混在一起。

## Step 5：试驾
- 冷启动
- warning lights
- acceleration/shift
- brake vibration/noise
- steering alignment
- highway speed
- AC/heat
- camera/sensors
- tire tread/uneven wear
- leaks/smell

## Step 6：PPI
找独立 mechanic 做 pre-purchase inspection。
如果卖家/dealer 坚决不允许合理 PPI，风险明显上升。

## Step 7：Dealer 只谈 OTD
要 itemized written quote：
`sale price + tax + title/registration + doc/dealer fees + mandatory? add-ons = OTD`

### 不要先谈月供
月供可以通过更长 term 做低，但总利息显著提高。

### 常见 add-on
- VIN etching
- paint/fabric protection
- nitrogen
- service contract
- tire/wheel
- anti-theft/tracker

要求逐项价格、是否 optional、能否 remove。

## FTC Buyers Guide
美国经销商销售大多数 used car 时受 FTC Used Car Rule 约束，需要 Buyers Guide，说明 as-is / warranty 等。合同中的 warranty promise 必须落书面。

## “买完三天能退车”是常见误区
不要默认汽车购买有全国统一 3-day cooling-off。退车/取消权取决于州法、dealer policy、合同和具体交易。买前确认，不要靠“回头再退”。

## Financing
比较：
- credit union
- bank
- dealer financing

统一比较：
`APR | term | amount financed | total of payments | prepayment penalty(if any)`

无 SSN/无信用历史时可融资与否完全取决于 lender；不要为了获批接受不可承受 APR。

## Private-party 交易
州 DMV 实时核对：
- title 是否在卖家名下
- lien / lien release
- odometer disclosure
- bill of sale
- tax
- temp permit/tag
- inspection/emissions
- registration deadline

钱交出前确认 title transfer 路径。

## 租车
### 真正 checkout total
`base + taxes + airport surcharge + under-25 + additional driver + one-way + toll plan + fuel + insurance + roadside`

### 保险
先看：
- 你自己的 auto policy
- 信用卡 rental coverage 的 primary/secondary、车型/国家/租期 exclusions
- rental company LDW/CDW / liability

不要默认“信用卡全包 liability”。

### 取车拍视频
车四周 + 轮毂 + 玻璃 + interior + fuel/charge + mileage。

## Agent 输出
`VIN/车型 | asking | OTD | market comp | title/history | recall | PPI | insurance/mo | finance | 5y cost | red flags | score`

## 来源
- FTC used car dealer guide: https://consumer.ftc.gov/articles/buying-used-car-dealer
- FTC auto financing/leasing: https://consumer.ftc.gov/articles/financing-or-leasing-car
- FTC renting a car: https://consumer.ftc.gov/articles/renting-car
- NHTSA recalls: https://www.nhtsa.gov/recalls
