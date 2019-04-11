# T课程接口文档-ELE大漂浮

### gameType = 14
### 需注意处理重新组装数据

1、 题类型（queType）参数说明

|值  | 说明 |
| --- | --- |
| 2 | 首音 |
| 3 | 中音 |
| 4 | 尾音 |

2、 返回参数说明

|名称  | 类型 | 说明 |
| --- | --- | --- |
| queContentId | long | 游戏问题内容项ID |
| queType | integer | 题类型 |
| itmeElement | string | 单词 |
| itmeAudio | string | 对应音频 |
| itmeImage | string | 对应图片 |
| itmeHint | string | 提示 |
| isRight | integer | 是否正确答案 0:否 1:是 |

3、 JSON返回示例
```
[
            {
                "1": [
                    {
                        "isRight": 1,
                        "itmeElement": "apple",
                        "queContentId": 39,
                        "queType": 2,
                        "itmeAudio": "http://pkzn2yuaa.bkt.clouddn.com/501a763f-1471-44ae-824d-527f5a037321.wav",
                        "itmeImage": "http://pkzn2yuaa.bkt.clouddn.com/39295ef4-e45a-42b1-b748-8446e9e1721a.png",
                        "itmeHint": "a"
                    },
                    {
                        "isRight": 0,
                        "itmeElement": "blue",
                        "queContentId": 40,
                        "queType": 2,
                        "itmeAudio": "http://pkzn2yuaa.bkt.clouddn.com/501a763f-1471-44ae-824d-527f5a037321.wav",
                        "itmeImage": "http://pkzn2yuaa.bkt.clouddn.com/39295ef4-e45a-42b1-b748-8446e9e1721a.png",
                        "itmeHint": "b"
                    }
                ]
            },
            {
                "2": [
                    {
                        "isRight": 0,
                        "itmeElement": "apple",
                        "queContentId": 41,
                        "queType": 2,
                        "itmeAudio": "http://pkzn2yuaa.bkt.clouddn.com/501a763f-1471-44ae-824d-527f5a037321.wav",
                        "itmeImage": "http://pkzn2yuaa.bkt.clouddn.com/39295ef4-e45a-42b1-b748-8446e9e1721a.png",
                        "itmeHint": "a"
                    },
                    {
                        "isRight": 1,
                        "itmeElement": "blue",
                        "queContentId": 42,
                        "queType": 2,
                        "itmeAudio": "http://pkzn2yuaa.bkt.clouddn.com/501a763f-1471-44ae-824d-527f5a037321.wav",
                        "itmeImage": "http://pkzn2yuaa.bkt.clouddn.com/39295ef4-e45a-42b1-b748-8446e9e1721a.png",
                        "itmeHint": "b"
                    }
                ]
            }
]

```