### apk 版本操作接口文档 ###
---

### 获取比给定version大的apk版本信息

|URL|http://zd.doinggo.com/api/apk/version/query?versionCode=|
|---|---|
|method|GET|

参数说明

|参数名|参数描述|
|---|--|
|versionCode|客户端上当前版本号|

返回值

没有更新的版本信息

```json
{
  "code": 204,
  "msg": "not upgrade version"
}
```

有更新的版本信息

```json
{
  "code": 200,
  "data": {
    "createTime": 1522568583,
    "description": "1.添加无网络提示。\r\n2.添加Launcher Flag，通过成为桌面达到应用自启的目的。",
    "downloadUrl": "http://zd.doinggo.com/download/apk/zd_emenu_beta_1.0010.01.apk",
    "id": 2,
    "version": 1001001
  },
  "msg": "success"
}
```

返回值参数说明

|参数名|参数描述|
|---|--|
|id|主键Id|
|version|版本号|
|downloadUrl|版本更新地址|
|description|版本更新描述信息|
|createTime|时间戳|
