# T课程接口文档-ELE捕鱼战

### gameType = 5
### 需注意处理重新组装数据

1、 题类型（queType）参数说明

|值  | 说明 |
| --- | --- |
| 5 | 大写钓小写 |
| 6 | 小写钓大写 |

2、 返回参数说明

|名称  | 类型 | 说明 |
| --- | --- | --- |
| queContentId | long | 游戏问题内容项ID |
| queType | integer | 题类型 |
| itmeElement | string | 单词 |
| itmeAudio | string | 对应音频 |
| itmeHint | string | 提示 匹配对应答案 |
