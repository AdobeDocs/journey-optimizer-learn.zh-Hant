---
title: 設定訓練沙箱 - 簡介
description: 瞭解如何設定沙箱以供訓練之用。 逐一完成設定方案、擷取範例資料和建立事件所需的步驟。
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
jira: KT-9382
role: Admin
level: Beginner
last-substantial-update: 2023-02-01T00:00:00Z
exl-id: 8fa673de-9be9-4ab2-94cf-cfa8ac518223
source-git-commit: 81f5cc22d46f89ee1c7164a92988311ca6036b8b
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 100%

---

# 設定訓練沙箱 - 簡介和先決條件

![橫幅教學課程 - 設定訓練沙箱](./assets/ajo-banner-configure-training-sandbox.png)

本教學課程專為負責提供 Adobe [!DNL Journey Optimizer]訓練環境的管理員及資料工程師所設計。瞭解設定方案、擷取範例資料和建立事件所需的步驟。 您也可以建立三個測試設定檔，讓學習者檢查其工作。

提供的範例資料以一家名為&#x200B;_[!DNL Luma]_的虛構運動服裝公司為基礎。[!DNL Luma]在多個國家/地區設有商店、線上網站以及行動應用程式。 [!DNL Luma] 使用 Adobe Journey Optimizer 來為客戶提供連結、情境式和個人化的體驗。

在本教學課程結束時，您將擁有一個支援 [Journey Optimizer 挑戰](/help/challenges/introduction-and-prerequisites.md)區段的實作練習中介紹的[!DNL Luma]範例沙箱。

## 先決條件

開始設定訓練沙箱之前，請確定您具備：

1. 專屬開發[沙箱](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/access-control/create-and-manage-sandboxes.html?lang=zh-Hant)。

1. [電子郵件訊息預設集](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/set-up-email-channel.html?lang=zh-Hant)已針對行銷及異動訊息設定。

1. **[!UICONTROL 歷程管理員]**&#x200B;和&#x200B;**[!UICONTROL 資料管理員]**&#x200B;訓練沙箱的權限。

1. 您的[組織 ID](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=zh-Hant)。

1. 包含範例資料的 JSON 檔案，已設定至您的 Journey Optimizer 執行個體：

   1. 在此處](/help/tutorial-configure-a-training-sandbox/assets/luma-data/luma-sample-data.zip)下載該`luma-sample-data.zip`檔案[，其中包含本教學課程所需的所有 JSON 檔案。

   1. 從下載資料夾中，將`luma-data.zip`檔案移至您電腦的所需位置，然後加以解壓縮。

      這些檔案包含訓練沙箱的範例資料。

   1. 開啟每個檔案並查找&#x200B;**`yourOrganizationID`**，然後將其替換為[組織 ID](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=zh-Hant)。

   1. 儲存檔案。

## 我們開始吧

從[手動資料設定](/help/tutorial-configure-a-training-sandbox/manual-data-set-up.md)開始。

在此步驟中，您會定義所需的資料結構。 完成資料設定後，您可以將資料內嵌至沙箱，然後設定事件。
