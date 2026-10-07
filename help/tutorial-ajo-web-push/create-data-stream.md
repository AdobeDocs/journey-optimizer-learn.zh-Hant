---
title: 建立資料串流
description: 此頁面會引導您在Adobe Experience Platform中建立資料串流，這是從Web SDK收集資料，並將其路由至AEP和Adobe Journey Optimizer的必要條件。 資料串流會作為網頁應用程式與Adobe服務之間的連線，以便處理推播訂閱和事件資料。
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00.000Z
jira: KT-20879
exl-id: d419f6a4-67d5-46b5-9ae7-5a317300d1ad
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
source-wordcount: '298'
ht-degree: 0%
---
# 建立資料串流

Adobe Experience Platform (AEP)中的資料串流會作為端點，用於接收從網站SDK傳送的資料。 它會將此資料路由至已設定的服務，例如AEP、Adobe Analytics或Adobe Journey Optimizer。 在本教學課程中，資料串流可用來將網頁推送訂閱資料和price.drop事件傳送至AEP以進行啟用。

## 建立事件結構描述以追蹤推播通知

建立名稱為`SchemaForPushNotification`的新XDM ExperienceEvent結構描述。 將`Push Notification Tracking`和`Commerce Details`欄位群組新增至此結構描述。 Commerce詳細資料欄位群組中的欄位將用來擷取產品資訊及觸發自訂price.drop事件。

![event-schema](assets/event-schema.png)

## 建立設定檔結構描述以儲存使用者的同意

在本教學課程中，我們使用現成可用的`AJO Push Profile Schema`。 此結構描述儲存使用者的推送訂閱詳細資料，包括傳送Web推送通知所需的推送代號。

![profile_schema](assets/profile-schema.png)

## 為結構描述建立資料集

使用先前建立的事件結構描述建立名為`DataSetForPushNotification`的資料集。 若是設定檔資料，請使用與推播設定檔結構描述關聯的現成可用的`AJO Push Profile Dataset`。 記下`DataSetForPushNotification` ID，因為稍後在教學課程中透過.env檔案設定應用程式時，會需要記下。

## 使用事件和設定檔資料集建立資料串流

使用上一步中建立的事件和設定檔資料集，建立名為WebPushDataStream的新資料流。 記下資料串流ID，因為稍後透過.env檔案設定應用程式時，教學課程會要求記下此ID。

![資料流](assets/datastream.png)
