---
title: 擷取使用者許可權
description: 建立網頁以擷取使用者對接收推播通知的同意。
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
source-git-commit: 45f86aeb8fca071436785cc55225d853bb21998f
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# 擷取使用者許可權

此網頁會擷取使用者接收推播通知的同意。 它會提示使用者使用瀏覽器的通知API來啟用通知，並在接受通知後，使用網頁SDK向Adobe Experience Platform註冊推播訂閱。 這可確保只有選擇加入的使用者才有資格透過Adobe Journey Optimizer中的行銷活動和歷程接收推播通知。

若要啟用Web推播通知，頁面會先透過呼叫初始化函式內的fetch(&quot;/config&quot;)來載入設定檔。 此設定由Node.js應用程式提供，並包含資料流ID、組織ID、VAPID公開金鑰、應用程式ID和追蹤資料集ID等金鑰值。 載入設定後，就會初始化Adobe Web SDK，並註冊Service Worker以支援推送訊息。 當使用者按一下啟用通知時，瀏覽器會提示他們使用網頁通知API取得許可權。 如果授予許可權，網路SDK會將推送訂閱傳送至Adobe Experience Platform，使用者會在24小時內標籤為已選擇加入，以避免重複提示。 啟動伺服器後，您可以在[範例應用程式](http://localhost:3000/)中包含的本機網頁shop-smart.html上嘗試此流程。

![request-permissions](assets/request-notifications.png)

