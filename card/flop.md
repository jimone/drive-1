# 翻牌游戏接口
---

### 获取当前活动相关信息
参数 | 含义 | 值
---|---|---
controller | 控制器 | flop
action | 行为 | activity
option | 执行 | getLotteryDetail
activityId | 活动id | 例：'1' 

data返回 | 含义
---|---
id | 编号
member_id | 所属企业编号
title | 活动名称
intro | 简介
image | 图片地址
address | 领奖地址
contacts | 联系人
tel | 联系电话
probability | 获奖概率
awards_date | 发放奖品时间
start_date | 领奖开始时间
end_date | 领奖结束时间
dateline | 添加时间

---

### 获取当前活动奖品列表
参数 | 含义 | 值
--- | --- | ---
controller | 控制器 | flop
action | 行为 | activity
option | 执行 | getPrizeList
activityId | 活动id | 例：'1'

主要返回 | 含义
--- | ---
id | 编号
member_id | 所属企业编号
activity_id | 活动id
grade | 奖项等级
title | 奖项名称
type | 奖品类型0=>实物，1=>红包，2=>话费
intro | 奖品说明
num | 个数/总金额(单位：分)
surplus | 剩余个数/余额(单位：分)
probability | 概率
image | 图片地址
money_up | 如果为红包其额度上限(单位：分)
money_down | 如果为红包其额度下限（单位：分）
dateline | 时间

---

### 获取当前用户所有码
参数 | 含义 | 值
--- | --- | ---
controller | 控制器 | flop
action | 行为 | code
option | 执行 | getList

主要返回 | 含义
--- | ---
id | 编号
member_id | 所属企业编号
activity_id | 活动id
user_id | 用户id
code | 码
is_win | 是否中奖0=>未开奖/未中奖 1=>中奖
rank | 中奖等次
prize_id | 奖品id
dateline | 创建时间

---
### 通过核销码兑奖
参数 | 含义 | 值
--- | --- | ---
controller | 控制器 | flop
action | 行为 | activity
option | 执行 | checkCode
verifiCode | 核销员输入的核销码 | 由页面获取
codeId | 对应的码id | 例：'1'
activityId | 活动id | 例：'1'

返回code | 含义
--- | ---
false | 核销失败，打印错误信息
true | 核销成功
