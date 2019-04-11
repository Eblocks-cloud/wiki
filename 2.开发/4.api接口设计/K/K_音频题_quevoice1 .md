#音频题(主观题)  quevioce1 字典id=1  
#请求音频题地址, 数据库字典表sys_dic进行标识音频类型

1,url(测试环境): 

    47.95.218.118:10301/student/question/video?courseId=2003&id=2314&unitId=108
    
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
        "id": 2314,
        "list": [
            "what is your name？",
            "你叫什么名字，骚年？"
        ],
        "material": "http://qiniu.eblockschina.com/ueditor/jsp/upload/video/20190403/1554259434703040117.mp3",
       
        "itemTitleUs": "Listen and read",
        "itemTitleCn": "听一听，读一读。"
      
    }
}
```

5,返回参数说明:

                          |     字段    | 字段类型 | 字段说明 |
                          | :---------: | :------:|:--------:|
                           code           String     000000为成功
                           msg            String     为返回的提示语
                           
                           id              int          题组id
                           questionType     String      题组的类型,此类型就在字典表(sys_dic)中主键id
                           list            Array        音频对应的句子可能是英文短句,也可能是中文短句,也可能都含有
                           itemTitleCn     String       题组的中文标题(可有可无)
                           itemTitleUs     String       题组的英文标题(可有可无)
                           material        String       音频的地址
