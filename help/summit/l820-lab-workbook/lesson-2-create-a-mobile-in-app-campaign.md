---
title: 第2課 — 建立行動應用程式內行銷活動
description: 建立並觸發行動應用程式內行銷活動。
feature: In App
role: User
level: Intermediate
doc-type: Article
duration: 0
recommendations: noDisplay, noCatalog
jira: KT-14983
thumbnail: KT-14983.jpeg
exl-id: fe18eca7-229c-4867-ab34-1862bad63124
source-git-commit: befde57252ebc12c5d6df31fde8078e4535d1261
workflow-type: tm+mt
source-wordcount: '1433'
ht-degree: 1%

---

# 第2課 — 建立行動應用程式內行銷活動

在本課程中，您將建立並觸發行動應用程式內訊息。

## 學習目標

* 瞭解應用程式內訊息的觸發方式。
* 瞭解如何建立行動應用程式內行銷活動。
* 觸發應用程式內訊息。

## 練習2.1 — 登入Journey Optimizer

1. 開啟 [Adobe Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-ajo-lab/journey-optimizer/home){target="_blank"}
2. 使用下列詳細資料登入：
   <br>
   **使用者名稱：** L820+**`<your seat number>`**@adobeeventlab.com
   **密碼：**   Adobe2024！
   <br>
您可以在實驗室機器案頭上找到登入的詳細資料。 使用Adobe ID和密碼。
   ![案頭](/help/summit/l820-lab-workbook/assets/desk-top.png)

   ![登入畫面](/help/summit/l820-lab-workbook/assets/2-1-1-ajo-sign-in.png)
   <br>
3. 您可以略過下列兩個畫面：
   <br>
   ![電話號碼](/help/summit/l820-lab-workbook/assets/2-1-3-ajo-add-phone.png)
   <br>
   ![個人化快顯視窗](/help/summit/l820-lab-workbook/assets/2-1-4-ajo-personalization-pop-up.png)


>[!SUCCESS]
>
>您應該登入Journey Optimizer並在首頁上：
>
>![ajo首頁](/help/summit/l820-lab-workbook/assets/2-1-5-ajo-homepage.png)


## 練習2.2建立行動應用程式內行銷活動

在本練習中，您會建立應用程式內傳訊行銷活動，此活動會在您開啟應用程式時觸發。

1. 在Journey Optimizer的左側導覽區中選取「 」 **[!UICONTROL 行銷活動]**.

1. 按一下 **[!UICONTROL 建立行銷活動]**.

   ![建立行銷活動](/help/summit/l820-lab-workbook/assets/2-3-1-1-create-campaign.png)

1. 在 **[!UICONTROL 建立行銷活動]** 頁面，在  **[!UICONTROL 動作]** 區段，選取 **[!UICONTROL 應用程式內訊息]** 核取方塊。

1. 從 **[!UICONTROL 傳送至]** 下拉式清單，選取 **[!DNL Mobile]**.

1. 從 **[!UICONTROL 應用程式表面]** 下拉式清單，選取 **[!DNL Frecopa Mobile App]**.

1. 按一下&#x200B;**[!UICONTROL 建立]**。

   ![應用程式表面](/help/summit/l820-lab-workbook/assets/3-1-1-1-create.png)

>[!SUCCESS]
>
>您現在應該位於行銷活動屬性上：
>
> ![行銷活動屬性](/help/summit/l820-lab-workbook/assets/3-1-1-2-campaign-properties.png)

## 練習2.3設定行銷活動

### 2.3.1 [!UICONTROL 屬性區段]

為行銷活動命名。 請務必以您的座位編號作為名稱開頭，以便輕鬆找到您的促銷活動。

例如，如果您的座位數為99：  `99 - Welcome Campaign`.

![屬性區段](/help/summit/l820-lab-workbook/assets/3-1-2-1-properties-section.png)

### 2.3.2設定自訂觸發規則

1. 向下捲動至 **[!UICONTROL Triggers區段]**，然後按一下 **[!UICONTROL 編輯觸發程式]**.

   ![修改](/help/summit/l820-lab-workbook/assets/3-2-1-2-edit-triggers.png)

1. 在規則產生器中，按一下 **[!UICONTROL 應用程式啟動]** 並從下拉式清單中選取  *已將資料傳送至Platform*.
   ![已傳送至資料平台](/help/summit/l820-lab-workbook/assets/trigger-drop-down-sent-to-platform.png)

1. 按一下以新增條件 **[!UICONTROL 新增條件]**.

   ![新增條件按鈕](/help/summit/l820-lab-workbook/assets/3-2-1-3-add-condition.png)

1. 從 **[!UICONTROL 選取特徵]** 下拉式清單，選取 **[!UICONTROL XDM事件型別]**.

   ![XDM事件型別](/help/summit/l820-lab-workbook/assets/4-1-2-dropdown-xdm-event.png)

1. 在下列文字欄位中，新增 *`<custom string value>`* 您可以記住的資訊。

1. 若要儲存值，請按一下**[!UICONTROL 新增**] `<custom string value>`.

   此自訂字串值稍後會用來觸發您的訊息。

   >[!TIP]
   > 將座位編號新增至自訂字串值，讓您擁有專屬名稱且更容易記憶。
   > 
   > 例如︰`99exerciseTrigger`

   ![新增自訂觸發字串值](/help/summit/l820-lab-workbook/assets/3-1-2-2-add-custom-trigger.png)

1. 按一下 **[!UICONTROL 完成]** 右上角。

>[!SUCCESS]
>
>您現在已使用自訂觸發事件定義應用程式內訊息。
>
>![已定義自訂觸發器的行銷活動](/help/summit/l820-lab-workbook/assets/3-1-2-2-campaign-with-custom-trigger.png)


### 2.3.3編輯應用程式內訊息的內容

在 **[!UICONTROL 動作]** 區段，按一下 **[!UICONTROL 編輯內容]**.

![編輯內容按鈕](/help/summit/l820-lab-workbook/assets/3-1-3-1-edit-content-button.png)

此 [!UICONTROL 應用程式內訊息] 編輯器會隨即顯示，您可在此處設定應用程式內訊息內容。

#### 2.3.3.1版面

選取應套用至訊息的配置。

例如，按一下 **[!UICONTROL 強制回應]** 將應用程式內訊息設為模組配置。

![強制回應按鈕](/help/summit/l820-lab-workbook/assets/3-1-3-2-modal-button.png)

#### 2.3.3.2撰寫訊息並發佈行銷活動

1. 在媒體區段中，貼入下列URL：  `https://t3.ftcdn.net/jpg/02/79/42/52/240_F_279425217_Hr9VBkknMr4fTpuZbxZXfcYdC7jSvGl2.jpg`
   <br>
當您按一下離開值欄位時，您的影像應該會出現。

   ![預覽中顯示的媒體](/help/summit/l820-lab-workbook/assets/3-1-3-2-media.png)

2. 在以下內容中 **[!UICONTROL 內容]** 區段，新增您自己的自訂文字，以便在訊息中顯示您的 **[!UICONTROL 頁首]** 和 **[!UICONTROL 內文]**.

   ![頁首與內文](/help/summit/l820-lab-workbook/assets/3-1-3-2-content.png)

3. 其他選項：
   1. **按鈕：**

      ![按鈕區段](/help/summit/l820-lab-workbook/assets/3-1-3-2-buttons.png)

      1. 在編輯器的此區段中，您可以透過編輯按鈕文字欄位來自訂CTA按鈕的文字。

      2. 此 **[!UICONTROL 互動事件]** 欄位是用來定義當使用者按下CTA時傳遞至SDK的值。

      3. 此 **[!UICONTROL Target]** 欄位可用來定義您希望CTA將使用者帶往何處。 其中包括URL與深層連結。 例如，您可以將此深層連結新增至產品頁面，例如 `dxdemo://exoticVibes`.

      4. 您可以按下「 」以新增其他按鈕 **[!UICONTROL +新增按鈕]**.

      5. 當訊息中新增第二個按鈕時，您現在可以選擇使用下拉式方塊變更按鈕配置。


   2. **進階格式**

      ![進階格式切換](/help/summit/l820-lab-workbook/assets/3-1-3-2-advanced-formatting-toggle.png)

      啟用此切換將在編輯器中提供額外的自訂選項。

      1. 媒體大小
      1. 字型
      1. Pt大小
      1. 字型顏色
      1. 對齊方式

      ![進階格式選項](/help/summit/l820-lab-workbook/assets/3-1-3-2-advanced-formatting-options.png)

   3. **設定標籤**

      將移至此標籤並在 **[!UICONTROL 預覽]** 區段，您可以變更 **應用程式預覽**.
      <br>\
      ![設定標籤](/help/summit/l820-lab-workbook/assets/3-1-3-1-settings-tab.png)
      <br>

      1. 此 **[!UICONTROL 版面]** 部分提供將影像作為背景或純色的選項。

      2. 此 **[!UICONTROL 訊息]** 區段提供可針對訊息啟用的自訂互動：
         1. 自訂手勢
         2. UI接管
         3. 自訂UI接管
         4. 自訂大小
         5. 自訂位置
         6. 自訂動畫
         7. 訊息圓角
   <br>
4. 當您完成內容的編寫並對您的訊息感到滿意時，請按一下 **[!UICONTROL 檢閱以啟動] 按鈕**.

   >[!SUCCESS]
   >
   > 您現在已完成行動應用程式內訊息的製作。 您現在應該已加入行銷活動 **[!UICONTROL 檢閱以啟動]** 頁面。
   >
   >![檢閱並啟動](/help/summit/l820-lab-workbook/assets/3-1-4-1-review-and-activate.png)
   >
   > 您將在這裡看到訊息的完整摘要。
   >
   > *請記下您用來作為觸發規則的自訂值。 此值將用於引發您的應用程式內訊息。 可在摘要頁面的醒目區域找到使用的值。*

   >[!NOTE]
   >應用程式內訊息的目前觸發器為預設值 **應用程式啟動事件發生**，這表示應用程式啟動時會觸發應用程式內訊息。 您可在以下位置看到此內容： **[!UICONTROL 「排程」段落]**.

5. 如果您已完成檢閱行銷活動，請按下「啟動」按鈕以發佈行銷活動。
   <br>
   ![啟用](/help/summit/l820-lab-workbook/assets/3-1-4-2-activate.png)


>[!SUCCESS]
>
> 您現在應該會看到「行銷活動」控制面板。 透過捲動或使用搜尋功能找到您的行銷活動。 當您的行銷活動將狀態變更為 **[!UICONTROL 即時]** （~1分鐘），您的行銷活動現已發佈。
>
> ![已發佈的行銷活動](/help/summit/l820-lab-workbook/assets/3-1-3-2-published-campaign.png)
>


## 練習2.4觸發行動應用程式內訊息

若要重新整理裝載並下載新發佈的行銷活動：

1. 在您的行動裝置上，完全關閉Fréscopa應用程式。
2. 重新開啟Fréscopa應用程式。
3. 現在，導覽至應用程式上的練習標籤。

   ![練習按鈕](/help/summit/l820-lab-workbook/assets/3-2-3-app-exercise-button.png)

4. 在文字欄位中，輸入您在Campaign中定義的自訂觸發值。 然後按下「提交」。


   ![修改](/help/summit/l820-lab-workbook/assets/3-2-2-1-app-condition.PNG){width="250" align="center" zoomable="yes"}

>[!SUCCESS]
>
>按一下「提交」後，您就會手動觸發觸發器，而您建立的應用程式內通知會彈出：
>
>![應用程式內訊息](/help/summit/l820-lab-workbook/assets/3-1-3-3-in-app-message.png)
>
> *如果您在觸發訊息時發生問題，請檢查下列專案：*
> 
> * *在行動應用程式的「事件名稱」欄位中，確定您輸入的觸發規則值與Campaign中的值完全相同。*
> * *請確定大小寫正確，且沒有開頭和結尾的空格。*
> * *若返回「行銷活動檢閱」頁面，按一下「行銷活動控制面板」上的「返回行銷活動」 ，即可查詢您所使用的觸發規則值。*

您剛才已撰寫並發佈第一個Journey Optimizer應用程式內訊息！


## 額外練習：複製裝置上的行銷活動和預覽

此 **複製行銷活動** 和 **在裝置上預覽** 功能是立即可用功能，可讓您複製行銷活動，並直接在裝置上測試及檢閱應用程式內訊息，然後再啟用。 在本練習中，您將學習如何使用此功能並預覽您在練習3.1中建立的訊息。

1. 按一下「行銷活動」控制面板頁面中的行銷活動名稱，開啟您剛才建立的行銷活動，以開啟行銷活動。 這會將您帶回 **[!UICONTROL 檢閱行銷活動]** 頁面。
1. 按下 **[!UICONTROL 「複製」按鈕]**. 這將會開啟新的提示，為您正在複製的新行銷活動命名。 新增容易記住或使用預設名稱的新名稱，其中 **[!DNL _copy]** 預設會新增。

   ![複製行銷活動](/help/summit/l820-lab-workbook/assets/3-2-duplicate-campaign.png)

1. 按下「重複」按鈕後，就會建立您的重複行銷活動，且您會回到「行銷活動控制面板」。
1. 複製行銷活動後，請開啟新的行銷活動。

1. 您可以存取裝置上的預覽功能。 **[!UICONTROL 行銷活動評論]** 頁面或 **[!UICONTROL 行銷活動作者]** 步驟。

   ![在裝置上預覽按鈕](/help/summit/l820-lab-workbook/assets/3-3-1-1-preview-on-device-button.png)
   <br>

1. 接下來，按一下 **[!UICONTROL 開始按鈕]** 從「連線至裝置」畫面。

   ![開始按鈕](/help/summit/l820-lab-workbook/assets/3-3-1-2-connect-to-device-start.png)
   <br>

1. 輸入已設定為啟動Fréscopa應用程式的基底URL： `dxdemo://`

   ![預覽url](/help/summit/l820-lab-workbook/assets/3-3-1-3-preview-url.png)

   <br>

1. 請依照畫面上的指示操作：
   1. 使用行動裝置掃描QR碼，Fréscopa應用程式就會開啟，畫面會讓您輸入顯示的圖釘。
   2. 在裝置的「保證」畫面上，輸入AJO中顯示的pin，然後按一下「連線」按鈕，當您輸入pin後，此按鈕就會出現在右下方。


   ![輸入圖釘](/help/summit/l820-lab-workbook/assets/3-3-1-5-enter-pin.PNG){width="250" align="center" zoomable="yes"}
   <br>
1. 此快顯視窗會顯示在您的電腦熒幕上

   ![快顯視窗](/help/summit/l820-lab-workbook/assets/3-3-pop-up.png)

1. 按一下完成按鈕。 這將會關閉對話方塊，而且您的手機現在已連線到裝置上的預覽。


>[!SUCCESS]
>
> 您的應用程式內訊息會顯示在裝置上。
>
> *連線後，每次按一下「 」時，應用程式內訊息都會顯示。 **[!UICONTROL 在裝置上預覽] 按鈕**.

## 其他資源

**操作說明影片：**

* [建立應用程式內行銷活動](/help/channels/create-an-in-app-campaign.md)
* [撰寫應用程式內訊息](/help/channels/author-in-app-messages.md)

**產品檔案：**

* [開始使用應用程式內頻道](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/get-started-in-app)
* [建立行動應用程式內訊息](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/create-in-app)
* [設計您的應用程式內內容](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/design-in-app)
* [檢查並傳送您的應用程式內通知](/https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/send-in-app)
