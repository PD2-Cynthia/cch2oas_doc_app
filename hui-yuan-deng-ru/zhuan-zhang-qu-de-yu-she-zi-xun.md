# 轉賬取得預設資訊

{% api-method method="get" host="http://domain name/cch2oas" path="/usr/quota/transfer/default/{method}" %}
{% api-method-summary %}
取得轉賬面版預設顯示資訊
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="method" type="string" required=true %}
first:只讀取第一筆的產品餘額，all 或 為空時視為查詢全部
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
        "from": "ID_CCHOSTING",
        "fromName": "CCH平台",
        "fromQuota": 4613.44,
        "productQuotaList": [
            {
                "productId": "BB",
                "name": "波音",
                "balance": 0.0,
                "inTransit": 0.0
            },
            {
                "productId": "AGIN",
                "name": "AG",
                "balance": 0.0,
                "inTransit": 0.0
            },
            {
                "productId": "KY",
                "name": "开元",
                "balance": 1500.0,
                "inTransit": 0.0
            }
        ],
        "productList": [
            {
                "productId": "ID_CCHOSTING",
                "name": "CCH平台"
            },
            {
                "productId": "BB",
                "name": "波音"
            },
            {
                "productId": "AGIN",
                "name": "AG"
            },
            {
                "productId": "KY",
                "name": "开元"
            }
        ],
        "err": [
            {
                "keyword": "AGIN",
                "name": "AG",
                "message": null
            }
        ]
    },
    "resourceKey": "api.response.code.getSuccess",
    "isOK": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



