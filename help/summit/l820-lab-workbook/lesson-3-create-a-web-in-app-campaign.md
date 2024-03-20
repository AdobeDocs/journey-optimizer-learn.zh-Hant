---
title: 第3課 — 建立網頁應用程式內行銷活動
description: 建立並觸發網頁應用程式內行銷活動。
feature: In App
role: User
level: Intermediate
doc-type: Article
duration: 0
recommendations: noDisplay, noCatalog
jira: KT-13983
thumbnail: KT-13983.jpeg
source-git-commit: c509c768d07984d07ed2ec65634e000c54bb6ff1
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 0%

---



# 第3課 — 建立網頁應用程式內行銷活動

現在您已建立應用程式的行動體驗，在本課程中，您將建立您在Fréscopa網站上看到的其中一個體驗。 您可以建立網站應用程式內行銷活動。 您可以設計和自訂訊息，並定義觸發訊息的觸發因子。

## 學習目標

* 瞭解如何建立網頁應用程式內行銷活動。
* 觸發應用程式內訊息。

## 練習3.1建立網頁應用程式內行銷活動

在本練習中，您將建立行銷活動，並定義應用程式內訊息會出現在哪個網頁。

1. 在Journey Optimizer的左側導覽列中的 **歷程管理** 選取 **行銷活動**.

1. 按一下 **建立行銷活動**.

   ![CreateCampaign](/help/summit/l820-lab-workbook/assets/4-1-create-campaign.png)

1. 在 **建立行銷活動** 頁面，在 **動作** 區段，選取 **應用程式內訊息** 核取方塊。

1. 從 **傳送至** 下拉式清單，選取 **Web。**

1. 輸入下列URL： **https://dsn.adobe.com/web/adobe-summit-2024/exercise** - *這是您的訊息將會顯示的網頁。*

   ![應用程式內URL](/help/summit/l820-lab-workbook/assets/4-1-1-in-app-url.png)

1. 按一下&#x200B;**[!UICONTROL 建立]**。

## 練習3.2設定您的行銷活動

您可以在此頁面上定義促銷活動的屬性，以及觸發應用程式內訊息出現在網頁中的事件。 將所有其他設定保留為預設值。 進行此練習時，您不需要定義特定對象。

### 3.2.1 [!UICONTROL 屬性區段]

1. 在 **屬性** 區段，為您的行銷活動提供唯一 **名稱**：

   >[!NOTE]
   > 請務必以您的座位編號作為名稱開頭，以便您能輕鬆使用
   > 稍後尋找您的行銷活動。
   > 
   > 例如，如果您的座位數為99： 
   >
   > ![屬性名稱](/help/summit/l820-lab-workbook/assets/4-1-2-properties-name.png)


### 3.2.2設定自訂觸發規則

在此區段中，您可以定義要在網站上顯示訊息的觸發條件。 您可以定義一個唯一觸發器，讓您將訊息只傳送給自己。

1. 向下捲動至 **[!UICONTROL Triggers區段]**，然後按一下 **[!UICONTROL 編輯觸發程式]**.

   ![修改](/help/summit/l820-lab-workbook/assets/3-2-1-2-edit-triggers.png)

1. 在規則產生器中，按一下 **[!UICONTROL 應用程式啟動]** 並從下拉式清單中選取  *已將資料傳送至Platform*.
   ![觸發事件下拉式清單](/help/summit/l820-lab-workbook/assets/trigger-drop-down-sent-to-platform.png)

1. 按一下以新增條件 **[!UICONTROL +新增條件]**.

   ![新增條件按鈕](/help/summit/l820-lab-workbook/assets/3-2-1-3-add-condition.png)

1. 從 **[!UICONTROL 選取特徵]** 下拉式清單，選取 **[!UICONTROL XDM事件型別]**.

   ![XDM事件型別](/help/summit/l820-lab-workbook/assets/4-1-2-dropdown-xdm-event.png)


1. 在下列文字欄位中，新增 *`<custom string value>`* 您可以記住的資訊，然後按下 **[!UICONTROL 新增]** `<custom string value>` 以儲存值。

   此自訂字串值稍後會用來觸發您的訊息。

   >[!TIP]
   > 將座位編號新增至自訂字串值，會使其獨特且更易於記憶。
   > 
   > 例如︰`99web`
   > 

   ![新增自訂觸發字串值](/help/summit/l820-lab-workbook/assets/4-1-2-add-custom-trigger-dropdown.png)

1. 按下 **[!UICONTROL 完成]** 按鈕。

>[!SUCCESS]
>
>您現在已使用自訂觸發事件定義您的網頁應用程式內訊息。
>
>![已定義自訂觸發器的網頁行銷活動](/help/summit/l820-lab-workbook/assets/4-1-2-2-web-campaign-with-custom-trigger.png)


### 3.2.3編輯應用程式內訊息的內容

您可以在此區段中定義訊息的內容、設計和配置。

1. 按一下 **編輯內容** 中的按鈕 **動作** 區段來存取編寫建構。

   ![編輯內容按鈕](/help/summit/l820-lab-workbook/assets/3-1-3-1-edit-content-button.png)

1. 編寫程式與您在上述「行動應用程式內」練習中完成的程式相同。 請花點時間，以您自己的標題、內文和媒體內容自由編輯您的訊息。

   如果您使用模式或全熒幕版面配置，則可新增按鈕。 您可以使用此URL來開啟產品頁面： **https://dsn.adobe.com/web/adobe-summit-2024/P2WsaDPf_**

1. 當您完成訊息編輯時，請按一下 **[!UICONTROL 檢閱以啟動]**.

1. 如果檢閱畫面上的所有專案看起來正常，請按一下 **[!UICONTROL 啟動]** 以發佈您的網頁應用程式內訊息。

1. 您會返回Campaign控制面板。

   等待單元您的行銷活動狀態變更為 **即時** 移至4.1.4之前。

## 練習3.3觸發網頁應用程式內訊息

1. 前往Fréscopa網站並導覽至 **練習** 頁面。

   ![網路練習連結](/help/summit/l820-lab-workbook/assets/4-2-frescopa-web-exercise-link.png)

1. 請務必重新整理網頁。

1. 輸入您在行銷活動中定義的唯一字串值。

   ![練習頁面](/help/summit/l820-lab-workbook/assets/4-2-exercise-page.png)

1. 按一下 **[!UICONTROL 傳送]**.

>[!SUCCESS]
>
>按一下具有唯一值的「傳送」按鈕將會觸發您的網頁應用程式內訊息，進而引發。 而且您應該會在畫面上看到您的網頁應用程式內訊息。
>
>此練習會模擬您透過Fréscopa客戶體驗所看到的自訂XDM傳送事件。
