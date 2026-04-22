---
title: 在AJO中偵錯Web推播
description: 此頁面提供用於偵錯Web推播通知流程的實用提示，包括驗證Web SDK請求
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
source-git-commit: 45f86aeb8fca071436785cc55225d853bb21998f
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# 在AJO中偵錯Web推播

This page provides helpful tips to debug the web push notification flow, including verifying Web SDK requests, checking the ECID and user profile in AEP, and ensuring that events like price.drop are correctly sent and received.

- **使用Adobe Experience Platform Debugger （Chrome擴充功能）**\
  安裝適用於Chrome[的](https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob)AEP Debugger擴充功能，以更輕鬆地檢查Web SDK活動：

此工具可讓您：
 — 檢視網頁SDK請求和回應\
 — 檢查ECID (Experience Cloud ID)\
 — 驗證資料流設定和裝載

- **檢查使用者是否已識別(ECID)**\
  使用AEP Debugger或瀏覽器主控台，確認已產生ECID。 此ID可用來跨AEP和AJO追蹤使用者。

- **使用[網路]索引標籤來驗證要求**\
  開啟瀏覽器開發人員工具中的&#x200B;**網路標籤**，並篩選網頁SDK提出的要求（尋找`/collect`或`interact`）。
   - Confirm requests are being sent when the page loads and when actions are triggered
   - 檢查`price.drop`事件是否包含在承載中

- **在AEP中查詢使用者設定檔**\
  使用ECID在Adobe Experience Platform中搜尋使用者設定檔。 這有助於確認可辨識使用者，且其資料（例如推送訂閱）可正確儲存。

- **確認已收到`price.drop`事件**\
  從網頁觸發事件後，如果事件已擷取並與相同ECID建立關聯，請存取AEP。
檢查`feedback.status`的message.feedback事件的json。 狀態值應為`sent`
  ![降價](assets/price-drop-profile-event.png)

- **確認推播通知已啟用**\
  Ensure that:
   - The user accepted the browser notification prompt
   - A push token exists in the user&#39;s profile

- **檢查歷程設定**\
  請確定歷程已發佈並設定為接聽`price.drop`事件。

