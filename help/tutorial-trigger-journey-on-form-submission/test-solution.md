---
title: 測試解決方案
description: 建立歷程，以在表單提交時傳送電子郵件
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-12-25T00:00:00Z
jira: KT-20014
source-git-commit: 043f41acd8f7f7165d9ec416d8f789f78d407ca1
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# 測試解決方案


測試解決方案
>[!VIDEO](https://video.tv.adobe.com/v/3478546)

## 部署範例資產

如果您尚未安裝Node.js，請從這裡[下載並](https://nodejs.org/)安裝

執行以驗證安裝：

`node -v`

`npm -v`

## 設定專案資料夾

使用下列命令為範例應用程式建立新目錄：

`mkdir trigger-journey `

`cd trigger-journey`

## 初始化專案

`npm init -y`

## 安裝必要的架構

`npm install express dotenv axios cors`

## 複製資產檔案

* 解壓縮[project-root.zip](assets/project-root.zip)的內容，並將其放在`trigger-journey`資料夾中。

* 在`public`資料夾中建立名為`trigger-journey`的資料夾
* 將[index.zip]的內容解壓縮至公用資料夾
* 以適當的值更新`.env`檔案。 建立HTTP Source連線時，可從下載的cURL命令取得這些值

## 執行伺服器

確定您位於`trigger-journey`目錄中。
執行命令`node server.js`
將瀏覽器指向[網頁](http://localhost:3000/)
填寫並提交表單。 歷程會觸發，並傳送電子郵件至表單中輸入的電子郵件ID。


