---
title: 建立忠誠度狀態歡迎電子郵件 — 挑戰
description: 瞭解在歷程畫布中建立歷程的基本概念。
kt: 8109
feature: Journeys
role: User
level: Beginner
hide: true
source-git-commit: 957515149af1281d29a45b24ca499ef097656eb8
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 8%

---


# 建立忠誠度狀態歡迎電子郵件 — 挑戰

![AJO忠誠度狀態歡迎電子郵件 — 質詢橫幅](/help/challenges/assets/email-assets/luma-transactional-onboarding-1.png)

| 挑戰 | 建立忠誠度狀態歡迎電子郵件 |
|---|---|
| 角色 | Journey Manager |
| 所需技能 | <ul><li>[使用訊息編輯器建立電子郵件內容](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-email-content-with-the-message-editor.html?lang=en)</li> <li>[使用內容事件資訊進行個人化](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-contextual-event-information-for-personalization.html?lang=en)</li><li>[使用協助程式功能進行個人化](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-helper-functions-for-personalization.html?lang=en)</li></ul> |
| 要下載的資產 | [訂購確認資產](/help/challenges/assets/email-assets/order-confirmation-assets.zip) |

## 故事

Luma提供忠誠計畫，作為吸引及留住客戶的方式。 該計畫提供四個不同級別：銀，金，白金，鑽石。

每個忠誠度等級會獲得不同的等級或獎勵、折扣和其他特殊獎勵，作為對其重複業務的獎勵。

加上特殊鑽石狀態。 Luma想要在客戶到達鑽石階層時，向其發送歡迎電子郵件。

## 您的挑戰

您的任務是設定歷程，當客戶達到鑽石忠誠度等級時，會自動傳送歡迎電子郵件給客戶。

>[!NOTE]
> 如果您在共用訓練沙箱中工作，最佳實務是將您的名稱或縮寫為預先修正，加入您建立之任何元素的名稱。

### 建立Luma鑽石狀態區段。

在Journey Optimizer中建立區段，稱為 **您的名稱 — Luma — 鑽石狀態**.

### 建立Luma — 新狀態 — Diamond — 交易式電子郵件訊息

建立歡迎電子郵件訊息

1. 建立標題為的交易式電子郵件訊息 `(your name)_Luma – New Status – Diamond – Transactional email message`.
2. 為電子郵件提供主旨行 `Welcome to Diamond Status, (recipient's first name)!`.
3. 使用提供的HTML檔案 **[DiamondStatusEmail.html](/help/challenges/assets/email-assets/DiamondStatusEmail.html)** 用於電子郵件內文。


### **Journey #3 - Diamond狀態升級歡迎電子郵件**

當忠誠度客戶移至新層級時，請傳送電子郵件，祝賀並告知他們新的優點。

1. 建立當客戶移入鑽石新忠誠度層時觸發的歷程（尤其是當客戶進入為新鑽石層級成員定義的區段時），以傳送「Luma — 新狀態 — 鑽石 — 交易」電子郵件
2. 完成後，將歷程置於測試模式，並觸發歷程以傳送給您自己  

成功標準

您應會收到個人化的「Luma — 新狀態 — 鑽石交易」電子郵件。
