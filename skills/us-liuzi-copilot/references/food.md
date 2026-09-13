# 🍜 附近中国人爱吃什么：餐馆 / 奶茶 / 约会吃饭 Playbook

## 默认行为
用户说“附近两个人晚饭吃啥”，如果已有大致位置：**直接搜，不先问十个问题。**
默认：2 人、正常晚餐预算、中国胃友好；再根据反馈调整。

## 菜系不要只写“Chinese”
可按需求识别：
- 川湘 / 辣
- 东北 / 烧烤
- 粤菜 / 早茶
- 上海/江浙
- 西北 / 面食
- 火锅 / 串串
- 烤鱼
- 奶茶甜品
- 韩餐/日料/越南/泰餐
- late-night Chinese

## 实时抓字段
`name | cuisine | distance | drive/transit | open_now | price | recent rating | review_count | recent sentiment | menu | signature | wait | reservation | parking | noise/date vibe`

## 评价怎么读
优先：
1. 官方 menu / hours
2. Google Maps 近期 reviews/photos
3. Reddit/local community “regulars”
4. 中餐可额外看中文/亚洲食客评价信号

不要只按 rating 排。4.4/2000 reviews 和 4.7/30 reviews 的稳定性不同。

## 近期 review 搜关键词
中餐：
`authentic | spicy | portion | oily | service | wait | changed owner | new chef | parking`

## 不同场景
### 穷鬼吃饭
lunch special / food court / campus-adjacent / takeout combo；必须算 checkout + tip/delivery。

### 约会
灯光、噪音、可聊天、reservation、停车、附近续场。

### 大群
大桌/包间/拼桌/automatic gratuity/停车。

### 深夜
营业时间当天核对，不用旧攻略。

## 外卖比价
`menu markup + service fee + delivery + small order + tax + tip`
与 pickup 对比。不要只看“$0 delivery fee”。

## 输出
- **首选 1 家**：一句为什么最适合
- **备选 2–5 家**：分别代表更便宜/更近/更有氛围
- 3+ 个地点时用地图
- 顺手给“点什么”，但菜品要基于当前 menu/reviews
