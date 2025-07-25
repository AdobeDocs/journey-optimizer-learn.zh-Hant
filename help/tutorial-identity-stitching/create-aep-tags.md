---
title: 傳送CRMID至Adobe Experience Platform
description: 建立Adobe Experience Platform標籤，以將從瀏覽器收到的CRMID傳送到Adobe Experience Platform
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18089
exl-id: 894ad6b7-c4b4-465e-8535-3fdcd77e00eb
source-git-commit: 40690024e5348dd3ac05f350e49a67a99d5e455e
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 9%

---

# 傳送CRMID至Adobe Experience Platform

Adobe Experience Platform Tags是用來將CRMID傳送至Adobe Experience Platform (AEP)，因為它提供靈活、事件導向的機制，以便直接從瀏覽器傳輸身分資料。 使用者登入後傳送CRMID可讓AEP將匿名ECID與已知CRM設定檔連結，以實現精確的身分拼接。 此連結構成在Adobe Journey Optimizer (AJO)中建立統一客戶設定檔、合格對象及提供即時個人化體驗的基礎。

已建立名為&#x200B;_**FinWise**_&#x200B;的Experience Platform Tags屬性。 已將下列擴充功能新增至Tags屬性

![標籤延伸模組](assets/tags-extensions.png)

使用在上一步建立的Financial Advisors DataStream，設定AEP Web SDK擴充功能。
Experience Cloud ID Service是新增至標籤屬性的選用擴充功能，以供除錯之用。

## 標籤資料元素

建立下列資料元素

| 資料元素 | 擴充功能 | 資料元素型別 | 自訂設定 |
|--------------|-----------------------------------|---------------------------|----------------------------------------|
| crmid | Adobe使用者端資料層 | 資料層計算狀態 | user.crmid |
| ECID | Experience Cloud ID 服務 | ECID |                                        |
| 身分識別 | Adobe Experience Platform Web SDK | 身分對應 | ![影像](assets/identity-settings.png) |
| XDMVariable | Adobe Experience Platform Web SDK | 變數 | ![影像](assets/xdmvariable.png) |

## 建立規則

使用下列事件和動作建立名為userLoggedin的規則

事件
![事件](assets/data-pushed-event.png)

更新變數動作
![更新變數](assets/update-variable.png)
傳送事件動作
![傳送事件](assets/send-event.png)

## 儲存並建置

儲存變更、建立及建置程式庫。
