# 取得個人最新資訊

Exception Code List:

401 Token Exception, 408 ReLogin Exception, 409 VendorException, 411 AccountException, 500 interal Server error, 412 APIException

{% api-method method="get" host="http://domain name/cch2oas" path="/usr/refresh" %}
{% api-method-summary %}
取得最新個人資訊
{% endapi-method-summary %}

{% api-method-description %}
Response回傳的code及內容請follow會員登入即可，不再重複贅述
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="lang" type="string" required=true %}
depends on CCHAPI說明，default: zh\_CN
{% endapi-method-parameter %}

{% api-method-parameter name="role" type="string" required=true %}
APP:APP開發介接  
MOBILE：行動網頁版
{% endapi-method-parameter %}

{% api-method-parameter name="token" type="string" required=true %}
登入時系統核發的token.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "code": 200,
    "exceptionCode": 0,
    "message": "取得资料成功",
    "token": null,
    "data": {
        "vendorId": "CCTEST",
        "siteId": "SITE1",
        "account": "RD104",
        "bankSet": false,
        "withdrawPasswordSet": false,
        "pause": "N",
        "quota": 0.0,
        "gradeName": "VIP0",
        "unreadCount": 0  //未讀訊息個數
    },
    "resourceKey": "api.response.code.getSuccess",
    "isOK": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



