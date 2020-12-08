# 產品錢包餘額\(含在途\)

{% api-method method="get" host="http://domain name/cch2oas" path="/usr/quota/product/{productId}" %}
{% api-method-summary %}
取得產品錢包餘額及在途餘額
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="productId" type="string" required=true %}
productId可以傳ID\_CCOSTING查CCH平台餘額，CB, CCPEG回傳的都會是CCH平台餘額，產品錢包餘額主要查的是外站產品錢包，KY, AGIN, BB
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

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
        "productId": "KY",                    //產品id
        "name": "开元",                        //產品名稱
        "balance": 0.0,                       //錢包餘額
        "inTransit": 0.0                      //在途餘額
    },
    "resourceKey": "api.response.code.getSuccess",
    "isOK": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

