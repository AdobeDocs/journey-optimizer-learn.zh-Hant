---
title: 在Adobe Journey Optimizer中建立對象
description: 瞭解如何在AJO中定義及建立目標對象，以強化個人化客戶歷程及即時決策
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00.000Z
jira: KT-17923
exl-id: d90f1868-0514-49b2-832d-82460883b6e4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d2971708-e780-44bb-9e2a-72f139796afd
    internal-label: Customer
subfeature_v2:
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%
---
# 在Adobe Journey Optimizer中建立對象


Adobe Experience Platform中的受眾是根據動作、偏好設定或設定檔資訊建立的使用者群組，用以提供個人化體驗。

* 登入Journey Optimizer
* 導覽至「客戶 — >對象 — >建立對象」
* 使用建置規則方法建立對象

  ![客群](assets/rule-based-audience.png)

* 建立下列3個對象

  * 對股票感興趣的客戶

  * 對債券感興趣的客戶

  * 對CD感興趣的客戶


* 確定每個對象的評估方法已設定為&#x200B;_&#x200B;**Edge**&#x200B;_，以便即時取得資格。
  ![邊緣對象](assets/audience-edge.png)

* 使用PreferredFinancialInstrument欄位，根據使用者選取的投資興趣（例如股票、債券或光碟）來劃分使用者

![事件](assets/event-attribute.png)

![PreferredFinancialInstrument](assets/stock-customers.png)




>[!NOTE]
>
>&#x200B;>如果PreferredFinancialInstrument欄位未顯示在events標籤中，請按一下設定圖示並切換Show the full XDM schema。



![toggle-full-xdm-schema](assets/show-custom-fields.png)
