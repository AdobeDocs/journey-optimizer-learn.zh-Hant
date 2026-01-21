---
title: 測試解決方案
description: 建立簡單網頁以擷取優惠方案上的曝光次數和點選事件。
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-07-18T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18526
exl-id: 6b6c66d3-218d-4f5b-adb0-a2eca05989ab
source-git-commit: bef6d831c639d40514552dae3ff20132626a4a09
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# 測試解決方案

## 部署範例資產

如果您尚未安裝Node.js，請從這裡[下載並](https://nodejs.org/)安裝

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

開啟位於`frequency-capping.js`中的`public\scripts`並更新介面屬性以符合行銷活動中使用的管道設定

## 啟動節點js伺服器

導覽至`c:\frequency-capping`資料夾。 執行`node server.js`命令以啟動連線埠3000上的節點js伺服器


## 更新Adobe Experience Platform標籤屬性

在文字編輯器中開啟位於`frequency-capping.html`資料夾中的`public`檔案，並將指令碼標籤取代為在本教學課程的前一個步驟中建立之Adobe Experience Platform標籤屬性的指令碼標籤。 請務必儲存檔案

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
