
### 查看工区学习计划列表

**接口描述** 

查看工区学习计划列表，月份和工区id作为可选筛选条件。月份格式yyyy-MM，筛选开始时间和结束时间。

**接口地址** `/jeecg-boot/cdplancreate/cdPlanCreate/org`

**请求方式** `GET`

**请求参数**
|参数名称|说明|参数类型|是否必须|类型|schema|
|-|-|-|-|-|-|
|monthDate|月份筛选|query|false|string|2021-02|
|orgId|工区id|query|false|string||
|pageNo|分页|query|false|string|1|
|pageSize|分页|query|false|string|10|

**响应参数**
|参数名称|说明|类型|schema|
|-|-|-|-|
|createTime|计划发布时间|string||
|content|标题内容|string||
|planId|计划id|string||
|org|参与的工区名称|string|为空意味全部工区都参与|
|beginTime|计划开始学习时间|string||
|endTime|计划截止学习时间|string||

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
            "org": "综采二区",
            "beginTime": "2021-02-20 00:00:00",
            "endTime": "2021-02-22 00:00:00"
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
