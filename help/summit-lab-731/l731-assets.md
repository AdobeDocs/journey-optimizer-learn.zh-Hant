---
title: L731速查表
description: 本頁面包含 L731 Summit Lab 正在使用的文字及連結。
feature: In App, SMS, Push, Email
doc-type: article
role: User
level: Beginner
recommendations: noDisplay, noCatalog
hide: true
hidefromtoc: true
exl-id: ffc5e8c8-8729-4e7e-aa51-d74f91b0cf29
source-git-commit: c0b7fa47fac1ad16121d0f568de358c83de44a90
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 51%

---

# Summit Lab L731  — 速查表

本頁面包含 L731 Summit Lab 正在使用的文字及連結。 它可讓您將內容複製並貼上到 Journey Optimizer 訊息。

## 練習1.1 — 下載並安裝應用程式

掃描QR碼以下載應用程式

>[!BEGINTABS]

>[!TAB iOS]

![適用於iOS的QR碼](/help/assets/lab731-ios-qr-code.png)

>[!TAB Android]

![Android適用的QR碼](/help/assets/lab731-android-qr-code.png)

>[!ENDTABS]

## 練習1.3:登入Adobe Journey Optimizer

[按一下這裡以登入Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-2023-ajo-lab/journey-optimizer/home)

**登入詳細資料：**

* **用戶名：** `L731+<your seat number>@summitlab.us` (範例：L731+001@summitlab.us)
* **密碼：** Adobe2023!


## 練習 2.1 建立應用程式內行銷活動

| 欄位 | 文字 | 連結 |
|----|----|----|
| 促銷活動名稱 | `<your seat number> March Vegas Campaign` |  |
| 符合 | 布恩 |  |
| 媒體 URL 選項 |  | https://mcfadyen.com/wp-content/uploads/2023/01/Adobe-Summit-2023-Banner.png |
| 標題 | 正在發生，而且是線上即時！ |  |
| 內文 | Adobe Summit 將於 2023 年 3 月 21 日至 23 日重返拉斯維加斯。準備好迎接鼓舞人心的演講者、技能擴展會議以及認識新的人。 |  |
| 按鈕 | 立即預訂酒店並節省 10% 費用 | lab://booking?suite=presidential&amp;discount=10 |
| 按鈕：互動式事件 | 應用程式內CTA |  |
| 基礎 URL |  | iOS:lab:// <br>Android:https://lab |


## 第 3 課建立全通路歷程

>[!BEGINTABS]

>[!TAB 推送訊息]

**標題:**\
維加斯逗留歡迎你！

**內文:**\
免排隊並使用行動應用程式辦理登記入住手續

**深層連結：** lab://checkin

**媒體:**

https://experienceleague.adobe.com/docs/journey-optimizer-learn/assets/vegas_online_check_in.jpg?lang=en


這是我們用於推播通知的影像：

![線上登記入住](/help/assets/vegas_online_check_in.jpg)

>[!TAB SMS訊息]

**訊息：**
歡迎來維加斯逗留。 免排隊並使用行動應用程式辦理登記入住手續：lab://checkin

>[!TAB 電子郵件訊息]

**主旨行：**
{{profile.person.name.firstName}}，您已登入，現在請查看我們的優惠方案以供您入住！

>[!ENDTABS]