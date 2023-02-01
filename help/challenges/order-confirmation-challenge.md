---
title: 建立訂單確認電子郵件
description: 測試您關於如何建立和個人化異動訊息的知識
kt: 7531
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: ec86e2ac-081d-47aa-a948-007107baa2b4
source-git-commit: 70815c3cd30de22aad7ec667b8baf9b4c8642491
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 82%

---


# 建立訂單確認電子郵件

![訂購確認](/help/challenges/assets/email-assets/luma-transactional-order-confirmation.png)

| 挑戰 | 建立訂單確認異動電子郵件 |
|---|---|
| 角色 | Journey Manager |
| 所需技能 | <ul><li>[使用訊息編輯器建立電子郵件內容](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-email-content-with-the-message-editor.html?lang=zh-Hant)</li> <li>[使用內容事件資訊進行個人化](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-contextual-event-information-for-personalization.html?lang=zh-Hant)</li><li>[使用協助程式功能進行個人化](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-helper-functions-for-personalization.html?lang=zh-Hant)</li></ul> |
| 要下載的資產 | [訂購確認資產](/help/challenges/assets/email-assets/order-confirmation-assets.zip) |

## 故事

Luma 正在啟動其線上商店，希望在客戶下訂單後，提供訂單確認電子郵件，以保障良好的客戶體驗。



## 您的挑戰

建立歷程，當 Luma 客戶完成線上訂單時傳送訂單確認電子郵件。 

>[!BEGINTABS]

>[!TAB 工作]

1. 建立名為`Luma - Order Confirmation`的歷程
2. 使用事件： `LumaOnlinePurchase`
3. 建立訂單確認電子郵件，名為`Luma - Order Confirmation`：

* 類別異動 - 請務必選取異動電子郵件表面
* 主旨列必須以收件者的名字個人化，且必須包含「感謝您的購買」的片語
* 使用`Luma - Order summary`範本並加以修改：
   * 移除 `You may also like` 區段
   * 在電子郵件底部新增取消訂閱連結

電子郵件應有如下的結構：
<table>
<tr>
<td>
  <div>
     <strong> 標題區段</strong>
      </div>
  </td>
  <td>
      <p>
     <li>luma_logo.png</li>
    <li>應該會有 Luma 網站的連結：https://publish1034.adobedemo.com/content/luma/us/en.html</li>
    <p>
    </td>
  </tr>
  <tr>
  <td>
  <div>
    <strong>訂購確認區段
    </strong>
  </td>
  <td>
    <p>
    <strong>文字</strong><p>
    <em>嗨{firstName}</em><p>
   <div>
    <p>
     <em>已下訂單。
    <p>您的包裹出貨後，我們會向您傳送一封包含追蹤號碼的電子郵件，供您追蹤訂單。</p></em>
    </strong>
    </tr>
  </td>
 <td>
  <div>
     <strong> 收貨區</strong>
      </div>
      <p>
      <li>名字和姓氏來自設定檔
      <li>以 <b>運送地址</b>
      <li>地址詳細資料是來自事件的情境屬性（街1號、城市、郵遞區號、州）
      <li> 移除折扣、總計、送達</p>
  </td>
  <td>
  <p> 收貨方：</p>
      <em>{firstName} {lastName}<br>
     {街1}<br>
     {City}, {State} {postalCode}<br></em></p>
  </td>
 <tr>
<td>
  <div>
     <strong>訂購詳細資訊區段</strong>
      </div>
       <p><li>在 <b>收貨方</b> 區段。
      </p><br>
      <p><b>提示:</b>
      <li>對本節使用結構元件「左1:2列」
      <li>這是內容事件資訊。
      <li>使用 [!UICONTROL helper function]: [!UICONTROL Each]
      <li>切換至程式碼編輯器格式以新增內容資料。
  </td>
  <td>
    <strong>Header</strong>
    <p>
    <em>順序：`purchaseOrderNumber`</em>
    </p>
    <strong>訂購的產品清單：
  </strong>
  <p>每個項目的格式應如下所示：
   <img alt="訂購" src="./assets/c2-order.png"> 
</p>
</td>
  </tr>
</table>


>[!TIP]
>
>若要讓您疑難排解歷程，最佳實務是在逾時或錯誤的情況下，為所有訊息動作新增替代路徑。

>[!TAB 成功標準]

觸發您在測試模式中建立的歷程，並傳送電子郵件給您自己：

1. 按一下眼睛符號來顯示隱藏的值：
   1. 在電子郵件參數中，按一下 T 符號 (啟用參數覆寫
      ![覆寫電子郵件參數](/help/challenges/assets/c3-override-email-paramters.jpg)
   2. 按一下「地址」欄位
   3. 在下一個畫面中，以括弧新增您的電子郵件地址： 在運算式編輯器中新增 *yourname@yourdomain* ，並按一下「確定」。
2. 將歷程置於測試模式
3. 使用下列參數觸發事件：
   * 將設定檔識別碼設為：身分值：`a8f14eab3b483c2b96171b575ecd90b1`
   * 事件類型：commerce.purchases
   * `Quantity`: 1
   * `Price Total:` 69
   * `Purchase Order Number:` 6253728
   * `SKU:` LLMH09
   * `City:` 華盛頓
   * `Postal Code:` 20099
   * `State`:DC
   * `Street:` 蒂埃勒特勒斯

您應會收到包含指定產品的個人化購買確認電子郵件。

* 主旨列應有測試設定檔的名字：Leora
* 訂單詳細資訊區段應填入您在測試時輸入的訂購詳細資料

>[!TAB 檢查您的工作]

**歷程**

![歷程](/help/challenges/assets/c2-journey.png)


**電子郵件**

**主旨列：**

謝謝你的購買， {{ profile.person.name.firstName }}!

以下是您電子郵件內文的外觀：

![電子郵件](//help/challenges/assets/c2-email.png)

**收貨區段：**

以下是您的程式碼應呈現的外觀：

```javascript
{{ profile.person.name.firstName }} {{ profile.person.name.lastName }}
{{context.journey.events.454181416.commerce.shipping.address.street1}}
{{context.journey.events.454181416.commerce.shipping.address.city}}, {{context.journey.events.454181416.commerce.shipping.address.state}} {{context.journey.events.454181416.commerce.shipping.address.postalCode}}
```

*event.45481416* 會是另一個數字。

提示：每一列都進行個人化

**訂購詳細資訊：**

以下是您的程式碼應呈現的外觀：

標頭:

```javascript
Order #: {{context.journey.events.1627840522.commerce.order.purchaseOrderNumber}}
```

**產品清單：**

使用協助程式函式「each」來建立產品清單。 在一個表格中顯示它們。這是程式碼應該看起來的樣子（搭配您的特定變數，例如事件ID），而非 `454181416` 和你的組織I，而不是 `techmarketingdemos` ):

```javascript
{{#each context.journey.events.454181416.productListItems as |product|}}<tr> <th class="colspan33"><div class="acr-fragment acr-component image-container" data-component-id="image" style="width:100%;text-align:center;" contenteditable="false"><!--[if mso]><table cellpadding="0" cellspacing="0" border="0" width="100%"><tr><td style="text-align: center;" ><![endif]--><img src="{{context.journey.events.454181416.productListItems.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.imageUrl}}" style="height:auto;width:100%;" height="233" width="233"><!--[if mso]></td></tr></table><![endif]--></div></th> <th class="colspan66"><div class="acr-fragment acr-component" data-component-id="text" contenteditable="false"><div class="text-container" contenteditable="true"><p><span style="font-weight:700;">{{context.journey.events.454181416.productListItems.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.name}}</span></p></div></div><div class="acr-fragment acr-component" data-component-id="text" contenteditable="false"><div class="text-container" contenteditable="true"><p>${{context.journey.events.454181416.productListItems.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.price}}.00</p><p>Quantity: {{context.journey.events.454181416.productListItems.quantity}}</p></div></div></th></tr> {{/each}}
```

**總價：**

總計:`${{context.journey.events.1627840522.commerce.order.priceTotal}}.00`


>[!ENDTABS]