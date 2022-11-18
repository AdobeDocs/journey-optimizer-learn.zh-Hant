---
title: 建立夏季系列發佈 — 挑戰
description: 將夏季系列公告傳送至現有客戶的區段，以推廣新的Luma夏季系列。
kt: 8109
role: User
level: Beginner
last-substantial-update: 2022-11-16T00:00:00Z
hide: true
source-git-commit: 3cd8b1a5b98adbe822cd82db8c27137b534c16e3
workflow-type: tm+mt
source-wordcount: '1250'
ht-degree: 2%

---


# 建立夏季系列發佈 — 挑戰

![AJO夏季收藏發佈橫幅](/help/challenges/assets/email-assets/luma-transactional-onboarding-3.png)

| 挑戰 | 建立夏季系列公告 |
|---|---|
| 角色 | Journey Manager |
| 所需技能 | <ul><li>[建立區段](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html?lang=en)</li><li> [匯入及編寫 HTML 電子郵件內容](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-emails/import-and-author-html-email-content.html?lang=en)</li><li>[使用案例 - 讀取區段](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment.html?lang=en)</li> |
| 要下載的資產 | [季節性收集電子郵件檔案](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip) |

>[!NOTE]
> 這些練習是根據Luma樣本資料編製的。 我們建議設定一個訓練沙箱，並以範例資料進行設定。 請造訪教學課程 [將範例資料匯入Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/tutorials/import-sample-data.html?lang=zh-Hant) 以取得詳細指示。

## 故事

虛構的運動服裝公司Luma正尋求推廣其最新的服裝和服裝系列，並推動現有客戶的銷售。 Luma即將推出新的夏季系列，並想明確鎖定不同的客戶區段。

## 您的挑戰

Luma行銷團隊會要求您在Journey Optimizer中實施夏季系列行銷活動。

您的難題是在Journey Optimizer中建立歷程。 尤其是，您必須建立必要的區段、建立四則訊息，並建置歷程。

>[!NOTE]
> 如果您在共用訓練沙箱中工作，最佳作法是在您建立之任何元素的名稱中新增您的名稱或縮寫為首碼。

### 步驟1:定義區段 — 作用中客戶

>[!BEGINTABS]

>[!TAB 工作]

在Journey Optimizer中建立區段，稱為 **您的名稱 — 活動客戶**.

* 區段必須僅包含有效的Luma客戶。
* 活躍客戶的定義是在Luma的忠誠度計畫（銀級、金級、白金級或鑽石級）中擁有層級的客戶。


>[!TAB 成功標準]

在區段產生器中，您可以看到預估合格設定檔數。 如果您在使用Luma範例資料的訓練沙箱中工作，則 [!UICONTROL 估計合格用戶] 應該是292個500個用戶檔案。

**區段已新增合格設定檔：**

您可以導覽至區段「詳細資料」檢視上所列之其中一個設定檔，以檢查已新增至區段的設定檔資格。

在設定檔頁面上，檢查 [!UICONTROL 屬性] 以確認其符合資格：層次應為銀、金、鉑或鑽石。

![設定檔屬性](assets/C1-S1-profile-attributes.png)

您也可以檢查 [!UICONTROL 區段成員資格] 標籤：您的區段應已列出。

>[!NOTE]
>由於需要回填現有設定檔，因此現有設定檔可能需要最多24小時才會顯示區段成員資格。

![區段成員資格](assets/C1-S1-profile-segment-membership.png)

>[!TAB 檢查您的工作]

區段欄位： [!UICONTROL 屬性] > [!UICONTROL XDM個別設定檔] > [!UICONTROL 忠誠度] > [!UICONTROL 階層]

以下是區段的外觀：

![區段 — 活躍客戶](/help/challenges/assets/C1-S1.png)

在「編輯」區段畫面右下角的「事件」下方，勾選代碼。

程式碼應如下所示：

```javascript
loyalty.tier.equals("diamond", false) or loyalty.tier.equals("gold", false) or loyalty.tier.equals("platinum", false) or loyalty.tier.equals("silver", false)
```

>[!ENDTABS]


### 步驟2:建立歷程 — 夏季系列公告

>[!BEGINTABS]

>[!TAB 工作]

將夏季系列公告傳送至推廣新Luma夏季系列之現有客戶電子郵件區段。

一家機構向您提供了四份HTML檔案，其中包含電子郵件的設計： [下載季節性收集電子郵件檔案](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip)

建立以下歷程： `(your name) - Summer collection announcement` 根據下列准則：

1. 傳送Luma — 新的季節性收集公告電子郵件至Luma-Active Customers區段，將10%的受眾視為控制組
   * 訊息標題 `(your name)_Luma New Seasonal Collection Announcement`.
   * 主旨行 `(recipient's first name), the new Luma collection is here!`.
   * 使用提供的HTML檔案 *CherryCollectionEmail.html* 用於電子郵件內文。
2. 等候兩天，然後傳送後續電子郵件訊息，其中包含更具針對性的內容：
   * 男性客戶應接收 **Luma Men&#39;s Collection電子郵件**
      * 訊息標題： **（您的名稱）_Luma男裝系列**
      * 主旨行： **（收件人的名字），探索男子新運動裝備！**
      * 電子郵件內文： *MensCollectionEmail.html* 用於電子郵件內文。
   * 女性客戶應 **Luma Women&#39;s Collection電子郵件**
      * 訊息標題： **（您的名稱）_Luma Women&#39;s Collection**
      * 主旨行： **（收件者的名字），請探索Luma的Women Collection!**
      * 電子郵件內文： *WomensCollectionEmail.html*
   * 其他客戶應接收 **Luma — 收集電子郵件的折扣為20%**
      * 訊息標題： **（您的名稱）_Luma - 20%關閉集合**
      * 主旨行：**（收件者的名字），享受20%的銷售額！**
      * 電子郵件內文： *20OffCollectionEmail.html*
3. 在上方傳送目標電子郵件後，請等待兩天才開啟電子郵件
4. 如果目標電子郵件未在2天內開啟，請傳送 **Luma - 20 %off集合電子郵件** 作為最終的重新定位嘗試


>[!TAB 成功標準]

#### 預覽電子郵件

**電子郵件#1-新季節性收集公告**

使用身分命名空間預覽電子郵件： *電子郵件* 和Identity值： *Jenna_Palmer9530@emailsim.io*

* 主題行應為：珍娜，新的盧瑪系列來了！
* 電子郵件內文應與您在預覽中看到的內容相符： [新的季節性收集公告](/help/challenges/assets/email-assets/SeasonalCollectionEmail.html)


**電子郵件#2 - Luma Men&#39;s Collection**

向自己發證

* 輸入您的電子郵件地址
* 選取測試設定檔：Chris_Scott1244@emailsim.io

您應會收到電子郵件。 主題應該是「克里斯，探索男子新運動裝備！」 而電子郵件內文應與您在預覽中看到的內容相符： [鹿馬門集](/help/challenges/assets/email-assets/MensCollectionEmail.html)

**電子郵件訊息#3 - Luma Women&#39;s Collection**

使用身分命名空間預覽電子郵件： *電子郵件* 和Identity值： *Jenna_Palmer9530@emailsim.io*

* 主題行應為： *珍娜，探索盧瑪的女裝系列！*
* 電子郵件內文應與您在預覽中看到的內容相符： [鹿馬女子集](/help/challenges/assets/email-assets/WomensCollectionEmail.html)


**電子郵件訊息#4 - Luma 20%關閉集合**

使用身分命名空間預覽電子郵件： *電子郵件* 和Identity值： *Benny_Steer4909@emailsim.io*

* 主題行應為： *班尼，享受20%的銷售！*
* 電子郵件內文應與您在預覽中看到的內容相符： [Luma優惠20%](/help/challenges/assets/email-assets/20OOffCollectionEmail.html)

**別忘了發佈電子郵件！**

#### 測試您的歷程

>[!IMPORTANT]
>
>將歷程設定至測試模式之前：
>
>1. 請確定「讀取區段活動」的命名空間已設為「電子郵件」
>1. 對於每封電子郵件，覆寫電子郵件的預設「電子郵件」參數，以便將其傳送至您的電子郵件地址：
>1. 按一下眼睛符號來顯示隱藏的值。
>1. 在電子郵件參數中，按一下T符號（啟用參數覆蓋）

   >
   >      ![覆寫電子郵件參數](/help/challenges/assets/c3-override-email-paramters.jpg)
> 
>1. 按一下「Address（地址）」欄位
>1. 在下一個畫面中，以括弧新增您的電子郵件地址： *yourname@yourdomain* 在運算式編輯器中，按一下「確定」。

>


測試歷程，並將電子郵件傳送至您自己的帳戶：

1. 將歷程置於測試模式
2. 一次選取單一設定檔
3. 等待時間：將計時器設為120秒（在欄位中輸入）。
4. 觸發配置檔案入口
5. 您可以使用下列其中一個電子郵件地址作為設定檔識別碼，以測試每個分支：
   * 女性：珍娜·帕爾默：Jenna_Palmer9530@emailsim.io
   * 男性：克里斯·斯科特：Chris_Scott1244@emailsim.io
   * 未指定性別：本尼·斯蒂爾：Benny_Steer4909@emailsim.io

6. 一旦觸發設定檔入口，您應該會收到第一封電子郵件，標題應該會根據您所選取的設定檔個人化。
7. 歷程應繼續進入個別分支，您應會收到相關電子郵件（例如，如果您選擇Jenna，應會收到「Luma Women&#39;s Collection」電子郵件）。
8. 開啟第二封電子郵件，歷程應該會結束
9. 您可以重複步驟4。 - 7. 來檢查所有分支是否正常運作。
10. 若要測試逾時，請將等待時間設為30秒，然後再次觸發項目。
11. 請勿開啟您收到的電子郵件(請勿預覽電子郵件(!)) 讓等待時間過去。

您應會收到下列電子郵件：

* Luma — 新的季節性收藏公告
* 根據您使用的測試設定檔，您應會收到下列其中一封電子郵件：
   * 珍娜：鹿馬女子集
   * 克里斯：鹿馬門集
   * 本尼：Luma — 優惠20%
* 如果您未開啟第二封電子郵件：Luma,20%的優惠

>[!TAB 檢查您的工作]

以下是您歷程的外觀：

![歷程](/help/challenges/assets/c3-j1-journey.png)

**條件 — 控制組：**

![控制組](/help/challenges/assets/c3-j1-condition-control-group.png)

**條件 — 性別：**\

![條件 — 性別](/help/challenges/assets/c3-j1-condition-gender.png)
>[!ENDTABS]
