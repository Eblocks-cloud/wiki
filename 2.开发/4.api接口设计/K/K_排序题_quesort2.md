#排序题  quesort1 字典id=26
#请求排序题地址, 数据库字典表sys_dic进行标识排序题型
1,url(测试环境): 

    47.95.218.118:10301/student/question/sort?courseId=2003&id=2108&unitId=108
    
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
        "id": 2108,
        "filed": "　",
        "list": [
            {
              
                "option": "We're still on the ground.2",
                "sort": "2",
             
            },
            {
             
                "option": "We're still on the ground.5",
                "sort": "5",
              
            },
            {
                
                "option": "We're still on the ground.1",
                "sort": "1",
             
            },
            {
               
                "option": "We're still on the ground.4",
                "sort": "4",
             
            },
            {
              
                "option": "We're still on the ground.3",
                "sort": "3",
              
            },
            {
               
                "option": "We're still on the ground.6",
                "sort": "6",
              
            }
        ],
     
        "question": "Question:",
        "itemTitleUs": "Listen and order",
        "itemTitleCn": "听一听并排序。",
     
    }
}
```
5,返回参数说明:
                
                       |     字段    | 字段类型 | 字段说明 |
                       | :---------: | :------:|:--------:|
                        code         String     000000为成功
                        msg          String     为返回的提示语
                        
                        id           int          题组id
                        list--option   String     排列项的数据
                        list--sort   String       排序的正确答案
                        itemTitleUs   String      题组的英文标题
                        itemTitleCn   String      题组的中文标题

