---
title: 擷取曝光次數和互動事件
description: 擷取曝光和互動事件，並準備資料以在Journey Optimizer中報告。
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
recommendations: noDisplay, noCatalog
last-substantial-update: 2025-07-18T00:00:00Z
jira: KT-18526
exl-id: 7e6014b5-c5a6-467b-8e31-58c5d966464c
source-git-commit: bfeab1e933f2a510506c0ecf911df41e66cb959b
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 0%

---

# 擷取曝光次數和互動事件

若要啟用AJO Decisioning中的選件曝光數與點按數報告功能，必須設定下列元件：
>[!NOTE]
>
> 這些先決條件已在[先前教學課程](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/create-schema-and-dataset)的建立結構描述和資料集區段中完成

## &#x200B;1. Adobe Experience Platform (AEP)中的資料集

- 以&#x200B;**XDM ExperienceEvent**&#x200B;結構描述為基礎的資料集。

結構描述必須包括`Web Details`欄位群組，以擷取頁面URL、反向連結等。

## 2.資料流設定

- 必須在Adobe Experience Platform中建立&#x200B;**資料串流**。
- 此資料流必須連結至以上設定的資料集，以確保所有Web SDK事件皆正確擷取至正確的目的地。

## &#x200B;3. Adobe Experience Platform Tags屬性

- AEP Web SDK擴充功能已設定為使用先前步驟中建立的資料流。
- Experience Cloud ID服務已設定
- 名稱為ECID的資料元素會新增至屬性
- 在轉譯優惠方案的網站上實作。


若要啟用選件效能報表，第一個步驟是擷取選件顯示時間（曝光數）和點選時間（互動數）。 這些事件為測量參與度、計算點進率，以及分析Adobe Experience Platform中的選件有效性奠定了基礎。

alloy(「sendEvent」)函式可用來記錄使用者與Adobe Journey Optimizer (AJO)傳回之選件的互動。

sendEvent裝載包含事件型別（用於曝光次數的decisioning.propositionDisplay或用於點選次數的decisioning.propositionInteract）、唯一事件ID、時間戳記和使用者身分識別(identityMap)，以擷取優惠互動。 此外也包含顯示或點按的優惠方案（主張）清單，以及追蹤權杖，以確保精確的歸因。 此結構可讓您在Adobe Journey Optimizer中報告並最佳化個人化優惠效能。

會擷取兩種型別的互動事件：

## 曝光事件

當優惠呈現在頁面上且使用者可看到時，就會產生印象。 使用decisioning.propositionDisplay事件型別追蹤事件。


```javascript
 alloy("sendEvent", {
            xdm: {
              _id: generateUUID(),
              timestamp: new Date().toISOString(),
              eventType: "decisioning.propositionDisplay",
              identityMap: {
                    ECID: [{
                      id: _satellite.getVar("ECID"),
                      authenticatedState: "authenticated",
                      primary: true
                    }]
                  },
              _experience: {
                decisioning: {
                  propositionEventType: {
                    display: 1
                  },
                    propositionAction: {
                            id: offerId,
                            tokens: [trackingToken]
                  },
                  
                   propositions: window.latestPropositions
                  
                }
              }
            }
          });
        }
```

## 優惠互動

當使用者按一下轉譯選件內的call-to-action (CTA)時，會記錄互動。 使用decisioning.propositionInteract事件型別追蹤事件。

```javascript
alloy("sendEvent", {
                xdm: {
                  _id: generateUUID(),
                  timestamp: new Date().toISOString(),
                  eventType: "decisioning.propositionInteract",
                  identityMap: {
                    ECID: [{
                      id: _satellite.getVar("ECID"),
                      authenticatedState: "ambiguous",
                      primary: true
                    }]
                  },
                  _experience: {
                    decisioning: {
                      propositionEventType: {
                        interact: 1
                      },
                      propositionAction: {
                        id: offerId,
                        tokens: [trackingToken]
                      },
                       propositions: window.latestPropositions
                    }
                  }
                }
              })
```

在點按和曝光事件中包含主張對於Adobe Journey Optimizer中的準確選件報告至關重要。 這些主張代表呈現給使用者的確切優惠方案，可讓Adobe將使用者互動（例如曝光數或點按次數）歸因於系統所做的特定決策。

主張中的每個優惠方案都包含一個追蹤權杖，這是Adobe產生的唯一識別碼。 此Token必須完全依照收到的方式在對應點選或曝光事件中傳遞（不會變更）。 比對追蹤權杖可確保Adobe能夠準確地將使用者動作與正確的優惠決定建立關聯，以啟用下游報告和人工智慧為基礎的最佳化。
