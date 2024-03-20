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
source-git-commit: c590b47ad3dfc54badbac0d8fcaff6b9dd053cc1
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

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

1. 在Journey Optimizer的左側導覽列中的 **[!UICONTROL 歷程管理]** 區段，選取 **行銷活動**.

1. 按一下 **[!UICONTROL 建立行銷活動]**.

   ![建立行銷活動](/help/summit/l820-lab-workbook/assets/2-3-1-1-create-campaign.png)

1. 在 **[!UICONTROL 建立行銷活動]** 頁面，在  **[!UICONTROL 動作]** 區段，選取 **[!UICONTROL 推播通知]** 核取方塊。

1. 從 **[!UICONTROL 應用程式表面]** 下拉式清單，選取 *[!DNL Frecopa-Push]*.

1. 按一下 **[!UICONTROL 建立]** 以建立推播行銷活動。

   ![應用程式表面](/help/summit/l820-lab-workbook/assets/2-3-1-2-app-surface.png)

>[!SUCCESS]
>
>您現在應該在Campaign屬性頁面上：
> ![行銷活動屬性](/help/summit/l820-lab-workbook/assets/2-3-1-2-campaign-properties.png)

## 練習4.2 — 設定行銷活動

您可以在此頁面上設定行銷活動的屬性、對象、動作和排程。

### 4.2.1 [!UICONTROL 屬性區段]

為行銷活動命名。 請務必以您的座位編號作為名稱開頭，以便在搜尋時輕鬆找到您的促銷活動。

例如，如果您的座位數為99： `99 - 10% Discount Campaign`.

### 4.2.2 **[!UICONTROL 對象區段]**

1. 在對象區段中，按一下 **[!UICONTROL 選取對象]**.

   ![對象區段](/help/summit/l820-lab-workbook/assets/2-3-2-5-audience-section.png)

1. 在 **[!UICONTROL 選取對象]** 畫面，搜尋對象：

   **實驗室 — 座位`your seat number`**

1. 選取對象，然後按一下 **[!UICONTROL 儲存]**.

   ![對象選擇](/help/summit/l820-lab-workbook/assets/2-3-2-7-select-audience.png)

### 4.2.3編輯推播通知的內容

在本練習中，您將設計和自訂推播通知。

1. 在 **[!UICONTROL 動作]** 區段，按一下 **[!UICONTROL 編輯內容] 按鈕**.

   ![編輯內容按鈕](/help/summit/l820-lab-workbook/assets/2-3-action-edit-content-button.png)

1. 在下一個畫面，根據您擁有的行動裝置，選取 [!DNL iOS™] 或 [!DNL Android™] 索引標籤來設定您的內容。

>[!BEGINTABS]

>[!TAB iOS]

![iOS索引標籤](/help/summit/l820-lab-workbook/assets/2-3-ios-tab.png)

>[!TAB Android]

![Android索引標籤](/help/summit/l820-lab-workbook/assets/2-3-android-tab.png)

>[!ENDTABS]

#### 4.2.3.1 [!UICONTROL 撰寫訊息] 區段

1. **撰寫訊息：** 歡迎您新增任何想要的文字。 以下是您可以使用的範例：

   * 標題： `Get 10% off today!`
   * 內文： `Today only! Get 10% off on your House Blend coffee purchase!`

     ![撰寫訊息](/help/summit/l820-lab-workbook/assets/2-3-compose-message.png)

#### 4.2.3.2將訊息的點按行為變更為 **開啟產品頁面**

1. 在 **[!UICONTROL 點按行為]** 區段，選取 **[!UICONTROL 深層連結]** 從 **[!UICONTROL 內文點按行為]** 下拉式清單。

1. 將下列URL複製並貼到 **url欄位**：

   `dxdemo://exoticVibes`

   ![深層連結](/help/summit/l820-lab-workbook/assets/2-3-deeplink.png)

#### 4.2.3.3新增影像至訊息

1. 在 **[!UICONTROL 新增媒體]** 區段，按一下 **[!UICONTROL 新增媒體]**.

   ![新增媒體按鈕](/help/summit/l820-lab-workbook/assets/2-3-3-3-add-media-buttons.png)

1. 在 **[!UICONTROL 選取資產]** 畫面，在左側導覽列中，開啟 **Fréscopa資料夾** 並從該資料夾中選取影像。

   例如︰`HouseBlend.png`

1. 按一下影像，然後按一下 **[!UICONTROL 選取] 按鈕** 以將影像新增至推播通知。

   ![選取影像](/help/summit/l820-lab-workbook/assets/2-3-3-3-select-image.png)

   >[!SUCCESS]
   >
   > 1. 在預覽畫面上，按一下 **[!UICONTROL 展開檢視]**.
   > 1. 預覽您的訊息。
   > <br>
   >
   > ![展開檢視](/help/summit/l820-lab-workbook/assets/2-3-3-expand-view.png)

### 額外練習

如果您已完成這部分的練習，但仍有一些時間，請嘗試附加練習：

+++ 額外練習

#### 新增收件者的名字，個人化您傳送的訊息

1. 按一下 **個人化對話方塊** 在 **[!UICONTROL 內文]** 欄位。

   ![個人化按鈕](/help/summit/l820-lab-workbook/assets/2-3-personalization-button.png)

1. 在 **個人化對話方塊** 熒幕上，將游標放在您要新增文字名字的位置。

1. 確保 **設定檔屬性** 都會在左側導覽中選取。

   ![設定檔屬性](/help/summit/l820-lab-workbook/assets/2-3-personalize-body-profile-attributes.png)

1. 在 **搜尋欄位**，搜尋： `first name`.

1. 按一下 **+** 在 **名字（「設定檔屬性」>「人員」>「全名」）** 將個人化欄位新增至您的文字。

   ![搜尋名字](/help/summit/l820-lab-workbook/assets/2-3-personalize-search-first-name.png)

   >[!SUCCESS]
   >
   > 以下是您文字的外觀：
   > 
   >![個人化權杖](/help/summit/l820-lab-workbook/assets/2-3-personalization-token.png)

1. 按一下 **[!UICONTROL 儲存]** 以儲存個人化。


   >[!SUCCESS]
   >
   > 1. 在預覽畫面上，按一下 **[!UICONTROL 展開檢視]**.
   > 1. 預覽您的訊息。
   > 
   > ![展開檢視](/help/summit/l820-lab-workbook/assets/2-3-3-expand-view.png)

+++

### 4.2.4.檢閱並啟用

如果您對訊息內容感到滿意，可以啟用訊息：

1. 按一下 **[!UICONTROL 檢閱以啟動]**.

   ![檢閱並啟動按鈕](/help/summit/l820-lab-workbook/assets/2-3-4-review-and-activate-button.png)

1. 在 **[!UICONTROL 檢閱以啟動]** 熒幕，按一下 **[!UICONTROL 啟動]**.

   ![檢閱以啟動畫面](/help/summit/l820-lab-workbook/assets/2-3-4-review-to-activate.png)

>[!SUCCESS]
> 在 **行銷活動概觀頁面**，尋找您的行銷活動並檢查狀態。
>
> ![行銷活動狀態](/help/summit/l820-lab-workbook/assets/2-3-push-completed.png)
> 
> 狀態從處理變更為即時，再變更為已完成 — 這可能需要幾分鐘的時間。
> 一旦狀態變更為完成：
>
> ![推送結果](/help/summit/l820-lab-workbook/assets/2-3-push-notification-result.png)


**感謝您！**

感謝您的參與。 請完成Summit應用程式中的Lab 820會議問卷調查，提供意見反應，說明我們的做法以及實驗室是否符合您的期望。

