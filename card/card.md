![image](https://github.com/MelonYii/images/blob/master/%E5%89%8D%E5%8F%B0%E6%9E%B6%E6%9E%84%E5%9B%BE.jpg)
### 菜单获取

```javascript
参数：
{
    'controller':'card',
    'action':'menu',
    'option':'getList'
}
返回：
{
    "msg": "成功",
    "code": true,
    "data": {
        "interface": {
            "id": "2",
            "member": "4",
            "title": "众旅云",
            "logo": "http://wx.qlogo.cn/mmopen/PLc9fhw8iashRwVh0RnTAPKty3I92cDzKzwsmSbv8tYplCB3Wj4T5rfuOE2nGC8UxDnibrhN7FXcrYkRxQdoYltZ5zjwgOmZna/0",
            "service": "2",
            "appuser": "gh_dd71d4eef1bf",
            "qrcode_url": "http://mmbiz.qpic.cn/mmbiz/7aiaADrlRXiar2iaZ0VJQI5fficEfFs9SLmtw95laC6icGqjgv1GbfsRR2n6tbTer3ia0aDzjjbL31ClE31ibpBwibABtg/0"
        },
        "menu": [
            {
                "id": "2",
                "member_id": "4",
                "name": "用户信息",
                "url": "www.baidu.com",
                "order": "12",
                "dateline": "1464329680"
            },
            {
                "id": "3",
                "member_id": "4",
                "name": "订单管理",
                "url": "www.world.com",
                "order": "5",
                "dateline": "1464329720"
            }
        ]
    }
}
```
---
### 年卡列表
```javascript
参数：
{
    'controller': 'card',
    'action': 'card',
    'option': 'getList'
}
返回：
{
    "msg": "成功",
    "code": true,
    "data": {
        "interface": {'略'},
        "cardList": [
            {
                "id": "3",
                "member_id": "4",
                "image": "http://testtmpimage.b0.upaiyun.com/201605/03/146224483062210259.jpg",//年卡图片
                "configure": "360500*",
                "name": "新余旅游年卡",
                "free": "150.00",//年卡线下价格
                "delete": "0",
                "dateline": "1464224290",//时间
                "money": "90.99",//年卡线上价格
                "back_image": "http://testtmpimage.b0.upaiyun.com/201605/13/146312803163893373.jpg",//背部图片
                "type": "1", //排版模式1为竖版,2为横板
                "now_sale": 0.2 //年卡线上折扣
            },
            {
                "id": "5",
                "member_id": "4",
                "image": "http://testtmpimage.b0.upaiyun.com/201605/20/146373482392500255.jpg",
                "configure": "",
                "name": "测试",
                "free": "0.10",
                "delete": "0",
                "dateline": "1463734823",
                "money": "0.10",
                "back_image": "http://testtmpimage.b0.upaiyun.com/201605/20/146373482405790041.jpg",
                "type": "1",
                "now_sale": 0.1
            }
        ],
    }
}
```
---
### 年卡详情
```javascript
参数
{
    'controller':'card',
    'action':'card',
    'cardId':,   //年卡id
    'option':'getDetail',
    'isDesc':   //是否获取详情（1=>获取use_desc,buy_desc（年卡使用，购买详情）      0=>不获取use_desc,buy_desc）
}
返回
{
    "msg": "成功",
    "code": true,
    "data": {
        "interface": {"略"},
        "cardRow": {
            "id": "5",
            "member_id": "4",
            "buy_desc": "略",
            "use_desc": "略",
            "configure": "",
            "name": "测试",
            "delete": "0",
            "dateline": "1464596757",
            "money": "0.10",
            "free": "0.10",
            "image": "http://testtmpimage.b0.upaiyun.com/201605/20/146373482392500255.jpg",
            "back_image": "http://testtmpimage.b0.upaiyun.com/201605/20/146373482405790041.jpg",
            "type": "1"
        },
        "saleRow": {
            "id": "18",
            "member_id": "4",
            "card_id": "5",
            "starttime": "1464579600",
            "endtime": "1464677400",
            "sale": "10",
            "delete": "0",
            "desc": "<p>说啥呢</p>",
            "isonline": "1",
            "name": "第二个测试"
        }
    }
}
```
---
### 年卡申请
```javascript
参数
{
    'controller':'card',
    'action':'card',
    'option':'apply',
    'tel':'',
    'IDcard':'',
    'name':'',
    'userId':'',  //可选
    'dealerId':"",
    'cardId':"",
    'gender':"",
    'id_type':"",
    'front_img':"",
    'reverse_img':"",
    'type_img':"",
}
返回
{
    "msg": "成功",
    "code": true,
    "data": {
        "interface": {'略'},
        "userId": "" 
    }
}
```
---
### 用户详情获取
```javascript
参数
{
    'controller':'card',
    'action':'user',
    'option':'getDetail',
    'userId':'17'  //用户userId
    'getCard': ''   //是否获取对应cardRow  1=> 获取
    'getDealer' : ''  //是否获取对应dealerRow   1=> 获取
}
返回
{
    "msg": "成功",
    "code": true,
    "data": {
        "interface": {"略"},
        "userRow": {
            "id": "17",
            cardNum:"BBB0000000085",   //年卡编号
            "member_id": "4",
            "dealer_id": "2",
            "name": "黄婷婷",
            "gender": "female",
            "address": "杭州途记科技有限公司",
            "id_type": "1",
            "money": "0.10",
            "IDcard": "452123199110013767",
            "status": "5",
            "openid": "",
            "front_img": "http://testtmpimage.b0.upaiyun.com/201605/03/146225008804888134.jpg",
            "reverse_img": "http://testtmpimage.b0.upaiyun.com/201605/03/146225008838188064.jpg",
            "reg_date": "1462250087",
            "check_date": "1462250087",
            "tel": "18768120876",
            "card_id": "3",
            "is_get": "1",
            "expire_date": "1493786087",
            "last_img": "http://testtmpimage.b0.upaiyun.com/201605/03/146225008943432337.jpg",
            "pay_date": "0",
            "type_img": "",
            "enable_date": "0",
            "is_warn": "0"
        }
    }
}
```
---
### 获取支付信息
```javascript
参数
{
    'controller':'card',
    'action':'order',
    'option':'getPayData',
    'userId':'17'
}
返回
{
    "msg": "成功",
    "code": true,
    "data": {
        "interface": {'略'},
        "data": {
            "appid": "20160309140730672098",
            "fee": 9099,
            "tradeId": "C20160503123400000017",
            "body": "新余旅游年卡",
            "redirectUrl": "/index.php/4/#/card/index/?option=myDetail&do=payCallBack&dealerId=&userId=17",
            "timeStamp": 1464830951
        },
        "sign": "bc44b1dc2d87a833930f8705aa666179"
    }
}
```
---
### 实体卡绑定线上卡
```javascript
参数
    {
        'controller':'card',
        'action':'card',
        'option':'bind',
        'cardNum':'AAR0000000084',   //实体卡编号
        'IDcard':'250722199402114236'  //身份证编号
    }
返回
{
    "msg": "绑定成功",
    "code": true,
    "data": {
        "interface": {'略'},
        "id": "84"   //返回userId
    }
}
```
---
### 用户获取当前拥有年卡
```javascript
参数
{
    'controller':'card',
    'action':'user',
    'option':'getList'
}
返回
{
    "msg": "成功",
    "code": true,
    "data": {
        "interface": {'略'},
        "userList": [            //status   6=>即将到期 7=>已经到期
            {
                "id": "17",
                "member_id": "4",
                "dealer_id": "2",
                "name": "黄婷婷",
                "gender": "female",
                "address": "杭州途记科技有限公司",
                "id_type": "1",
                "money": "0.10",
                "IDcard": "452123199110013767",
                "status": "5",
                "openid": "",
                "front_img": "http://testtmpimage.b0.upaiyun.com/201605/03/146225008804888134.jpg",
                "reverse_img": "http://testtmpimage.b0.upaiyun.com/201605/03/146225008838188064.jpg",
                "reg_date": "1462250087",
                "check_date": "1462250087",
                "tel": "18768120876",
                "card_id": "3",
                "is_get": "1",
                "expire_date": "1493786087",
                "last_img": "http://testtmpimage.b0.upaiyun.com/201605/03/146225008943432337.jpg",
                "pay_date": "0",
                "type_img": "",
                "enable_date": "0",
                "is_warn": "0",
                "cardID": "AAA0000000017"
            },
            {
                "id": "18",
                ...略
            }
        ],
        "cardRow": {     //cardId为键，对应cardRow为值
            "3": {
                "id": "3",
                "member_id": "4",
                "configure": "360500*",
                "name": "新余旅游年卡",
                "delete": "0",
                "dateline": "1464224290",
                "money": "90.99",
                "free": "150.00",
                "image": "http://testtmpimage.b0.upaiyun.com/201605/03/146224483062210259.jpg",
                "back_image": "http://testtmpimage.b0.upaiyun.com/201605/13/146312803163893373.jpg",
                "type": "1"
            },
            "5": {
                "id": "5",
                "member_id": "4",
                "name": "测试",
                "delete": "0",
                "dateline": "1464596757",
                "money": "0.10",
                "free": "0.10",
                "image": "http://testtmpimage.b0.upaiyun.com/201605/20/146373482392500255.jpg",
                "back_image": "http://testtmpimage.b0.upaiyun.com/201605/20/146373482405790041.jpg",
                "type": "1"
            }
        }
    }
}
```
---
### 用户入园记录
```javascript
参数
{
    'controller':'card',
    'action':'scenic',
    'option':'getList',
    'userId':'26'
}
返回
{
    "msg": "获取成功",
    "code": true,
    "data": {
        "logsList": [
            {
                "dateline": "2016年05月04日 11:54:33",
                "scenic_name": "仙女湖景区",
                "is_pass" : '0'     
            },
            {
                "dateline": "2016年05月03日 18:02:10",
                "scenic_name": "仙女湖景区"
                "is_pass" : '0'     
            }
        ]
    }
}
```
---
### 获取续费支付信息
```javascript
参数
{
    'controller':'card',
    'action':'order',
    'option':'getRenewData',
    'userId':'17'
}
返回
{
    "msg": "成功",
    "code": true,
    "data": {
        "interface": {'略'},
        "data": {
            "appid": "20160309140730672098",
            "fee": 9099,
            "tradeId": "C20160503123400000017",
            "body": "新余旅游年卡",
            "redirectUrl": "/index.php/4/#/card/index/?option=myDetail&do=payCallBack&dealerId=&userId=17",
            "timeStamp": 1464830951
        },
        "sign": "bc44b1dc2d87a833930f8705aa666179"
    }
}
```
---
### 代售点列表接口
```javascript
参数
{
    'controller':'card',
    'action':'dealer',
    'option':'getList'
}
返回
{
    "msg": "成功",
    "code": true,
    "data": {
        "interface": {'略'},
        "dealerList": {
        [
                {
                    "id": "1",
                    "member_id": "4",
                    "name": "代售点122",
                    "address": "杭州西斗门路天堂软件园",
                    "tel": "18768120987",
                    "lng": "",
                    "lat": "",
                    "delete": "0",
                    "dateline": "1464226203",
                    "username": "5820120@zlvyun.com",
                    "passwd": "c64125ee5219cc527dc7501372b7a738",
                    "tag": "AAR",
                    "openid": "o6D74tyLSAE-wCKIjgzOxtlvOlD8",
                    "profit": "0.01",
                    "issend": "0",
                    "isfit": "0"
                },
                {
                    "id": "2",
                    "member_id": "4",
                    "name": "代售点1",
                    "address": "杭州西斗门路天堂软件园",
                    "tel": "18768120987",
                    "lng": "",
                    "lat": "",
                    "delete": "0",
                    "dateline": "1462245008",
                    "username": "5820120@zlvyun.com",
                    "passwd": "728620f5ca58e1836093dfda592b96ae",
                    "tag": "AAA",
                    "openid": "o6D74tyLSAE-wCKIjgzOxtlvOlD8",
                    "profit": "0.00",
                    "issend": "0",
                    "isfit": "0"
                },
                {
                    "id": "3",
                    "member_id": "4",
                    "name": "测试地址",
                    "address": "浙江",
                    "tel": "15757160309",
                    "lng": "",
                    "lat": "",
                    "delete": "0",
                    "dateline": "1464061978",
                    "username": "yyxx",
                    "passwd": "fd7f0f5b6afa610ad3e334acad32b0e4",
                    "tag": "BBB",
                    "openid": "",
                    "profit": "0.00",
                    "issend": "0",
                    "isfit": "0"
                }
        }
    }
}
```
### 订单列表获取
```javascript
参数
{
    'controller':'card',
    'action':'order',
    'option':'getList'
}
返回
{
    "msg": "成功",
    "code": true,
    "data": {
        "interface": {'略'},
        "moneyList": {
                {
                    "id": "1",
                    "dealer_id": "1",
                    "card_id": "3",
                    "user_id": "32",
                    "isonline": "1",
                    "isrenew": "1",
                    "order_id": "1994050130",
                    "money": "20.00",
                    "delete": "0",
                    "dateline": "131",
                    "member_id": "4",
                    "is_pay": "0"
                },
                {
                    "id": "4",
                    "dealer_id": "1",
                    "card_id": "3",
                    "user_id": "79",
                    "isonline": "0",
                    "isrenew": "1",
                    "order_id": "1994050133",
                    "money": "25.00",
                    "delete": "0",
                    "dateline": "1461600400",
                    "member_id": "4",
                    "is_pay": "0"
                }
        }
    }
}
```
---
```javascript
参数
{
    'controller':'card',
    'action':'dealer',
    'option':'getDetail',
    'dealerId' :'3'
}
返回
{
    "msg": "获取代售点详情成功",
    "code": true,
    "data": {
        "interface": {略},
        "dealerRow": {
            "id": "3",
            "member_id": "4",
            "name": "测试地址",
            "address": "浙江",
            "tel": "15757160309",
            "lng": "",
            "lat": "",
            "delete": "0",
            "dateline": "1464061978",
            "username": "yyxx",
            "passwd": "fd7f0f5b6afa610ad3e334acad32b0e4",
            "tag": "BBB",
            "openid": "",
            "profit": "0.00",
            "issend": "0",
            "isfit": "0"
        }
    }
}
```
### app接口验证登陆
```javascript
参数
{
    'controller':'card',
    'action':'app',
    'option':'login', 
    'username':'',
    'password':'',
    'timeStamp:''
}
```
### app接口获取用户信息
```javascript
参数
{
    'controller':'card',
    'action':'app',
    'option':'select', 
    'userId':'',
    'perId':'',
    'timeStamp':''
}
```
### app接口通过入库
```javascript
{
    'controller':'card',
    'action':'app',
    'option':'pass', 
    'userId':'',
    'perId':'',
    'timeStamp':''
}
```
### app接口不通过入库
```javascript
{
     'controller':'card',
    'action':'app',
    'option':'refuse',
    'userId':'',
    'perId':'',
    'timeStamp':'',
    'remarks'(可空)
}
```
---
### 年卡申请流程图
![image](https://github.com/MelonYii/images/blob/6633066c8216e169c716e5bd5133d6c74a3ecbba/cardApply.png)
---
### 信息提交引导页
![image](https://github.com/MelonYii/images/blob/master/%E4%BF%A1%E6%81%AF%E6%8F%90%E4%BA%A4%E5%BC%95%E5%AF%BC%E9%A1%B5.png)
---
### 支付页面
![image](https://github.com/MelonYii/images/blob/master/%E6%94%AF%E4%BB%98%E9%A1%B5%E9%9D%A2.png)
---
### 续费api
![image](https://github.com/MelonYii/images/blob/master/%E7%BB%AD%E8%B4%B9api.png)
