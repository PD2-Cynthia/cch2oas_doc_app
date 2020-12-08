# 取得首頁資訊

Exception Code:

401 Token Exception, 408 ReLogin Exception, 409 VendorException, 411 AccountException, 500 interal Server error

{% api-method method="post" host="http://domain name/cch2oas" path="/home" %}
{% api-method-summary %}
get all information for Home page
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="role" type="string" required=true %}
APP
{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=true %}
zh\_CN
{% endapi-method-parameter %}

{% api-method-parameter name="token" type="string" required=false %}
使用者若未登入，首頁取得的遊戲loginUrl會是null，若已登入請代入token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="vendorId" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="siteId" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="userAgent" type="string" required=true %}
請帶入request header的user-agent的參數, 此參數未來得到的遊戲登入後會與會員的瀏覽器比對唷
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
會員未登入，首頁回傳json格式如下：
{
    "code": 200,
    "exceptionCode": 0,
    "message": "取得资料成功",
    "token": null,
    "data": {
        "bulletins": [ //最新公告
            {
                "seqNo": "2",            //公告編號
                "type": "代理",           //公告類別名稱
                "title": "代理公告二-简体",  //公告標題
                "content": "<p class=\"Bulletin\" class=\"Bulletin\">代理公告二-简体</p>", //公告內容
                "beginTime": "2020/05/02 12:00"  //公告開始時間
            },
            {
                "seqNo": "1",
                "type": "代理",
                "title": "代理公告一-简体",
                "content": "<p class=\"Bulletin\" class=\"Bulletin\">代理公告一-简体</p>",
                "beginTime": "2020/05/01 12:00"
            }
        ],
        "home": [
            {
                "seqNo": "1",
                "pageType": "HOME",
                "sort": 1,
                "name": "雙十一開跑囉",
                "imgUrl": "https://sokoban.fn76.com/CCBAO/a59a755ed09732790726005899a2bef7f70faed06550e80be366569d3db2be54",
                "outUrl": "http://172.16.2.110/CCGEGWS/EPCEG490010.action?SID=42ee6a5c19a61fb4e7c64f8f139430de330a51550aa44825aefe2069539d5f01&UID=CCP5579&lang=zh_CN&timeZone=plus8:00&gameKey=FORTUNEINGOT",
                "linkType": "PRODUCT"  //連結類型, product需判斷是否登入，未登入則需先請會員登入或註冊
            },
            {
                "seqNo": "2",
                "pageType": "HOME",
                "sort": 2,
                "name": "outer link",
                "imgUrl": "https://sokoban.fn76.com/CCBAO/a59a755ed0973279c96df3b2451045b61121a61ea39f5c02",
                "outUrl": "https://moose.cc-bao.cc/moose/baopic/wechat_cn.jpg",
                "linkType": "OUTER"  //站外連結
            }
        ],
        "products": [ //遊戲連結
            {
                "productId": "CB",  //產品ID
                "loginUrl": null,   //可登入的網址
                "isMaintain": "N",  //是否在維護
                "beginTime": null,  //維護開始時間, Y才會有時間
                "endTime": null,     //維護結束時間, Y才會有時間
                "message":"exception錯誤訊息內容"
            },
            {
                "productId": "CCPEG",
                "loginUrl": null,
                "isMaintain": "Y",
                "beginTime": "2020-09-14 08:30",
                "endTime": "2020-09-14 11:50",
                "message":"exception錯誤訊息內容"
            },
            {
                "productId": "BB",
                "loginUrl": null,
                "isMaintain": "N",
                "beginTime": null,
                "endTime": null,
                "message":"exception錯誤訊息內容"
            },
            {
                "productId": "AGIN",
                "loginUrl": null,
                "isMaintain": "N",
                "beginTime": null,
                "endTime": null,
                "message":"exception錯誤訊息內容"
            },
            {
                "productId": "KY",
                "loginUrl": null,
                "isMaintain": "N",
                "beginTime": null,
                "endTime": null,
                "message":"exception錯誤訊息內容"
            }
        ]
    },
    "resourceKey": "api.response.code.getSuccess",
    "isOK": true
}

會員登入，範例如下:
{
    "code": 200,
    "exceptionCode": 0,
    "message": "取得资料成功",
    "token": null,
    "data": {
        "bulletins": [
            {
                "seqNo": "2",
                "type": "代理",
                "title": "代理公告二-简体",
                "content": "<p class=\"Bulletin\" class=\"Bulletin\">代理公告二-简体</p>",
                "beginTime": "2020/05/02 12:00"
            },
            {
                "seqNo": "1",
                "type": "代理",
                "title": "代理公告一-简体",
                "content": "<p class=\"Bulletin\" class=\"Bulletin\">代理公告一-简体</p>",
                "beginTime": "2020/05/01 12:00"
            }
        ],
        "home": [
            {
                "seqNo": "1",
                "pageType": "HOME",
                "sort": 1,
                "name": "幸運大轉盤",
                "imgUrl": "https://moose.cc-bao.com/moose/baopic/b_wechat.jpg"
            }
        ],
        "products": [
            {
                "productId": "CB",
                "loginUrl": "http://PORTAL.COM/PortalUSR/EPCB1000001.jsp?txtAccount=U-RD102&txtLoginKey=ed1ab365fe62054fe5969397aa84cebc&txtProductID=CB&txtDevice=MOBILE&p=PortalOpenAPI",
                "isMaintain": "N",
                "beginTime": null,
                "endTime": null
            },
            {
                "productId": "CCPEG",
                "loginUrl": "http://PORTAL.COM/PortalUSR/EPCB1000001.jsp?txtAccount=U-RD102&txtLoginKey=ed1ab365fe62054fe5969397aa84cebc&txtProductID=CCPEG&txtDevice=MOBILE&p=PortalOpenAPI",
                "isMaintain": "N",
                "beginTime": null,
                "endTime": null
            },
            {
                "productId": "BB",
                "loginUrl": "http://PORTAL.COM/PortalUSR/EPCB1000001.jsp?txtAccount=U-RD102&txtLoginKey=ed1ab365fe62054fe5969397aa84cebc&txtProductID=BB&txtDevice=MOBILE&p=PortalOpenAPI",
                "isMaintain": "N",
                "beginTime": null,
                "endTime": null
            },
            {
                "productId": "AGIN",
                "loginUrl": "http://PORTAL.COM/PortalUSR/EPCB1000001.jsp?txtAccount=U-RD102&txtLoginKey=ed1ab365fe62054fe5969397aa84cebc&txtProductID=AGIN&txtDevice=MOBILE&p=PortalOpenAPI",
                "isMaintain": "N",
                "beginTime": null,
                "endTime": null
            },
            {
                "productId": "KY",
                "loginUrl": "http://PORTAL.COM/PortalUSR/EPCB1000001.jsp?txtAccount=U-RD102&txtLoginKey=ed1ab365fe62054fe5969397aa84cebc&txtProductID=KY&txtDevice=MOBILE&p=PortalOpenAPI",
                "isMaintain": "N",
                "beginTime": null,
                "endTime": null
            }
        ]
    },
    "resourceKey": "api.response.code.getSuccess",
    "isOK": true
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```
{    "message": "Ain't no cake like that."}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



