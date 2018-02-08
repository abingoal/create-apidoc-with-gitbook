# 用户信息

#### 接口功能

> 接口的描述接口的描述接口的描述接口的描述

#### 请求 URL

> [http://api.xxx.com/userinfo](api.xxx.com/userinfo)

#### 请求方式

> `GET`

#### 请求参数

| 参数   | 必选 | 类型     | 说明                                    |
| :----- | :--- | :------- | :-------------------------------------- |
| _name_ | ture | `string` | 请求的项目名                            |
| _type_ | true | `number` | 请求项目的类型。1：类型一；2：类型二 。 |

#### 返回格式

> `JSON`

#### 返回字段

| 返回字段  | 字段类型 | 说明         |
| :-------- | :------- | :----------- |
| _code_    | `number` | 返回结果状态 |
| _result1_ | `string` | 结果 1       |
| _result2_ | `object` | 结果 2       |
| _result3_ | `string` | 结果 3       |

#### 结果示例

```javascript
{
    "code": 0,
    "result1": "result1",
    "result2": {
        "result3":"result3"
    },
}
```
