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
source-git-commit: 69bc8aace3cc502a18e691584824176833413c7e
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# 測試解決方案

若要端對端測試解決方案，[weather-offers.html](assets/weather-offers.html)和[capture-impressions-click-events.js](assets/capture-impressions-click-events.js)檔案必須託管於Web伺服器或公用託管服務（例如Github Pages）。 這是必要的，因為瀏覽器的地理位置API只能透過HTTPS或localhost運作

## 下載提供的檔案

[HTML檔案](assets/weather-offers.html)

[Javascript檔案](assets/capture-impressions-click-events.js)

## 更新javascript檔案中的表面URL

開啟`capture-impressions-click-events.js`並以託管HTML檔案的實際網域取代` "web://yourdomain.com/weather/weather-offers.html#offerContainer"`以更新`yourdomain.com`。


## 更新Adobe Experience Platform標籤屬性

在文字編輯器中開啟weather-offers.html檔案，並將指令碼標籤取代為Adobe Experience Platform標籤屬性的指令碼標籤（於本教學課程的前一步中建立）。 請務必儲存檔案

```
<script src="https://assets.adobedtm.com/AEM_TAGS/launch-ENabcd1234.min.js" async></script>
```

## 與優惠方案互動

- 在您最愛的瀏覽器中開啟網頁。

- 允許&#x200B;_**位置追蹤**_。 根據您的位置取得天氣詳細資料需要此功能。

- 按一下選件中的按鈕，以觸發互動事件。

## 檢視報告

- 登入Journey Optimizer

- 導覽至「歷程管理」 ->「行銷活動」

- 按一下行銷活動，然後從報表功能表中選取適當的報表。
