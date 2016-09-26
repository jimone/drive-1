# 数据库

--------------------------------------------------------------------------------

## 设备管理表 (db_sqpaper_device)

列名           | 数据类型         | 是否为空     | 约束条件              | 列名说明
:----------- | :----------- | :------- | :---------------- | :-------------
id           | Smallint(5)  | Not null | AUTO_INCREMENT pk | 编号
member_id    | Mediumint(8) | Not null | 默认为''             | 所属企业编号
code         | tinytext     | Not null | 默认为''             | 设备码
desc         | tinytext     | Not null | 默认为''             | 设备描述
count        | int(10)      | Not null | 默认为''             | 使用频数
spot_id      | Mediumint(8) | Not null | 默认为''             | 景点编号(对应商圈中的店铺)
spot_name    | varchar(40)  | Not null | 默认为''             | 景点名(对应商圈中的店铺)
operate_date | int(10)      | Not null | 默认为''             | 最后操作时间
dateline     | int(10)      | Not null | 默认为''             | 添加时间

## 活动表 (db_sqpaper_activity)

列名            | 数据类型         | 是否为空     | 约束条件              | 列名说明
:------------ | :----------- | :------- | :---------------- | :-----------------
id            | Smallint(5)  | Not null | AUTO_INCREMENT pk | 编号
member_id     | Mediumint(8) | Not null | 默认为''             | 所属企业编号
name          | varchar(60)  | Not null | 默认为''             | 活动名称
participation | tinytext     | Not null | 默认为''             | 参与方式
rules         | tinytext     | Not null | 默认为''             | 参与规则(序列化)
rules_desc    | tinytext     | Not null | 默认为''             | 参与规则详情
money         | decimal(9,2) | Not null | 默认为''             | 单个红包金额
money_num     | int(10)      | Not null | 默认为''             | 单次获取红包最大数量
money_total   | decimal(9,2) | Not null | 默认为''             | 个人红包获取总额 0 为无限
delete        | tinyint(3)   | Not null | 默认为''             | 是否回收 默认0 ，0正常 1 回收
lottery_id    | Mediumint(8) | Not null | 默认为''             | 抽奖活动id
start_date    | int(10)      | Not null | 默认为''             | 活动开始时间
end_date      | int(10)      | Not null | 默认为''             | 活动结束时间
dateline      | int(10)      | Not null | 默认为''             | 创建时间

--------------------------------------------------------------------------------

## 用户表 (db_sqpaper_user)

列名             | 数据类型         | 是否为空     | 约束条件              | 列名说明
:------------- | :----------- | :------- | :---------------- | :--------------------------------------------
id             | Smallint(5)  | Not null | AUTO_INCREMENT pk | 编号
member_id      | Mediumint(8) | Not null | 默认为''             | 所属企业编号
nickname       | varchar(60)  | Not null | 默认为''             | 微信获取昵称
name           | varchar(60)  | Not null | 默认为''             | 游客姓名
id_card        | varchar(60)  | Not null | 默认为''             | 身份证
nation         | varchar(60)  | Not null | 默认为''             | 民族
sex            | tinyint(1)   | Not null | 默认为''             | 性别 0 男 1女
address        | varchar(60)  | Not null | 默认为''             | 住处
birthday       | varchar(60)  | Not null | 默认为''             | 出生日期
office         | varchar(60)  | Not null | 默认为''             | 签证机关
openid         | tinytext     | Not null | 默认为''             | openid
mobile         | char(20)     | Not null | 默认为''             | 手机号码
head_img       | tinytext     | Not null | 默认为''             | 微信头像
head_card      | tinytext     | Not null | 默认为''             | 身份证头像
grant_way      | tinyint(3)   | Not null | 默认为''             | 发放方式(-1=>用户未填写过相关信息，0=>微信红包,1=>支付宝账号,2=>银行转账)
alipay_account | varchar(40)  | Not null | 默认为''             | 支付宝账号
alipay_name    | varchar(40)  | Not null | 默认为''             | 支付宝昵称
bank_account   | varchar(40)  | Not null | 默认为''             | 银行账号
bank           | varchar(40)  | Not null | 默认为''             | 银行名称
bank_name      | varchar(40)  | Not null | 默认为''             | 银行户名
bank_title     | varchar(40)  | Not null | 默认为''             | 开户行
total          | decimal(9,2) | Not null | 默认为''             | 累计获得红包
dateline       | int(10)      | Not null | 默认为''             | 创建时间

--------------------------------------------------------------------------------

## 入园记录表 (db_sqpaper_enter)

列名          | 数据类型         | 是否为空     | 约束条件              | 列名说明
:---------- | :----------- | :------- | :---------------- | :----------------------------------
id          | Smallint(5)  | Not null | AUTO_INCREMENT pk | 编号
member_id   | Mediumint(8) | Not null | 默认为''             | 所属企业编号
activity_id | Mediumint(8) | Not null | 默认为''             | 活动id
id_card     | varchar(40)  | Not null | 默认为''             | 身份证
shop_id     | Mediumint(8) | Not null | 默认为''             | 景点编号(对应商圈 店铺id)
device_id   | varchar(40)  | Not null | 默认为''             | 扫描设备id
amount      | int(10)      | Not null | 默认为''             | 票数量
is_use      | int(10)      | Not null | 默认为''             | 是否使用(0=>未使用 1=>使用中 2=>成功使用 3=>使用失败)
order_id    | Smallint(5)  | Not null | 默认为''             | 订单编号(order中的id)
dateline    | Int(10)      | Not null | 默认为0              | 入园时间

--------------------------------------------------------------------------------

## 订单表 (db_sqpaper_order)

列名                   | 数据类型         | 是否为空     | 约束条件              | 列名说明
:------------------- | :----------- | :------- | :---------------- | :-----------------------------------------------------
id                   | Smallint(5)  | Not null | AUTO_INCREMENT pk | 编号
member_id            | Mediumint(8) | Not null | 默认为''             | 所属企业编号
activity_id          | Mediumint(8) | Not null | 默认为''             | 活动id
user_id              | Varchar(40)  | Not null | 默认为''             | 用户编号
order_code           | varchar(40)  | Not null | 默认为''             | 订单编号
id_card              | varchar(40)  | Not null | 默认为''             | 操作身份证号
hotel_title          | varchar(40)  | Not null | 默认为''             | 酒店名称
hotel_enter_date     | Int(10)      | Not null | 默认为''             | 酒店入住时间
hotel_left_date      | Int(10)      | Not null | 默认为''             | 酒店离开时间
hotel_amount         | varchar(40)  | Not null | 默认为''             | 酒店房间数
hotel_number         | varchar(40)  | Not null | 默认为''             | 酒店房间号
hotel_person         | varchar(40)  | Not null | 默认为''             | 入住人数
invoice_code         | varchar(80)  | Not null | 默认为''             | 发票 凭证单号
invoice_img          | tinytext     | Not null | 默认为''             | 发票 凭证图片
check_date           | int(10)      | Not null | 默认为0              | 提交审核时间
check_status         | tinyint(3)   | Not null | 默认为0              | 审核状态 默认为0 0=>提交未审核 1=>初审核未通过 2=>初审核通过 3=>财政未通过 4=>财政通过
money                | decimal(9,2) | Not null | 默认为''             | 发放金额
default_grant_status | tinyint(3)   | Not null | 默认为0              | 支付宝/银行发放状态 默认为0 0 =>未发放 1 =>发放中 2=>发放成功 3/other =>发放失败
grant_status         | tinyint(3)   | Not null | 默认为0              | 微信发放状态 默认为0 0 =>未发放 1=>发放成功 3=> 发放失败
grant_back_status    | varchar(40)  | Not null | 默认为0              | 微信返回状态码
grant_date           | int(10)      | Not null | 默认为0              | 发放时间
grant_way            | tinyint(3)   | Not null | 默认为0              | 发放方式(0=>微信红包,1=>支付宝账号,2=>银行转账)
user_config          | text         | Not null | 默认为0              | 入住人信息(序列化)

--------------------------------------------------------------------------------

## 操作记录表 (db_sqpaper_operate_log)

列名          | 数据类型         | 是否为空     | 约束条件              | 列名说明
:---------- | :----------- | :------- | :---------------- | :---------------------------------------------------------------
id          | Smallint(5)  | Not null | AUTO_INCREMENT pk | 编号
member_id   | Mediumint(8) | Not null | 默认为''             | 所属企业编号
activity_id | Mediumint(8) | Not null | 默认为''             | 活动id
operate_id  | varchar(40)  | Not null | 默认为''             | 工作人员编号
user_id     | Mediumint(8) | Not null | 默认为''             | 用户id
order_code  | varchar(40)  | Not null | 默认为''             | 操作订单号(order表中的order_code)
id_card     | varchar(40)  | Not null | 默认为''             | 操作身份证号
status      | tinyint(3)   | Not null | 默认为''             | 操作类型(1=>初审核未通过 2=>初审核通过 3=>财政未通过 4=>财政通过 6=>发放成功 7=>发放失败 8=>发放中)
log         | text         | Not null | 默认为''             | 操作内容(红包个数/原因)
desc        | text         | Not null | 默认为''             | 操作细节(建议总额/详情)
dateline    | int(10)      | Not null | 默认为''             | 时间

--------------------------------------------------------------------------------

## 红包发放记录表 (db_sqpaper_grant_log)

列名          | 数据类型         | 是否为空     | 约束条件              | 列名说明
:---------- | :----------- | :------- | :---------------- | :---------------------------------
id          | Smallint(5)  | Not null | AUTO_INCREMENT pk | 编号
member_id   | Mediumint(8) | Not null | 默认为''             | 所属企业编号
activity_id | Mediumint(8) | Not null | 默认为''             | 活动id
user_id     | Mediumint(8) | Not null | 默认为''             | 用户id
id_card     | varchar(40)  | Not null | 默认为''             | 用户身份证
pay_way     | tinyint(3)   | Not null | 默认为''             | 支付方式(0=>微信红包 1=>支付宝账号 2=>银行转账)
money       | decimal(9,2) | Not null | 默认为''             | 发放金额
account     | tinytext     | Not null | 默认为''             | 发放账号(微信openid 支付宝账号+昵称 银行转账 相应信息 )
operate_id  | varchar(40)  | Not null | 默认为''             | 发放操作员id(operate_log表中的operate_id)
dateline    | int(10)      | Not null | 默认为''             | 操作时间
