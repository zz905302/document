
### 查看我的学习计划列表

**接口描述** 

查看我的学习计划列表，正在学习的，未学习的，累计完成学习的，可使用月份进行筛选，带分页。月份格式yyyy-MM，筛选开始时间和结束时间。

**接口地址** `/jeecg-boot/cdplancreate/cdPlanCreate/mine`

**请求方式** `GET`

**请求参数**
|参数名称|说明|参数类型|是否必须|类型|schema|
|-|-|-|-|-|-|
|orgId|工区id|query|true|string||
|userId|用户id|query|true|string||
|state|学习状态|query|true|string|全部0，未学习1，学习中2，学习完成3|
|monthDate|月份筛选|query|false|string|2021-02|
|pageNo|分页|query|false|string|1|
|pageSize|分页|query|false|string|10|

**响应参数**
|参数名称|说明|类型|schema|
|-|-|-|-|
|createTime|计划发布时间|string||
|content|标题内容|string||
|planId|计划id|string||
|state|此计划我的学习状态|int|未学习1，学习中2，学习完成3|
|beginTime|计划开始学习时间|string||
|endTime|计划截止学习时间|string||
|videoNum|计划中视频学习的数量|int||
|documentNum|计划中文档学习的数量|int||

**响应示例**
```json
{
    "success": true,
    "message": "操作成功！",
    "code": 200,
    "result": {
        "records": [{
            "createTime": "2021-02-20 00:00:00",
            "content": "测试",
            "planId": "1",
            "state": 1,
            "beginTime": "2021-02-20 00:00:00",
            "endTime": "2021-02-22 00:00:00",
            "videoNum": 1,
            "documentNum": 2
        }],
        "total": 1,
        "size": 10,
        "current": 1,
        "orders": [],
        "optimizeCountSql": true,
        "hitCount": false,
        "searchCount": true,
        "pages": 1
    },
    "timestamp": 1613959778251
}
```
