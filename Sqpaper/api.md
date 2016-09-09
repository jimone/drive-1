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

## 获取当前用户可使用的入园记录

- **请求URL(controller/action/option)**

  > [sqpaper/order/getList](#)

- **请求参数**

请求参数       | 参数说明     | 参考值
:--------- | :------- | :-------------------------------
oauthToken | 授权 | 略


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

请求参数       | 参数说明     | 参考值
:--------- | :------- | :-------------------------------
oauthToken | 授权 | 略


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
