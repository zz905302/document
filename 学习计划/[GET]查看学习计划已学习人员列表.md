
### 查看学习计划已学习人员列表

**接口描述** 

通过学习计划的id查看此计划已经学习的人员列表，按照完成学习的时间排序，最先完成的在前面，带分页。

**接口地址** `/jeecg-boot/`

**请求方式** `GET`

**请求参数**
|参数名称|说明|参数类型|是否必须|类型|schema|
|-|-|-|-|-|-|
|planId|学习计划id|query|true|string||
|pageNo|分页|query|false|int|1|
|pageSize|分页|query|false|int|10|

**响应参数**
|参数名称|说明|类型|schema|
|-|-|-|-|
|updateTime|完成学习的时间|string|yyyy-MM-dd HH:mm:ss|
|planId|学习计划id|string||
|userId|完成学习的用户id|string||
|realName|完成学习的用户姓名|string||
|orgId|完成学习的用户所在工区id|string||
|org|完成学习的用户所在工区|string||

**响应示例**
```json
{
    "success": true,
    "message": "操作成功！",
    "code": 200,
    "result": {
        "records": [{
            "updateTime": "2021-02-20 00:00:00",
            "planId": "1",
            "userId": "abc",
            "realName": "赵杰",
            "orgId": "abcd",
            "org": "综采二区"
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
