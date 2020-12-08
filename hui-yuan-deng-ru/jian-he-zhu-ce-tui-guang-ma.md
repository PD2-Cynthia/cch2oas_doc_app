# 檢核註冊推廣碼

{% api-method method="post" host="http://domain name/cch2oas" path="/usr/promote/check" %}
{% api-method-summary %}
檢核是否有此推廣代碼 
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="lang" type="string" required=true %}
依CCHAPI提供的語系代碼為主，預設為zh\_CN
{% endapi-method-parameter %}

{% api-method-parameter name="role" type="string" required=true %}
APP:APP介接  
MOBILE：行動網頁版  
  
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="vendorId" type="string" required=true %}
業主id，請傳大寫
{% endapi-method-parameter %}

{% api-method-parameter name="siteId" type="string" required=true %}
子網id，請傳大寫
{% endapi-method-parameter %}

{% api-method-parameter name="partnerId" type="string" required=true %}
推廣代碼
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
會員賬密驗證OK，且回傳token
{% endapi-method-response-example-description %}

```javascript
{
    "code": 200,
    "exceptionCode": 0,
    "message": "取得资料成功",
    "token": null,
    "data": null,
    "resourceKey": "api.response.code.getSuccess",
    "isOK": false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### 



