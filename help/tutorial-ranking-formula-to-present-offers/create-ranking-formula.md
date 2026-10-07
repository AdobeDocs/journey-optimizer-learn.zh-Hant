---
title: 建立排名公式
description: Adobe Journey Optimizer中的排名公式會在Offer Decisioning期間使用，尤其是在選取策略中，用來決定合格優惠方案的優先順序。
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-30T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-18188
exl-id: eee1b86e-b33f-408e-9faf-90317bc5e861
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
source-wordcount: '346'
ht-degree: 0%
---
# 建立排名公式

Adobe Journey Optimizer中的排名公式會在Offer Decisioning期間使用，尤其是在選取策略中，用來決定合格優惠方案的優先順序。 適用性篩選之後，排名公式就會開始起作用，當多個優惠符合指定設定檔的資格時，但應根據商業邏輯或設定檔內容只顯示前一個（或少數個）。

* 登入Journey Optimizer

* 決策 — >策略設定 — >排名公式 — >建立公式

排名公式
![name_description](assets/formuala-ranking.png)

排名公式中的條件是指用於將分數指派給優惠方案的條件規則。 這些條件會比較優惠方案與設定檔或內容的屬性，以判斷優惠方案與特定個人的相關性。



條件1

此條件會篩選決定專案（優惠方案） **以僅包含**&#x200B;標示為「IncomeLevel」的優惠方案。
接著，系統會根據您定義的其他邏輯，繼續下一步驟（例如排名或傳送）。
![criteria_one](assets/income-related-formula.png)


下列運算式可用來建立排名分數

```pql
if(   offer._techmarketingdemos.offerDetails.zipCode = _techmarketingdemos.zipCode,   _techmarketingdemos.annualIncome / 1000 + 10000,   if(     not offer._techmarketingdemos.offerDetails.zipCode,     _techmarketingdemos.annualIncome / 1000,     -9999   ) )
```

公式的作用

* 如果優惠方案與使用者有相同的郵遞區號，請將分數設定為非常高，系統就會先挑選優惠方案。

* 如果優惠完全沒有郵遞區號（這是一般優惠方案），請根據使用者的收入給予正常分數。

* 如果優惠方案的郵遞區號與使用者不同，請將分數設定為非常低，以免選取優惠方案。

如此一來，系統：

* 一律先嘗試顯示郵遞區號相符的選件，

* 如果找不到相符專案，則會回覆為一般選件，並避免顯示專供其他郵遞區號使用的選件。


如果優惠方案專案不符合任何篩選條件（例如沒有「IncomeLevel」標籤），優惠方案會收到10的預設排名分數。




