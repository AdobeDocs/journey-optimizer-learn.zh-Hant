---
title: 傳送CRMID至Adobe Experience Platform
description: 建立Adobe Experience Platform標籤，以將從瀏覽器收到的CRMID傳送到Adobe Experience Platform
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-18089
exl-id: 894ad6b7-c4b4-465e-8535-3fdcd77e00eb
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d2971708-e780-44bb-9e2a-72f139796afd
    internal-label: Customer
subfeature_v2:
  - id: ef9a83ca-eefa-47cf-aa34-f1a34715583a
    internal-label: Profiles
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 9%
---
# 傳送CRMID至Adobe Experience Platform

Adobe Experience Platform Tags是用來將CRMID傳送至Adobe Experience Platform (AEP)，因為它提供靈活、事件導向的機制，以便直接從瀏覽器傳輸身分資料。 使用者登入後傳送CRMID可讓AEP將匿名ECID與已知CRM設定檔連結，以實現精確的身分拼接。 此連結構成在Adobe Journey Optimizer (AJO)中建立統一客戶設定檔、合格對象及提供即時個人化體驗的基礎。

已建立名為&#x200B;_&#x200B;**FinWise**&#x200B;_&#x200B;的Experience Platform Tags屬性。 已將下列擴充功能新增至Tags屬性

![標籤延伸模組](assets/tags-extensions.png)

使用在上一步建立的Financial Advisors DataStream，設定AEP Web SDK擴充功能。
Experience Cloud ID Service是新增至標籤屬性的選用擴充功能，以供偵錯之用。

## 標籤資料元素

建立下列資料元素

| 資料元素 | 擴充功能 | 資料元素型別 | 自訂設定 |
|--------------|-----------------------------------|---------------------------|----------------------------------------|
| crmid | Adobe使用者端資料層 | 資料層計算狀態 | user.crmid |
| ECID | Experience Cloud ID 服務 | ECID |                                        |
| 身分識別 | Adobe Experience Platform Web SDK | 身分對應 | ![影像](assets/identity-settings.png) |
| XDMVariable | Adobe Experience Platform Web SDK | 變數 | ![影像](assets/xdmvariable.png) |

## 建立規則

使用下列事件和動作建立名為LoginEvent的規則

事件
![事件](assets/data-pushed-event1.png)

更新變數動作
![更新變數](assets/update-variable1.png)
傳送事件動作
![傳送事件](assets/send-event1.png)

## 儲存並建置

儲存變更、建立及建置程式庫。
