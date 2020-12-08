# 取得會員基本資料

401 Token Exception, 408 ReLogin Exception, 409 VendorException, 411 AccountException, 500 interal Server error

### 2020/10/7 modified:

realName-&gt;nickName 

isValidateName移除

{% api-method method="get" host="http://domain name/cch2oas" path="/usr/data" %}
{% api-method-summary %}
Get member's data
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
 系統核發的合法驗證連線資訊
{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=true %}
Default : zh\_CN
{% endapi-method-parameter %}

{% api-method-parameter name="role" type="string" required=true %}
APP
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "code": 200,
    "exceptionCode": 0,
    "message": "取得资料成功",
    "token": null,
    "data": {
        "account": "RMB1",
        "yearBirthday": "1976",
        "monthBirthday": "08",
        "dayBirthday": "12",
        "nickName": "這是暱稱",
        "telAreaCode": "86",
        "telphoneNo": "0911123566",
        "email": "",
        "weChat": "cynthia",
        "qqAccount": "",
        "isValidateMail": false,
        "isValidateTel": false,
        "isValidateWechat": false,
        "isValidateQQ": false,
        "isValidateWithdraw": false
    },
    "resourceKey": "api.response.code.getSuccess",
    "isOK": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



