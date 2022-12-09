---
title: 建立夏季系列發佈 — 挑戰
description: 傳送夏季系列公告給現有客戶區段，以推廣新的Luma夏季系列。
kt: 8109
role: User
level: Beginner
last-substantial-update: 2022-11-16T00:00:00Z
hide: true
exl-id: ae457be7-2c67-4950-a072-1d7030b0e17b
source-git-commit: f5b0529ee13067fe945e32494a164959adfd7d6c
workflow-type: tm+mt
source-wordcount: '1175'
ht-degree: 2%

---

# 建立夏季系列發佈 — 挑戰

![AJO夏季收藏發佈橫幅](/help/challenges/assets/email-assets/luma-transactional-onboarding-3.png)

| 挑戰 | 建立夏季集合公告 |
|---|---|
| 角色 | Journey Manager |
| 所需技能 | <ul><li>[建立區段](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html?lang=en)</li><li> [匯入及編寫 HTML 電子郵件內容](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-emails/import-and-author-html-email-content.html?lang=en)</li><li>[使用案例 - 讀取區段](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment.html?lang=en)</li> |
| 要下載的資產 | [季節性收集電子郵件檔案](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip) |

## 故事

虛構的運動服裝公司Luma正在推廣其最新的服裝和服裝系列，並推動現有客戶的銷售。 Luma即將推出新的夏季系列，並且想要特別鎖定不同的客戶區段。

## 您的挑戰

Luma行銷團隊會要求您在Journey Optimizer中實施夏季系列行銷活動。 您面臨的挑戰是：

* 建立區段，定義哪些設定檔有資格接收促銷活動。
* 建立歷程.

### 步驟1:定義區段 — 作用中客戶

>[!BEGINTABS]

>[!TAB 工作]

#### 在中建立區段 [!DNL Journey Optimizer]

* 在中建立區段 [!DNL Journey Optimizer] 呼叫 *有效客戶*.
* 區段必須僅包含有效的Luma客戶。
* 活躍客戶是指在Luma的忠誠度計畫（銅、銀、金或白金）中擁有層級的客戶。


>[!TAB 成功標準]

在區段產生器中，您可以看到預估合格設定檔數。 如果您使用訓練沙箱資料，1.29 K中有約753個合格設定檔。

>[!NOTE]
>由於需要回填現有設定檔，因此現有設定檔可能需要最多24小時才會顯示區段成員資格。

**區段已新增合格設定檔：**

您可以導覽至區段詳細資料檢視上所列之其中一個設定檔，以檢查已新增至區段的設定檔是否符合資格。

在設定檔頁面上，檢查 [!UICONTROL 屬性] 以確認其符合資格：層次應為銀、金、鉑或鑽石。

![設定檔屬性](assets/C1-S1-profile-attributes.png)

您也可以檢查 [!UICONTROL 區段成員資格] 標籤：您的區段應已列出。

![區段成員資格](assets/C1-S1-profile-segment-membership.png)

>[!TAB 檢查您的工作]

區段欄位： [!UICONTROL 屬性] > [!UICONTROL XDM個別設定檔] > [!UICONTROL 忠誠度] > [!UICONTROL 階層]

以下是區段的外觀：

![區段 — 活躍客戶](/help/challenges/assets/C1-S1.png)

程式碼應如下所示：

```javascript
stringCompare("equals", loyalty.tier, ["diamond", "gold", "platinum", "silver"], false)
```

>[!ENDTABS]


### 步驟2:建立歷程 — 夏季集合公告

>[!BEGINTABS]

>[!TAB 工作]

#### 傳送夏季收藏公告

一家機構向您提供了四份HTML檔案，其中包含電子郵件的設計：

* `SeasonalCollectionEmail.html`
* Luma Men&#39;s Collection電子郵件
* Luma Women&#39;s Collection電子郵件
* Luma — 收集電子郵件的折扣為20%

1. [下載季節性收集電子郵件檔案](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip).

2. 建立以下歷程： *Luma — 夏季系列發佈* 根據下列准則：

   1. 傳送 *Luma — 全新夏季系列發佈* 電子郵件至 *有效客戶* 區段，將10%的受眾視為控制組
      * 訊息標題 *Luma — 夏季系列發佈*
      * 主旨行 *（收件者的名字），新的Luma夏季系列就在此！*
      * 使用提供的HTML檔案 `SeasonalCollectionEmail.html` 用於電子郵件內文。
   2. 等候兩天，然後傳送後續電子郵件訊息，其中包含更具針對性的內容：
      * 男性客戶應接收 **鹿馬門集** 電子郵件。
         * 訊息標題： *鹿馬門集*
         * 主旨行： *（收件人的名字），探索男子新運動裝備！*
         * 電子郵件內文： `MensCollectionEmail.html` 用於電子郵件內文。
      * 女性客戶應 **鹿馬女子集** 電子郵件。
         * 訊息標題： *鹿馬女子集*
         * 主旨行： *（收件者的名字），請探索Luma的Women Collection!*
         * 電子郵件內文： `WomensCollectionEmail.html`
      * 其他客戶應接收 **Luma - 20%優惠** 電子郵件。
         * 訊息標題： *Luma - 20%優惠*
         * 主旨行： *（收件者的名字），享受20%的銷售額！*
         * 電子郵件內文： `20OOffCollectionEmail.html`
   3. 在上方傳送目標電子郵件後，請等待兩天才開啟電子郵件
   4. 如果目標電子郵件未在2天內開啟，請傳送 **Luma - 20 %off集合電子郵件** 作為最終的重新定位嘗試


>[!TAB 成功標準]

#### 預覽電子郵件

**電子郵件訊息#1 - Luma — 夏季集合公告**

預覽電子郵件：

1. 新增測試設定檔：露易絲·佩蒂：
   1. 身份命名空間： *Luma CRM ID*
   2. 身分值： *d1f132f9f9502bba047a6ec86c4b61f9*

結果:
* 主題行應為：露易絲，新的盧瑪系列來了！
* 電子郵件內文應與您在預覽中看到的內容相符： [新的季節性收集公告](/help/challenges/assets/email-assets/SeasonalCollectionEmail.html)


**電子郵件#2 - Luma Men&#39;s Collection**

向自己發送證明：

1. 新增測試設定檔：斯坦利·斯托克：
   1. 身份命名空間： *Luma CRM ID*
   1. 身分值： `4f34057d9d9e792c28ba18ecae378e98`
1. 選取測試設定檔：斯坦利·斯托克。
1. 自己傳證。

結果:\
您應會收到電子郵件。 主題行應為 *斯坦利，探索男子新運動裝備！* 而電子郵件內文應與您在預覽中看到的內容相符： [鹿馬門集](/help/challenges/assets/email-assets/MensCollectionEmail.html)

>[!NOTE]
>你可能需要幾分鐘才能收到證明。

**電子郵件#3 - Luma Women&#39;s Collection**

使用測試設定檔預覽電子郵件 *露易絲·佩蒂。*

* 主題行應為： *露易絲，探索盧瑪的女裝系列！*
* 電子郵件內文應與您在預覽中看到的內容相符： [鹿馬女子集](/help/challenges/assets/email-assets/WomensCollectionEmail.html)


**電子郵件訊息#4 - Luma 20%關閉集合**

使用測試設定檔預覽電子郵件 *露易絲·佩蒂。*

* 主題行應為： *露易絲，享受20%的銷量！*
* 電子郵件內文應與您在預覽中看到的內容相符： [Luma優惠20%](/help/challenges/assets/email-assets/20OOffCollectionEmail.html)


#### 測試您的歷程

>[!IMPORTANT]
>
>將歷程設定至測試模式之前：
>
>1. 請確定 [!UICONTROL 閱讀區段活動] 命名空間已設為 **Luma CRM id(lumaCrmId)**
>1. 對於每封電子郵件，覆寫電子郵件的預設電子郵件參數，以便將其傳送至您的電子郵件地址：
   >    * 按一下眼睛符號來顯示隱藏的值。
   >    * 在電子郵件參數中，按一下T符號（啟用參數覆寫）。

      >
      >      ![覆寫電子郵件參數](/help/challenges/assets/c3-override-email-paramters.jpg)
   > 
   >    * 按一下 [!UICONTROL 地址] 欄位
   >    * 在下一個畫面中，以括弧新增您的電子郵件地址： `"yourname@yourdomain"` 在運算式編輯器中，按一下「確定」。

>


測試歷程，並將電子郵件傳送至您自己的帳戶：

1. 將歷程置於測試模式。
1. 選擇 **[!UICONTROL 一次單一設定檔]**.
1. 等待時間：將計時器設為120秒（在欄位中輸入）。
1. 觸發配置檔案入口
1. 您可以使用以下任一項來測試每個分支 *Luma CRM Id* 作為設定檔識別碼：
   * 女性：Leora Dietsche，身份值：`a8f14eab3b483c2b96171b575ecd90b1`
   * 男性：Stanleigh Stooke，身份值： `4f34057d9d9e792c28ba18ecae378e98`
   * 未指定性別：Louise Petti，身份價值： `d1f132f9f9502bba047a6ec86c4b61f9`

1. 觸發設定檔入口後，您應會收到第一封電子郵件。 標題應根據您選取的設定檔進行個人化。
1. 歷程應繼續進入個別分支，您應會收到相關電子郵件(例如，如果您選擇 *珍娜*，您應會收到 *鹿馬女子集* 電子郵件)。
1. 開啟第二封電子郵件，歷程應該會結束。
1. 您可以重複步驟4。 - 7. ，以檢查分支是否正常運作。
1. 若要測試逾時，請將等待時間設為30秒，然後再次觸發項目。
1. 請勿開啟您收到的電子郵件(請勿預覽電子郵件(!)) 讓等待時間過去。

您應會收到下列電子郵件：

* Luma — 新的季節性收藏公告
* 根據您使用的測試設定檔，您應會收到下列其中一封電子郵件：
   * 萊奧拉：鹿馬女子集
   * 斯坦利：鹿馬門集
   * 露易絲：Luma — 優惠20%
* 如果您未開啟第二封電子郵件：Luma,20%的優惠

>[!TAB 檢查您的工作]

以下是您歷程的外觀：

![歷程](/help/challenges/assets/c3-j1-journey.png)

**條件 — 控制組：**

![控制組](/help/challenges/assets/c3-j1-condition-control-group.png)

**條件 — 性別：**\

![條件 — 性別](/help/challenges/assets/c3-j1-condition-gender.png)
>[!ENDTABS]
