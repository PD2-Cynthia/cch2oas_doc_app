# 取得指定優惠

Exception Code List:

401 Token Exception, 408 ReLogin Exception, 409 VendorException,410 CouponException, 411 AccountException, 500 interal Server error

{% api-method method="get" host="http://domain name/cch2oas" path="/coupon/check/{couponCode}" %}
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

```javascript
{
    "code": 200,
    "exceptionCode": 0,
    "message": "取得资料成功",
    "token": null,
    "data": "目标洗码是4天，完成目标5倍洗码",
    "resourceKey": "api.response.code.getSuccess",
    "isOK": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

