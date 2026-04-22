---
title: Create journey
description: Create journey that is triggered on price.drop event
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
source-git-commit: 3d342c5c4de4dda221ce4427b1e4aef7ef8c22cc
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Create Journey

在此步驟中，您將會在Adobe Journey Optimizer中建立由自訂price.drop事件觸發的歷程。 收到此事件時，歷程會即時開始，並傳送推播通知給選擇加入的使用者，以啟用事件導向參與。

若要建立在price.drop事件上觸發的歷程，請遵循下列步驟

* 登入Journey Optimizer
* 導覽至歷程管理|歷程|建立歷程

![create-journey](assets/create-journey.png)

## 新增PriceDropEvent

將`PriceDropEvent`從事件區段拖曳到畫布
![價格捨棄事件](assets/add-price-drop-event.png)

## 新增推播動作

Expand the Actions section. Drag and drop the `Action` activity on to the canvas and select Push as the action type
![push-action](assets/add-push-action.png)

## Configure the Push Action

選取推播通知活動，然後按一下設定動作

![設定 — 推播 — 動作](assets/configure-push-action.png)

## 推播通知管道設定

將教學課程中先前建立的`MyFirstWebPushChannel`設定與此推播通知建立關聯

![頻道設定](assets/journey-actions.png)

## 撰寫推播通知訊息

使用個人化編輯器，將靜態和動態內容的組合新增至推播通知，讓訊息更具吸引力及相關性。

To begin composing the message, click on `Content` to open the content tab, where you can define both the fixed text and the dynamic fields derived from the event data.
![content-push](assets/compose-message.png)

Specify the title of the push message, then open the personalization editor to compose the message body. The content will dynamically include the names of the product(s) whose prices have dropped. To achieve this, use the each [helper function](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/personalization/functions/helpers#each)
to iterate over the list of products and render their names within the message.

## 撰寫訊息內文

從協助程式函式選單中選取並插入`Each`函式。
![協助程式函式](assets/journey-content-helper-function.png)

選取內容屬性| Journey Orchestration |事件| PriceDropEvent | productListItems |名稱

按一下「+」圖示，將陣列插入個人化編輯器內的每個回圈中。 然後，更新訊息內容以符合參考熒幕擷取畫面中顯示的格式。 請注意，您環境中顯示的事件ID可能與畫面不同。

![內容屬性](assets/journey-content-context-attributes.png)

最後，儲存所有變更並發佈歷程。 發佈後，歷程會變成使用中並監聽傳入的price.drop事件。 Whenever such an event is received, the journey is triggered in real time, and a push notification is sent to users who have opted in to receive notifications, ensuring timely and relevant engagement.

## Test the solution

To trigger the price.drop event, open the [price drop trigger page,](http://localhost:3000/price-drop-trigger.html) select one or more products, and click Trigger Price Drop. This sends the event through the Adobe Data Layer using AEP Tags, which then initiates the journey and delivers the push notification in real time.



