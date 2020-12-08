---
description: >-
  401 Token Exception, 406 QuotaException, 408 ReLogin Exception, 409
  VendorException, 410 CouponException, 411 AccountException, 412 APIException,
  500 internal server error
---

# 修改會員基本資料

### 2020/10/7 modified:

realName-&gt;nickName 

isValidateName移除

{% api-method method="post" host="http://domain name/cch2oas" path="/usr/data/edit" %}
{% api-method-summary %}
Modify member's data
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
系統核發的合法連線驗證資訊
{% endapi-method-parameter %}

{% api-method-parameter name="role" type="string" required=true %}
APP
{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=true %}
Default : zh\_CN
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="yearBirthday" type="string" required=false %}
YYYY, 出生日的西元年，year & monthi & day三個欄位必須同時有值，請務必注意
{% endapi-method-parameter %}

{% api-method-parameter name="monthBirthday" type="string" required=false %}
MM, 出生日的月份, 二碼
{% endapi-method-parameter %}

{% api-method-parameter name="dayBirthday" type="string" required=false %}
dd, 出生日的日期, 二碼
{% endapi-method-parameter %}

{% api-method-parameter name="nickName" type="string" required=false %}
暱稱
{% endapi-method-parameter %}

{% api-method-parameter name="telAreaCode" type="string" required=false %}
電話區域碼， 預設是86，請帶數字，不要帶+86
{% endapi-method-parameter %}

{% api-method-parameter name="telphoneNo" type="string" required=false %}
手機號碼
{% endapi-method-parameter %}

{% api-method-parameter name="weChat" type="string" required=false %}
微信賬號
{% endapi-method-parameter %}

{% api-method-parameter name="qqAccount" type="string" required=false %}
QQ賬號
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=false %}
電子郵件
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "code": 200,
    "exceptionCode": 0,
    "message": "修改成功",
    "token": null,
    "data": null,
    "resourceKey": "api.response.code.ModifySuccess",
    "isOK": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



