# 會員登入

Exception Code：409 VendorException, 411 AccountException, 500 interal Server error

{% api-method method="post" host="http://domain name/cch2oas" path="/usr/login" %}
{% api-method-summary %}
驗證會員登入資訊並回傳token
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

{% api-method-parameter name="password" type="string" required=true %}
會員輸入的密碼，以MD5編碼後，以小寫傳送
{% endapi-method-parameter %}

{% api-method-parameter name="account" type="string" required=true %}
會員賬號，請傳大寫
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
    "message": "会员登入成功.",
    "token": "eyJhbGciOiJIUzI1NiJ9.eyJ2ZW5kb3JJZCI6IkNDVEVTVCIsInNpdGVJZCI6IlNJVEUxIiwiYWNjb3VudCI6IlJEMTAyIiwiZXhwIjoxNTk1MDM0MjMwfQ.OAhFChnxU-sIAxgPvO9aFvhTB2YXP7YDQVALLhueOeE",
    "data": {
        "vendorId": "CCTEST",
        "siteId": "SITE1",
        "account": "RD102",
        "bankSet": true,
        "withdrawPasswordSet": false,
        "pause": "N",
        "quota": 1482.4,
        "err": null,
        "gradeName": "VIP1",
        "unreadCount": 0  //未讀訊息個數
    },
    "resourceKey": "api.response.code.loginSuccess",
    "isOK": true
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=411 %}
{% api-method-response-example-description %}
 賬戶錯誤且錯誤代碼為10111, 10102, 10109時，會出現如下範例
{% endapi-method-response-example-description %}

```javascript
{
    "code": 411,
    "exceptionCode": 10123,
    "message": "帐号或密码错误，请重新登入。<BR>温馨提示：连续错误超过5次将锁定帐号。",
    "token": null,
    "data": {
        "usrWrongPasswordTimes": 5
    },
    "resourceKey": "Exception.Account.PasswordWrongWarmTip",
    "isOK": false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### Request body sample

```javascript
{
	"vendorId":"CCTEST",
	"siteId":"SITE1",
	"account":"RD102",
	"password":"5690dddfa28ae085d23518a035707282"
}
```

### Response body回傳data說明

| 欄位 | 型態 | 說明 |
| :--- | :--- | :--- |
| vendorId | 文字 | 業主id |
| siteId | 文字 | 子網id |
| account | 文字 | 會員賬號 |
| bankSet | boolean | 銀行卡已設定，true為已設定 |
| withdrawPasswordSet | boolean | 提現密碼已設定，true為已設定 |
| pause | 文字 | Y：賬戶凍結，會員可登入、可查報表、可存提款。app需卡控不可作錢包轉換及玩遊戲。其他值:表正常狀態 |
| lang | 文字 | 該使用者註冊時的預設語系 |
| quota | 數字 | 錢包總額 |
| err | JSON | keyword:錢包代碼，message:錯誤訊息 |
| gradeName | String | 等級名稱 |
| unReadCount | int | 未讀訊息個數 |



