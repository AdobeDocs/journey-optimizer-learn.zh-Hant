---
title: 使用Adobe Web SDK擷取優惠方案互動，以進行AI模型訓練
description: 本文主要說明如何使用Adobe Experience Platform Web SDK (alloy.js)擷取使用者互動資料，例如選件曝光次數和點按次數。 此資料可當作在Adobe Journey Optimizer (AJO)中訓練AI模型的基礎，以便根據使用者行為和內容訊號來智慧地排名選件。
feature: Decisioning
topic: Integrations
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2025-07-08T00:00:00Z
jira: KT-18451
source-git-commit: dfb280df3453e7811dffd95b9af664b873a9af31
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---


# 使用Adobe Web SDK擷取優惠方案互動，以進行AI模型訓練

本文示範如何透過直接在Adobe Experience Platform程式碼中呼叫alloy(&quot;sendEvent&quot;， ...)，使用JavaScript Web SDK擷取優惠方案互動事件（例如曝光數或點按數）。 資料將會內嵌至AEP，並用於在Adobe Journey Optimizer (AJO)中訓練AI模型，以根據即時行為更聰明地排名選件。

## 先決條件

開始之前，請確定已具備下列專案：

- 已安裝搭配Adobe Web SDK擴充功能使用的啟動Adobe Experience Platform屬性。

- 已設定[資料串流](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/decisioning/experience-decisioning/collect-event-data/create-dataset)並對應至您的AEP沙箱。

- 部署Launch的網站。


## 建立選件互動事件的結構和資料集

若要收集體驗事件，您必須先建立要傳送這些事件的資料集。

依照此[文章中提及的步驟建立所需的結構描述和資料集](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/decisioning/experience-decisioning/collect-event-data/create-dataset)

## 在AEP中建立資料串流

![資料流](assets/ai-model-data-stream.png)
將Adobe Experience Platform服務新增至資料流
![資料流服務](assets/data-stream-service.png)

## 使用網頁SDK設定Adobe Experience Platform標籤

在擴充功能設定中：

設定Adobe Experience Platform Web SDK擴充功能，以使用已建立的資料流
