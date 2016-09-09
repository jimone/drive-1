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

- **返回示例**

```javascript
{
    "msg": "xxx",
    "code": true,
    "data": {  
          //用户信息
    }
}
```

## 当前用户详细信息

- **请求URL(controller/action/option)**

  > [sqpaper/user/getDetail](#)

- **请求参数**

请求参数       | 参数说明 | 参考值
:--------- | :--- | :--
oauthToken | 授权   | 略

- **返回示例**

```javascript
{
    "msg": "xxx",
    "code": true,
    "data": {  
          //用户详细信息
    }
}
```

## 获取当前用户可使用的入园记录

- **请求URL(controller/action/option)**

  > [sqpaper/enter/getList](#)

- **请求参数**

请求参数       | 参数说明 | 参考值
:--------- | :--- | :--
oauthToken | 授权   | 略

- **返回示例**

```javascript
{
    "msg": "获取成功",
    "code": true,
    "data": {
        "7": {
            "id": "7",
            "shop_name": "项王故里",  //当前景点相关信息
            ...
            "enterList": [      //该景点入园记录
                {
                    "id": "1",
                    "member_id": "4",
                    ...
                },
                {
                    ...
                },
                ...
            ]
        },
        "9": {
            "id": "9",
            "shop_name": "三台山",
            ...
        }
    }
}
```

## 获取当前用户可使用的入园记录

- **请求URL(controller/action/option)**

  > [sqpaper/enter/getList](#)

- **请求参数**

请求参数       | 参数说明 | 参考值
:--------- | :--- | :--
oauthToken | 授权   | 略

- **返回示例**

```javascript
{
    "msg": "获取成功",
    "code": true,
    "data": {
        "7": {
            "id": "7",
            "shop_name": "项王故里",  //当前景点相关信息
            ...
            "enterList": [      //该景点入园记录
                {
                    "id": "1",
                    "member_id": "4",
                    ...
                },
                {
                    ...
                },
                ...
            ]
        },
        "9": {
            "id": "9",
            "shop_name": "三台山",
            ...
        }
    }
}
```

## 当前用户提交凭证

- **请求URL(controller/action/option)**

  > [sqpaper/order/submit](#)

- **请求参数**

请求参数(*必须)         | 参数说明                 | 参考值
:---------------- | :------------------- | :---------------------
*enter_ids        | 用户选择入园记录id(array)    | [1,4]
*hotel_title       | 酒店名称                 | 用户输入
*hotel_enter_date  | 酒店入住时间               | 用户输入
*hotel_left_date   | 酒店离开时间               | 用户输入
*hotel_amount      | 酒店房间数                | 用户输入
*hotel_number      | 酒店房间号                | 用户输入
*hotel_person      | 入住人数                 | 用户输入
*invoice_code      | 发票 凭证单号              | 用户输入
*invoice_img       | 发票 凭证图片              | 用户输入
*oauthToken        | 授权                   | 略
----------------- | -------------------- | ------------
*grant_way         | 发放方式                 | 0=>微信,1=>支付宝账号,2=>银行转账
alipay_account    | 支付宝账号                | 用户输入
alipay_name       | 支付宝昵称                | 用户输入
bank_account      | 银行账号                 | 用户输入
bank              | 银行名称                 | 用户输入
bank_name         | 银行户名                 | 用户输入
bank_title        | 开户行                  | 用户输入

- **返回示例**

```javascript
{
    "msg": "获取成功",
    "code": true,
    "data": {
        "7": {
            "id": "7",
            "shop_name": "项王故里",  //当前景点相关信息
            ...
            "enterList": [      //该景点入园记录
                {
                    "id": "1",
                    "member_id": "4",
                    ...
                },
                {
                    ...
                },
                ...
            ]
        },
        "9": {
            "id": "9",
            "shop_name": "三台山",
            ...
        }
    }
}
```
