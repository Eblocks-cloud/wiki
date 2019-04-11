# 作业-数据结构设计

## 1.自主作业

| 集合名称  |     服务模块     |       java实体        |   集合描述   |
| :-------: | :--------------: | :-------------------: | :----------: |
| ehomework | EHomeworkService | com.eblocks.ehomework | 自主作业信息 |

| 字段名称     | 必选 |  类型   | 规则                              | 初始值 | 简介             |
| :----------- | :--: | :-----: | --------------------------------- | ------ | ---------------- |
| homeworkId   | true | Number  |                                   |        | 作业id           |
| homeworkName | true | String  |                                   |        | 作业名称         |
| classInfo    | true |  Array  |                                   |        | 发布作业对象班级 |
| classId      | true | Number  |                                   |        | 班级id           |
| className    | true | String  |                                   |        | 班级名称         |
| teacherInfo  | true | Object  |                                   |        | 发布作业教师     |
| teacherId    | true | Number  |                                   |        | 教师id           |
| teacherName  | true | String  |                                   |        | 教师姓名         |
| status       | true | Number  | 0：初始<br />1：发布<br />2：取消 | 0      | 作业状态         |
| isDel        | true | Boolean |                                   | false  | 删除标志         |

数据示例：

```json
{
    "string":"★",
    "number":43,
    "boolean":false,
    "regexp":"hG8",
    "function":0.40959214364551144,
    "array":[
        {
            "foo":1,
            "bar":"★★★★★★★★★★"
        }
    ],
    "items":[
        1,
        true,
        "hello",
        "9TY25nI2Ny"
    ],
    "object":{
        "foo":1,
        "bar":"★★★"
    },
    "placeholder":"Biyf Clckuzfl Rsbxoidu Tholv Zryjmkem Vleq"
}
```

