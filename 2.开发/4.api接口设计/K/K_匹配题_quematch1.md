#匹配题  quematch1 字典id=12 
#请求匹配题地址, 数据库字典表sys_dic进行标识匹配题类型

1,url(测试环境): 

    47.95.218.118:10301/student/question/match?courseId=2003&id=2334&unitId=108
    
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
    "data": {
        "id": 2334,
        "list": [
            {
                "id": 644,
                "leftPair": "http://qiniu.eblockschina.com/ueditor/jsp/upload/video/20190403/1554260230472054704.mp3",
                "rightPair": "http://qiniu.eblockschina.com/ueditor/jsp/upload/image/20190403/1554260348631072693.jpg"
               
            },
            {
                "id": 645,
                "leftPair": "http://qiniu.eblockschina.com/ueditor/jsp/upload/video/20190403/1554260253404000247.mp3",
                "rightPair": "http://qiniu.eblockschina.com/ueditor/jsp/upload/image/20190403/1554260335497019677.png"
               
            },
            {
                "id": 646,
                "leftPair": "http://qiniu.eblockschina.com/ueditor/jsp/upload/video/20190403/1554260262637096935.mp3",
                "rightPair": "http://qiniu.eblockschina.com/ueditor/jsp/upload/image/20190403/1554260330776079702.png"
               
            },
            {
                "id": 647,
                "video": null,
                "imageurl": null,
                "classId": null,
                "leftPair": "http://qiniu.eblockschina.com/ueditor/jsp/upload/video/20190403/1554260273389080348.wav",
                "rightPair": "http://qiniu.eblockschina.com/ueditor/jsp/upload/image/20190403/1554260326246072365.png"
              
            }
        ],
       
        "randomList": [
            "http://qiniu.eblockschina.com/ueditor/jsp/upload/image/20190403/1554260335497019677.png",
            "http://qiniu.eblockschina.com/ueditor/jsp/upload/image/20190403/1554260330776079702.png",
            "http://qiniu.eblockschina.com/ueditor/jsp/upload/image/20190403/1554260326246072365.png",
            "http://qiniu.eblockschina.com/ueditor/jsp/upload/image/20190403/1554260348631072693.jpg"
        ],
        
        "itemTitleUs": "Listen and choose",
        "itemTitleCn": "听一听，选择正确答案。"
       
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
