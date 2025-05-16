---
title: AEP中的身分拼接
description: 在已知使用者(CRMID)和匿名Web訪客(ECID)之間建立身分拼接，在Adobe Journey Optimizer (AJO)中啟用統一設定檔以進行即時個人化和優惠方案決策。
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00Z
jira: KT-18089
source-git-commit: 502cdc41b666959141ff4dfc63608cc463009811
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# 使用案例說明

在現代客戶體驗中，跨裝置和管道統一使用者身分至關重要。 此使用案例示範如何在Adobe Experience Platform (AEP)中實作身分拼接，方法是連結已知的CRM ID （於使用者登入期間擷取）與Adobe Web SDK產生的匿名Experience Cloud ID (ECID)。 透過即時將這些身分拼接在一起，AEP可以建立更完整的客戶個人檔案，該個人檔案跨越匿名行為和已驗證的資料。 這可讓您在Adobe Journey Optimizer (AJO)等工具中，進行更準確的對象細分、個人化和決策。

