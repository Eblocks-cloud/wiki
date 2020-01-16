#排序题  quesort1 字典id=27
#请求排序题地址, 数据库字典表sys_dic进行标识排序题型

1,url(测试环境): 

    47.95.218.118:10301/student/question/sort?courseId=2003&id=2099&unitId=108
    
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
        "id": 2099,
        "filed": "First Flight　　Mr. Johnson had never been up in an aerophane before and he had read a lot about air accidents, so one day when a friend offered to take him for a ride in his own small phane, Mr. Johnson was very worried about accepting. Finally, however, his friend persuaded him that it was very safe, and Mr. Johnson boarded the plane.　　His friend started the engine and began to taxi onto the runway of the airport. Mr. Johnson had heard that the most dangerous part of a flight were the take-off and the landing, so he was extremely frightened and closed his eyes.　　After a minute or two he opened them again, looked out of the window of the plane, and said to his friend, Look at those people down there. They look as small as ants, don't they?　　Those are ants, answered his friend. We're still on the ground.",
        "list": [
            {
              
                "option": "We're still on the ground.1",
                "sort": "1",
              
            },
            {
               
                "option": "We're still on the ground.4",
                "sort": "4",
             
            },
            {
              
                "option": "We're still on the ground.2",
                "sort": "2",
             
            },
            {
             
                "option": "We're still on the ground.3",
                "sort": "3",
              
            }
        ],
        "itemTitleUs": "Read the text and order",
        "itemTitleCn": "阅读文章并将下列句子排序。",
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
                                      filed         String      英语短文
