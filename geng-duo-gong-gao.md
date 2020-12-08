# 更多公告

Exception Code:409 VendorException, 500 Exception

{% api-method method="post" host="http://domain name/cch2oas" path="/bulletins/list" %}
{% api-method-summary %}
取得系統公告列表
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="role" type="string" required=true %}
APP:APP開發介接  
MOBILE:行動網頁版
{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=true %}
depends on CCHAPI說明，default : zh\_CN
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="vendorId" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="siteId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
取得公告成功
{% endapi-method-response-example-description %}

```javascript
{
    "code": 200,
    "exceptionCode": 0,
    "message": "取得资料成功",
    "token": null,
    "data": {
        "bulletins": [
            {
                "seqNo": "2",   //公告編號
                "type": "代理",  //公告類別
                "title": "代理公告二-简体", //公告標題
                "content": "<p class=\"Bulletin\" class=\"Bulletin\">代理公告二-简体</p>", //公告內容
                "beginTime": "2020-05-02 12:00:00" //公告開始時間
            },
            {
                "seqNo": "1",
                "type": "代理",
                "title": "代理公告一-简体",
                "content": "<p class=\"Bulletin\" class=\"Bulletin\">代理公告一-简体</p>",
                "beginTime": "2020-05-01 12:00:00"
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

|  |
| :--- |


