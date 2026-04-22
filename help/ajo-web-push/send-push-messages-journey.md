---
title: 在歷程中傳送推送訊息
description: Adobe Journey Optimizer中的頻率上限會套用至個別優惠方案層級，而且有賴擷取優惠方案曝光次數和點選事件。 這需要使用Adobe Web SDK來追蹤decisioning.propositionDisplay和decisioning.propositionInteract事件，並將它們對應到Adobe Experience Platform中更新的XDM體驗事件結構描述。
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00Z
jira: KT-18526
source-git-commit: 3d342c5c4de4dda221ce4427b1e4aef7ef8c22cc
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# 在歷程中傳送推送訊息

根據價格下降事件觸發歷程可讓使用者即時進行行為導向的參與。 在真實情境中，此事件通常源自於產品價格更新時的後端定價系統。 在本教學課程中，我們會使用AEP標籤，透過Adobe資料層傳送自訂price.drop事件（包括名稱和SKU等產品詳細資訊），以模擬該行為。 此事件會擷取至Adobe Experience Platform，並當作Adobe Journey Optimizer中歷程的進入觸發器。 歷程收到後，可以立即向合格使用者傳送個人化推播通知，通知他們價格下降並鼓勵及時採取行動。

使用自訂事件觸發歷程涉及以下步驟

## 在Journey Optimizer中建立自訂事件

登入Adobe Journey Optimizer並導覽至「管理」→「設定」→「事件」，然後選取「建立事件」。 建立名為PriceDropEvent的新事件，並將其與教學課程中先前建立的事件結構描述SchemaForPushNotification建立關聯。 請確定事件屬性已設定為如參考影像中所示。

![event-properties](assets/price-drop-event.png)

從結構描述中，選取必要欄位，以使其可用於個人化。 具體來說，包括ProductListItems物件中的`Name`和`SKU`，以及identityMap中的識別碼。 然後，您就可以在個人化編輯器中存取這些欄位，讓您根據產品和使用者內容動態撰寫推播通知訊息。

## 建立標籤屬性

此屬性是透過AEP Web SDK設定，而後者已連線至教學課程中先前建立的WebPushDataStream。 tag屬性會偵聽Adobe資料層上的price.drop事件，並透過更新ProductListItems資料元素來對應相關產品詳細資訊。 準備資料後，tag屬性中的規則會引發，並透過Web SDK將price.drop事件傳送至AEP。 然後，此事件會當作Adobe Journey Optimizer中歷程的進入點，以便根據價格下降立即傳送推播通知。



