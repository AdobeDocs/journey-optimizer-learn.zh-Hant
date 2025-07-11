---
title: 根據郵遞區號和收入使用排名公式個人化優惠
description: 使用Adobe Journey Optimizer的排名公式，根據每位使用者的郵遞區號和收入層級，以動態方式提供最相關的金融優惠方案，以提高參與度和智慧型個人化。
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-27T00:00:00Z
jira: KT-18188
exl-id: 11685f7c-8048-4318-9c28-71bd7da8f7ff
source-git-commit: 85d3def3afb1d073b133df40e4cbf32d00a3a5c9
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# 使用根據使用者郵遞區號和收入的排名公式來個人化優惠

此使用案例示範如何在Adobe Journey Optimizer中運用郵遞區號和年收入等使用者屬性，提供個人化的財務優惠方案。 透過使用排名公式，優惠方案會根據特定地點促銷活動與收入型資格進行智慧評分與優先順序。 例如，高收益CD可促銷給富裕郵遞區號的使用者，而新興投資者則可獲得多樣化的投資選項。 排名公式可確保每位使用者都能收到相關且經濟上適當的選件。 排名標準是使用設定檔屬性、情境式訊號和選用的AI模型來定義，以進一步提升決策精確度。 選件會透過網路或電子郵件通道即時傳送，有助於提高參與度和轉換率。 此方法結合商業邏輯與資料導向的個人化，以提升使用者體驗和行銷影響。

## 先決條件

本教學課程以Adobe Journey Optimizer和Adobe Experience Platform的重要概念為基礎。 繼續之前，請確定符合下列先決條件：

* [身分拼接教學課程](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorial-on-identity-stitching-in-aep/introduction)已完成，CRM ID已成功與Adobe Experience Platform中的ECID建立關聯。

* 熟悉如何在AJO中建立優惠專案，包括內容定義、中繼資料設定和適用性規則。

* 熟悉設定用於選件傳送的管道（例如Web或電子郵件）。

* 熟悉如何在AJO中建立和啟用行銷活動。

* 熟悉使用Adobe Launch （標籤）來部署網路SDK，以及傳送包含身分和設定檔資料的事件。

本教學課程涵蓋Offer Decisioning的後續步驟：

* 使用設定檔屬性（例如郵遞區號和年收入）建立排名方法。

* 定義選取策略以將優惠分組，並排定優先順序。

* 建立決定政策，向每一個人提供最相關的優惠方案。
