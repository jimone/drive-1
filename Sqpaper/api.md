# 推广红包接口

## 入园记录绑定相应微信

- **请求URL(controller/action/option)**

  > [sqpaper/user/binding](#)

- **请求参数**

请求参数       | 参数说明     | 参考值
:--------- | :------- | :-------------------------------
id_card    | 用户输入身份证  | 350733211585445425
card_sign  | 签名       | 21d38201457661ca58ab83cfc7c6f54b
oauthToken | **显性**授权 | 略

- **返回参数**

返回参数    | 参数类型    | 参数说明
:------ | :------ | :-------
success | boolean | 请求成功与否
code    | Integer | 执行结果code
message | String  | 执行结果消息

- **返回示例**

```javascript
{
    "msg": "xxx",
    "code": true,
    "data": {    //用户信息
        "id": "1",
        "member_id": "4",
        "nickname": "",
        "name": "游亦鑫",
        "id_card": "350733211585445425",
        "openid": "o6D74t682tWBXiPUh1Hj154omKSI",
        "mobile": "15757160309",
        "head_img": "",
        "grant_way": "0",
        "alipay_account": "312321321@qq.com",
        "alipay_name": "支付宝名称",
        "bank_account": "银行账号",
        "bank": "银行名称",
        "bank_name": "银行户名",
        "bank_title": "开户行",
        "total": "1472.30",
        "dateline": "1234324234",
        "nation": "民族",
        "sex": "0",
        "address": "绍兴",
        "birthday": "1994年2月3日",
        "office": "柯桥区公安局"
    }
}
```
