# 取得可轉賬產品列表

{% api-method method="get" host="http://domain name/cch2oas" path="/product/list" %}
{% api-method-summary %}
取得可轉賬產品列表
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
token
{% endapi-method-parameter %}

{% api-method-parameter name="role" type="string" required=true %}
APP:APP開發介接  
MOBILE:行動網頁版
{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=true %}
depends on CCHAPI說明，default : zh\_CN
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
取得成功
{% endapi-method-response-example-description %}

```javascript
{
    "code": 200,
    "exceptionCode": 0,
    "message": "取得资料成功",
    "token": null,
    "data": [
        {
            "productId": "ID_CCHOSTING",
            "name": "CCH平台",
            "sort": 0
        },
        {
            "productId": "BB",
            "name": "波音",
            "sort": 3
        },
        {
            "productId": "AGIN",
            "name": "AG",
            "sort": 4
        },
        {
            "productId": "KY",
            "name": "开元",
            "sort": 5
        }
    ],
    "resourceKey": "api.response.code.getSuccess",
    "isOK": false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

