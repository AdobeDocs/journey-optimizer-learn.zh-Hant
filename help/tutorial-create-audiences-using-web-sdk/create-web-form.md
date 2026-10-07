---
title: 建立網路表單
description: 在您的HTML頁面中建立表單，讓使用者可選取其投資偏好設定
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-17923
exl-id: 20de8dec-aac8-43ed-8305-e723f82a5dd9
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
source-wordcount: '125'
ht-degree: 0%
---
# 建立網路表單

已建立下列HTML表單以擷取使用者偏好設定
![html-form](assets/web-form.png)

當使用者按一下網頁上的按鈕時，會擷取他們選取的財務偏好設定（例如「股票」、「債券」或CD）並將其推送至Adobe資料層。 此事件(assetClassSelection)會即時儲存使用者的選擇。 Adobe Launch接著會監聽此事件，擷取選取的投資選項(PreferredFinancialInstrument)，並可觸發動作，例如將資料傳送至Adobe Experience Platform (AEP)或更新個人化規則

下列JavaScript是用來處理表單提交的

```javascript
function handleSubmission() {
  window.adobeDataLayer = window.adobeDataLayer || [];

  const selectedAssetClass = document.querySelector('input[name="assetclass"]:checked');
  const errorMessage = document.getElementById("error-message");
  const messageBox = document.getElementById("message");

  if (!selectedAssetClass) {
    errorMessage.textContent = "Please select a financial instrument.";
    messageBox.textContent = "";
    return;
  }

  errorMessage.textContent = "";

  const subscriptionEvent = {
    event: "assetClassSelection",
    xdm: {
      eventType: "assetClassSelection",
      eventID: "investment_preference_event",
      timestamp: new Date().toISOString(),
      FinancialInterest: {
        PreferredFinancialInstrument: selectedAssetClass.value
      }
    }
  };

  console.log("📩 Sending asset class data to AEP:", subscriptionEvent);
  window.adobeDataLayer.push(subscriptionEvent);

  // ✅ Show thank-you message
  messageBox.textContent = `Thank you for selecting "${selectedAssetClass.value}". We'll use this to personalize your experience.`;
}
```

[本教學課程提供範例HTML表單](assets/webform.zip)
