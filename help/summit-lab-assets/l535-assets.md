---
title: L535速查表
description: 本頁有文字和連結，用於L535 Summit Lab。
feature: In App, SMS, Push, Email
doc-type: article
role: User
level: Beginner
recommendations: noDisplay, noCatalog
hide: true
hidefromtoc: true
exl-id: 1c3f4341-1293-463d-bee0-57440fcff23a
source-git-commit: 34e2ae2ed4db21415aede46a27091b896277b70f
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 22%

---

# Summit Lab L535：速查表

本頁有文字和連結，用於L535 Summit Lab。 它可讓您將內容複製並貼上到 Journey Optimizer 訊息。

## 連結

* [SecurFinancial網站](https://dsn.adobe.com/web/hausmann-FTTN?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFub255bW91cyIsImVtYWlsIjoiYW5vbnltb3VzQGFkb2JlLmNvbSIsIm5hbWUiOiJBbm9ueW1vdXMiLCJpc1N1cGVyVXNlciI6ZmFsc2UsImlzc3VlciI6ImhhdXNtYW5uIiwicHJvamVjdHMiOnsiaGF1c21hbm4tRlRUTiI6InZpZXcifSwiaWF0IjoxNzQwNzU2NTYxLCJleHAiOjE3NDMzNDg1NjF9.ryOTsqDH9B33436RlIo4AHFxx8aGjNEMqv9FAxLZb9U){target="_blank"}
* [Adobe Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:ajo-summit-lab/journey-optimizer/journeys){target="_blank"}
* [L535活頁簿](/help/summit-lab-assets/assets/summit_lab_manual_l535-final-v4.pdf){target="_blank"}
* [下載應用程式](https://demo-system-next.s3.amazonaws.com/dxdemo/summit/index.html){target="_blank"}

## 複製並貼上練習內容

### 練習2.1 — 登入Journey Optimizer

使用下列詳細資料登入：

電子郵件地址：    L535+*您的座位號碼*@adobeeventlab.com

密碼：       Adobe4Summit！


### 練習2.3 — 撰寫電子郵件訊息

#### 提示

```
Generate a welcome email for new SecurFinancial customers who just opened a new checking account. 
Add a call to action to install the SecurFinancial mobile app.
```

### 練習3.1 — 將動態內容套用至簡訊訊息

#### 程式碼

```
{%#if select _Push_details1 from profile.pushNotificationDetails where
_Push_details1.token.isNotNull()%}
Welcome to your new SecurFinancial checking account! Discover the
SecurFinancial mobile app, designed for effortless banking. Manage accounts,
transfer funds, and monitor transactions securely, anytime, anywhere. Open the
app
{%else%}
Welcome to your new SecurFinancial checking account! Discover the
SecurFinancial mobile app, designed for effortless banking. Manage accounts,
transfer funds, and monitor transactions securely, anytime, anywhere. Click here
to install the app: https://demo-systemnext.
s3.amazonaws.com/dxdemo/summit/index.html
{%/if%} 
```

### 練習4.2 — 設定處理方式

#### 標題

```
Welcome to SecurFinancial
```

#### 內文

```
Did you know you can find an ATM near in the SecurFinancial app? Try it now!
```

#### URL

```
dxdemo://atm
```

### 練習6 — 內容卡

#### 標題

```
Welcome to SecurFinancial!
```

#### 內文

```
Thank you for downloading the app. You can find ATMs, track your spending and more. All within the app.
```

#### 媒體 URL

```
https://demo-system-next.s3.amazonaws.com/assets/securfinancial/home-loan.jpg
```

#### 按鈕標題

```
Find ATMs
```

#### 目標 URL

```
dxdemo://atm
```

## 影像

![SecureFinancial標誌](/help/summit-lab-assets/assets/SecureFinancial-logo.png)


![行動電話](/help/summit-lab-assets/assets/online-banking-app-01.png)


