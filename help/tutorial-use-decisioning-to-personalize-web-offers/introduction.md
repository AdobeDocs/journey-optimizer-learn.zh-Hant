---
title: 使用Decisioning個人化Web優惠
description: 瞭解如何使用Journey Optimizer (AJO) Decisioning，透過Experience Platform (AEP)內建的受眾細分在網頁上提供個人化優惠。
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00.000Z
jira: KT-17728
exl-id: 382ee746-e8cd-4843-bfe9-913df8914136
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
source-wordcount: '239'
ht-degree: 7%
---
# 使用Decisioning個人化Web優惠

本教學課程以先前使用Adobe Experience Platform (AEP) Web SDK建立的對象細分設定為基礎。 在[先前的教學課程](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/create-audiences-using-web-sdk/introduction)中，已擷取使用者偏好設定(例如股票、債券或存款證(CD)中的利息)，並將這些偏好設定用於在Experience Platform中將個人細分為目標受眾。 本教學課程在此基礎上再接再厲，使用Adobe Journey Optimizer (AJO) Decisioning即時為這些對象提供個人化財務優惠方案，強化參與和轉換結果。


## 本教學課程的先決條件

* 存取Experience Platform

* 基本瞭解Experience Platform概念（設定檔、對象、資料集）

* 熟悉Journey Optimizer

* JavaScript基本知識（閱讀和撰寫簡單函式）

* 能夠使用瀏覽器DevTools （控制檯和網路標籤）


## 目標

本教學課程會引導您在使用Journey Optimizer的網站上提供個人化投資選件，例如股票、債券或CD。 運用對象細分和決策策略，您就能瞭解如何確保每位訪客都能根據其偏好看到最相關的優惠方案。

## 使用的工具

* Adobe Experience Platform (AEP)
* Adobe Journey Optimizer (AJO)
* Adobe Experience Platform標籤
* AEP Web SDK (`Alloy.js`)
* AEP Edge區段
* 顯示優惠方案的網頁
