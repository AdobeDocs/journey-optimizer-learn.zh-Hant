---
title: 使用Web SDK建立對象
description: 在本教學課程中，您將瞭解如何透過網頁表單擷取使用者偏好設定、即時將該資料傳送至Adobe Experience Platform (AEP)，以及根據使用者的選擇以動態方式將其符合目標對象的資格。 結合Adobe Tags (Launch)、AEP Web SDK (Alloy.js)和Edge Segmentation，您就能為對股票、債券或存款證(CD)感興趣的客戶帶來立即的個人化機會。
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00.000Z
jira: KT-17923
exl-id: ebaa3aa5-0a08-43fd-8d06-8e4b5d8dee05
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d2971708-e780-44bb-9e2a-72f139796afd
    internal-label: Customer
subfeature_v2:
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%
---
# 使用Web SDK建立對象

在本教學課程中，您將瞭解如何透過網頁表單擷取使用者偏好設定、即時將該資料傳送至Adobe Experience Platform (AEP)，以及根據使用者的選擇以動態方式將其符合目標對象的資格。 結合Adobe Tags (Launch)、AEP Web SDK (Alloy.js)和Edge Segmentation，您就能為對股票、債券或存款證(CD)感興趣的客戶帶來立即的個人化機會。

## 本教學課程的先決條件

* 存取Adobe Experience Platform

* 基本瞭解Adobe Experience Platform概念（設定檔、對象、資料集）

* 熟悉Adobe標籤(Launch) — 設定資料元素和規則

* JavaScript基本知識（閱讀和撰寫簡單函式）

* 能夠使用瀏覽器DevTools （主控台和網路標籤）


## 目標

本教學課程的目標是在Adobe Experience Platform (AEP)中建立並限定三個不同的對象：

* 對股票感興趣的客戶

* 對債券感興趣的客戶

* 對CD感興趣的客戶

使用者透過網路表單提交其偏好設定，而使用Adobe Launch透過AEP Web SDK擷取這些偏好設定，以啟用即時對象資格。

## 使用的工具

* Adobe Experience Platform (AEP)

* Adobe Experience Platform標籤

* AEP Web SDK (Alloy.js)

* AEP Edge區段

* 具有偏好設定表單的網頁
