# 接口名称

#### 接口功能

> 接口的描述接口的描述接口的描述接口的描述

#### 身份验证

> `true`

#### 请求 URL

> [http://api.xxx.com/userinfo](api.xxx.com/userinfo)

#### 请求方式

> `POST`

#### 请求参数

| 参数   | 必选   | 类型     | 说明                                    |
| :----- | :----- | :------- | :-------------------------------------- |
| _name_ | **是** | `string` | 请求的项目名                            |
| _type_ | **否** | `number` | 请求项目的类型。1：类型一；2：类型二 。 |

#### 返回格式

> `JSON`

#### 返回结果

> **字段说明**

| 参数      | 类型     | 说明         |
| :-------- | :------- | :----------- |
| _code_    | `number` | 返回结果状态 |
| _result1_ | `string` | 结果 1       |
| _result2_ | `object` | 结果 2       |

> **result2 字段**

| 参数      | 类型     | 说明   |
| :-------- | :------- | :----- |
| _result3_ | `string` | 结果 3 |

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

#### 其他补充

发送 POST 数据时，建议将`Content-Type`设置为`application/json`