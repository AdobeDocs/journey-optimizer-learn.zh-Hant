---
title: L731 速查表
description: 本頁面包含 L731 Summit Lab 正在使用的文字及連結。
feature: In App, SMS, Push, Email
doc-type: article
role: User
level: Beginner
recommendations: noDisplay, noCatalog
hide: true
hidefromtoc: true
exl-id: ffc5e8c8-8729-4e7e-aa51-d74f91b0cf29
source-git-commit: ea4ba49056ad3e575c0953ad963966bcecf54c9f
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 53%

---

# Summit Lab L731- 速查表

本頁面包含 L731 Summit Lab 正在使用的文字及連結。 它可讓您將內容複製並貼上到 Journey Optimizer 訊息。

## 練習 1.1 - 下載並安裝應用程式

掃描QR碼以下載應用程式

>[!BEGINTABS]

>[!TAB iOS]

![適用於 iOS 的 QR 碼](/help/assets/lab731-ios-qr-code.png)

系統會要求您安裝Testflight（步驟1至4）。 安裝Testflight後，請按照步驟5到8安裝Vegas Stay App:

<table>
<tr>
</tr>
<tr>
<td>
 <div>
      <p>
      <b>步驟 1 </b>
      <p>
      <a href="Step 1:">
        <img alt="testflight 1" src="../assets/l731-ios-install/ios-install-1.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>步驟 2 </b>
      <p>
      <a href="Step 1:">
        <img alt="testflight 1" src="../assets/l731-ios-install/ios-install-2.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>步驟 3 </b>
      <p>
      <a href="Step 1:">
        <img alt="testflight 1" src="../assets/l731-ios-install/ios-install-3.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>步驟 4 </b>
      <p>
      <a href="Step 4">
        <img alt="testflight 1" src="../assets/l731-ios-install/ios-install-4.PNG"/>
      </a>
      </div>
  </td>
  </tr>
  <tr>
<td>
 <div>
      <p>
      <b>步驟 5 </b>
      <p>
      <a href="Step 1:">
        <img alt="testflight 1" src="../assets/l731-ios-install/ios-install-5.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>步驟 6 </b>
      <p>
      <a href="Step 1:">
        <img alt="testflight 1" src="../assets/l731-ios-install/ios-install-6.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>步驟 7 </b>
      <p>
      <a href="Step 1:">
        <img alt="testflight 1" src="../assets/l731-ios-install/ios-install-7.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>步驟 8 </b>
      <p>
      <a href="Step 4">
        <img alt="testflight 1" src="../assets/l731-ios-install/ios-install-8.PNG"/>
      </a>
      </div>
  </td>
  </tr>
</table>
&gt;[!TAB Android™]

![Android適用的QR碼](/help/assets/lab731-android-qr-code.png)

如果您使用Android模擬器，請使用此連結： [https://ajolab.s3.amazonaws.com/ajolabapp-release.apk](https://ajolab.s3.amazonaws.com/ajolabapp-release.apk)

由於應用程式未在Google Play商店註冊，因此您會收到警告訊息：

![Android警告畫面](/help/assets/lab731-install-android.png)

按一下 **仍要安裝**

>[!ENDTABS]

## 練習 1.3：登入 Adobe Journey Optimizer

[按一下這裡以登入 Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-2023-ajo-lab/journey-optimizer/home)

**登入詳細資料：**

* **用戶名：** `L731+<your seat number>@summitlab.us` (範例：L731+001@summitlab.us)
* **密碼：** Adobe2023!


## 練習 2.1 建立應用程式內行銷活動

| 欄位 | 文字 | 連結 |
|----|----|----|
| 行銷活動名稱 | `<your seat number> March Vegas Campaign` |  |
| 符合 | 現在預訂 |  |
| 媒體 URL 選項 |  | https://mcfadyen.com/wp-content/uploads/2023/01/Adobe-Summit-2023-Banner.png |
| 標題 | 正在發生且正在運行！ |  |
| 內文 | Adobe Summit 將於 2023 年 3 月 21 日至 23 日重返拉斯維加斯。準備好迎接鼓舞人心的演講者、技能擴展會議以及認識新的人。 |  |
| 按鈕 | 立即預訂酒店並節省 10% 費用 | lab://booking?suite=presidential&amp;discount=10 |
| 按鈕：互動式事件 | 應用程式內 CTA |  |
| 基礎 URL |  | iOS:lab:// <br>Android™:https://lab |


## 第 3 課建立全通路歷程

**歷程標籤：**
<your seat number>  — 歡迎歷程

>[!BEGINTABS]

>[!TAB 推送訊息]

**標籤：**
歡迎訊息

**標題:**\
歡迎來到 Vegas Stay！

**內文:**\
免排隊並使用行動應用程式辦理登記入住手續

**深層連結：** lab://checkin

**媒體:**

https://experienceleague.adobe.com/docs/journey-optimizer-learn/assets/vegas_online_check_in.jpg?lang=en


這是我們用於推播通知的影像：

![線上登記入住](/help/assets/vegas_online_check_in.jpg)

>[!TAB SMS訊息]

**標籤：**
歡迎訊息

**訊息：**
歡迎來維加斯逗留。 免排隊並使用行動應用程式辦理登記入住手續：lab://checkin

>[!TAB 電子郵件訊息]

**標籤：**
確認訊息

**主旨行：**
{{profile.person.name.firstName}}，您已登入，現在請查看我們的優惠方案以供您入住！

>[!ENDTABS]
