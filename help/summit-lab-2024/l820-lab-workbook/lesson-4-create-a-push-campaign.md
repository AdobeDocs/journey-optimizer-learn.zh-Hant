---
title: 第4課 — 建立推播行銷活動
description: 檢閱設定檔資料，並瞭解如何在Journey Optimizer中建立推播通知並傳送對象至。
feature: Push
role: User
level: Intermediate
doc-type: Tutorial
duration: 0
recommendations: noDisplay, noCatalog
jira: KT-14980
exl-id: 0f82d6a5-18c0-45f2-968e-a678fc2d5768
source-git-commit: 55ba1a46c1473d94847e7fccc69ed2a33badb54c
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 2%

---

# 第4課 — 建立推播行銷活動

在上一個練習中，您是咖啡愛好者、Fréscopa客戶。 您透過品牌網站和Fréscopa應用程式與品牌互動，並收到許多交易式訊息。 這些訊息會透過使用者與網站或應用程式的互動觸發。

在本練習中，您將會讓行銷人員加入並實施Frésopa的行銷活動，其將利用推播通道來鎖定目標Fréscopa應用程式使用者。 推播通知可用來讓應用程式使用者隨時瞭解情況（即使他們未使用應用程式），也可以讓他們透過應用程式重新互動。 目的是透過提供10%的折扣，鼓勵客戶購買混合式房屋。

## 學習目標

* 瞭解如何建立推播行銷活動。
* 瞭解如何設計推送訊息。

<br>

## 練習4.1 — 建立推播行銷活動

在本練習中，您將建立推播行銷活動、設計並自訂推播通知，並將推播通知傳送至您自己的裝置。

1. 在Journey Optimizer的左側導覽列的&#x200B;**[!UICONTROL 歷程管理]**&#x200B;區段中，選取&#x200B;**行銷活動**。

1. 按一下&#x200B;**[!UICONTROL 建立行銷活動]**。

   ![建立行銷活動](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-1-1-create-campaign.png)

1. 在&#x200B;**[!UICONTROL 建立行銷活動]**&#x200B;頁面的&#x200B;**[!UICONTROL 動作]**&#x200B;區段中，選取&#x200B;**[!UICONTROL 推播通知]**&#x200B;核取方塊。

1. 從&#x200B;**[!UICONTROL 應用程式表面]**&#x200B;下拉式清單中，選取&#x200B;*[!DNL Frecopa-Push]*。

1. 按一下&#x200B;**[!UICONTROL 建立]**&#x200B;以建立推播行銷活動。

   ![應用程式表面](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-1-2-app-surface.png)

>[!SUCCESS]
>
>您現在應該在Campaign屬性頁面上：
> ![行銷活動屬性](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-1-2-campaign-properties.png)

## 練習4.2 — 設定行銷活動

您可以在此頁面上設定行銷活動的屬性、對象、動作和排程。

### 4.2.1 [!UICONTROL 屬性區段]

為行銷活動命名。 請務必以您的座位編號作為名稱開頭，以便在搜尋時輕鬆找到您的促銷活動。

例如，如果您的座位數為99： `99 - 10% Discount Campaign`。

### 4.2.2 **[!UICONTROL 對象區段]**

1. 在對象區段中，按一下&#x200B;**[!UICONTROL 選取對象]**。

   ![對象區段](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-2-5-audience-section.png)

1. 在&#x200B;**[!UICONTROL 選取對象]**&#x200B;畫面上，搜尋對象：

   **實驗室 — 座位`your seat number`**

1. 選取對象，然後按一下[儲存]。****

   ![對象選擇](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-2-7-select-audience.png)

### 4.2.3編輯推播通知的內容

在本練習中，您將設計和自訂推播通知。

1. 在&#x200B;**[!UICONTROL 動作]**&#x200B;區段中，按一下&#x200B;**[!UICONTROL 編輯內容]按鈕**。

   ![編輯內容按鈕](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-action-edit-content-button.png)

1. 在下一個畫面，根據您擁有的行動裝置，選取[!DNL iOS™]或[!DNL Android™]索引標籤以設定您的內容。

>[!BEGINTABS]

>[!TAB iOS]

![iOS索引標籤](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-ios-tab.png)

>[!TAB Android]

![Android索引標籤](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-android-tab.png)

>[!ENDTABS]

#### 4.2.3.1 [!UICONTROL 撰寫訊息]區段

1. **撰寫您的訊息：**&#x200B;請隨意新增您想要的任何文字。 以下是您可以使用的範例：

   * 標題： `Get 10% off today!`
   * 內文： `Today only! Get 10% off on your House Blend coffee purchase!`

     ![撰寫訊息](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-compose-message.png)

#### 4.2.3.2將訊息的點按行為變更為&#x200B;**開啟產品頁面**

1. 在&#x200B;**[!UICONTROL 點選行為]**&#x200B;區段中，從&#x200B;**[!UICONTROL 內文點選行為]**&#x200B;下拉式清單中選取&#x200B;**[!UICONTROL 深層連結]**。

1. 將下列URL複製並貼到&#x200B;**URL欄位**&#x200B;中：

   `dxdemo://exoticVibes`

   ![深層連結](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-deeplink.png)

#### 4.2.3.3新增影像至訊息

1. 在&#x200B;**[!UICONTROL 新增媒體]**&#x200B;區段中，按一下&#x200B;**[!UICONTROL 新增媒體]**。

   ![新增媒體按鈕](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-3-3-add-media-buttons.png)

1. 在&#x200B;**[!UICONTROL 選取Assets]**&#x200B;畫面上，在左側導覽中開啟&#x200B;**Fréscopa資料夾**，並從該資料夾中選取影像。

   例如︰`HouseBlend.png`

1. 按一下影像，然後按一下&#x200B;**[!UICONTROL 選取]按鈕**，將影像新增至推播通知。

   ![選取影像](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-3-3-select-image.png)

   >[!SUCCESS]
   >
   > 1. 在預覽畫面上，按一下&#x200B;**[!UICONTROL 展開檢視]**。
   > 1. 預覽您的訊息。
   > <br>
   >
   > ![展開檢視](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-3-expand-view.png)

### 額外練習

如果您已完成這部分的練習，但仍有一些時間，請嘗試附加練習：

+++ 額外練習

#### 新增收件者的名字，個人化您傳送的訊息

1. 按一下&#x200B;**內文**&#x200B;欄位旁的&#x200B;**[!UICONTROL 個人化對話方塊]**。

   ![個人化按鈕](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-personalization-button.png)

1. 在&#x200B;**個人化對話方塊**&#x200B;畫面上，將游標放在您要新增文字名字的位置。

1. 請確定已在左側導覽中選取&#x200B;**設定檔屬性**。

   ![設定檔屬性](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-personalize-body-profile-attributes.png)

1. 在&#x200B;**搜尋欄位**&#x200B;中，搜尋： `first name`。

1. 按一下&#x200B;**名字（設定檔屬性>人員>全名）**&#x200B;旁的&#x200B;**+**，將個人化欄位新增至您的文字。

   ![搜尋名字](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-personalize-search-first-name.png)

   >[!SUCCESS]
   >
   > 以下是您文字的外觀：
   > 
   >![Personalization Token](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-personalization-token.png)

1. 按一下&#x200B;**[!UICONTROL 儲存]**&#x200B;以儲存個人化。


   >[!SUCCESS]
   >
   > 1. 在預覽畫面上，按一下&#x200B;**[!UICONTROL 展開檢視]**。
   > 1. 預覽您的訊息。
   > 
   > ![展開檢視](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-3-expand-view.png)

+++

### 4.2.4.檢閱並啟用

如果您對訊息內容感到滿意，可以啟用訊息：

1. 按一下&#x200B;**[!UICONTROL 檢閱以啟動]**。

   ![檢閱及啟動按鈕](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-4-review-and-activate-button.png)

1. 在&#x200B;**[!UICONTROL 檢閱以啟動]**&#x200B;畫面上，按一下&#x200B;**[!UICONTROL 啟動]**。

   ![檢閱以啟動熒幕](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-4-review-to-activate.png)

>[!SUCCESS]
> 在&#x200B;**行銷活動概觀頁面**&#x200B;上，尋找您的行銷活動並檢查狀態。
>
> ![行銷活動狀態](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-push-completed.png)
> 
> 狀態從處理變更為即時，再變更為已完成 — 這可能需要幾分鐘的時間。
> 一旦狀態變更為完成：
>
> ![推送結果](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-push-notification-result.png)

## 其他資源

**操作說明影片：**

* [設定和傳送推播行銷活動](/help/channels/create-a-push-campaign.md)

**產品檔案：**

* [開始使用推播通知](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/get-started-push)
* [建立推播通知](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/create-push)
* [設計推播通知](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/design-push)
* [檢查並傳送推播通知](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/send-push)
