---
title: 建立對象
description: 根據使用者投資偏好設定（股票、債券、CD）建立AJO受眾
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00Z
jira: KT-17923
source-git-commit: f970a1780b1bdf717675cd79c98a38ac422a679f
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---


# 根據使用者投資偏好設定（股票、債券、CD）建立AJO受眾

在本教學課程中，您將瞭解如何透過網路表單擷取使用者偏好設定、即時將該資料傳送至Adobe Experience Platform (AEP)，以及根據使用者的選擇以動態方式將其符合目標對象的資格。 結合Adobe Tags (Launch)、AEP Web SDK (Alloy.js)和Edge Segmentation，您就能為對股票、債券或存款證(CD)感興趣的客戶帶來立即的個人化機會。

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

使用者會透過網頁表單提交其偏好設定，這些偏好設定會透過Adobe Launch的AEP Web SDK內嵌，以啟用即時對象資格。

## 使用的工具

* Adobe Experience Platform (AEP)

* Adobe Experience Platform標籤

* AEP Web SDK (Alloy.js)

* AEP Edge區段

* 具有偏好設定表單的網頁





