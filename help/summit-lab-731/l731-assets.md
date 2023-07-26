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
source-git-commit: 01869838bb08e0d7848934f345afdd54824aaa75
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 90%

---

# Summit Lab L731- 速查表

本頁面包含 L731 Summit Lab 正在使用的文字及連結。 它可讓您將內容複製並貼上到 Journey Optimizer 訊息。

## 練習 1.1 - 下載並安裝應用程式

掃描 QR 碼以下載應用程式

>[!BEGINTABS]

>[!TAB iOS]

![適用於 iOS 的 QR 碼](/help/assets/lab731-ios-qr-code.png)

>[!IMPORTANT]
>
>若系統要求提供兌換代碼，請關閉 TestFlight 應用程式，然後再次掃描 QR 碼。
>
>請允許通知。
>

系統會要求您安裝 Testflight，步驟 1 至 4。 安裝 Testflight 後，請按照步驟 5 到 8 安裝 Vegas Stay 應用程式：

<table>
<tr>
</tr>
<tr>
<td>
 <div>
      <p>
      <b>步驟 1 </b>
      <p>
      <a>
        <img alt="testflight 1" src="../assets/l731-ios-install/ios-install-1.png"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>步驟 2 </b>
      <p>
      <a>
        <img alt="testflight 1" src="../assets/l731-ios-install/ios-install-2.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>步驟 3 </b>
      <p>
      <a>
        <img alt="testflight 1" src="../assets/l731-ios-install/ios-install-3.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>步驟 4 </b>
      <p>
      <a>
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
      <a>
        <img alt="testflight 1" src="../assets/l731-ios-install/ios-install-5.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <a>
     <b>步驟 6 </b>
      <p>
        <img alt="testflight 1" src="../assets/l731-ios-install/ios-install-6.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <a>
      <b>步驟 7 </b>
      <p>
        <img alt="testflight 1" src="../assets/l731-ios-install/ios-install-7.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <a>
      <b>步驟 8 </b>
      <p>
        <img alt="testflight 1" src="../assets/l731-ios-install/ios-install-8.PNG"/>
      </a>
      </div>
  </td>
  </tr>
</table>

>[!TAB Android]

![適用於 Android 的 QR 碼](/help/assets/lab731-android-qr-code.png)

由於應用程式未於 Google Play 商店註冊，因此您會收到警告訊息：

![Android 警告畫面](/help/assets/lab731-install-android.png)

按一下&#x200B;**仍要安裝**

>[!ENDTABS]

## 練習 1：登入 Adobe Journey Optimizer

[按一下這裡以登入 Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-2023-ajo-lab/journey-optimizer/home){target="_blank"}

**登入詳細資料**

* **使用者名稱：**`L731+<your seat number>@summitlab.us`(範例：L731+001@summitlab.us)
* **密碼：Adobe2023!**


## 練習 2 建立應用程式內行銷活動

| 區域 | 欄位 | 文字 | 連結 |
|----|----|----|----|
| **屬性** | 行銷活動名稱 | `<your seat number> Vegas Stay Campaign` |  |
| **觸發器** | 狀態 | 現在預訂 |  |
| **編輯內容：** 媒體 | 媒體 URL 選項 |  | https://i.ibb.co/NstLhjW/Firefly-Poster-with-heading-Adobe-Max-84773.jpg |
| **編輯內容：** 內容 | 標題 | 取得早鳥折扣！ |  |
| **編輯內容：** 內容 | 內文 | Adobe Max 重返拉斯維加斯。 準備好迎接鼓舞人心的演講者、技能擴展會議以及認識新的人。立即預訂套裝，可享有九折優惠。 |  |
| **編輯內容：** 按鈕 | 按鈕 | 取得九折優惠！ | lab://booking?suite=presidential&amp;discount=10 |
| **編輯內容：** 按鈕 | 互動事件 | 應用程式內 CTA |  |
| **在裝置上預覽** | 要在裝置上預覽的基本URL |  | **iOS:** lab:// <br>**Android**: https://lab |

## 練習 3：建立推播通知

| 欄位 | 文字 | 連結 |
|----|----|----|
| 行銷活動名稱 | `<your seat number> Max Push Campaign` |  |
| 標題 | 您好！ |  |
| 內文 | 您知道嗎，Adobe Max 即將重返拉斯維加斯。立即預訂您的房間，可享有九折優惠。 |  |
| 媒體 URL 選項 |  | https://i.ibb.co/1M0BnZn/Firefly-Big-conference-big-stage-with-ADBE-text-on-screen-40178.jpg |
