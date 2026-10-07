---
title: 測試解決方案
description: 建立歷程，以在表單提交時傳送電子郵件
feature: Journeys
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-12-25T00:00:00.000Z
jira: KT-20014
exl-id: 9b4a3e0c-d153-4a6b-a7de-b926bd669f6a
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
    internal-label: Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%
---
# 測試解決方案


測試解決方案
>[!VIDEO](https://video.tv.adobe.com/v/3478546)

## 部署範例資產

如果您尚未安裝Node.js，請從這裡](https://nodejs.org/)下載並[安裝

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

* 在`trigger-journey`資料夾中建立名為`public`的資料夾
* 以適當的值更新`.env`檔案。 建立HTTP Source連線時，可從下載的cURL命令取得這些值。
* 將[index.zip](assets/index.zip)的內容解壓縮至`public`資料夾

## 執行伺服器

確定您位於`trigger-journey`目錄中。
執行命令 `node server.js`
將瀏覽器指向[網頁](http://localhost:3000/)
填寫並提交表單。 歷程會觸發，並傳送電子郵件至表單中輸入的電子郵件ID。
