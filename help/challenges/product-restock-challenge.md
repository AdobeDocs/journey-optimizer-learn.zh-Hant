---
title: 產品補充挑戰
description: 套用您建立區段所學的知識，並測試您的技能。
kt: 8417
feature: Segments
role: User
level: Beginner
hide: true
exl-id: 305aaf4c-7f5d-4f6f-abeb-466208f1fe48
source-git-commit: 7ecbed1b722d7f05ffd4a7c7071358d993cb1392
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 72%

---

# 產品補充挑戰

| 挑戰 | 產品補充 |
|---|---|
| 角色 | Journey Manager |
| 所需技能 | <ul><li>[建立區段](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html?lang=zh-Hant)</li><li> [匯入及編寫 HTML 電子郵件內容](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/import-and-author-html-email-content.html?lang=en)</li><li>[使用案例 - 讀取區段](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment.html?lang=zh-Hant)</li> |
| 要下載的資產 | [產品重新儲存電子郵件檔案](/help/challenges/assets/email-assets/ProductRestockEmail.html.zip) |

## 故事

瀏覽Luma網站時，客戶可將他們感興趣的產品新增至願望清單，這可讓Luma傳送客戶目標式行銷訊息和產品相關資訊。

## 您的挑戰

Luma 要求您在 Journey Optimizer 中實施歷程，當此項目有庫存時，此歷程會通知客戶 (其願望清單上有先前無庫存的項目)。創意團隊會提供 [產品重新儲存電子郵件檔案](/help/challenges/assets/email-assets/ProductRestockEmail.html.zip).

>[!BEGINTABS]

>[!TAB 工作]

## 1.定義區段 — 無存貨意願清單項目

若要在產品已補充庫存時鎖定潛在感興趣的客戶，請建立由客戶組成的區段:

* 已將至少一個項目新增至其願望清單(使用事件類型： [!UICONTROL 商務儲存以供延遲使用])
* 過去三個月無存貨（使用存貨量= 0）
* 而且自那時起就沒有購買過商品。

>[!TIP]
>從以下項目排除 SKU 符合 SKU 的所有「購買」事件類型： *儲存以供稍後使用事件*。您可以在 *瀏覽變數* 區段。

為此區段命名： `Out-of-stock-Wishlist`


### 2.建立歷程 — 產品重新儲存通知

當先前缺貨的項目重新補充庫存時，通知已新增缺少庫存項目並致電開始購物的客戶，該項目已補充庫存。

1. 呼叫歷程： `Product Restock`
2. 當產品重新補充庫存時，即應觸發歷程
3. 傳送 *產品重新儲存電子郵件* to
4. 已將此項目新增至其願望清單 (無庫存) 的使用者

>[!TAB 成功標準]

測試您的歷程:

1. 請確定讀取區段事件具有命名空間= `Luma CRM ID`
1. 覆寫預設的電子郵件參數，並將其設為您自己的電子郵件地址 (如需指示，請參閱電子郵件 #1)
1. 將歷程設為測試模式
1. 觸發事件 - 輸入下列資料：

   * 說明：您只需使用 Harmony Lumaflex Length Band Kit，即可輕鬆享受令人驚嘆的健身。 該套件提供您進行一系列強化和調整練習所需的一切。
   * 名稱：Harmony Lumaflex 彈力帶套件
   * 價格：22
   * 產品 ID：2003 年 8 月 24 日
   * 產品影像 URL：https://publish1034.adobedemo.com/content/dam/luma/en/products/gear/fitness-equipment/ug03-bk-0.jpSKU: 24-UG03
   * 庫存事件類型：重新補充庫存
   * 設定檔識別碼：Jenna_Palmer9530@emailsim.io

您應該會收到「Luma 電子郵件產品補充」電子郵件，內含產品詳細資訊及 Jenna 的個人化內容。

>[!TAB 檢查您的工作]

區段可能會以這種方式呈現：

![區段 - 無庫存願望清單項目](/help/challenges/assets/C1-S2.png)


以下是您歷程的外觀：

![產品補充歷程](/help/challenges/assets/c3-j3-journey.png)

條件：在願望清單中

![條件 - 在願望清單中](/help/challenges/assets/c3-j3-condition.png)

條件代碼：

```in(@{LumaProductRestock._wwfovlab065.sku},#{ExperiencePlatform.ExperienceEvents.experienceevent.all(currentDataPackField.eventType=="commerce.saveForLaters").productListItems.all().SKU})```


>[!TIP]
> * 在&#x200B;*瀏覽變數*&#x200B;區段的「儲存以便稍後使用」下方選取 SKU
> * 將 SKU 拖曳至「儲存以便稍後使用」欄位時，請使用比較選項


在「編輯」區段畫面右下角的「事件」下方，勾選代碼。 程式碼應如下所示：

程式碼:
```(Include have at least 1 Save For Laters event where ((Stock Quantity equals 0)) THENExclude all  Purchases events where ((SKU equals Save For Laters1 SKU)) ) and occurs in last 3 month(s)```

>[!ENDTABS]

### 建立電子郵件 - Luma 產品補充

通知已新增無庫存項目且致電開始購物的客戶，該項目已有庫存。



>[!TIP]
>
> 使用現有業務事件。 新增條件，以檢查重新儲存的SKU是否包含在（任何）事件類型中，並儲存至延遲。



