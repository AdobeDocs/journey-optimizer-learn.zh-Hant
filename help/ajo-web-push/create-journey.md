---
title: 建立歷程
description: 建立在price.drop事件上觸發的歷程
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
exl-id: 14342b47-5485-4f7f-9312-cff1ee0f8972
source-git-commit: fe5ce1bd62e4cf628d0adf67389e4301660a223a
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# 建立歷程

在此步驟中，您將會在Adobe Journey Optimizer中建立由自訂price.drop事件觸發的歷程。 收到此事件時，歷程會即時開始，並傳送推播通知給選擇加入的使用者，以啟用事件導向參與。

若要建立在price.drop事件上觸發的歷程，請遵循下列步驟

* 登入Journey Optimizer
* 導覽至歷程管理 |歷程 |建立歷程

![create-journey](assets/create-journey.png)

## 新增PriceDropEvent

將`PriceDropEvent`從事件區段拖曳到畫布。
![價格捨棄事件](assets/add-price-drop-event.png)

## 新增推播動作

展開動作區段。 將`Action`活動拖放到畫布上，並選取「推播」作為動作型別
![推播動作](assets/add-push-action.png)

## 設定推送動作

選取推播通知活動，然後按一下設定動作

![設定 — 推播 — 動作](assets/configure-push-action.png)

## 推播通知管道設定

將教學課程中先前建立的`MyFirstWebPushChannel`設定與此推播通知建立關聯

![頻道設定](assets/journey-actions.png)

## 撰寫推播通知訊息

使用個人化編輯器，將靜態和動態內容的組合新增至推播通知，讓訊息更具吸引力及相關性。

若要開始撰寫訊息，請按一下`Content`以開啟內容標籤，您可以在其中定義固定文字和衍生自事件資料的動態欄位。
![內容推播](assets/compose-message.png)

指定推送訊息的標題，然後開啟個人化編輯器以撰寫訊息內文。 內容會動態包含價格已下跌的產品名稱。 若要實現此目的，請使用每個[協助程式函式](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/personalization/functions/helpers#each)
重複產品清單，並在訊息中呈現其名稱。

## 撰寫訊息內文

從協助程式函式選單中選取並插入`Each`函式。
![輔助函式](assets/journey-content-helper-function.png)

選取內容屬性 |Journey Orchestration |活動 | PriceDropEvent | productListItems |名稱

按一下「+」圖示，將陣列插入個人化編輯器內的每個回圈中。 然後，更新訊息內容以符合參考熒幕擷取畫面中顯示的格式。 請注意，您環境中顯示的事件ID可能與畫面不同。

![內容屬性](assets/journey-content-context-attributes.png)

最後，儲存所有變更並發佈歷程。 發佈後，歷程會變成使用中並監聽傳入的price.drop事件。 每當收到這類事件時，就會即時觸發歷程，並傳送推播通知給選擇接收通知的使用者，以確保及時且相關的參與。

## 測試解決方案

若要觸發price.drop事件，請開啟[價格下降觸發程式頁面，](http://localhost:3000/price-drop-trigger.html)選取一或多個產品，然後按一下[觸發價格下降]。 這會使用AEP標籤透過Adobe資料層傳送事件，接著起始歷程並即時傳送推播通知。
