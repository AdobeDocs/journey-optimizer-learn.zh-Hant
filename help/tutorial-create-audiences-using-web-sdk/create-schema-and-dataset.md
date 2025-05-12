---
title: 在AEP中設定XDM結構描述、資料集和資料流
description: 建立XDM結構描述、資料集和資料流
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00Z
jira: KT-17923
exl-id: 0efa418a-5b4f-4012-a6fc-afaa34a59285
source-git-commit: 15b2379c251ed0d7583a01fb6af67815322456cf
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# 在AEP中設定XDM結構描述、資料集和資料流

## 建立XDM結構描述

* 登入Adobe Experience Platform
* 資料管理 — >方案 — >建立方案

* 建立名為&#x200B;_財務顧問_&#x200B;的XDM事件型結構描述。 如果您不熟悉建立結構描述，請依照此[檔案](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/create-schema-ui)操作

* 將下列結構新增至您的結構描述。 PreferredFinancialInstrument元素會儲存使用者對Stocks、Bonds、CD的偏好設定。 **__techmarketingdemos_**&#x200B;是租使用者ID，在您的環境中將會不同。
  ![xdm-schema](assets/xdm-schema.png)

* PreferredFinancialInstrument元素具有如下所示的列舉值
  ![列舉值](assets/enum-values.png)

* 請確定設定檔已啟用此結構描述。

## 根據結構建立資料集

Adobe Experience Platform (AEP)**中的**&#x200B;資料集是結構化儲存容器，用來根據定義的XDM結構描述擷取、儲存及啟用資料。


* 資料管理 — >資料集 — >建立資料集
* 根據上一步建立的XDM結構描述(Financial Advisors)，建立名為&#x200B;_Financial Advisors資料集_&#x200B;的資料集。

* 請確定資料集已啟用設定檔

## 建立資料串流

Adobe Experience Platform中的資料串流就像將您的網站或應用程式連線到Adobe服務的安全管道（或高速公路），可讓資料流入，而個人化內容流回。

* 資料收集>資料串流，然後按一下新增資料串流。 命名資料流&#x200B;_財務顧問資料流_

* 提供下列詳細資訊，如下方熒幕擷圖所示
  ![資料流](assets/datastream.png)
* 按一下儲存，然後按一下新增對應並新增Adobe Experience Platform服務和事件資料集，如圖所示
  ![資料流對應](assets/datastream-service.png)

* 選擇適當的事件資料集（先前建立）。

* 儲存資料串流

