---
title: 建立推播頻道
description: 推播通道設定會定義如何傳送Web推播通知，包括應用程式設定和平台專屬詳細資訊。 它也會將您的推播設定連結至所需的憑證，例如VAPID金鑰，使AJO能夠傳送通知給已訂閱的使用者。
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00Z
jira: KT-20879
source-git-commit: 3d342c5c4de4dda221ce4427b1e4aef7ef8c22cc
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# 建立推播頻道

第一步是在Adobe Journey Optimizer中建立推播頻道。 在此設定過程中，您需要產生VAPID金鑰，這是驗證和啟用Web推播通知所需。 這些金鑰隨後用於推送通道設定，讓AJO能夠安全地傳送通知給已訂閱的使用者。

## 產生VAPID金鑰

VAPID （自願應用程式伺服器識別）是一種網頁推送標準，可讓您的伺服器使用公開/私密金鑰組來識別自己，以推送服務（例如Chrome、Edge等），讓推送提供者知道誰在傳送通知。

這會使用web-push generate-vapid-keys之類的工具產生，這會建立公開金鑰（與瀏覽器共用）和私密金鑰（儲存在伺服器上），共同用來驗證及安全傳送推送訊息。

在本教學課程中，我們已使用Node.js產生VAPID金鑰。

請確定您已安裝Node.js。 然後發出以下命令
```npm install web-push -g ```

![網頁推播](assets/install-web-push.png)

```web-push generate-vapid-keys```

![vapid](assets/vapid-keys.png)

## 建立推播認證

* 登入Journey Optimizer

* 導覽至管理|管道|推送設定|推送認證|建立推送認證

* ![推播認證](assets/push-credential.png)

## 建立頻道設定

* 登入Journey Optimizer

* 導覽至管理|管道|建立管道設定
  ![頻道設定](assets/push-channel.png)
