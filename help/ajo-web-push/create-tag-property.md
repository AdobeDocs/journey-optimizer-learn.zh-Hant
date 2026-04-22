---
title: 建立標籤屬性
description: 標籤屬性會透過Web SDK將資料從瀏覽器傳送至AEP。
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00Z
jira: KT-20879
source-git-commit: 3d342c5c4de4dda221ce4427b1e4aef7ef8c22cc
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---

# 建立標籤屬性

在本教學課程的第二部分，您將學習如何透過手動傳送自訂price.drop事件來即時觸發推播通知。 此方法使用AEP資料收集（標籤）從網頁擷取事件，並將其傳送至Adobe Experience Platform。 擷取事件後，它會在Adobe Journey Optimizer中觸發歷程，可讓您根據使用者動作或業務事件視需要傳送推播通知。

此屬性是透過AEP Web SDK設定，而後者已連線至教學課程中先前建立的`WebPushDataStream`。 標籤屬性會偵聽Adobe資料層上的`price.drop`事件，並透過更新ProductListItems資料元素來對應相關產品詳細資料。 準備資料後，tag屬性中的規則會引發，並透過Web SDK將price.drop事件傳送至AEP。 然後，此事件會當作Adobe Journey Optimizer中歷程的進入點，以便根據價格下降立即傳送推播通知。

## 標籤元素

用於儲存產品詳細資料的ProductListItems

![標籤元素](assets/product-list-items-element.png)

xdmvariable對應至`schemaForPushNotification`

![xdm-variable](assets/xdmvariable-data-element.png)

## 建立規則

聆聽price.drop事件
![資料推送事件](assets/tag-rule-event.png)

使用更新變數更新productListItems
![更新變數](assets/update-variable.png)
最後，將price.drop事件傳送至AEP並更新xdmvariable
![傳送事件](assets/send-event.png)

以下javascript程式碼會從網頁將price.drop事件傳送至AEP Tags

```javascript
 <script>
      window.adobeDataLayer.push({
        event: "price.drop",
        productListItems: productListItems
      });
  </script>
```



