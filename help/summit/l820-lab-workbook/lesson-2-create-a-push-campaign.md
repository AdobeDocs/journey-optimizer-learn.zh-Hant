---
title: 第2課 — 建立推播行銷活動
description: 檢閱設定檔資料，並瞭解如何在Journey Optimizer中建立推播通知並傳送對象至。
feature: Push
role: User
level: Intermediate
doc-type: Tutorial
duration: 0
recommendations: noDisplay, noCatalog
jira: KT-14980
thumbnail: KT-14980.jpeg
source-git-commit: fa9fbe66fe020dd1cfb21cfabfce541fa9510293
workflow-type: tm+mt
source-wordcount: '818'
ht-degree: 0%

---


# 第2課 — 建立推播行銷活動

在本課程中，您將檢閱您在Frescopa網站上註冊並完成調查時所建立的設定檔和相關設定檔屬性。 然後，您將瞭解如何建立推播行銷活動並傳送訊息。

## 學習目標

* 瞭解設定檔和設定檔屬性
* 瞭解如何建立推播行銷活動
* 瞭解如何設計和個人化推送訊息

## 練習

>[!BEGINTABS]

>[!TAB Excercise 2.1 — 登入Journey Optimizer]

### Excercise 2.1 — 登入Journey Optimizer

1. 開啟 [Adobe Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-ajo-lab/journey-optimizer/home){target="_blank"}
2. 使用下列詳細資料登入：

   **使用者名稱：**   L820+**您的座位號碼**@adobeeventlab.com
   **密碼：**   Adobe2024！

   ![登入畫面](/help/summit/l820-lab-workbook/assets/2-1-1-ajo-sign-in.png)

3. 您可以略過下列兩個畫面：

   ![電話號碼](/help/summit/l820-lab-workbook/assets/2-1-3-ajo-add-phone.png)

   ![個人化快顯視窗](/help/summit/l820-lab-workbook/assets/2-1-4-ajo-personalization-pop-up.png)


>[!SUCCESS]
>
>您應該登入Journey Optimizer並在首頁上：
>
>![ajo首頁](/help/summit/l820-lab-workbook/assets/2-1-5-ajo-homepage.png)

>[!TAB 練習2.2 — 檢閱您的設定檔]

### 練習2.2 — 檢閱您的設定檔

1. 在Adobe Journey Optimizer左側導覽器中，導覽至 **[!UICONTROL 客戶]** -> **[!UICONTROL 設定檔]**.
2. 在 **[!UICONTROL 設定檔]** 概覽頁面，導覽至 [!UICONTROL 瀏覽] 標籤。
3. 從 **[!UICONTROL 身分名稱空間]** 下拉式清單，選取 **[!UICONTROL 電子郵件]**
   ![選取身分名稱空間](/help/summit/l820-lab-workbook/assets/2-2-1-select-identity-namespace.png)
4. 按一下 **[!UICONTROL 設定檔ID]** 存取設定檔資料的連結
   ![設定檔ID](/help/summit/l820-lab-workbook/assets/2-2-2-profiles.png)
5. 在設定檔詳細資訊頁面上：複查資訊：

所有資料都是透過行動網站和行動應用程式收集，並已新增至設定檔。 它可用來個人化您傳送的訊息。

1. 在 **[!UICONTROL 區塊會籍]** 標籤：
   1. 檢查對象會籍
   2. 確認設定檔是以下對象的一部分：

      **Lab-Seat *您的座位號碼*** （例如Lab-Seat）

      ![對象會籍](/help/summit/l820-lab-workbook/assets/2-2-3-audience-membership.png)

>[!NOTE]
>
>在接下來的練習中，您需要坐在實驗席上的受眾。 這可保證您只將推送訊息和應用程式內通知傳送至您自己的裝置。
>
>如果您看到您是位址編號與您的位址不同的對象成員，您可能會收到該位址實驗室出席者的訊息。

>[!TAB 練習2.3 — 建立推播行銷活動]

### 練習2.3 — 建立推播行銷活動

在本練習中，您將建立推播行銷活動、設計和自訂推播通知，並將推播通知傳送至您自己的裝置。

#### 2.3.1 — 建立行銷活動

1. 在Journey Optimizer的左側導覽區中選取「促銷活動」 。
2. 按一下 **[!UICONTROL 建立行銷活動]** 按鈕
   ![建立行銷活動](/help/summit/l820-lab-workbook/assets/2-3-1-1-create-campaign.png)
3. 在 **[!UICONTROL 建立行銷活動]** 頁面，在  **[!UICONTROL 動作]** 區段，選取選**[!UICONTROL 推播通知] 核取方塊
4. 從 **[!UICONTROL 應用程式表面]** 下拉式清單選取 *[!DNL Frecopa-Push]*
5. 按一下 **[!UICONTROL 建立]** 按鈕
   ![應用程式表面](/help/summit/l820-lab-workbook/assets/2-3-1-2-app-surface.png)

>[!SUCCESS]
>
>您現在應該位於行銷活動屬性上：
> ![行銷活動屬性](/help/summit/l820-lab-workbook/assets/2-3-1-2-campaign-properties.png)

#### 2.3.2 — 設定行銷活動

在本節中，您將設定行銷活動的屬性、對象、動作和排程：

##### 1. [!UICONTROL 屬性區段]

![屬性區段](/help/summit/l820-lab-workbook/assets/2-3-1-4-properties-section.png)

1. 為行銷活動命名。 請務必以您的座位編號作為名稱開頭，以便輕鬆找到您的促銷活動。 例如，如果您的座位數為99： `99 - 10% Discount Campaign`.
2. 您也可以新增說明，但本練習並不需要此說明。


##### 2. **[!UICONTROL 對象區段]**

![屬性區段](/help/summit/l820-lab-workbook/assets/2-3-2-5-audience-section.png)

1. 在對象區段中，按一下 **[!UICONTROL 選取對象]** 按鈕。
2. 在 **[!UICONTROL 選取對象]** 畫面，搜尋對象 **實驗室 — 座位`your seat number`**. 您建立的設定檔應該是實驗室對象 [!DNL Frescopa] 指派給。
3. 選取對象並按一下 [!UICONTROL 儲存]

![對象選擇](/help/summit/l820-lab-workbook/assets/2-3-2-7-select-audience.png)

#### 2.3.3。  — 編輯推播通知的內容

1. 在**中[!UICONTROL 動作] 區段，按一下 [!UICONTROL 編輯內容] 按鈕。

在本節中，您將設計和自訂推播通知。

1. 視您擁有的行動裝置而定，選取 [!DNL iOS] 或 [!DNL Android] 索引標籤來設定您的內容。

歡迎您新增任何想要的文字，我們會提供您可使用的範例：

1. 將標題新增至標題欄位：
   `10% today!`
2. 新增內文：
   `Today only! Get 10% off on your House Blend coffee purchase!`
3. 個人化您的內文 — 新增收件者的名字：
   1. 按一下 **個人化對話方塊圖示** 在 **[!UICONTROL 內文]** 欄位
   2. 在**動個人化對話方塊**熒幕上，將游標放在您要新增文字名稱的位置。
   3. 確定 **設定檔屬性** 都會在左側導覽中選取。
   4. 在 **搜尋欄位**，搜尋：
      `first name`
   5. 在中央導覽區中，按一下 **+** 在 **名字（「設定檔屬性」>「人員」>「全名」）** 將個人化欄位新增至您的文字。
   6. 按一下 **[!UICONTROL 儲存]** 按鈕以儲存個人化

   >[!SUCCESS]
   >
   >這是您文字的外觀
   >

4. **[!UICONTROL 點按行為]：**
   1. 選取 **[!UICONTROL 深層連結]** 從 **[!UICONTROL 內文點按行為]** 下拉式清單。
   2. 將下列URL複製並貼到 **url欄位**： `dxdemo://exoticVibes`
5. **[!UICONTROL 新增媒體]：** 按一下 **[!UICONTROL 新增媒體] 按鈕**
   1. 在**上[!UICONTROL 選取資產] 熒幕，向下捲動至Frescopa > Products資料夾並選取影像。
   2. 按一下影像，然後按一下 **[!UICONTROL 選取] 按鈕** 以將影像新增至推播通知。

   >[!SUCCESS]
   >
   > 1. 在預覽畫面上，按一下 **[!UICONTROL 展開檢視]**
   > 2. 預覽您的訊息。
   >

#### 2.3.4。  — 檢閱並啟動

如果您對訊息內容感到滿意，可以啟用訊息：

1. 按一下 **[!UICONTROL 檢閱以啟動] 按鈕**.
2. 在 **[!UICONTROL 檢閱以啟動] 畫面**，按一下 **[!UICONTROL 啟動] 按鈕**.


>[!ENDTABS]
