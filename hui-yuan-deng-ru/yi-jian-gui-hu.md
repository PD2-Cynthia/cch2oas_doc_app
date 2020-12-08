# 一鍵歸戶

{% api-method method="post" host="http://domain name/cch2oas" path="/usr/quota/revokeAll" %}
{% api-method-summary %}
將外站錢包餘額取回至CCH平台
{% endapi-method-summary %}

{% api-method-description %}

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
若取回沒有錯誤，err則為null
{% endapi-method-response-example-description %}

```javascript
{
    "code": 200,
    "exceptionCode": 0,
    "message": "一键取回成功",
    "token": null,
    "data": {
        "err": [
            {
                "keyword": "BB",
                "name": "波音",
                "message": "API忙碌中"
            },
            {
                "keyword": "AGIN",
                "name": "AG",
                "message": "API忙碌中"
            }
        ],
        "quota": {
            "productId": "ID_CCHOSTING",
            "name": "CCH平台",
            "balance": 6113.44,
            "inTransit": 0.0
        }
    },
    "resourceKey": "api.response.code.revokeAllSuccess",
    "isOK": false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

