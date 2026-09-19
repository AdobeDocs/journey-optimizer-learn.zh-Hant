---
title: 在 Adobe Journey Optimizer 中使用網頁 SDK 以即時天氣資料個人化產品建議
description: 本教學課程展示如何使用即時內容資料和 Adobe Web SDK 個人化 API，在 Adobe Journey Optimizer 中提供動態、天氣感知的產品建議。 您將了解如何從您的網站傳遞天氣屬性 (例如溫度和天氣狀況) 至 Adobe Experience Platform，將它們對應至您的事件結構描述，並在決策規則和排名公式中使用它們，以在頁面載入時個人化產品建議。 非常適合想要透過即時環境內容增強數位體驗的行銷人員和開發人員。
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10
jira: KT-18258
exl-id: f40dd541-470c-4f42-8181-eb1c277ebaa3
source-git-commit: b4cf9b677c6bc142e1013649db16b3a70b405052
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 42%
---
# 使用案例說明

在Adobe Journey Optimizer (AJO)中使用與天氣相關的資料來提供選件，可讓企業根據即時實際的環境條件來個人化客戶體驗。 天氣是強大的情境訊號。 人們的需求和行為會依天氣而改變。 透過使用天氣資料：

提供與客戶情緒和環境相符的相關優惠方案

在炎熱的日子，顯示冷飲或AC機種的優惠方案。 下雨天促銷夾克或雨傘

基於天氣的選件範例


![天氣選件](assets/offers-use-case.png)



## 本教學課程的先決條件

* 存取Experience Platform。

* 對Adobe Experience Platform標籤的基本瞭解。

* 基本瞭解Experience Platform概念（設定檔、對象、資料集）。

* 熟悉Journey Optimizer。

* 基本JavaScript知識（閱讀和撰寫簡單函式）。

* 能夠使用瀏覽器DevTools （主控台和網路標籤）。
