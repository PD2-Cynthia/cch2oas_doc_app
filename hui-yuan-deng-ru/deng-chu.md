# 登出

{% api-method method="get" host="http://domain name/cch2oas" path="/usr/logout" %}
{% api-method-summary %}
User logout
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="lang" type="string" required=true %}
depends on CCHAPI說明，default : zh\_CN
{% endapi-method-parameter %}

{% api-method-parameter name="role" type="string" required=true %}
APP：APP開發介接  
MOBILE：行動網頁版介接
{% endapi-method-parameter %}

{% api-method-parameter name="token" type="string" required=true %}
系統合法發出的連線資訊
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

