---
title: 在本機執行應用程式
description: 在本機設定範例應用程式，以使用AJO來探索Web推播通知流程。
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
source-git-commit: 45f86aeb8fca071436785cc55225d853bb21998f
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# 在本機執行應用程式

此頁面會引導您在本機設定範例應用程式，讓您能夠使用Adobe Journey Optimizer測試和探索網頁推播通知流程。 您將複製存放庫、設定環境變數，並在本機系統上執行應用程式。


請依照下列步驟，在本機系統上執行範例應用程式。

## 1.安裝Node.js

確定您的系統上已安裝&#x200B;**Node.js （版本16或更新版本）**。

您可以[在此下載：](https://nodejs.org/)

驗證安裝

```node -v```

```npm -v```


## 2.複製存放庫

```git clone https://github.com/gbedekar489/ajo-web-push.git```

```cd ajo-web-push```

## 3.安裝相依性

```npm install```

## 4.設定環境變數

在根目錄中建立.env檔案，並新增下列內容：

```
DATASTREAM_ID=your_datastream_id
ORG_ID=your_org_id
VAPID_PUBLIC_KEY=your_vapid_public_key
APP_ID=your_app_id
DATASET_ID=your_profile_dataset_id
PORT=3000
```

在本機執行時，會從.env檔案讀取這些值。 在生產（例如轉譯）中，它們會設定為環境變數。