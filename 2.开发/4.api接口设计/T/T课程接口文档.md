# T课程接口文档
1、 接口地址：

        http://gameapi.eblockschina.com/game/t_cource/selectById
    
2、 返回格式

        json
    
3、 请求方式

        get

4、 请求示例

        http://gameapi.eblockschina.com/game/t_cource/selectById?questionId=5

5、 请求参数说明

|名称  | 必填 | 类型 | 说明 |
| --- | --- | --- | --- |
| questionId | Y | Long | T课程题ID |

6、 返回参数说明

|名称  | 类型 | 说明 |
| --- | --- | --- |
| isSuccess | boolean | 是否成功 |
| resultMsg | string | 结果信息|
| data | object | 返回结果集 |
| --- | --- | --- |
| id | long | 题ID |
| courseId | integer | 课程ID |
| courseName | string | 课程名称 |
| unitId | integer | 单元ID |
| unitName | string | 单元名称 |
| queType | integer | 题类型 详见 7 题类型说明 |
| gameType | integer | 游戏类型 详见 8 游戏类型说明 |
| sort | integer | 排序 |
| isDelete | integer | 是否删除 0:正常 1:已删除 |
| nextQuestionId | long | 下一题ID 正常返回下一题ID，如最后一题返回 -1 |
| questionAmount | integer | 该单元内题总数量，展示糖果数量 |
| questionTContents | array | 题内容结果集 根据gameType返回不同数据 详见游戏类型说明对应文档 |

7、 题类型（queType）参数说明

|值  | e_name | 说明 |
| --- | --- | --- |
| 0 | Follow | 跟读 |
| 1 | Spell | 单词拼写|
| 2 | Listen | 听音频辨音 |
| 3 | Letter | 匹配字母大小写 |

8、 游戏类型（gameType）参数说明

|值  | e_name | 说明 |
| --- | --- | --- |
| 0 | RunningElephants | 奔跑的小象 |
| 1 | FriendsRescue | 好友大营救 |
| 2 | Wheel | 旋转大转盘 该游戏待定 |
| 3 | Egg | 彩蛋联排战 |
| 4 | Key | 钥匙大作战 |
| 5 | Fishing | ELE捕鱼战 |
| 6 | Jigsaw | 线索拼图 |
| 7 | Racing | 赛车冲冲冲 |
| 8 | Shoot | 射门游戏 |
| 9 | NightSky | 夜空大战 |
| 10 | Gemstone | 宝石大探险 |
| 11 | HappyDoll | 开心娃娃机 |
| 12 | GrabSeats | 座椅抢位战 |
| 13 | Transport | 运输分类战 |
| 14 | LargeFloating | ELE大漂浮 |

9、 JSON返回示例
```
{
	
    "isSuccess":true,
	"resultMsg":"执行成功！",
    "data":{
		"id": 4,
        "courseId": 1,
        "courseName": "T1",
        "unitId": 1,
        "unitName": "uint1",
        "queType": 1,
        "gameType": 1,
        "sort": 1,
        "isDelete": 0,
        "nextQuestionId": -1,
		"questionAmount": 2,
        "questionTContents": [""]
	}

}

```
