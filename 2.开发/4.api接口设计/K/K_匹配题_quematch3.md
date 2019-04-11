#匹配题  quematch1 字典id=14
#请求匹配题地址, 数据库字典表sys_dic进行标识匹配题类型

1,url(测试环境): 

    47.95.218.118:10301/student/question/match?courseId=2003&id=2342&unitId=108
    
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
        "id": 2342,
        "list": [
            {
                "id": 648,
                "leftPair": "one",
                "rightPair": "1"
            },
            {
                "id": 649,
                "leftPair": "two",
                "rightPair": "2"
            },
            {
                "id": 650,
                "leftPair": "three",
                "rightPair": "3"
            },
            {
                "id": 651,
                "leftPair": "four",
                "rightPair": "4"
                
            }
        ],
        "randomList": [
            "3",
            "4",
            "2",
            "1"
        ],
        "itemTitleUs": "Readandmatch",
        "itemTitleCn": "读一读，选一选。"
    }
}
```

5,返回参数说明:
           

                                 |     字段    | 字段类型 | 字段说明 |
                               | :---------: | :------:|:--------:|
                                code           String     000000为成功
                                msg            String     为返回的提示语
                                
                                id              int          题组id
                                questionType    String       题组的类型,此类型就在字典表(sys_dic)中主键id
                                list--id        int          子类地址的id
                                list--leftPair  String       匹配题对应的音频地址
                                list--rightPair String       匹配题对应的图片地址
                                itemTitleCn     String       题组的中文标题
                                itemTitleUs     String       题组的英文标题
                                randomList      Array        随机排序的图片数组


