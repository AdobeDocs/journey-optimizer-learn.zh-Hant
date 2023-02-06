---
title: 設定事件
description: 設定實作Journey Optimizer挑戰所需的三個事件
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
recommendations: noDisplay, noCatalog
hide: true
exl-id: c7826818-c28a-493b-8aba-9d8a8102336d
source-git-commit: 7ecbed1b722d7f05ffd4a7c7071358d993cb1392
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 10%

---

# 設定事件

在本節中，您可以在 [Journey Optimizer挑戰](/help/challenges/introduction-and-prerequisites.md).

以下影片說明如何建立事件：

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

## 建立Luma線上購買事件

使用此事件時，Journey Optimizer會在使用者線上購買luma產品時收到資訊。

1. 使用下列參數建立事件：

   | [!UICONTROL 參數] | [!UICONTROL 值] |
   |-------------|-----------|
   | [!UICONTROL 名稱] | `LumaOnlinePurchase` |
   | [!UICONTROL 類型] | [!UICONTROL 單一] |
   | [!UICONTROL 事件ID類型] | [!UICONTROL 規則型] |
   | [!UICONTROL 方案] | `Luma Web Events Schema` |
   | [!UICONTROL 欄位] | `eventType` <br>`commerce.order.priceTotal`<br>`commerce.order.purchaseOrderNumber`<br>`commerce.shipping.adress.street1`<br>`commerce.shipping.adress.city`<br>`commerce.shipping.adress.postalCode`<br>`commerce.shipping.adress.state`<br>`productListItems.quantity`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.name`<br>`productListItems.Luma Product Catalog Schema._your Organization_IDprice`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.imageURL`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.url` |

2. 新增 [!UICONTROL 事件ID條件]: `LumaOnlinePurchase.eventType is commerce.purchases`

   1. 選取鉛筆圖示以編輯欄位
   2. 在 [!UICONTROL 新增事件ID條件] 強制回應視窗，拖放 `eventType` 在畫布上
   3. 選擇 `commerce.purchases`
   4. 在畫布上選擇「確定」
   5. 在強制回應視窗上選取「確定」

![新增事件條件](/help/tutorial-configure-a-training-sandbox/assets/Event-lumaOnlinePurchase-condition-1.png)

1. 選擇 [!UICONTROL 命名空間]: `Luma CRM ID (lumaCrmId)`

2. 選取「**[!UICONTROL 儲存]**」。

## 建立 *[!DNL Luma Wishlist Add]* 事件

| [!UICONTROL 參數] | [!UICONTROL 值] |
|-------------|-----------|
| [!UICONTROL 名稱] | `LumaWishlistAdd` |
| [!UICONTROL 類型] | [!UICONTROL 單一] |
| [!UICONTROL 事件ID類型] | [!UICONTROL 規則型] |
| [!UICONTROL 方案] | `Luma Product Interactions` |
| [!UICONTROL 欄位] | EventType<br>productListItem.quantity<br><b>在產品清單項目> Luma產品> _*[!DNL yourOrganizationID]* >產品：</b> <br>名稱<br>價格<br> ProductImageURL<br>ProductURL |
| [!UICONTROL 條件] | [!DNL LumaWishlistAdd.eventType is commerce.saveForLaters] |
| [!UICONTROL 命名空間] | 電子郵件(EMail) |

## 建立 *[!DNL Luma Product Restock]* 事件

| [!UICONTROL 參數] | [!UICONTROL 值] |
|-------------|-----------|
| [!UICONTROL 名稱] | `LumaProductRestock` |
| [!UICONTROL 類型] | [!UICONTROL 商務] |
| [!UICONTROL 方案] | [!DNL Luma Product Inventory Events] |
| [!UICONTROL 欄位] | SKU <br> stockEventType<br><b> yourOrganizationID > product:</b> <br>名稱<br>價格<br> ImageURL<br>說明 |
| [!UICONTROL 條件] | LumaProductRestock。_`your organization's ID`.inventoryEvent.stockEventType為重新存貨 |

## 恭喜

您的沙箱現已可供使用！
