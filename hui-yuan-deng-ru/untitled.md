# 錢包記錄

{% api-method method="get" host="http://domain name/cch2oas" path="/usr/quota/log/{transType}?page=&pageSize=&days=" %}
{% api-method-summary %}
取得錢包異動記錄
{% endapi-method-summary %}

{% api-method-description %}
依不同的transType查詢記錄
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="transType" type="string" required=true %}
若為空，系統預設也會是ALL，帶ALL可查詢全部
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="lang" type="string" required=true %}
depends on CCHAPI說明，default：zh\_CN
{% endapi-method-parameter %}

{% api-method-parameter name="role" type="string" required=true %}
APP：APP開發介接  
MOBILE：行動網頁版
{% endapi-method-parameter %}

{% api-method-parameter name="token" type="string" required=true %}
系統核發的合法連線資訊
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="page" type="integer" required=true %}
查詢第？頁，index從1開始代表第一頁
{% endapi-method-parameter %}

{% api-method-parameter name="pageSize" type="integer" required=true %}
一頁要顯示幾筆
{% endapi-method-parameter %}

{% api-method-parameter name="days" type="integer" required=true %}
查詢天數，從今天起算往前查的天數
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
資料取得成功
{% endapi-method-response-example-description %}

```javascript
{
    "code": 200,
    "exceptionCode": 0,
    "message": "取得资料成功",
    "token": null,
    "data": {
        "currentPage": 1,
        "pageSize": 20,
        "qutoaTrans": [
            {
                "subTransType": "COUPON_OFFSET",
                "subTransTypeName": "优惠冲销",
                "transDate": "2020-07-27 10:16:27",
                "linkNo": "優惠測試20200710",
                "amount": -30.0
            },
            {
                "subTransType": "COUPON",
                "subTransTypeName": "优惠金",
                "transDate": "2020-07-16 09:52:28",
                "linkNo": "優惠測試20200710",
                "amount": 30.0
            },
            {
                "subTransType": "COUPON",
                "subTransTypeName": "优惠金",
                "transDate": "2020-07-14 18:50:40",
                "linkNo": "優惠金88",
                "amount": -88.0
            },
            {
                "subTransType": "COUPON",
                "subTransTypeName": "优惠金",
                "transDate": "2020-07-14 18:05:15",
                "linkNo": "優惠金88",
                "amount": 88.0
            },
            {
                "subTransType": "COUPON",
                "subTransTypeName": "优惠金",
                "transDate": "2020-07-14 18:04:52",
                "linkNo": "優惠測試一",
                "amount": -50.0
            },
            {
                "subTransType": "COUPON",
                "subTransTypeName": "优惠金",
                "transDate": "2020-07-14 18:04:25",
                "linkNo": "優惠測試一",
                "amount": 50.0
            },
            {
                "subTransType": "COUPON",
                "subTransTypeName": "优惠金",
                "transDate": "2020-07-14 18:02:55",
                "linkNo": "優惠測試20200710",
                "amount": -77.0
            },
            {
                "subTransType": "COUPON",
                "subTransTypeName": "优惠金",
                "transDate": "2020-07-14 17:57:35",
                "linkNo": "優惠測試20200710",
                "amount": 77.0
            },
            {
                "subTransType": "COUPON",
                "subTransTypeName": "优惠金",
                "transDate": "2020-07-14 17:57:14",
                "linkNo": "優惠測試20200710",
                "amount": -77.0
            },
            {
                "subTransType": "COUPON",
                "subTransTypeName": "优惠金",
                "transDate": "2020-07-14 17:47:28",
                "linkNo": "優惠測試20200710",
                "amount": 77.0
            },
            {
                "subTransType": "COUPON",
                "subTransTypeName": "优惠金",
                "transDate": "2020-07-14 13:54:42",
                "linkNo": "優惠測試20200710",
                "amount": 77.0
            },
            {
                "subTransType": "COUPON",
                "subTransTypeName": "优惠金",
                "transDate": "2020-07-14 13:54:34",
                "linkNo": "優惠測試一",
                "amount": -50.0
            },
            {
                "subTransType": "COUPON",
                "subTransTypeName": "优惠金",
                "transDate": "2020-07-09 09:28:41",
                "linkNo": "優惠測試一",
                "amount": 50.0
            },
            {
                "subTransType": "COUPON",
                "subTransTypeName": "优惠金",
                "transDate": "2020-07-03 18:17:17",
                "linkNo": "測試優惠送50",
                "amount": 50.0
            },
            {
                "subTransType": "COUPON",
                "subTransTypeName": "优惠金",
                "transDate": "2020-07-03 18:05:14",
                "linkNo": "優惠金88",
                "amount": -88.0
            },
            {
                "subTransType": "COUPON",
                "subTransTypeName": "优惠金",
                "transDate": "2020-07-03 15:46:57",
                "linkNo": "優惠金88",
                "amount": 88.0
            }
        ],
        "totalPages": 1,
        "totalRecords": 16,
        "transType": [
            {
                "type": "DEPOSIT",
                "name": "充值"
            },
            {
                "type": "WITHDRAW",
                "name": "提现"
            },
            {
                "type": "MANUAL_DW",
                "name": "人工充值提现"
            },
            {
                "type": "COUPON",
                "name": "优惠金"
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

### Result 200回傳欄位說明

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x6B04;&#x4F4D;</th>
      <th style="text-align:left">&#x578B;&#x614B;</th>
      <th style="text-align:left">&#x8AAA;&#x660E;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">subTransType</td>
      <td style="text-align:left">&#x6587;&#x5B57;</td>
      <td style="text-align:left">&#x5B50;&#x79D1;&#x76EE;&#x985E;&#x5225;&#xFF0C;&#x8ACB;&#x53C3;&#x7167;&#x57FA;&#x672C;&#x8AAA;&#x660E;</td>
    </tr>
    <tr>
      <td style="text-align:left">subTransTypeName</td>
      <td style="text-align:left">&#x6587;&#x5B57;</td>
      <td style="text-align:left">&#x5B50;&#x79D1;&#x76EE;&#x540D;&#x7A31;</td>
    </tr>
    <tr>
      <td style="text-align:left">transDate</td>
      <td style="text-align:left">&#x6587;&#x5B57;</td>
      <td style="text-align:left">&#x5EFA;&#x7ACB;&#x65E5;&#x671F;</td>
    </tr>
    <tr>
      <td style="text-align:left">linkNo</td>
      <td style="text-align:left">&#x6587;&#x5B57;</td>
      <td style="text-align:left">
        <p>&#x55AE;&#x865F;</p>
        <p>&#x5145;&#x503C;&#x3001;&#x63D0;&#x73FE;&#x9700;&#x986F;&#x793A;&#x55AE;&#x865F;</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">amount</td>
      <td style="text-align:left">&#x6578;&#x5B57;</td>
      <td style="text-align:left">&#x5165;&#x8CEC;&#x91D1;&#x984D;</td>
    </tr>
    <tr>
      <td style="text-align:left">currentPage</td>
      <td style="text-align:left">&#x6578;&#x5B57;</td>
      <td style="text-align:left">&#x76EE;&#x524D;&#x9801;&#x6578;</td>
    </tr>
    <tr>
      <td style="text-align:left">pageSize</td>
      <td style="text-align:left">&#x6578;&#x5B57;</td>
      <td style="text-align:left">&#x4E00;&#x9801;N&#x7B46;</td>
    </tr>
    <tr>
      <td style="text-align:left">totalRecords</td>
      <td style="text-align:left">&#x6578;&#x5B57;</td>
      <td style="text-align:left">&#x7E3D;&#x7B46;&#x6578;</td>
    </tr>
    <tr>
      <td style="text-align:left">totalPages</td>
      <td style="text-align:left">&#x6578;&#x5B57;</td>
      <td style="text-align:left">&#x7E3D;&#x9801;&#x6578;</td>
    </tr>
  </tbody>
</table>

