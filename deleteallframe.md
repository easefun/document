# 删除视频的全部打点信息

### deleteKeyFrame

作用：通过API删除视频的全部视频打点信息

### URL

[http://api.polyv.net/v2/video/{userid}/deleteKeyFrame](http://api.polyv.net/v2/video/{userid}/deleteKeyFrame)

### 支持格式

JSON

### HTTP请求方式

POST,GET

### 请求数限制

TRUE

### 请求参数

| 参数名 |
| :--- |


|  | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| ptime | 是 | string | 当前时间的毫秒级时间戳（13位），3分钟内有效 |
| vid | 是 | string | 视频ID |
| sign | 是 | string | 签名，为40位大写的SHA1值 |



### JSON示例

| `{` |
| :--- |


| `code: 200,` |
| :--- |


| `status:"success",` |
| :--- |


| `message:"success",` |
| :--- |


| `data:"success"` |
| :--- |


| `}` |
| :--- |


### 字段说明

| 字段 | 说明 |
| :--- | :--- |
| status | 成功/失败状态 |
| code | 成功/失败代码 |
| message | 成功/失败信息 |
| data | 成功/失败数据 |

### php请求示例

| `<?php` |
| :--- |


| `$userid="8f8482aaab";` |
| :--- |


| `$secretkey="AiDQw1mAmi";` |
| :--- |


| `$ptime=time()*1000;` |
| :--- |


| `$str="ptime=$ptime&vid=$vid".$secretkey;` |
| :--- |


| `$sign=strtoupper(sha1($str));` |
| :--- |


| `$vid="8f8482aaab8fe7ea12e3314a11a061fc_8";` |
| :--- |


| `$url="http://api.polyv.net/v2/video/$userid/deleteKeyFrame?ptime=$ptime&vid=$vid&sign=$sign";` |
| :--- |


| `$content=file_get_contents($url);` |
| :--- |


| `echo$content;` |
| :--- |


| `?>` |
| :--- |


### 签名规则

将请求参数（sign除外）按照参数名字典顺序排列，用“

&

”连接参数名与参数值,并在最后加上secretkey的值，生成40位大写的SHA1值，作为sign。

以下是示例过程：

**1. 将请求参数按照参数名字典顺序排列为：**

ptime=”

1476753635000

“;

vid=”8f8482aaab8fe7ea12e3314a11a061fc\_8″;

**2. 连接字符串**

 用“

&

”连接参数名与参数值,并在最后加上secretkey的值，生成40位大写的SHA1值，作为sign（本示例的值为AiDQw1mAmi），如下： ptime=

1476753635000

&

vid=8f8482aaab8fe7ea12e3314a11a061fc\_8

AiDQw1mAmi

**3. 生成签名sign**

sign为40位大写的SHA1值：B2E2D7AAB9DFCC8CBFE7EDC919B5F8F6F4E104BC

