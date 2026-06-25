---
title: 建立客群
description: 在Adobe Experience Platform中定義區段，將目標鎖定於有資格接收推播通知的使用者。
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
exl-id: 427bb35a-d607-48be-845d-9587c4cad86b
source-git-commit: 676c21ca09e0df8d404b05081d71b147755d65d5
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 9%

---

# 建立客群

若要建立促銷活動的對象，請在Adobe Experience Platform中定義區段，將目標鎖定於有資格接收推播通知的使用者。在本教學課程中，使用者若擁有使用中的推播訂閱（存在推播權杖）、未選擇退出通知（封鎖清單旗標為false），且與指定的應用程式設定相關聯（應用程式識別碼等於`my-first-push`）。這些使用者完全符合在Adobe Journey Optimizer中透過行銷活動或歷程接收網頁推播通知的資格。建立對象後，請確定已經過評估，以便填入設定檔並準備好進行目標定位。
然後此對象會用於行銷活動中，以僅將排程的網頁推送訊息傳送給已訂閱的使用者。

![建立對象](assets/push-audience.png)
