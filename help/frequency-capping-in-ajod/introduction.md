---
title: 對透過AJO Decisioning提供的Adobe Journey Optimizer (AJO)優惠實作頻率上限
description: 本教學課程透過對使用Adobe Journey Optimizer Decisioning提供的選件啟用頻率上限，來擴充現有的AJO (AJO)實作。 它概述如何擷取用於頻率上限的曝光和互動事件。
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00.000Z
jira: KT-18526
exl-id: ae74485f-9ea1-428d-9c07-5db0c5cf93fb
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
source-wordcount: '214'
ht-degree: 7%
---
# 對透過AJO Decisioning提供的Adobe Journey Optimizer (AJO)優惠實作頻率上限

本教學課程示範如何對Adobe Journey Optimizer中的優惠方案套用頻率限定，以控制使用者隨時間看到相同優惠方案的頻率。

本教學課程假設您已依照根據天氣條件個人化優惠方案的[教學課程，設定AJO行銷活動](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/introduction)

透過Adobe Web SDK擷取decisioning.propositionDisplay和decisioning.propositionInteract事件，並將這些事件對應至Adobe Experience Platform (AEP)中的XDM結構，Adobe Journey Optimizer可以準確地追蹤優惠閱聽和互動，並啟用頻率上限來限制向使用者顯示優惠的頻率。

## 本教學課程的先決條件

繼續之前，請確定您使用決策的Adobe Journey Optimizer行銷活動有效，且正在主動提供選件至網頁表面。

本教學課程假設選件傳送已正常運作，並專注於設定和驗證頻率上限行為。




