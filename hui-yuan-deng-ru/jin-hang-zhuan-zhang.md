# 額度轉移

{% api-method method="post" host="http://domain name/cch2oas" path="/usr/quota/transfer/" %}
{% api-method-summary %}
取得轉賬面版預設顯示資訊
{% endapi-method-summary %}

{% api-method-description %}
 注意事項：轉賬不能遊戲互轉，from or to需有其中一個ID\_CCHOSTING
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

{% api-method-body-parameters %}
{% api-method-parameter name="from" type="string" required=true %}
 來源產品Id
{% endapi-method-parameter %}

{% api-method-parameter name="to" type="string" required=true %}
目的產品Id
{% endapi-method-parameter %}

{% api-method-parameter name="amount" type="number" required=true %}
轉賬額度
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "code": 200,
    "exceptionCode": 0,
    "message": "额度转移成功",
    "token": null,
    "data": [
        {
            "productId": "ID_CCHOSTING",
            "name": "CCH平台",
            "balance": 1555.47,
            "inTransit": 0.0
        },
        {
            "productId": "KY",
            "name": "开元",
            "balance": 0.0,
            "inTransit": 0.0
        }
    ],
    "resourceKey": "api.response.code.quotaTransferSuccess",
    "isOK": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

