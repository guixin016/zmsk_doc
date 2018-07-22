### App应用升级信息接口文档 ###

---

### 获取最新版本的应用下载地址信息

|URL|face.doinggo.com/api/device/app/info/latest?version=&deviceId=|
|---|---|
|method|GET|

参数说明

|参数名|描述|是否必填|
|---|---|---|
|version|版本号|是|
|deviceId|设备Id|否|

返回值

未找到升级信息

```json
{
  "code": 204,
  "msg": "not app version fund"
}
```

成功

```json
{
  "code": 200,
  "data": {
    "appUrl": "app.face.doingg.com/adfsd/edd/134ddd.apk",
    "appVersion": 3,
    "ctime": 1532271494,
    "description": "test",
    "deviceId": 12,
    "id": 1
  },
  "msg": "success"
}
```

返回值参数说明

|参数名|描述|
|---|---|
|id|主键|
|appVersion|版本号|
|appUrl|app更新地址|
|description|描述信息|