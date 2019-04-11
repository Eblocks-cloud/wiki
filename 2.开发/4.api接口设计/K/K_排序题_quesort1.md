#排序题  quesort1 字典id=17
#请求排序题地址, 数据库字典表sys_dic进行标识排序题型
1,url(测试环境): 

    47.95.218.118:10301/student/question/sort?courseId=2003&id=2344&unitId=108
    
2,请求方式: 

    get
    
3,入参数说明:

              |------------|--------------|----------|
                 数据字段       数据类型     字段说明
                 courseId        int          级别id
                 id              int          题组id
                 unitId          int          单元id
4,返回参数格式:

```
{
    "success": null,
    "code": "000000",
    "msg": "成功",
    "description": null,
    "data": {
        "id": 2344,
        "list": [
            {
                "id": 2345,
                "filed": "(it1) (is1) (ok1)",
                "list": [
                    "is1",
                    "ok1",
                    "it1"
                ],
            },
        ],
        "question": "Question:",
        "itemTitleUs": "Rearrange the words to make sentences",
        "itemTitleCn": "重新排序单词组成句子。"
    }
}
```
5,返回参数说明:
    
       |     字段    | 字段类型 | 字段说明 |
       | :---------: | :------:|:--------:|
        code         String     000000为成功
        msg          String     为返回的提示语
        id           int         题组id
        list--id     int         子题题组的id
        list--field   String     排序的正确答案
        list--list    Array      随机展示的排序
        itemTitleUs   String     题组的英文标题
        itemTitleCn   String     题组的中文标题
    
