# 設定會員提現賬戶資訊

Excption Code List:

401 Token Exception, 408 ReLogin Exception, 409 VendorException, 411 AccountException, 500 interal Server error, 410 CouponException, 412 APIException, 416 RebateException, 418 ExchangeRateException

410 CouponException, 412 APIException, 416 RebateException, 418 ExchangeRateException

### 2020/10/7 modified

realName -&gt; bankAccountName

{% api-method method="post" host="http://domain name/cch2oas" path="/usr/withdrawBank" %}
{% api-method-summary %}
 提現賬戶資料設定
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="lang" type="string" required=false %}
depends on CCHAPI說明，default：zh\_CN
{% endapi-method-parameter %}

{% api-method-parameter name="role" type="string" required=true %}
APP：APP開發介接  
MOBILE：行動網頁版
{% endapi-method-parameter %}

{% api-method-parameter name="token" type="string" required=true %}
系統登入時提供的合法token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="telAreaCode" type="string" required=false %}
手機號區域碼
{% endapi-method-parameter %}

{% api-method-parameter name="telPhoneNo" type="string" required=false %}
手機號
{% endapi-method-parameter %}

{% api-method-parameter name="bankAccountName" type="string" required=true %}
戶名
{% endapi-method-parameter %}

{% api-method-parameter name="bankOther" type="string" required=false %}
bankNo與bankOther只能擇一，若其他銀行有資料，bankNo請給空值或null
{% endapi-method-parameter %}

{% api-method-parameter name="bankNo" type="string" required=true %}
銀行代碼
{% endapi-method-parameter %}

{% api-method-parameter name="bankAccountNo" type="string" required=true %}
銀行賬號
{% endapi-method-parameter %}

{% api-method-parameter name="bankBranch" type="string" required=true %}
銀行網關\(分行\)
{% endapi-method-parameter %}

{% api-method-parameter name="bankProvince" type="string" required=true %}
 省
{% endapi-method-parameter %}

{% api-method-parameter name="bankCity" type="string" required=true %}
 市
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
提現賬戶設定成功
{% endapi-method-response-example-description %}

```javascript
{
    "code": 200,
    "exceptionCode": 0,
    "message": "提现账户设定成功",
    "token": null,
    "data": null,
    "resourceKey": "api.response.code.withdrawBankSuccess",
    "isOK": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### Request Body Sample

```javascript
{
	"bankNo":"5",
	"bankAccountNo":"30150526314",
	"bankBranch":"前鎮加工區分行",
	"bankProvince":"71",
	"bankCity":"000006",
	"bankOther":""
}
```



