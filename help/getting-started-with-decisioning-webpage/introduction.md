---
title: 使用AJO Decisioning根據對象製作個人化網頁選件
description: 瞭解如何使用Adobe Journey Optimizer (AJO) Decisioning，透過Adobe Experience Platform (AEP)內建的受眾細分在網頁上提供個人化優惠。
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00Z
jira: KT-17728
exl-id: 382ee746-e8cd-4843-bfe9-913df8914136
source-git-commit: 5ab637d9b9955ab334ee67ed887e34026b04206d
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---

# 使用AJO Decisioning根據對象製作個人化網頁選件

本教學課程以先前使用Adobe Experience Platform (AEP) Web SDK建立的對象細分設定為基礎。 在上一個教學課程中，擷取了使用者偏好設定(例如股票、債券或存款證(CD)中的利息)，並將其用來將個人細分為Adobe Experience Platform (AEP)內的目標受眾。 本教學課程在此基礎上再接再厲，使用Adobe Journey Optimizer (AJO) Decisioning即時為這些對象提供個人化財務優惠方案，強化參與和轉換結果。

您可以使用以下連結即時測試個人化AJO優惠。
[按一下這裡以檢視即時示範](https://gbedekar489.github.io/finwise/welcome.html) — 頁面會根據您的投資偏好顯示即時優惠。

## 本教學課程的先決條件

* 存取Adobe Experience Platform

* 基本瞭解Adobe Experience Platform概念（設定檔、對象、資料集）

* 熟悉Adobe Journey Optimizer

* JavaScript基本知識（閱讀和撰寫簡單函式）

* 能夠使用瀏覽器DevTools （控制檯和網路標籤）


## 目標

本教學課程會引導您使用Adobe Journey Optimizer (AJO)在網站上提供個人化投資選件（例如股票、債券或CD）。 運用對象細分和決策策略，您就能瞭解如何確保每位訪客都能根據其偏好看到最相關的優惠方案。

## 使用的工具

* Adobe Experience Platform (AEP)
* Adobe Journey Optimizer (AJO)
* Adobe Experience Platform標籤
* AEP Web SDK (Alloy.js)
* AEP Edge區段
* 顯示優惠方案的網頁
