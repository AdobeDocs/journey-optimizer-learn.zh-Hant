---
title: 建立決定原則
description: 使用決定原則來定義邏輯，以決定在個人化期間將哪些優惠提供給使用者。
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-17728
exl-id: 186e4a7d-6077-401f-9958-2f955214bc35
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: a984631b-2bae-4860-9b15-69c41a799dcb
    internal-label: APIs and SDKs
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
    internal-label: Decisioning API
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%
---
# 建立決定原則

決策原則是您優惠方案的容器，可運用[!UICONTROL 決策]引擎，根據對象挑選最佳內容進行傳遞。

1. 在個人化編輯器中，按一下左側導覽中的&#x200B;**[!UICONTROL 決定原則]**&#x200B;專案，然後按一下&#x200B;**[!UICONTROL 新增決定原則]**。

   ![create-decision-policy](assets/decision-policy.png)

1. 按一下&#x200B;**[!UICONTROL 新增]**&#x200B;以選取選取策略。

   ![決定原則](assets/decision-policy2.png)

1. 按一下&#x200B;**[!UICONTROL 選取遞補]**&#x200B;以選取遞補優惠。
1. 按一下&#x200B;**[!UICONTROL 下一步]**&#x200B;以檢閱決定原則。
1. 按一下[建立&#x200B;****]完成建立決定原則的程式。

## 在程式碼編輯器中使用決定原則

1. 在個人化編輯器中，按一下&#x200B;**[!UICONTROL 插入原則]**。

   已新增與決定原則對應的程式碼。

   在此階段，您可以直接在程式碼中包含任何必要的決定屬性。 這些屬性是在優惠方案目錄使用的結構描述中定義。 標準屬性是在`__experience`名稱空間下組織，而貴組織專屬的任何自訂屬性都儲存在`_<imsOrg>`名稱空間下。

   ![使用_decision_polcy](assets/Insert-policy.png)

   此程式碼會瀏覽為使用者選擇的個人化優惠清單，並在網頁上顯示每個優惠的文字。 它會顯示段落中每個選件的訊息（稱為`offerText`），讓使用者可以清楚看到他們自訂的內容。

   如果沒有可用的個人化優惠方案，則會顯示遞補優惠方案，以確保空間不會留空。

1. 按一下&#x200B;**[!UICONTROL 儲存]**，然後啟動行銷活動。
