---
title: 追蹤並報告Adobe Journey Optimizer (AJO)透過AJO Offer Decisioning提供的優惠方案
description: 本教學課程會擴充現有的Adobe Journey Optimizer (AJO)實作，後者會根據溫度等情境資料提供個人化優惠。 它概述如何擷取曝光和互動事件，以及準備資料以在Journey Optimizer中報告。
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00Z
jira: KT-18526
source-git-commit: fa4795d92cf290b867df23277a297c99d6222224
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# 將追蹤權杖新增至選件專案

若要修改個人化編輯器中的程式碼，請遵循下列步驟：

導覽至&#x200B;_&#x200B;**歷程管理 — >行銷活動**&#x200B;_

開啟適當的行銷活動，然後按一下&#x200B;_&#x200B;**停止行銷活動**&#x200B;_&#x200B;按鈕以停止行銷活動。

開啟已停止的行銷活動，然後按一下&#x200B;_&#x200B;**修改行銷活動**&#x200B;_&#x200B;按鈕。

按一下「_&#x200B;**內容**&#x200B;_」標籤，然後按一下「_&#x200B;**編輯代碼**&#x200B;_」按鈕以開啟個人化編輯器。

將兩個新資料屬性新增至div，如熒幕擷圖所示
![tracking-token](assets/offer-item-with-tracking-code.png)

若要新增trackingToken和ItemID，請按一下左側導覽的「決定原則」圖示，然後向下展開決定樹狀結構以選取itemID和trackingToken。
![tracking-token](assets/insert-tracking-token.png)

這可確保每個演算後的選件都包含資料追蹤代號，這對於精確曝光和點選事件追蹤至關重要。

儲存變更並啟動行銷活動。
