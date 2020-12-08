# 領取優惠

Exception Code List:

401 Token Exception, 406 QuotaException, 408 ReLogin Exception, 409 VendorException,410 CouponException, 411 AccountException, 412 APIException, 500 interal Server error,418 ExchangeRateException



{% api-method method="get" host="http://domain name/cch2oas" path="/coupon/apply/{couponCode}" %}
{% api-method-summary %}
get coupon information by coupon code
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="couponCode" type="string" required=true %}
指定優惠碼
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="role" type="string" required=true %}
APP
{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=true %}
zh\_CN
{% endapi-method-parameter %}

{% api-method-parameter name="token" type="string" required=true %}
請代入合法token
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

