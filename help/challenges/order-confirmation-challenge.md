---
title: 建立訂單確認電子郵件
description: 測試您關於如何建立和個人化交易式訊息的知識
kt: 7531
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: ec86e2ac-081d-47aa-a948-007107baa2b4
source-git-commit: 7a178b9c523ead0cf27aaa87d25b3752ef53f519
workflow-type: tm+mt
source-wordcount: '692'
ht-degree: 4%

---


# 建立訂單確認電子郵件

![訂購確認](/help/challenges/assets/email-assets/luma-transactional-order-confirmation.png)

| 挑戰 | 建立訂單確認交易式電子郵件 |
|---|---|
| 角色 | Journey Manager |
| 所需技能 | <ul><li>[使用訊息編輯器建立電子郵件內容](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-email-content-with-the-message-editor.html?lang=en)</li> <li>[使用內容事件資訊進行個人化](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-contextual-event-information-for-personalization.html?lang=en)</li><li>[使用協助程式功能進行個人化](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-helper-functions-for-personalization.html?lang=en)</li></ul> |
| 要下載的資產 | [訂購確認資產](/help/challenges/assets/email-assets/order-confirmation-assets.zip) |

## 故事

Luma正在啟動其線上商店，希望在客戶下訂單後，提供訂單確認電子郵件，以確保提供良好的客戶體驗。



## 您的挑戰

建立歷程，當Luma客戶完成線上訂單時傳送訂單確認電子郵件。 盧瑪

>[!BEGINTABS]

>[!TAB 工作]

1. 建立以下歷程： `Luma - Order Confirmation`
2. 使用事件： `LumaOnlinePurchase` 作為觸發器
3. 建立訂單確認電子郵件，名為 `Luma - Order Confirmation`:

* 類別交易 — 請務必選取交易式電子郵件表面
* 主旨行必須與收件者的名字個人化，且必須包含「感謝您購買」的片語
* 使用 `Luma - Order summary` 範本並加以修改：

電子郵件的結構應如下：
<table>
<tr>
<td>
  <div>
     <strong> 標題區段</strong>
      </div>
  </td>
  <td>
    <strong>Luma標誌</strong>
      <p>
     <li>luma_logo.png</li>
    <li>應該會有luma網站的連結：https://publish1034.adobedemo.com/content/luma/us/en.html</li>
    <p>
    </td>
  </tr>
  <tr>
  <td>
  <div>
    <strong>訂購確認部分
    </strong>
  </td>
  <td>
    <p>
    <strong>文字</strong><p>
    <em>嗨{名字}</em><p>
    <li>對齊方式：lef  </li>
   <li>文本顏色：rgb(69, 97, 162)#4461a2; 
   <li>字型大小：20px</li>
   <div>
    <p>
     <em>已下訂單。
    <p>您的包出貨後，我們會向您發送一封包含跟蹤號碼的電子郵件，以便您跟蹤訂單。</p></em>
    </strong>
    </tr>
  </td>
 <td>
  <div>
     <strong> 收貨區</strong>
      </div>
      <p><li>將範本中的硬式編碼地址更換為運送地址 
      <li>詳細資料是來自事件的情境屬性（街道、城市、郵遞區號、州）
      <li>名字和姓氏來自設定檔
      <li> 移除折扣、總計、到達</p>
  </td>
  <td>
  <p> 收貨方：</p>
      <em>名字姓氏<br>
      地址<br></em></p>
  </td>
 <tr>
<td>
  <div>
     <strong>訂單詳細資訊部分</strong>
      </div>
       <p><li>在 <b>收貨方</b> 區段和 <b>檢視順序</b> 按鈕
      </p><br>
      <p><b>提示:</b>
      <li>這是內容事件資訊。
      <li>使用[!UICONTROL幫助程式函式]:[!UICONTROL各]
      <li>切換至程式碼編輯器格式以新增內容資料。
      <li>使用DIV標籤將資訊放入容器中。
  </td>
  <td>
    <strong>Header</strong>
    <p>
    <em>順序：'purchaseOrderNumber'</em>
    </p>
    <strong>訂購的產品清單：
  </strong>
  <p>每個項目的格式應如下所示：
   <img alt="訂購" src="./assets/c2-order.png"> 
</p>
<strong>產品影像：</strong>
<li>類別：購物車椅
<li>樣式：邊框框：min-height:40px</li>
<li>邊框間距上下：20px</li>
<li>邊框間距左側：80px</li>
<li>border-radius:0px</li>
<li>作為容器的背景影像</li>
<li>背景位置：0% 50%</li>
<li>背景大小：60px</li>
<li>背景重複：無重複</li>
<p>
<strong>價格:</strong>
<li>格式= H5</li>
<li>style = box-sizing:border-box</li>
<li>margin-bottom:5px</li>
<li>margin-top:0px;</li>
<p>
<strong>名稱和數量：</strong>
<li>class=text-small</li>
<li>style=box-sizing:邊框框</li>
<li>邊框間距：5px</li>
<li>顏色：rgb(101, 106, 119)</li>
<li>font-size:14px</li>
<p>
</td>
  </tr>
</table>


>[!TIP]
>
>若要讓您疑難排解歷程，最佳實務是在逾時或錯誤的情況下，為所有訊息動作新增替代路徑。

>[!TAB 成功標準]

觸發您在測試模式中建立的歷程，並傳送電子郵件給您自己：

1. 按一下眼睛符號來顯示隱藏的值：
   1. 在電子郵件參數中，按一下T符號（啟用參數覆蓋）
      ![覆寫電子郵件參數](/help/challenges/assets/c3-override-email-paramters.jpg)
   2. 按一下「Address（地址）」欄位
   3. 在下一個畫面中，以括弧新增您的電子郵件地址： *yourname@yourdomain* 在運算式編輯器中，按一下「確定」。
2. 將歷程置於測試模式
3. 使用下列參數觸發事件：
   * 將設定檔識別碼設為：身分值：`a8f14eab3b483c2b96171b575ecd90b1`
   * 事件類型：commerce.purchases
   * 名稱：雪碧瑜伽伴侶套件
   * 數量：1
   * 總價：61
   * 訂單編號：6253728
   * SKU:24-WG080
   * productImageURL: <https://publish1034.adobedemo.com/content/dam/luma/en/products/gear/fitness-equipment/luma-yoga-kit-2.jpg>
   * 

您應會收到包含指定產品的個人化購買確認電子郵件。

* 主旨行應該具有測試設定檔的名字：萊奧拉
* 訂單詳細資訊區段應填入您在測試時輸入的訂單詳細資料
* 此 *收貨方* 區段應該會包含您的測試設定檔的城市和郵遞區號：

   華盛頓特里埃爾泰勒斯43913 20099



>[!TAB 檢查您的工作]

**歷程**

![歷程](/help/challenges/assets/c2-journey.png)


**電子郵件**

**主旨行：**

{{ profile.person.name.firstName }}，感謝您的購買！

**收貨區域：**

以下是您的程式碼應呈現的外觀：

```javascript
{{ profile.person.name.firstName }} {{ profile.person.name.lastName }}
{{context.journey.events.454181416.commerce.shipping.address.street1}}
{{context.journey.events.454181416.commerce.shipping.address.city}}, {{context.journey.events.454181416.commerce.shipping.address.state}} {{context.journey.events.454181416.commerce.shipping.address.postalCode}}
```

*event.45481416* 會是另一個數字。

提示：個人化每一行

**訂單詳細資訊部分：**

![訂單詳細資訊部分](/help/challenges/assets/c2-order-detail-section.png)

以下是您的程式碼應呈現的外觀：

標頭:

```javascript
Order: {{context.journey.events.1627840522.commerce.order.purchaseOrderNumber}}
```

產品清單：

使用協助程式函式「each」來建立產品清單。 以下是您的程式碼應呈現的外觀：

```javascript
{{#each context.journey.events.1911672547.productListItems as|product|}}
<div class="cart-item-chair" style="box-sizing:border-box;min-height:40px;padding-top:20px;padding-bottom:20px;padding-left:80px;border-radius:0px;background-image:url({{product._wwfovlab065.productImageURL}});background-position:0% 50%;background-size:60px;background-repeat:no-repeat;">
<h5 style="box-sizing:border-box;margin-bottom:5px;font-size:16px;line-height:20px;margin-top:0px;">${{product.priceTotal}}.00</h5>
<div class="text-small" style="box-sizing:border-box;padding-top:5px;color:rgb(101, 106, 119);font-size:14px;">{{product.name}}</div><div class="text-small" style="box-sizing:border-box;padding-top:5px;color:rgb(101, 106, 119);font-size:14px;">Quantity: {{product.quantity}}</div></div><div class="divider-small" style="box-sizing:border-box;height:1px;margin-top:10px;margin-bottom:10px;background-color:rgb(209, 213, 223);"> </div>
{{/each}}

Total: ${{context.journey.events.1627840522.commerce.order.priceTotal}} 
```

**客戶資訊部分**

![客戶地址](assets/c2-customer-information.png)

個人化應該如下所示：

```javascript
{{profile.homeAddress.street1}}
{{profile.homeAddress.city}},{{profile.homeAddress.state}} {{profile.homeAddress.postalCode}}
```

>[!ENDTABS]