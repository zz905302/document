
### 查看我的学习数量统计
**接口描述** 
统计我的学习计划学习情况，正在学习的数量，未学习的数量，累计完成学习的数量
**接口地址** `/jeecg-boot/cdplanresult/cdPlanResult/mine`
**请求方式** `GET`
**请求参数**
|参数名称|说明|参数类型|是否必须|类型|schema|
|-|-|-|-|-|-|
|orgId|工区id|query|true|string||
|userId|用户id|query|true|string||
**响应参数**
|参数名称|说明|类型|schema|
|-|-|-|-|
|learning|正在学习的计划数量|int||
|notYetLearn|未学习的计划数量|int||
|completed|累计完成学习的计划数量|int||
**响应示例**
```json
{
    "success": true,
    "message": "操作成功！",
    "code": 200,
    "result": {
        "learning": 1,
        "notYetLearn": 1,
        "completed": 1
    },
    "timestamp": 1613959949574
}
```
