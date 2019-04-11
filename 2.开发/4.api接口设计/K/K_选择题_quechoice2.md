#选择题  quechoice1 字典id=7
#请求音频题地址, 数据库字典表sys_dic进行标识音频类型

1,url(测试环境): 

    47.95.218.118:10301/student/question/select?courseId=2003&id=2318&unitId=108
    
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
    "data": [
        {
            "id": 2319,
            "filed": "http://qiniu.eblockschina.com/ueditor/jsp/upload/video/20190403/1554259724161077905.mp3"
            "list": [
                {
                    "result": 1,
                    "option": "http://qiniu.eblockschina.com/ueditor/jsp/upload/image/20190403/1554259730033097435.png"
                 
                },
                {
                    "result": 0,
                    "option": "http://qiniu.eblockschina.com/ueditor/jsp/upload/image/20190403/1554259732859052906.png"
                  
                },
                {
                    "result": 0,
                    "option": "http://qiniu.eblockschina.com/ueditor/jsp/upload/image/20190403/1554259737055070986.png"
                  
                }
            ]
        
          
        }
    ]
}
```
5,返回参数说明:

                                      |     字段    | 字段类型 | 字段说明 |
                                      | :---------: | :------:|:--------:|
                                       code           String     000000为成功
                                       msg            String     为返回的提示语
                                       
                                       id              int          题组id
                                       filed           String       音频地址
                                       list--result       int       1是正确选项,0是错误选项
                                       list--option    String         选择的选项数据
                                       itemTitleCn     String       题组的中文标题(可有可无)
                                       itemTitleUs     String       题组的英文标题(可有可无)
                                       randomList      Array        随机排序的图片数组
