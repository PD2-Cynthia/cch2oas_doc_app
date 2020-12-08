# 資金密碼設定

Exception Code List:

401 Token Exception, 408 ReLogin Exception, 409 VendorException, 411 AccountException, 500 interal Server error

{% api-method method="post" host="http://domain name/cch2oas" path="/usr/withdrawPassword" %}
{% api-method-summary %}
資金密碼設定
{% endapi-method-summary %}

{% api-method-description %}
依照URL的規則進行會員的提現密碼設定
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="lang" type="string" required=false %}
depends on CCHAPI說明，default: zh\_CN
{% endapi-method-parameter %}

{% api-method-parameter name="role" type="string" required=true %}
APP:APP開發介接  
MOBILE:行動網頁版介接
{% endapi-method-parameter %}

{% api-method-parameter name="token" type="string" required=true %}
會員登入驗證成功時，系統提供的token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="withdrawPasswordOrg" type="string" required=false %}
已設定過資金密碼者，需再以Base64傳送原資金密碼供API驗證
{% endapi-method-parameter %}

{% api-method-parameter name="withdrawPassword" type="string" required=true %}
會員要設定的提現密碼，以Base64進行編碼傳送
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
代表API連線OK，是否設定密碼成功，請見回傳內容
{% endapi-method-response-example-description %}

```javascript
{
    "code": 200,
    "exceptionCode": 0,
    "message": "密码设定成功",
    "token": null,
    "data": null,
    "resourceKey": "api.response.code.passwordSuccess",
    "isOK": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### API驗證流程

1. 檢查token是否逾時或格式錯誤
2. 變更提現密碼成功

### Response說明

| 欄位 | 型態 | example | 說明 |
| :--- | :--- | :--- | :--- |
| isOK | boolean | true or false | true代表設定密碼成功 |
| message | 文字 |  | 顯示失敗的錯誤訊息 |
| token | 文字 |  |  |
| data | 物件 |  |  |

