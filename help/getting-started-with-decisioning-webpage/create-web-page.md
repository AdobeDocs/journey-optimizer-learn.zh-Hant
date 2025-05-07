---
title: 建立網頁以測試解決方案
description: 用於測試使用決策提供的個人化優惠的網頁。
role: User
level: Beginner
doc-type: Tutorial
feature: Decisioning
last-substantial-update: 2025-05-05T00:00:00Z
jira: KT-17728
source-git-commit: 9695a4db0d0caa44a8c7d49e069320309ffc40a6
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---


# 建立網頁以測試解決方案

此網頁是用來測試透過Adobe Journey Optimizer Decisioning提供的個人化優惠。 它提供可觸發sendEvent呼叫並轉譯傳回之選件內容的受控環境，有助於驗證端對端個人化設定並確保決策如預期般運作。

以下指令碼負責使用Adobe Journey Optimizer在網頁上擷取和顯示個人化優惠方案。

1. 解碼HTML實體：有協助程式函式可安全地將選件內容中的任何特殊字元轉換為可讀取的HTML。

2. 執行個人化：
呼叫時，它會傳送要求(sendEvent)至Adobe的Web SDK，以取得頁面上特定區域的個人化內容(#ajo-offer元素)。
如果傳回選件，則會解碼HTML並將其插入頁面中。
如果未傳回任何專案，則會記錄警告。

3. 等待SDK：
由於Adobe的SDK (alloy)以非同步方式載入，因此指令碼會等到完全載入後再提出請求。
它會每200毫秒檢查一次合金，最多20次，以避免錯誤。

4. 頁面載入時：當頁面完成載入時，指令碼會呼叫waitForAlloy()來啟動程式。



```javascript
< script >
    function decodeHtmlEntities(html) {
        const txt = document.createElement("textarea");
        txt.innerHTML = html;
        return txt.value;
    }


function runPersonalization() {
    console.log("🚀 Sending personalization request to AJO...");
    alloy("sendEvent", {
        renderDecisions: true,
        personalization: {
            surfaces: ["#ajo-offer"]
        }
    }).then(result => {
        console.log("🔍 Web SDK decision response:", result);

        const decision = result.propositions?.[0];
        const html = decision?.items?.[0]?.data?.content;

        const container = document.getElementById("ajo-offer");
        if (html && container) {
            const decodedHtml = decodeHtmlEntities(html);
            console.log("✅ Offer HTML content (decoded):", decodedHtml);
            container.innerHTML = decodedHtml;
        } else {
            console.warn("⚠️ No personalized offer returned.");
        }


    }).catch(error => {
        console.error("❌ sendEvent failed:", error);
    });
}

function waitForAlloy(callback, retries = 20) {
    if (typeof alloy === "function") {
        callback();
    } else if (retries > 0) {
        console.log("⌛ Waiting for Alloy...");
        setTimeout(() => waitForAlloy(callback, retries - 1), 200);
    } else {
        console.error("❌ alloy is not loaded after waiting.");
    }
}

// Trigger initial personalization on page load
document.addEventListener("DOMContentLoaded", function() {
    waitForAlloy(() => runPersonalization());
}); <
/script>
```

[範例HTML頁面和相關資產可從這裡下載](assets/web-page-assets.zip)