# 取得會員提現賬戶資訊

### 2020/10/7 modified:

realName -&gt; bankAccountName

{% api-method method="get" host="http://domain name" path="/cch2oas/usr/withdrawBanks" %}
{% api-method-summary %}
取得會員可設定的提現銀行資訊
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="role" type="string" required=true %}
APP:APP開發介接  
MOBILE:行動網頁介接
{% endapi-method-parameter %}

{% api-method-parameter name="token" type="string" required=true %}
系統提供的合法token
{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=true %}
 語系，以CCH平台提供的語系代號為主  
主要是擷取銀行名稱是以哪種語系回傳
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
    "message": "取得资料成功",
    "data": {
        //有選擇銀行的
        "userBank": {
            "status": "3",
            "alreadyVerifyFlag": true,
            "bankAccountName": "辛小姐",
            "bankNo": "5",
            "bankAccountNo": "30150526314",
            "bankBranch": "前鎮加工區分行",
            "bankProvince": "71",
            "bankCity": "000006",
            "bankOther": null,
            "telAreaCode": "86",
            "telPhoneNo": "0912124473"
            
        },
        //沒有選擇銀行的
        "userBank": {
            "status": "3",
            "alreadyVerifyFlag": true,
            "bankAccountName": "辛小姐",
            "bankNo": "0",
            "bankAccountNo": "30150526314",
            "bankBranch": "前鎮加工區分行",
            "bankProvince": "71",
            "bankCity": "000006",
            "bankOther": "FUTUREBANK",
            "telAreaCode": "86",
            "telPhoneNo": "0912124473"
            
        },
        "provinces": [
            {
                "zipCode": "11",
                "name": "北京市",
                "upperZipCode": "China",
                "sort": 37
            },
            {
                "zipCode": "31",
                "name": "上海市",
                "upperZipCode": "China",
                "sort": 38
            },
            {
                "zipCode": "12",
                "name": "天津市",
                "upperZipCode": "China",
                "sort": 39
            },
            {
                "zipCode": "81",
                "name": "香港",
                "upperZipCode": "China",
                "sort": 68
            },
            {
                "zipCode": "82",
                "name": "澳门",
                "upperZipCode": "China",
                "sort": 69
            },
            {
                "zipCode": "71",
                "name": "台湾",
                "upperZipCode": "China",
                "sort": 70
            }
        ],
        "cities": [            
            {
                "zipCode": "330000",
                "name": "南昌市",
                "upperZipCode": "36",
                "sort": 1
            },
            {
                "zipCode": "350000",
                "name": "福州市",
                "upperZipCode": "35",
                "sort": 1
            },
            {
                "zipCode": "410000",
                "name": "长沙",
                "upperZipCode": "43",
                "sort": 1
            },
            {
                "zipCode": "430000",
                "name": "武汉",
                "upperZipCode": "42",
                "sort": 1
            },
            {
                "zipCode": "450000",
                "name": "郑州",
                "upperZipCode": "41",
                "sort": 1
            },
            {
                "zipCode": "510000",
                "name": "广州",
                "upperZipCode": "44",
                "sort": 1
            },
            {
                "zipCode": "530000",
                "name": "南宁",
                "upperZipCode": "45",
                "sort": 1
            },
            {
                "zipCode": "550001",
                "name": "贵阳",
                "upperZipCode": "52",
                "sort": 1
            },
            {
                "zipCode": "570003",
                "name": "海口市",
                "upperZipCode": "46",
                "sort": 1
            },
            {
                "zipCode": "610000",
                "name": "成都",
                "upperZipCode": "51",
                "sort": 1
            },
            {
                "zipCode": "650000",
                "name": "昆明",
                "upperZipCode": "53",
                "sort": 1
            },
            {
                "zipCode": "710000",
                "name": "西安",
                "upperZipCode": "61",
                "sort": 1
            },
            {
                "zipCode": "730000",
                "name": "兰州",
                "upperZipCode": "62",
                "sort": 1
            },
            {
                "zipCode": "750000",
                "name": "银川",
                "upperZipCode": "64",
                "sort": 1
            },
            {
                "zipCode": "810000",
                "name": "西宁",
                "upperZipCode": "63",
                "sort": 1
            },
            {
                "zipCode": "830000",
                "name": "乌鲁木齐",
                "upperZipCode": "65",
                "sort": 1
            },
            {
                "zipCode": "850000",
                "name": "拉萨",
                "upperZipCode": "54",
                "sort": 1
            },
            {
                "zipCode": "100044",
                "name": "港岛",
                "upperZipCode": "81",
                "sort": 1
            },
            {
                "zipCode": "999078",
                "name": "澳门",
                "upperZipCode": "82",
                "sort": 1
            },
            {
                "zipCode": "000001",
                "name": "台北市",
                "upperZipCode": "71",
                "sort": 1
            },
            {
                "zipCode": "100032",
                "name": "西城",
                "upperZipCode": "11",
                "sort": 2
            },
            {
                "zipCode": "200020",
                "name": "卢湾",
                "upperZipCode": "31",
                "sort": 2
            },
            {
                "zipCode": "402160",
                "name": "永川区",
                "upperZipCode": "50",
                "sort": 39
            },
            {
                "zipCode": "408400",
                "name": "南川区",
                "upperZipCode": "50",
                "sort": 40
            }
        ],
        "banks": [
            {
                "regionId": "CN",
                "regionName": "中國",
                "bankNo": "1",
                "bankName": "建设银行"
            },
            {
                "regionId": "CN",
                "regionName": "中國",
                "bankNo": "11",
                "bankName": "微信"
            },
            {
                "regionId": "CN",
                "regionName": "中國",
                "bankNo": "26",
                "bankName": "上海银行"
            },
            {
                "regionId": "CN",
                "regionName": "中國",
                "bankNo": "42",
                "bankName": "QQ钱包"
            },
            {
                "regionId": "CN",
                "regionName": "中國",
                "bankNo": "44",
                "bankName": "支付寶支付"
            }
        ],
        "region": [
            {
                "regionId": "CN",
                "regionName": "中國",
                "sort": 1
            },
            {
                "regionId": "TW",
                "regionName": "台灣",
                "sort": 1
            },
            {
                "regionId": "US",
                "regionName": "美國",
                "sort": 1
            }
        ]
    },
    "exceptionCode": 0
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### API流程描述

1. 檢查token是否逾時或格式錯誤
2. 以參數帶出會員可設定的提現銀行資訊\(地區選項資料、地區銀行及省市資料\)

### Http STATUS code=200回傳欄位說明

| 欄位 | 型態 | 說明 |
| :--- | :--- | :--- |
| status | 文字 | 1:未設定  2.未驗證  3.已驗證 |
| alreadyVerifyFlag | 文字 | true:為已驗證 |
| bankAccountName | 文字 | 戶名 |
| bankNo | 文字 | 只能放數字，銀行流水碼 |
| bankAccountNo | 文字 | 銀行賬號 |
| bankBranch | 文字 | 銀行網關 |
| bankProvince | 文字 | 省的zipCode |
| bankCity | 文字 | 市的zipCode |
| bankOther | 文字 | 可以是null，當選擇其他銀行時，這裡會放自行輸入的銀行名稱，bankNo請放0 |

#### regions欄位說明

| 欄位 | 型態 | 說明 |
| :--- | :--- | :--- |
| regionId | 文字 | 地區代碼 |
| regionName | 文字 | 地區名稱 |
| sort | 數字 | 排序，銀行卡設定頁地區下拉選單請依此欄位排序呈現 |

#### banks欄位說明

| 欄位 | 型態 | 說明 |
| :--- | :--- | :--- |
| regionId | 文字 | 地區代碼，銀行卡設定銀行需在地區選擇後，依此欄位作對應顯示 |
| regionName | 文字 | 地區名稱 |
| bankNo | 文字 | 銀行代碼 |
| bankName | 文字 | 銀行名稱 |

#### provinces & 回傳欄cities欄位說明

| 欄位 | 型態 | 說明 |
| :--- | :--- | :--- |
| zipCode | 文字 | 省市代碼 |
| upperZipCode | 文字 | “省"下拉選單，請過濾"China"的，”市“下拉選單，是以省的zipCod對應upperZipCode帶出下拉 |
| name | 文字 | 省市名稱 |
| sort | 數字 | 顯示順序，下拉選單請依sort排序 |

