---
title: 建置範例應用程式以模擬登入活動
description: 建立範例Node.js應用程式以模擬登入流程
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00Z
jira: KT-18089
source-git-commit: 502cdc41b666959141ff4dfc63608cc463009811
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# 建置範例應用程式以模擬登入活動

此範例應用程式建置並部署在Node.js伺服器上，示範如何在使用者登入時將CRM ID傳送至Adobe Experience Platform (AEP)。 應用程式會模擬在伺服器端驗證使用者憑證的登入流程。 成功登入後，系統會擷取使用者的CRM ID並推送至adobeDataLayer，觸發Adobe Experience Platform Tags (先前稱為Adobe Launch)中的對應規則。

attachLoginHandler函式會將送出事件接聽程式附加到登入表單。 在提交表單時，此動作會防止預設動作、根據預先定義使用者的物件驗證認證，並擷取CRM ID （若有效）。 函式會將具有CRM ID和驗證狀態的userloggedin事件推送至adobeDataLayer，然後Adobe Experience Platform標籤會挑選該事件，以將資料傳送至Adobe Experience Platform (AEP)。


```javascript
function attachLoginHandler() {
    const form = document.getElementById("loginForm");
    if (!form) return;

    form.addEventListener("submit", function(e) {
        e.preventDefault();
        const username = document.getElementById("username").value;
        const password = document.getElementById("password").value;

        if (users[username] && users[username].password === password) {
            const crmid = users[username].crmid;
            window.adobeDataLayer = window.adobeDataLayer || [];
            debugger;
            window.adobeDataLayer.push({
                event: "userloggedin",
                user: {
                    crmid: crmid,
                    authenticatedState: "authenticated"
                }
            });
        }
    });
}
```

Adobe Experience Platform標籤指令碼使用`<script>`標籤包含在HTML頁面的`<head>`區段中，通常如下所示：

`<script src="https://assets.adobedtm.com/b5eu4857867/4e4d84957/launch-b69e276bb9b5-development.min.js" async crossorigin="anonymous"></script>`

AEP Tags指令碼是透過發佈在先前步驟中建立的啟用Web SDK屬性，並從「環境」標籤複製內嵌程式碼來取得。


