---
title: AEP中的身分彙整
description: 在已知使用者 (CRMID) 和匿名網頁訪客 (ECID) 之間建立身分拼接，形成整合的輪廓，以在 Adobe Journey Optimizer (AJO) 中實現即時個人化，並提供產品建議決策。
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00.000Z
jira: KT-18089
exl-id: d6a1201a-3779-4718-8ea8-b88f925f53b6
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d2971708-e780-44bb-9e2a-72f139796afd
    internal-label: Customer
subfeature_v2:
  - id: ef9a83ca-eefa-47cf-aa34-f1a34715583a
    internal-label: Profiles
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 11%
---
# AEP中的身分拼接

在現代客戶體驗中，跨裝置和管道統一使用者身分至關重要。 此使用案例示範如何在Adobe Experience Platform (AEP)中實作身分拼接，方法是連結已知的CRM ID （於使用者登入期間擷取）與Adobe Web SDK產生的匿名Experience Cloud ID (ECID)。 透過即時將這些身分拼接在一起，AEP可以建立更完整的客戶個人檔案，該個人檔案跨越匿名行為和已驗證的資料。 這可讓您在Adobe Journey Optimizer (AJO)等工具中，進行更準確的對象細分、個人化和決策。

## 身分拼接教學課程所需的技能

若要善用本教學課程，建議您熟悉下列內容：

- **Adobe Experience Platform (AEP)核心概念**\
  瞭解結構描述、資料集、身分、合併原則和即時設定檔。

- **結構描述和身分模型**\
  能夠設定設定檔和事件架構中的身分欄位。

- **Adobe Launch （標籤）和網頁SDK (Alloy.js)**\
  具有使用網頁SDK設定資料元素和規則以傳送資料至AEP的經驗。

- **JavaScript基本知識**\
  熟悉使用函式來擷取使用者輸入、觸發事件和除錯API呼叫。

- **AEP偵錯工具**\
  能夠使用AEP Debugger和Identity Graph Viewer來驗證身分彙整。

- 在AEP中擷取&#x200B;**資料**\
  熟悉如何上傳範例資料到資料集並確保資料品質。


