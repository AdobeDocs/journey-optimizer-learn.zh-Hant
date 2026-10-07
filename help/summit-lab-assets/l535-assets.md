---
title: L535速查表
description: 本頁有文字和連結，用於L535 Summit Lab。
feature: In App, SMS, Push, Email
doc-type: article
role: User
level: Beginner
recommendations: noDisplay, noCatalog
hide: true
hidefromtoc: 'yes'
exl-id: 1c3f4341-1293-463d-bee0-57440fcff23a
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: 6eb7d9ad-3477-58b3-957a-080ef7738a30
    internal-label: SMS
  - id: 66e1fd99-672d-5d64-aa58-eca107f0fbae
    internal-label: Push
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
    internal-label: Email
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
    internal-label: Communication channels
subfeature_v2:
  - id: cc5c44e2-54a1-4927-b794-442cd87d8f74
    internal-label: In App channel
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 15%
---
# Summit Lab L535：速查表

本頁有文字和連結，用於L535 Summit Lab。 它可讓您將內容複製並貼上到您在 Journey Optimizer 中的訊息。

## 連結

* [SecurFinancial網站](https://dsn.adobe.com/web/hausmann-FTTN?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFub255bW91cyIsImVtYWlsIjoiYW5vbnltb3VzQGFkb2JlLmNvbSIsIm5hbWUiOiJBbm9ueW1vdXMiLCJpc1N1cGVyVXNlciI6ZmFsc2UsImlzc3VlciI6ImhhdXNtYW5uIiwicHJvamVjdHMiOnsiaGF1c21hbm4tRlRUTiI6InZpZXcifSwiaWF0IjoxNzQwNzU2NTYxLCJleHAiOjE3NDMzNDg1NjF9.ryOTsqDH9B33436RlIo4AHFxx8aGjNEMqv9FAxLZb9U){target="_blank"}
* [Adobe Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:ajo-summit-lab/journey-optimizer/journeys){target="_blank"}
* [L535活頁簿](/help/summit-lab-assets/assets/summit_lab_manual_l535-final-v4.pdf){target="_blank"}
* [下載應用程式](https://demo-system-next.s3.amazonaws.com/dxdemo/summit/index.html){target="_blank"}

## 複製並貼上練習內容

### 練習2.1 — 登入Journey Optimizer

使用下列詳細資料登入：

電子郵件地址：L535+*您的座位號碼*@adobeeventlab.com

密碼：Adobe4Summit！


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

#### 媒體URL

```
https://demo-system-next.s3.amazonaws.com/assets/securfinancial/home-loan.jpg
```

#### 按鈕標題

```
Find ATMs
```

#### 目標URL

```
dxdemo://atm
```

## 影像

![SecureFinancial標誌](/help/summit-lab-assets/assets/SecureFinancial-logo.png)


![行動電話](/help/summit-lab-assets/assets/online-banking-app-01.png)
