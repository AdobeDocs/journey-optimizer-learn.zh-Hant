---
title: 設定訓練沙箱 — 簡介
description: 了解如何設定沙箱以供訓練之用。 逐一完成設定結構、擷取範例資料和建立事件所需的步驟。
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
hide: true
exl-id: 8fa673de-9be9-4ab2-94cf-cfa8ac518223
source-git-commit: e377ddb8b84dccd503274caf9ffa3d4c73eedc28
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 9%

---

# 設定訓練沙箱 — 簡介和必要條件

![橫幅教學課程 — 設定訓練沙箱](./assets/ajo-banner-configure-training-sandbox.png)

本教學課程專為負責提供Adobe Journey Optimizer訓練環境的管理員和資料工程師所設計。 了解設定結構、擷取範例資料和建立事件所需的步驟。 您也將建立三個測試設定檔，讓學習者檢查其工作。

提供的樣本資料基於一個虛構的運動服裝公司，該公司稱為 _[!DNL Luma]_. [!DNL Luma] 在多個國家/地區擁有商店、線上網站和行動應用。 [!DNL Luma] 使用 Adobe Journey Optimizer 來為客戶提供連結、情境式和個人化的體驗。

在本教學課程結束時，您會有一個沙箱可支援 [!DNL Luma] 在 [Journey Optimizer挑戰](/help/challenges/introduction-and-prerequisites.md) 區段。

## 先決條件

開始設定訓練沙箱之前，請確定您具備：

1. 專屬開發 [沙箱](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/access-control/create-and-manage-sandboxes.html?lang=en).
1. [電子郵件訊息預設集](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/channel-configuration/set-up-email-channel.html?lang=en) 已針對行銷和交易式訊息設定。
1. **[!UICONTROL 歷程管理員]** 和 **[!UICONTROL 資料管理員]** 訓練沙箱的權限。
1. 您的 [組織ID](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=zh-Hant).
1. 包含範例資料的JSON檔案，已設定至您的Journey Optimizer例項：
   1. 下載 `luma-sample-data.zip` 檔案 [此處](/help/tutorial-configure-a-training-sandbox/assets/luma-data/luma-sample-data.zip)，其中包含本教學課程所需的所有JSON檔案。
   1. 從下載資料夾中，移動 `luma-data.zip` 檔案到電腦上的所需位置，然後解壓縮。這些檔案保存培訓沙箱的示例資料。
   1. 開啟每個檔案並查找 **`yourOrganizationID`** 將其替換為 [組織ID](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=zh-Hant).
   1. 儲存檔案。

## 開始吧

從 [手動設定資料](/help/tutorial-configure-a-training-sandbox/manual-data-set-up.md). 在此步驟中，您會定義所需的資料結構。 完成資料設定後，您可以將資料內嵌至沙箱，然後設定事件。
