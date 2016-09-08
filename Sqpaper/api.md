## 推广红包接口##

[TOC]

#### 接口说明

**1、**新增机器人

- **请求URL**
 [sqpaper/user/binding](#)


- **请求参数**
 | 请求参数      |     参数类型 |   参数说明   |
| :-------- | :--------| :------ |
| uid|  <mark>Long,**不可为空**</mark>|  机器人UID|
| status|   Integer,可为空|  机器人可用性,默认可用  **-1.不可使用 1.可用**|

- **返回参数**
 | 返回参数      |     参数类型 |   参数说明   |
| :-------- | :--------| :------ |
| success|   boolean|  请求成功与否|
| code|   Integer|  执行结果code|
| message|   String|  执行结果消息|

- **返回示例**
```javascript
{
  "success": true,
  "code": 200,
  "message": "操作正确"
}
```
