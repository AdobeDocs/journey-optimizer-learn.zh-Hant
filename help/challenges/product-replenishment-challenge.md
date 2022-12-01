---
title: 產品補充挑戰
description: 套用您建立區段所學的知識，並測試您的技能。
kt: 8417
feature: Segments
role: User
level: Beginner
hide: true
exl-id: 305aaf4c-7f5d-4f6f-abeb-466208f1fe48
source-git-commit: 0e83d8fbad6bd87ed25980251970898cb5b94bc0
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 2%

---

# 產品補充挑戰

| 挑戰 | 產品補充 |
|---|---|
| 角色 | Journey Manager |
| 所需技能 | <ul><li>[建立區段](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-segments.html?lang=en)</li><li> [匯入及編寫 HTML 電子郵件內容](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/import-and-author-html-email-content.html?lang=en)</li><li>[使用案例 - 讀取區段](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment.html?lang=en)</li> |
| 要下載的資產 | [季節性收集電子郵件檔案](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip) |

## 故事

瀏覽Luma網站時，客戶可將他們感興趣的產品新增至願望清單。 這可讓Luma傳送客戶目標式行銷訊息和產品資訊。

## 您的挑戰

Luma要求您在Journey Optimizer中實作歷程，當此項目有存貨時，此歷程會通知客戶（其願望清單上有先前無存貨的項目）。

## 定義區段 — 無存貨意願清單項目

若要在重新儲存產品時鎖定潛在感興趣的客戶，請建立由客戶組成的區段

* 已將至少一個項目新增至其願望清單(使用事件類型： [!UICONTROL 商務儲存以供延遲使用])
* 那是 **無庫存** 最近3個月（使用庫存量= 0）
* 而且自那時起就沒有購買過商品。

為此區段命名： *您的姓名 — 無庫存*

+++**檢查您的工作**

以下是區段的外觀：

![段 — 無庫存願望清單項](/help/challenges/assets/C1-S2.png)

已將項目新增至其願望清單的客戶，過去3個月內無存貨：

* 事件：儲存以更新
   * 至少包括1
   * 當庫存數量為0時

且自購買後未購買過項目：

* 從以下項目排除SKU符合SKU的所有「購買」事件類型： **儲存以供稍後使用事件**.

>[!TIP]
> * 在的「儲存更新」下方選取SKU, *瀏覽變數* 節
> * 將SKU拖曳至「儲存以供稍後使用」欄位時，請使用比較選項


在「編輯」區段畫面右下角的「事件」下方，勾選代碼。 程式碼應如下所示：

程式碼:
```(Include have at least 1 Save For Laters event where ((Stock Quantity equals 0)) THENExclude all  Purchases events where ((SKU equals Save For Laters1 SKU)) ) and occurs in last 3 month(s)```

+++

### 建立電子郵件 — Luma產品補充

通知已新增無存貨項目且呼叫開始購物的客戶，該項目已有存貨。

### 建立歷程 — 產品重新儲存通知

當先前缺貨的項目重新存貨時，通知已新增缺貨項目並呼叫開始購物的客戶，該項目已存貨。

1. 建立名為「您的name_Luma — 產品重新儲存」的歷程
1. 當產品重新存貨時，應觸發歷程
1. 傳送 *Luma — 產品補充* 電子郵件至
1. 已將此項目添加到其願望清單（無存貨）的用戶

>[!TIP]
>
> 使用現有業務事件。 您需要新增條件，以檢查重新儲存的SKU是否包含在（任何）事件類型中，以備延遲時使用。

+++**成功標準**

測試您的歷程:

1. 請確定區段資格事件具有「命名空間=電子郵件」
1. 覆寫預設的電子郵件參數，並將其設為您自己的電子郵件地址(如需指示，請參閱電子郵件#1)
1. 將歷程設為測試模式
1. 觸發事件 — 輸入下列資料：

   * 說明：您只需使用Harmony Lumaflex Length Band Kit，即可輕鬆享受令人驚嘆的鍛鍊。 該套件提供您進行一系列強化和調音練習所需的一切。
   * 名稱：Harmony Lumaflex強度帶套件
   * 價格：22
   * 產品ID:2003年8月24日
   * 產品影像URL:https://publish1034.adobedemo.com/content/dam/luma/en/products/gear/fitness-equipment/ug03-bk-0.jpSKU網站：2003年8月24日
   * 庫存事件類型：重新儲存
   * 設定檔識別碼：Jenna_Palmer9530@emailsim.io

您應該會收到「Luma電子郵件產品補充」電子郵件，內含產品詳細資訊和Jenna的個人化內容。

+++

+++**檢查您的工作**

以下是您歷程的外觀：

![產品補充歷程](/help/challenges/assets/c3-j3-journey.png)

條件：在願望清單中

![條件 — 在願望清單中](/help/challenges/assets/c3-j3-condition.png)

條件代碼：

```in(@{LumaProductRestock._wwfovlab065.sku},#{ExperiencePlatform.ExperienceEvents.experienceevent.all(currentDataPackField.eventType=="commerce.saveForLaters").productListItems.all().SKU})```

+++
