---
title: 建立忠誠度狀態歡迎電子郵件 - 挑戰
description: 瞭解在歷程畫布中建立歷程的基本概念。
kt: 8109
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: 6fd58b8e-7178-495d-a85d-eb67fc4f3acf
source-git-commit: 7a178b9c523ead0cf27aaa87d25b3752ef53f519
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 100%

---

# 建立忠誠度狀態歡迎電子郵件 - 挑戰

![忠誠度狀態歡迎電子郵件 - 挑戰橫幅](/help/challenges/assets/email-assets/luma-transactional-onboarding-1.png)

| 挑戰 | 建立忠誠度狀態歡迎電子郵件 |
|---|---|
| 角色 | Journey Manager |
| 所需技能 | <ul><li>[建立區段](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html?lang=zh-Hant)</li> <li>[區段資格](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment-qualification.html?lang=zh-Hant)</li><li>[匯入 HTML 內容](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-emails/import-and-author-html-email-content.html?lang=zh-Hant)</li></ul> |
| 要下載的資產 | [StatusUpgradeEmail.zip](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip) |

## 故事

Luma 提供忠誠計畫，作為吸引及留住客戶的方式。 該計畫提供四個不同的等級：銅、銀、金和白金。 每個忠誠度等級都會獲得不同的獎勵、折扣和其他特殊獎勵，作為對其重複消費的獎勵。

強調特殊白金等級。 Luma 希望在客戶達成白金級時向他們傳送歡迎電子郵件。

## 您的挑戰

系統已要求您設定歷程，當客戶達到白金級忠誠度時，會自動傳送歡迎電子郵件給客戶。

>[!BEGINTABS]

>[!TAB 工作]

當忠誠客戶符合白金級資格時，他們應會收到並傳送電子郵件，祝賀並告知他們新的福利。 創意團隊已提供 HTML 檔案 **[Luma – 狀態升級 – 歡迎電子郵件](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip)** 郵件內文。

1. 在 Journey Optimizer 建立一個名為`Luma – status upgrade`的[!UICONTROL 區段]。
2. 建立名為`Luma – New Status – platinum`的歷程。
   1. 當客戶符合白金忠誠度等級資格時，即會進入歷程。
   2. 客戶應會收到標示為`Luma – Platinum Status - Welcome`的電子郵件，主旨列為`Welcome to Platinum Status, (recipient's first name)!`以及創意團隊提供的電子郵件內文。 這是[!UICONTROL 異動]電子郵件。
   3. 上傳 HTML 檔案時，您會注意到電子郵件指的是「鑽石」狀態，而非「白金」。 請更新電子郵件設計工具中的電子郵件，而不是向創意團隊請求新檔案。

>[!TAB 成功標準]

測試您的歷程:

1. 請確定[!UICONTROL 閱讀區段活動]的[!UICONTROL 命名空間]設為&#x200B;**[!DNL Luma CRM id(lumaCrmId)]**
2. 覆寫預設的[!UICONTROL 電子郵件參數]，並將其設定為您自己的電子郵件地址
   * 按一下眼睛符號來顯示隱藏的值。
   * 在[!UICONTROL 電子郵件參數]，按一下 T 符號 (啟用參數覆寫)

       ![覆寫電子郵件參數](/help/challenges/assets/c3-override-email-paramters.jpg)
   
   * 按一下[!UICONTROL 地址欄位]
   * 在下一個畫面中，以括弧新增您的電子郵件地址： `"yourname@yourdomain"`在運算式編輯器中，按一下「確定」。


3. 將歷程設為測試模式
4. 觸發事件
5. 將以下[!DNL CRM ID]`Stanleigh Stooke`加入至[!UICONTROL 設定檔識別碼]欄位：`4f34057d9d9e792c28ba18ecae378e98`

**結果：**&#x200B;您應會收到個人化 *Luma – 白金狀態 – 歡迎*&#x200B;電子郵件。

>[!TAB 檢查您的工作]

以下是您歷程的外觀：

![platinum-status-upgrade-journey](/help/challenges/assets/journey-luma-status-upgrade.png)


這是電子郵件的外觀：

![Luma – 狀態升級 – 歡迎電子郵件](/help/challenges/assets/status-upgrade-welcome-email.png)

>[!ENDTABS]
