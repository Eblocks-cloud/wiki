## banner管理

### 轮播图 ele_banner

| 列名                | 类型     | 长度 | 是否主键 | 是否索引 | 是否为空 | 备注                         |
| ------------------- | -------- | ---- | -------- | -------- | -------- | ---------------------------- |
| id                  | bigint   | 20   | 是       | 是       | 否       | 自增主键                     |
| title               | varchar  | 64   | 否       | 否       | 否       | 标题                         |
| location            | varchar  | 64   | 否       | 否       | 否       | 所属位置                     |
| sort                | int      | 8    | 否       | 否       | 否       | 排序                         |
| img_url             | varchar  | 64   | 否       | 否       | 否       | 图片                         |
| img_link            | varchar  | 64   | 否       | 否       | 否       | 图片链接                     |
| begin_time          | datetime | 0    | 否       | 否       | 否       | 开始时间                     |
| end_time            | datetime | 0    | 否       | 否       | 否       | 结束时间                     |
| status              | tinyint  | 8    | 否       | 否       | 否       | 状态 0:未上架 1:上架 默认0   |
| is_delete           | bit      | 1    | 否       | 否       | 否       | 是否删除 0:正常 1:删除 默认0 |
| create_user_id      | bigint   | 64   | 否       | 否       | 否       | 创建人                       |
| create_time         | datetime | 0    | 否       | 否       | 否       | 创建时间                     |
| last_modify_user_id | bigint   | 64   | 否       | 否       | 否       | 最后修改人                   |
| last_modify_time    | datetime | 0    | 否       | 否       | 否       | 最后修改时间                 |



### 轮播图校区关系 ele_banner_school_relation

|           | 类型   | 长度 | 是否主键 | 是否索引 | 是否为空 | 备注     |
| --------- | ------ | ---- | -------- | -------- | -------- | -------- |
| id        | bigint | 20   | 是       | 是       | 否       | 自增主键 |
| banner_id | bigint | 64   | 否       | 否       | 否       | bannerID |
| school_id | bigint | 64   | 否       | 否       | 否       | 校区ID   |