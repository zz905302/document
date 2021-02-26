
### 提交学习计划的文件学习进度

**接口描述** 

提交文件的学习进度，包括视频学习和文档学习。

**接口地址** `/jeecg-boot/cdplanrecord/cdPlanRecord/add`

**请求方式** `POST`

**consumes** `["application/json"]`

**请求参数**
|参数名称|说明|参数类型|是否必须|类型|schema|
|-|-|-|-|-|-|
|fileId|学习文件ID|body|false|string||
|planId|学习计划ID|body|false|string||
|orgId|工区id|body|false|string||
|org|工区|body|false|string||
|userId|用户ID|body|false|string||
|realName|用户姓名|body|false|string||
|schedule|学习进度：视频学习的进度条读秒。不是视频默认值0即可|body|false|int32||
|state|学习状态0->未完成；1->已完成|body|false|int32||

**响应示例**
```json
{
    "code": 0,
    "message": "",
    "result": {},
    "success": true,
    "timestamp": 0
}
```
