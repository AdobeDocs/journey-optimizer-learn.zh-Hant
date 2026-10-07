---
title: 建立網頁以測試解決方案
description: 用於測試使用決策提供的個人化優惠的網頁。
role: User
level: Beginner
doc-type: Tutorial
feature: Decisioning
last-substantial-update: 2025-05-31T00:00:00.000Z
jira: KT-18188
recommendations: noDisplay, noCatalog
exl-id: 6b1eec78-153c-4ea5-acfe-2dcc6f1e6078
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
source-wordcount: '348'
ht-degree: 0%
---
# 建立網頁以測試解決方案

此範例應用程式會模擬真實世界的登入流程，在將CRM ID傳送至Adobe Experience Platform (AEP)之前，使用者憑證會在伺服器端驗證。 本機Node.js伺服器可用來安全地提供網頁、處理基本驗證邏輯，以及避免可能會干擾Adobe Launch或網頁SDK功能的瀏覽器限制（例如封鎖的本機檔案存取或遺失CORS標題）。 此設定可確保體驗更接近真實的生產環境。

個人化優惠只會在使用者登入後顯示，此時使用者的CRM ID與ECID (Experience Cloud ID)之間的身分拼接已完成。 此身分拼接可確保Adobe Journey Optimizer (AJO)可以準確識別設定檔並傳回目標選件。

成功登入後，系統會傳送個人化請求至AJO以擷取可用的選件供使用者使用。 這些優惠會以HTML片段的形式傳回，每個片段都內嵌了資料標籤屬性，例如data-tags=&quot;ajo offer-vacation-based-cd zip-92128 income-high&quot;，其中包括優惠方案名稱和區段細節，如郵遞區號和收入層級。

JavaScript接著會剖析這些HTML區塊，並將每個區塊包裝在輪播專案容器中。 專案會水準排列在輪播追蹤中，啟用可滑動導覽。 上一個和下一個按鈕（◀和▶）可讓使用者一次翻閱一個個人化優惠方案。

此設定提供回應式且量身打造的體驗，確保每位使用者都能看到與其財務設定檔相關的選件 — 只有在其身分識別跨平台安全拼接後才可看到。

## 測試此解決方案

* 在現有Node.js專案中建立名為ranking-formula的資料夾。

* 將[提供的檔案解壓縮至此排名公式資料夾。](assets/ranking-formula.zip)

* 導覽至資料夾並啟動伺服器，執行應用程式：
  * `cd ranking-formula`

  * `node server.js`


* 開啟瀏覽器並前往http://localhost:3000/formula.html。

* 使用alice/pass123登入

由於Alice位在92128郵遞區號中，因此會針對該位置顯示量身打造的選件。
