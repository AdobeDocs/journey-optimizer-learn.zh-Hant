---
title: 設定事件
description: 設定實作 Journey Optimizer 挑戰所需的三個事件
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
recommendations: noDisplay, noCatalog
exl-id: c7826818-c28a-493b-8aba-9d8a8102336d
source-git-commit: b2afc28f82967324ebed0ee17e291e83c85c3a4c
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 100%

---

# 設定事件

在本節中，您將設定 [Journey Optimizer 挑戰](/help/challenges/introduction-and-prerequisites.md)中的實作練習所需的三個事件。

以下影片說明如何建立事件：

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12&learn=on)

## 建立 Luma 線上購買事件

當使用此事件，Journey Optimizer 會在使用者線上購買 luma 產品時收到資訊。

1. 使用下列參數建立事件：

   | [!UICONTROL 參數] | [!UICONTROL 值] |
   |-------------|-----------|
   | [!UICONTROL 名稱] | `LumaOnlinePurchase` |
   | [!UICONTROL 類型] | [!UICONTROL 單一] |
   | [!UICONTROL 事件 ID 類型] | [!UICONTROL 規則型] |
   | [!UICONTROL 方案] | `Luma Web Events Schema` |
   | [!UICONTROL 欄位] | `eventType` <br>`commerce.order.priceTotal`<br>`commerce.order.purchaseOrderNumber`<br>`commerce.shipping.adress.street1`<br>`commerce.shipping.adress.city`<br>`commerce.shipping.adress.postalCode`<br>`commerce.shipping.adress.state`<br>`productListItems.quantity`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.name`<br>`productListItems.Luma Product Catalog Schema._your Organization_IDprice`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.imageURL`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.url` |

1. 新增[!UICONTROL 事件 ID 條件]：`LumaOnlinePurchase.eventType is commerce.purchases`：

   1. 選取鉛筆圖示以編輯欄位。

   1. 在&#x200B;**[!UICONTROL 新增事件 ID 條件]**&#x200B;模式，將`eventType`拖放到畫布。
   1. 選擇「`commerce.purchases`」。
   1. 在畫布上選取&#x200B;**[!UICONTROL 確定]**。
   1. 在模式中選取&#x200B;**[!UICONTROL 確定]**。

   ![新增事件條件](/help/tutorial-configure-a-training-sandbox/assets/Event-lumaOnlinePurchase-condition-1.png)

1. 選取[!UICONTROL 命名空間]：`Luma CRM ID (lumaCrmId)`

1. 選取「**[!UICONTROL 儲存]**」。

## 建立&#x200B;*[!DNL Luma Wishlist Add]*&#x200B;事件

| [!UICONTROL 參數] | [!UICONTROL 值] |
|-------------|-----------|
| [!UICONTROL 名稱] | `LumaWishlistAdd` |
| [!UICONTROL 類型] | [!UICONTROL 單一] |
| [!UICONTROL 事件 ID 類型] | [!UICONTROL 規則型] |
| [!UICONTROL 方案] | `Luma Product Interactions` |
| [!UICONTROL 欄位] | EventType<br>productListItem.quantity<br><b>在產品清單項目 > Luma 產品> _*[!DNL yourOrganizationID]* > 產品：</b> <br>名稱<br>價格<br> ProductImageURL<br>ProductURL |
| [!UICONTROL 條件] | [!DNL LumaWishlistAdd.eventType is commerce.saveForLaters] |
| [!UICONTROL 命名空間] | 電子郵件 (EMail) |

## 建立&#x200B;*[!DNL Luma Product Restock]*&#x200B;事件

| [!UICONTROL 參數] | [!UICONTROL 值] |
|-------------|-----------|
| [!UICONTROL 名稱] | `LumaProductRestock` |
| [!UICONTROL 類型] | [!UICONTROL 商務] |
| [!UICONTROL 方案] | [!DNL Luma Product Inventory Events] |
| [!UICONTROL 欄位] | SKU <br> stockEventType<br><b> yourOrganizationID > product:</b> <br>名稱<br>價格<br> ImageURL<br>說明 |
| [!UICONTROL 條件] | LumaProductRestock._`your organization's ID`.inventoryEvent.stockEventType 為重新進貨 |

恭喜！您的沙箱現已可供使用。
