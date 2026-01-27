---
title: 對透過AJO Decisioning提供的Adobe Journey Optimizer (AJO)優惠實作頻率上限
description: 本教學課程透過對使用Adobe Journey Optimizer Decisioning提供的選件啟用頻率上限，來擴充現有的AJO (AJO)實作。 它概述如何擷取用於頻率上限的曝光和互動事件。
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00Z
jira: KT-18526
exl-id: ae74485f-9ea1-428d-9c07-5db0c5cf93fb
source-git-commit: 441fdbc33486f027c22d1b94e03919c5666ca003
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# 對透過AJO Decisioning提供的Adobe Journey Optimizer (AJO)優惠實作頻率上限

本教學課程示範如何對Adobe Journey Optimizer中的優惠方案套用頻率限定，以控制使用者隨時間看到相同優惠方案的頻率。

本教學課程假設您已依照根據天氣條件個人化優惠方案的[教學課程，設定AJO行銷活動](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/introduction)

透過Adobe Web SDK擷取decisioning.propositionDisplay和decisioning.propositionInteract事件，並將這些事件對應至Adobe Experience Platform (AEP)中的XDM結構，Adobe Journey Optimizer可以準確地追蹤優惠閱聽和互動，並啟用頻率上限來限制向使用者顯示優惠的頻率。

## 本教學課程的先決條件

繼續之前，請確定您使用決策的Adobe Journey Optimizer行銷活動有效，且正在主動提供選件至網頁表面。

本教學課程假設選件傳送已正常運作，並專注於設定和驗證頻率上限行為。




