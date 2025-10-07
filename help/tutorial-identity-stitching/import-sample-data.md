---
title: 將範例CRM資料匯入AEP設定檔資料集
description: 匯入範例記錄（例如，含CRMID、電子郵件、收入、郵遞區號），以驗證AEP能否根據ECID等共用識別碼，正確地將那些設定檔與匿名Web訪客拼接。
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18089
exl-id: 33c8c386-f417-45a8-83cf-7312d415b47a
source-git-commit: 83b23f54594b796ec528526a360c5c40164fb5cb
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 5%

---

# 將範例CRM資料匯入AEP設定檔資料集

若要開始身分拼接，請將範例CRM設定檔資料匯入繫結至Adobe Experience Platform中啟用設定檔的結構描述的資料集

## 建立自訂名稱空間

* 導覽至「客戶 — >身分 — >建立身分名稱空間」
* 選取個別跨裝置ID，並提供顯示名稱和身分符號，如下方熒幕擷取畫面所示。
  ![自訂名稱空間](assets/custom-namespace.png)

## 建立已啟用設定檔的結構描述

建立名為&#x200B;**_FinWiseProfileSchema_**&#x200B;的個別設定檔結構描述。 包含annualIncome、email、firstName、lastName和loyaltyStatus等欄位。
新增身分欄位&#x200B;**_crmid_**，如圖所示。 將crmid欄位標示為身分和主要。
將_&#x200B;**同意和偏好設定詳細資料**&#x200B;_&#x200B;欄位群組新增到結構描述。 [同意和偏好設定](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/xdm/field-groups/profile/consents)是XDM個人設定檔類別的標準欄位群組，可擷取個別客戶的同意和偏好設定資訊。此處儲存的偏好設定會決定頻道層級的通訊偏好設定。


![設定檔結構描述](assets/finwise-profile-schema.png)

## 準備範例資料

將虛擬電子郵件地址更新為真實地址。 稍後透過Adobe Journey Optimizer傳送訊息時，將會使用這些選項。 將emailConsent設定為y以啟用設定檔的電子郵件傳送。

|   | crmId | 名字 | 姓氏 | 電子郵件 | loyaltyStatus | zipCode | 年收入 | emailConsent |
|---|--------|-----------|----------|-------------------------|---------------|---------|--------------|--------------|
|   | FIN001 | Alice | 黃 | alice.wong@example.com | 金級 | 92128 | 120000 | y |
|   | FIN002 | 鮑伯 | Smith | bob.smith@example.com | 銀級 | 92126 | 85000 | y |
|   | FIN003 | 查理 | Kim | charlie.kim@example.com | 白金 | 60614 | 175000 | y |
|   | FIN004 | Diana | 李 | diana.lee@example.com | 金級 | 30303 | 98000 | y |
|   | FIN005 | Ethan | 棕色 | ethan.brown@example.com | 銅級 | 75201 | 60000 | y |

## 擷取CSV檔案

* 根據先前步驟建立的&#x200B;**_FinWiseProfileSchema_**，建立名為&#x200B;**_FinWiseCustomerDataSetWithAnnualIncome_**&#x200B;的資料集

* 導覽至連線 — >來源 — >本機系統
* 選取本機檔案上傳下的&#x200B;**_新增資料_**。 請務必選取&#x200B;_&#x200B;**FinWiseCustomerDataSetWithAnnualIncome**&#x200B;_作為目標資料集。
  ![擷取 — csv](assets/ingest-csv-into-dataset.png)
* 導覽至下一個畫面。 上傳[csv檔案](assets/finwise_profiles.csv)並驗證對應
  ![對映](assets/mappings.png)

* 按一下完成，即可開始資料擷取程式

## 驗證設定檔

* 導覽至客戶 — >設定檔並搜尋等於FIN001或任何其他有效值的FinWise CRM ID
  ![驗證設定檔](assets/verify-profiles.png)
