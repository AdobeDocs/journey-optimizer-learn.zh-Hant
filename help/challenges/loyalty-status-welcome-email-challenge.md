---
title: 建立忠誠度狀態歡迎電子郵件 — 挑戰
description: 瞭解在歷程畫布中建立歷程的基本概念。
kt: 8109
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: 6fd58b8e-7178-495d-a85d-eb67fc4f3acf
source-git-commit: 758d0af0a93f110fd1692d8b0c364a3bbdac7494
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 4%

---

# 建立忠誠度狀態歡迎電子郵件 — 挑戰

![忠誠度狀態歡迎電子郵件 — 質詢橫幅](/help/challenges/assets/email-assets/luma-transactional-onboarding-1.png)

| 挑戰 | 建立忠誠度狀態歡迎電子郵件 |
|---|---|
| 角色 | Journey Manager |
| 所需技能 | <ul><li>[建立區段](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html)</li> <li>[區段資格](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment-qualification.html)</li><li>[匯入HTML內容](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-emails/import-and-author-html-email-content.html)</li></ul> |
| 要下載的資產 | [platinumStatusEmail.zip](/help/challenges/assets/email-assets/platinumStatusEmail.zip) |

## 故事

Luma提供忠誠計畫，作為吸引及留住客戶的方式。 該計畫提供四個不同級別：銅、銀、金和鉑。 每個忠誠度等級會獲得不同的等級或獎勵、折扣和其他特殊獎勵，作為對其重複業務的獎勵。

強調特殊白金狀態。 Luma想要在客戶達到白金級時，傳送歡迎電子郵件給客戶。

## 您的挑戰

系統已要求您設定歷程，當客戶達到白金級忠誠度時，會自動傳送歡迎電子郵件給客戶。

>[!BEGINTABS]

>[!TAB 工作]

當忠誠客戶符合白金級資格時，他們應會收到並寄送電子郵件，祝賀並告知他們新的優點。 創意團隊已提供HTML檔案 **[Luma — 狀態升級 — 歡迎電子郵件](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip)** 郵件內文。

1. 建立 [!UICONTROL 區段] 在Journey Optimizer `Luma – status upgrade`.
2. 建立以下歷程： `Luma – New Status – platinum`.
   1. 客戶符合白金忠誠度等級資格時，即會進入歷程。
   2. 客戶應會收到標示為 `Luma – Platinum Status - Welcome`，並搭配主旨行 `Welcome to Platinum Status, (recipient's first name)!` 創意團隊提供的電子郵件內文。
   3. 上傳HTML檔案時，您注意到電子郵件是指「鑽石」狀態，而非「白金」。 請更新電子郵件設計工具中的電子郵件，而不是向創意團隊請求新檔案。

>[小費！]
> 確定Luma — 白金狀態 — 歡迎電子郵件為[!UICONTROL 異動].


>[!TAB 成功標準]

測試您的歷程:

1. 請確定 [!UICONTROL 閱讀區段活動] 有 [!UICONTROL 命名空間] 設為 **[!DNL Luma CRM id(lumaCrmId)]**
2. 覆寫預設值 [!UICONTROL 電子郵件參數] 並將其設定為您自己的電子郵件地址

+++ 按一下這裡以取得如何覆寫 [!!UICONTROL電子郵件參數].
   * 按一下眼睛符號來顯示隱藏的值。
   * 在 [!UICONTROL 電子郵件參數]，按一下T符號（啟用參數覆蓋）

   ![覆寫電子郵件參數](/help/challenges/assets/c3-override-email-paramters.jpg)

   * 按一下 [!UICONTROL 地址欄位]
   * 在下一個畫面中，以括弧新增您的電子郵件地址： `"yourname@yourdomain"` 在運算式編輯器中，按一下「確定」。
+++


3. 將歷程設為測試模式
4. 觸發事件
5. 新增下列項目 [!DNL CRM ID] for [!DNL Stanleigh Stooke] 進入 [!UICONTROL 設定檔識別碼] 欄位： `4f34057d9d9e792c28ba18ecae378e98`

您應會收到個人化 *Luma — 白金狀態 — 歡迎* 電子郵件。

>[!TAB 檢查您的工作]

以下是您歷程的外觀：

![platinum-status-upgrade-journey](/help/challenges/assets/journey-luma-status-upgrade.png)


這是電子郵件的外觀：

![Luma — 狀態升級 — 歡迎電子郵件](/help/challenges/assets/status-upgrade-welcome-email.png)

>[!ENDTABS]
