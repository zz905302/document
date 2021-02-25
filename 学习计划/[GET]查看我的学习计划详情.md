
### 查看我的某个学习计划的学习详情

**接口描述** 

查看我的某个学习计划详情，列出计划内所有的视频学习列表，文档学习列表，列表中需要带着视频或文档的信息和学习进度。

**接口地址** `/jeecg-boot/cdplancreate/cdPlanCreate/detail`

**请求方式** `GET`

**请求参数**
|参数名称|说明|参数类型|是否必须|类型|schema|
|-|-|-|-|-|-|
|planId|学习计划id|query|true|string||
|userId|用户id|query|true|string||

**响应参数**
|参数名称|说明|类型|schema|
|-|-|-|-|
|createTime|计划发布时间|string||
|content|计划标题内容|string||
|planId|计划id|string||
|state|此计划我的学习状态|int|未学习1，学习中2，学习完成3|
|beginTime|计划开始学习时间|string||
|endTime|计划截止学习时间|string||
|videoNum|计划中视频学习的数量|int||
|documentNum|计划中文档学习的数量|int||
|fileId|文件表中文件的id|string||
|updateTime|文件更新时间|string||
|type|文件类型|string||
|fileSize|文件大小，字节数|int||
|videoTime|视频时长，秒|int||
|url|文件访问地址|string||
|schedule|学习进度|int||
|state|文件学习状态|int|未学习1，学习中2，学习完成3|

**响应示例**
```json
{
    "success": true,
    "message": "操作成功！",
    "code": 200,
    "result": {
        "videos": [{
            "fileId": "0dadda498ed8fb49cba16a6ea0ab160a",
            "updateTime": "2021-02-20 00:00:00",
            "type": "mp4",
            "fileSize": 2103767,
            "videoTime": 22,
            "url": "D:\\eapResource\\static\\a.mp4",
            "schedule": 0,
            "state": 0
        }],
        "documents": [{
            "fileId": "0dadda498ed8fb49cba16a6ea0ab160a",
            "updateTime": "2021-02-20 00:00:00",
            "type": "pdf",
            "fileSize": 10222,
            "videoTime": 0,
            "url": "D:\\eapResource\\static\\a.pdf",
            "schedule": 0,
            "state": 0
        }],
        "createTime": "2021-02-20 00:00:00",
        "content": "测试",
        "planId": "1",
        "state": 1,
        "beginTime": "2021-02-20 00:00:00",
        "endTime": "2021-02-22 00:00:00",
        "videoNum": 1,
        "documentNum": 2
    },
    "timestamp": 1613959778251
}
```
