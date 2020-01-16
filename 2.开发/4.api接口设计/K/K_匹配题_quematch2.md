#匹配题  quematch1 字典id=13
#请求匹配题地址, 数据库字典表sys_dic进行标识匹配题类型

1,url(测试环境): 

    47.95.218.118:10301/student/question/match?courseId=2003&id=2335&unitId=108
    
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
        "id": 2335,
        "video": "http://qiniu.eblockschina.com/ueditor/jsp/upload/video/20190403/1554260597599033359.mp3",
              "list": [
            [
                "what are you (d1o) now ?"
            ],
            [
                "what are you (d2o) now ?"
            ]
        ],
       
        "randomList": [
            "d2o",
            "d1o"
        ],
        "matchType": 13,
        "itemTitleUs": "Read and complete the sentences",
        "itemTitleCn": "读一读，选择正确的单词使句子成立。"
    }
}
```

5,返回参数说明:
            
            
                                                   |     字段    | 字段类型 | 字段说明 |
                                                   | :---------: | :------:|:--------:|
                                                    code           String     000000为成功
                                                    msg            String     为返回的提示语
                                                    
                                                    id              int          题组id
                                                    video           String       音频地址
                                                    list            Array       子题组的题干
                                                    matchType       int          题组的类型,此类型就在字典表(sys_dic)中主键id
                                                    itemTitleCn     String       题组的中文标题
                                                    itemTitleUs     String       题组的英文标题
                                                    randomList      Array        随机的选择数据

