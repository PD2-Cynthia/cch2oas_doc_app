# 基本說明

### Domain name\(for app設定\)

| 環境 | 網址 |
| :--- | :--- |
| 開發 | cch2oas.cchdev.com:2135\(請自行設定hosts 172.16.3.170\) |
| 測試 | cch2oas.cch.com:2135 |
| 線上測試區 | cch2oas.com:2135 |
| 正式區 | cch2oas.com:2135 |

### CCH平台語系代碼

CC寶2: zh\_CN

### Product ID列表

| **PRODUCTID** | **PRODUCTNAME** | **SORT** |
| :--- | :--- | :--- |
| CB | 彩球 | 1 |
| CCPEG | CC電子 | 2 |
| BB | BB真人 | 3 |
| AGIN | AG真人 | 4 |
| KY | 開元 | 5 |
| ID\_CCHOSTING | 中心錢包 | 0 |

### 錢包分類說明\(下拉選單\)

| 代碼 | 說明 |
| :--- | :--- |
| WITHDRAW | 提現 |
| DEPOSIT | 充值 |
| MANUAL\_DW | 人工存提款 |
| COUPON | 優惠金 |

### 錢包子科目

| 代碼 | 說明 |
| :--- | :--- |
| WITHDRAW | 提現 |
| WITHDRAW\_OFFSET | 提現沖銷 |
| DEPOSIT | 充值 |
| DEPOSIT\_OFFSET | 充值沖銷 |
| MANUAL\_DEPOSIT | 人工存款 |
| MANUAL\_WITHDRAW | 人工提現 |
| COUPON | 優惠金 |
| COUPON\_OFFSET | 取消優惠金 |

### 遊戲群組說明

| 代碼 | 群組名稱 |
| :--- | :--- |
| LOTTERY | 彩球 |
| EGAME | CC Casino |
| LIVE | 真人 |
| BOARD | 棋牌 |

### Http Response Code說明（請參照Change Log最新附件）

### 提現申請單狀態說明

| 狀態 | 說明 |
| :--- | :--- |
| WAIT | 等待處理 |
| AUDITNG | 初審中 |
| AUDITED | 初審完成 |
| REAUDITING | 出款中 |
| WITHDRAWED | 出款完成 |
| CANCELED | 已取消 |

## Exception Code List

{% file src=".gitbook/assets/cchapi-exception-code \(4\).xls" %}



