# 取得提現驗證資訊

Exception Code List:

401 Token Exception, 408 ReLogin Exception, 409 VendorException, 411 AccountException, 500 interal Server error

### 2020-10-08 modified:

realNameSet移除

realName - &gt; bankAccountName

{% api-method method="get" host="http://domain name/cch2oas" path="/usr/withdraw/check" %}
{% api-method-summary %}
Check user's withdraw data and verify
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
系統核發的合法連線驗證資訊
{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=true %}
Default : zh\_CN
{% endapi-method-parameter %}

{% api-method-parameter name="role" type="string" required=true %}
APP
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
取得資料成功
{% endapi-method-response-example-description %}

```javascript
{
    "code": 200,
    "exceptionCode": 0,
    "message": "取得资料成功",
    "token": null,
    "data": {
        "withdrawOpenFlag": "Y",        //是否可提現，若有提現單未完成，則為N不可提現
        "withdrawBankSet": true,        //是否已設定提現銀行
        "phoneSet": true,               //是否已設定手機號
        "withdrawPasswordSet": false,   //取得提現密碼是否已設定
        "bankAccountName": "辛小姐",            //戶名
        "telArea": "86",                //區域號
        "phoneNo": "0912124472",        //手機號
        "bankName": null,               //銀行名稱
        "bankProvince": "上海市",        //銀行省
        "bankCity": "浦东",              //銀行市
        "bankBranch": "浦東分行",         //銀行網關
        "bankAccountNo": "6012562345198",    //銀行賬號
        "bankOther": "其他大陸銀行",            //其他銀行
        "quota": 10492.98,                    //中心錢包餘額
        "adminFee": 0,                        //行政費用
        "totalWithdrawAmount": 0,             //當日已出款金額
        "minWithdrawAmount": 50,              //每次提現金額下限
        "maxWithdrawPerDay": 750,             //每日提現最高可提金額
        "usrFeePercent": 1,                   //手續費的百分比
        "minUsrFee": 2,                        //最低手續費
        "availableAmount": 5983.0,            //最大可提額度
        "favorAmount": 50.0,                  //鎖定優惠額度
        "profit": 0.0,                        //優惠盈利
        "applyInfoViews": [                       //提現申請單記錄
            {
                "withdrawNo": 912101657861,        //提現單號
                "status": "CANCELED",              //提現單狀態，請參考CCHAPI說明
                "amount": 120,                     //提現申請金額
                "adminFee": 0,                      //行政費用
                "usrFee": 2,                        //手續費
                "crTime": "2019-12-10 16:16:50",    //申請時間
                "paidAmount": "118"                 //實際出款金額
            },
            {
                "withdrawNo": 912101186866,
                "status": "WITHDRAWED",
                "amount": 300,
                "adminFee": 9,
                "usrFee": 2,
                "crTime": "2019-12-10 11:27:42",
                "paidAmount": "289"
            },
            {
                "withdrawNo": 908301349664,
                "status": "WITHDRAWED",
                "amount": 140,
                "adminFee": 85,
                "usrFee": 0,
                "crTime": "2019-08-30 13:47:24",
                "paidAmount": "55"
            },
            {
                "withdrawNo": 905141605265,
                "status": "CANCELED",
                "amount": 150,
                "adminFee": 83,
                "usrFee": 0,
                "crTime": "2019-05-14 16:00:54",
                "paidAmount": "67"
            },
            {
                "withdrawNo": 905141454262,
                "status": "CANCELED",
                "amount": 130,
                "adminFee": 80,
                "usrFee": 0,
                "crTime": "2019-05-14 14:27:06",
                "paidAmount": "50"
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



