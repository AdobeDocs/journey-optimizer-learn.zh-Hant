---
title: 使用Decisioning個人化Web優惠
description: 瞭解如何使用Journey Optimizer (AJO) Decisioning，透過Experience Platform (AEP)內建的受眾細分在網頁上提供個人化優惠。
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00Z
jira: KT-17728
exl-id: 382ee746-e8cd-4843-bfe9-913df8914136
source-git-commit: 71c406e7a06c49f01245970c280c6a7beb84da5f
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 1%

---

# 使用Decisioning個人化Web優惠

本教學課程以先前使用Adobe Experience Platform (AEP) Web SDK建立的對象細分設定為基礎。 在[先前的教學課程](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/create-audiences-using-web-sdk/introduction)中，已擷取使用者偏好設定(例如股票、債券或存款證(CD)中的利息)，並將這些偏好設定用於在Experience Platform中將個人細分為目標受眾。 本教學課程在此基礎上再接再厲，使用Adobe Journey Optimizer (AJO) Decisioning即時為這些對象提供個人化財務優惠方案，強化參與和轉換結果。

您可以使用以下連結即時測試個人化AJO優惠。
[按一下這裡以檢視即時示範](https://gbedekar489.github.io/finwise/welcome.html)。 頁面會根據您的投資偏好設定顯示即時優惠方案。

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
