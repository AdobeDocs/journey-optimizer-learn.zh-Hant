---
title: 建立忠誠度狀態歡迎電子郵件 - 挑戰
description: 建立歷程，當客戶達到忠誠度層級時，自動傳送歡迎電子郵件給客戶。
jira: KT-8109
feature: Journeys
role: User
level: Beginner
last-substantial-update: 2023-02-01T00:00:00Z
exl-id: 6fd58b8e-7178-495d-a85d-eb67fc4f3acf
source-git-commit: 7861e0ca17a616273f5ea1b4d850310f1f4ec8b8
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 100%

---

# 建立忠誠度狀態歡迎電子郵件 - 挑戰

| 挑戰 | 建立忠誠度狀態歡迎電子郵件 |
|---|---|
| 角色 | Journey Manager |
| 所需技能 | <ul><li>[建立區段](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html?lang=zh-Hant)</li> <li>[區段資格](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment-qualification.html?lang=zh-Hant)</li><li>[匯入 HTML 內容](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/import-and-author-html-email-content.html?lang=zh-Hant)</li></ul> |
| 要下載的資產 | [StatusUpgradeEmail.zip](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip) |

{style="table-layout:auto"}

## 故事

Luma 提供忠誠計畫，作為吸引及留住客戶的方式。 該計畫提供四個不同的等級：銅、銀、金和白金。 每個忠誠度等級都會獲得不同的獎勵、折扣和其他特殊獎勵，作為對其重複消費的獎勵。

為了強調特殊的白金層級，Luma 希望在客戶達到白金層級時，向他們傳送歡迎電子郵件。 

## 您的挑戰

系統已要求您設定歷程，當客戶達到白金級忠誠度時，會自動傳送歡迎電子郵件給客戶。

>[!BEGINTABS]

>[!TAB 工作]

當忠誠客戶符合白金層級資格時，他們應該會收到一封電子郵件，祝賀並告知他們新的權益。創意團隊已提供附有電子郵件內容的 HTML 檔案 **[Luma - 狀態升級 - 歡迎電子郵件](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip)**。

1. 在 Journey Optimizer 建立一個名為`Luma - platinum status`的[!UICONTROL 區段]。

1. 建立名為`Luma - New Status - platinum`的歷程。

   1. 當客戶符合白金忠誠度層級資格時，即會進入歷程。

   1. 客戶應會收到標示為`Luma - Platinum Status - Welcome`的電子郵件，主旨列為`Welcome to Platinum Status, {firstName}!`以及創意團隊提供的電子郵件內文。 這是[!UICONTROL 異動]電子郵件。

   1. 上傳 HTML 檔案時，您會注意到電子郵件指的是「鑽石」狀態，而非「白金」。 請更新[!UICONTROL 電子郵件設計工具]中的電子郵件，而不必向創意團隊請求新檔案。

>[!TAB 成功標準]

測試您的歷程:

1. 請確保[!UICONTROL 閱讀區段活動]的[!UICONTROL 命名空間]已設為&#x200B;**[!DNL Luma CRM id(lumaCrmId)]**。

1. 覆寫預設的[!UICONTROL 電子郵件參數]，並將其設定為您自己的電子郵件地址:
   * 在&#x200B;**[!UICONTROL 電子郵件參數]**&#x200B;中，按一下 T 符號 (啟用參數覆寫)。

   * 按一下&#x200B;**[!UICONTROL 地址]**&#x200B;欄位。

   * 在下一個畫面的運算式編輯器中，新增您的電子郵件地址：`"yourname@yourdomain"`，並加上括弧，然後按一下&#x200B;**[!UICONTROL 確定]**。

1. 將歷程設為測試模式。

1. 選取&#x200B;**[!UICONTROL 觸發事件]**。

1. 將以下`CRM ID` for `Stanleigh Stooke`加入至&#x200B;**[!UICONTROL 設定檔識別碼]**&#x200B;欄位：`4f34057d9d9e792c28ba18ecae378e98`

**結果：**&#x200B;您應會收到個人化 *Luma - 白金狀態 - 歡迎*&#x200B;電子郵件。

這是電子郵件的外觀：

![Luma - 狀態升級 - 歡迎電子郵件](/help/challenges/assets/status-upgrade-welcome-email.png)

>[!TAB 檢查您的工作]

區段可能會以這種方式呈現：

![Luma - 白金狀態 - 區段](/help/challenges/assets/segment-luma-platinum-status.png)

以下是您歷程的外觀：

![platinum-status-upgrade-journey](/help/challenges/assets/journey-luma-status-upgrade.png)

>[!ENDTABS]
