---
title: 測試解決方案
description: 建立簡單網頁以擷取優惠方案上的曝光次數和點選事件。
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-07-18T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-18526
exl-id: 6b6c66d3-218d-4f5b-adb0-a2eca05989ab
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: a984631b-2bae-4860-9b15-69c41a799dcb
    internal-label: APIs and SDKs
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
    internal-label: Decisioning API
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%
---
# 測試解決方案

## 部署範例資產

如果您尚未安裝Node.js，請從這裡[&#128279;](https://nodejs.org/)下載並安裝

執行以驗證安裝：

`node -v`

`npm -v`

## 設定專案資料夾

使用下列命令為範例應用程式建立新目錄：

`mkdir frequency-capping `

`cd frequency-capping `

## 初始化專案

`npm init -y`

## 安裝必要的架構

`npm install express`

## 複製資產檔案

* 解壓縮[server.zip](assets/server.zip)的內容，並將其放在`frequency-capping`資料夾中。
* 將[public.zip](assets/public.zip)的內容解壓縮至&#39;frequency-capping&#39;資料夾

## 更新javascript檔案中的表面URL

開啟位於`public\scripts`中的`frequency-capping.js`並更新介面屬性以符合行銷活動中使用的管道設定

## 啟動節點js伺服器

導覽至`c:\frequency-capping`資料夾。 執行`node server.js`命令以啟動連線埠3000上的節點js伺服器


## 更新Adobe Experience Platform標籤屬性

在文字編輯器中開啟位於`public`資料夾中的`frequency-capping.html`檔案，並將指令碼標籤取代為在本教學課程的前一個步驟中建立之Adobe Experience Platform標籤屬性的指令碼標籤。 請務必儲存檔案

```
<script src="https://assets.adobedtm.com/AEM_TAGS/launch-ENabcd1234.min.js" async></script>
```

## 與優惠方案互動

* 在您最愛的瀏覽器中開啟[網頁](http://localhost:3000)。
* 與優惠方案互動
* 重新整理頁面
* 根據頻率限定規則，您應該會看到新選件

## 檢視報告

* 登入Journey Optimizer
* 導覽至「歷程管理」 ->「行銷活動」
* 按一下行銷活動，然後從報表功能表中選取適當的報表。
