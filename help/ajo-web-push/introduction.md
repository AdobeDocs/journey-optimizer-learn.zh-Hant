---
title: AJO中的網頁推播
description: 本教學課程示範如何使用Adobe Journey Optimizer (AJO)實作Web推播通知。 您將瞭解如何使用Web SDK擷取使用者選擇加入、透過排程的行銷活動傳送通知，以及使用AEP Tags的自訂price.drop事件觸發即時推送訊息。
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
source-git-commit: 45f86aeb8fca071436785cc55225d853bb21998f
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Adobe Journey Optimizer中的網頁推播

網頁推播通知是即時重新與使用者互動的強大方法，本教學課程將逐步引導您使用Adobe Journey Optimizer (AJO)實作這些通知。 首先，您可以使用網頁SDK擷取推播通知的使用者選擇加入偏好設定，確保順暢且合規的訂閱體驗。 接下來，您將建立行銷活動，向選擇加入的使用者傳送推播通知，以啟用受眾型參與。 最後，您將瞭解如何運用AEP Tags來觸發自訂價格下降事件，這在AJO中起始歷程，並根據即時使用者行為提供及時、個人化的推播通知。

允許使用者選擇加入通知的網頁範例

![啟用通知](assets/enable-notifications.png)

觸發價格下降事件的範例網頁

![觸發價格下降](assets/trigger-price-drop-event.png)

## 先決條件

本教學課程的設計初衷是實作且易於遵循。 雖然不需深入專業知識，但熟悉下列概念將有所助益：

- Adobe Journey Optimizer （建立歷程或行銷活動）
- AEP資料收集（標籤）和網頁SDK
- 結構描述和事件等基本Adobe Experience Platform概念
- 部分JavaScript和一般Web開發概念
- 基本Node.js知識（用於產生VAPID金鑰及提供簡單的設定端點）

如果您是這些區域的新手，請不要擔心，教學課程將引導您完成過程中的關鍵步驟。
本教學課程著重於實作端對端Web推播通知使用案例，因此上述工具和概念的工作知識將幫助您有效遵循。


## 🔔啟用瀏覽器通知

如果通知遭到封鎖或未出現，您可能需要在瀏覽器設定中啟用通知。 請參閱以下指南：

- **Google Chrome (Windows/macOS)**\
  <https://support.google.com/chrome/answer/3220216>

- **Microsoft Edge (Windows)**\
  <https://support.microsoft.com/en-us/microsoft-edge/manage-website-notifications-in-microsoft-edge>

- **Safari (macOS)**\
  <https://support.apple.com/guide/safari/customize-website-notifications-sfri40734/mac>

- **Safari (iPhone/iPad)**\
  <https://support.apple.com/en-us/HT213893>


## 範例應用程式


為協助您依循步驟，您可使用完整的應用程式範例。

- [即時示範 — 選擇加入：](https://ajo-web-push.onrender.com/)

- [觸發價格下降事件：](https://ajo-web-push.onrender.com/price-drop-trigger.html)

- [Source代碼：](https://github.com/gbedekar489/ajo-web-push)

您可以探索即時示範以檢視動作流程，或複製存放庫以在本機執行專案。

