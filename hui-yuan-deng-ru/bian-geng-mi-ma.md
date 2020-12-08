# 變更密碼

401 Token Exception, 408 ReLogin Exception, 409 VendorException, 411 AccountException, 500 interal Server error

{% api-method method="post" host="http://domain name/cch2oas" path="/usr/password" %}
{% api-method-summary %}
變更會員密碼
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="lang" type="string" required=false %}
depends on CCHAPI說明提供語系，default is zh\_CN
{% endapi-method-parameter %}

{% api-method-parameter name="role" type="string" required=true %}
APP:APP開發介接  
MOBILE:行動網頁版介接
{% endapi-method-parameter %}

{% api-method-parameter name="token" type="string" required=true %}
會員於登入時系統發給的合法token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="newPassword" type="string" required=true %}
會員新密碼，請以base64編碼後傳送
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=true %}
會員舊密碼，請以MD5加密後，以小寫傳送
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
密碼設定成功
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



