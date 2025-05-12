---
title: 在Adobe Journey Optimizer中建立對象
description: 瞭解如何在AJO中定義及建立目標對象，以強化個人化客戶歷程及即時決策
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00Z
jira: KT-17923
source-git-commit: ba83be3caf214d2daaa8c99556d246686ff3f0cb
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# 在Adobe Journey Optimizer中建立對象


Adobe Experience Platform中的受眾是根據動作、偏好設定或設定檔資訊建立的使用者群組，用以提供個人化體驗。

* 登入Journey Optimizer
* 導覽至「客戶 — >對象 — >建立對象」
* 使用建置規則方法建立對象

  ![對象](assets/rule-based-audience.png)

* 建立下列3個對象

   * 對股票感興趣的客戶

   * 對債券感興趣的客戶

   * 對CD感興趣的客戶


* 確定每個對象的評估方法已設定為&#x200B;_**Edge**_，以便即時取得資格。
  ![邊緣對象](assets/audience-edge.png)

* 使用PreferredFinancialInstrument欄位，根據使用者選取的投資興趣（例如股票、債券或光碟）來劃分使用者

![事件](assets/event-attribute.png)

![PreferredFinancialInstrument](assets/stock-customers.png)




>[!NOTE]
>
>>如果PreferredFinancialInstrument欄位未顯示在events標籤中，請按一下設定圖示並切換Show the full XDM schema。



![toggle-full-xdm-schema](assets/show-custom-fields.png)


