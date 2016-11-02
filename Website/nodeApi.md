## node端接口


#### 获取首页信息展示
```
参数：
{
        'controller': 'website',
        'action': 'info',
        'option': 'getDetail',
        'status': '1'   // 0 轮播图 1 文字信息
}
返回：
{
    "msg": "获取成功",
    "code": true,
    "data": {
        "One": "4",
        "All": [
            {
                "iforder": "1",
                "id": "7",
                "member_id": "4",
                "title": "ces",
                "pic": "http://testtmpimage.b0.upaiyun.com/201608/23/147191313255414876.jpg",
                "desc": "<p>vhdaef</p>",
                "link": "http://1123.com123",
                "delete": "0",
                "status": "0",
                "order": "1",
                "dateline": "1471913921"
            },
            {
                "iforder": "1",
                "id": "9",
                "member_id": "4",
                "title": "测试",
                "pic": "http://testtmpimage.b0.upaiyun.com/201608/23/147191313255414876.jpg",
                "desc": "",
                "link": "http://1123",
                "delete": "0",
                "status": "0",
                "order": "1",
                "dateline": "1471913131"
            },
            略
        ]
    }
}
```
