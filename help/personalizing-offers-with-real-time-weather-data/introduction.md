---
title: 使用Web SDK在Adobe Journey Optimizer中使用即時天氣資料個人化優惠方案
description: 本教學課程示範如何使用即時情境資料和Adobe Journey Optimizer Web SDK Personalization API，在Adobe中提供動態的天氣感知選件。 您將瞭解如何從您的網站傳遞天氣屬性（例如溫度和條件）至Adobe Experience Platform，將它們對應至您的事件結構，並在決定規則和排名公式中使用它們，以在頁面載入時個人化優惠。 非常適合想要透過即時環境內容增強數位體驗的行銷人員和開發人員。
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00Z
jira: KT-18258
source-git-commit: d46c5a922b8448f57b8a730188284294c3caba96
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# 使用案例說明

在Adobe Journey Optimizer (AJO)中使用與天氣相關的資料來提供選件，可讓企業根據即時實際的環境條件來個人化客戶體驗。 天氣是強大的情境訊號。 人們的需求和行為會依天氣而改變。 透過使用天氣資料：

    提供符合客戶心情和環境的相關優惠方案。
    
    在炎熱的日子，顯示冷飲或交流電的優惠方案。 在雨天，促銷外套或雨傘

![天氣選件](assets/offers-use-case.png)