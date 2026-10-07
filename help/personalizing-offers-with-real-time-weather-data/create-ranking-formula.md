---
title: 建立排名公式
description: Adobe Journey Optimizer中的排名公式會在Offer Decisioning期間使用，尤其是在選取策略中，用來決定合格優惠方案的優先順序。
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-18258
exl-id: 23a9d36f-ac2c-42a5-b08d-79c7118920c9
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: a984631b-2bae-4860-9b15-69c41a799dcb
    internal-label: APIs and SDKs
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
    internal-label: Decisioning API
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%
---
# 建立排名公式

Adobe Journey Optimizer中的排名公式會在Offer Decisioning期間使用，尤其是在選取策略中，用來決定合格優惠方案的優先順序。 適用性篩選之後，排名公式就會開始起作用，當多個優惠符合指定設定檔的資格時，但應根據商業邏輯或設定檔內容只顯示前一個（或少數個）。

* 登入Journey Optimizer

* 導覽至&#x200B;_**決策 — >策略設定 — >排名公式 — >建立公式**_

為公式&#x200B;_**命名Weather - Related - Offers**_



排名公式中的條件是指用於將分數指派給優惠方案的條件規則。 這些條件會比較優惠方案和內容的屬性，以判斷優惠方案與特定個人的相關性。

定義下列3個條件來篩選優惠方案，然後將排名分數指派給合格優惠方案。 條件是使用條件產生器定義。 內容資料也可用於定義條件，如下方熒幕擷圖所示
![contxt-data](assets/context-data.png)

所有3個條件都使用選件屬性（標籤）和內容資料屬性（溫度）來定義條件。

## 條件一

| **選件標籤** | **內容資料條件** | **分數邏輯** |
|------------------|---------------------|-------------------------------------|
| **熱** | 溫度> 80 | score=溫度 |


## 條件二

| **天氣標籤** | **內容資料條件** | **分數邏輯** |
|------------------|---------------------------|----------------------------------------------|
| **春季** | 溫度> 65且&lt; 80 | score=temperate × 4 |

## 條件三

| **天氣標籤** | **內容資料條件** | **分數邏輯** |
|------------------|---------------------------|----------------------------------------------|
| **冷** | 溫度&lt; 65 | score =溫度 |
