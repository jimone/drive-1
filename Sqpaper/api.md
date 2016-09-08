## 推广红包接口##

[TOC]

#### 接口说明

**1、**新增机器人

- **请求URL**
>

 [sqpaper/user/binding](#)


- **请求参数**
>

 | 请求参数      |     参数类型 |   参数说明   |
| :-------- | :--------| :------ |
| uid|  <mark>Long,**不可为空**</mark>|  机器人UID|
| status|   Integer,可为空|  机器人可用性,默认可用  **-1.不可使用 1.可用**|

- **返回参数**
>

 | 返回参数      |     参数类型 |   参数说明   |
| :-------- | :--------| :------ |
| success|   boolean|  请求成功与否|
| code|   Integer|  执行结果code|
| message|   String|  执行结果消息|

- **返回示例**
>    


```java
{
  "success": true,
  "code": 200,
  "message": "操作正确"
}
```

#### 接口说明 **2、**查询机器人

- **请求URL**
>   [api/v2/operating/robotList](#)


- **请求方式**
>**GET**

- **请求参数**
>
 | 请求参数      |     参数类型 |   参数说明   |
| :-------- | :--------| :------ |
| status|   Integer,可为空|  机器人可用性 **-1.不可使用 1.可用**|
| curPage|   Integer,可为空|  当前页|
| pageSize|   Integer,可为空|  每页显示数量|

- **返回**
>

| 返回参数      |     参数类型 |   参数说明   |
| :-------- | :--------| :------ |
| success|   boolean|  请求成功与否|
| code|   Integer|  执行结果code|
| message|   String|  执行结果消息|
| results|   Object|  执行结果集|

- **返回示例**
>    


```java
{
  "success": true,
  "code": 200,
  "message": "操作正确",
  "results": [
    {
      "createdTs": 1471928107000,
      "updatedTs": 1471928107000,
      "id": 3,
      "uid": 23333,
      "useStatus": 1,(使用状态)
      "nickName": "朱阿便",
      "avatar": "http://7xljdd.com2.z0.glb.qiniucdn.com/fa767b500c58206f5f213a0fe4187e47.jpg"
    }
  ],
  "curPage": 1,
  "pageCount": 2,
  "count": 2,
  "hasRecords": true
}
```

#### 接口说明 **3、**修改机器人

- **请求URL**
> [api/v2/operating/updateRobot](#)


- **请求方式**
>**POST**

- **请求参数**
>

| 请求参数      |     参数类型 |   参数说明   |
| :-------- | :--------| :------ |
| uid|   <mark>Long,**不可为空**</mark>| 机器人UID|
| status|   Integer,可为空| 机器人可用性 **-1.不可使用 1.可用**|

- **返回**
>

| 返回参数      |     参数类型 |   参数说明   |
| :-------- | :--------| :------ |
| success|   boolean|  请求成功与否|
| code|   Integer|  执行结果code|
| message|   String|  执行结果消息|

- **返回示例**
>


```java
{
  "success": true,
  "code": 200,
  "message": "操作正确"
}
```

#### 接口说明 **4、**删除机器人

- **请求URL**
> [api/v2/operating/deleteRobot](#)


- **请求方式**
>**POST**

- **请求参数**
>

| 请求参数      |     参数类型 |   参数说明   |
| :-------- | :--------| :------ |
| uid|   <mark>Long,**不可为空**</mark>| 机器人UID|

- **返回**
>

 | 返回参数      |     参数类型 |   参数说明   |
| :-------- | :--------| :------ |
| success|   boolean|  请求成功与否|
| code|   Integer|  执行结果code|
| message|   String|  执行结果消息|

- **返回示例**
>

```java
{
  "success": true,
  "code": 200,
  "message": "操作正确"
}
```
