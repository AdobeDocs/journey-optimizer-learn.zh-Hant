---
title: 建立優惠方案以測試動態決策和排名。
description: 決策中的優惠方案專案代表可以根據定義的規則和條件傳送給使用者的單一個人化內容，例如訊息、影像、促銷活動或推薦。
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18258
source-git-commit: dac6b373226bd0be2533cf859e4f250018cf568b
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# 建立優惠方案以測試動態決策和排名

這些選件旨在根據透過Adobe Web SDK (alloy(「sendEvent」))傳遞的即時情境輸入（例如溫度），測試動態決策和排名。

建立優惠方案之前，優惠方案專案結構描述已擴充以包含新欄位： offerText

![選件結構描述](assets/offer-schema.png)。

建立下列3個選件


## 炎熱天氣選件(Tag：hot)

炎熱天氣選件的選件文字

```html
<div data-tags="weather hot skincare sunscreen" style="border: 1px solid #e0e0e0; padding: 1.5rem; border-radius: 10px; background-color: #fff3e0;">   <h2 style="color: #e65100;">Protect Your Skin This Summer</h2>   <p>High temperatures mean high UV risk. Get <strong>20% off</strong> our dermatologist-recommended sunscreens and skin protection kits.</p>   <p>Offer valid this week only for areas with temperatures over 90°F.</p>   <a href="#" style="display:inline-block; margin-top:1rem; padding:0.75rem 1.5rem; background:#e65100; color:white; border-radius:5px; text-decoration:none;">Shop Sunscreen</a> </div>
```


## 溫和天氣選件(Tag：spring)

輕度天氣的優惠方案文字

```html
<div data-tags="ajo offer-mild-weather">   <h2 style="color: #2e7d32;">🌤️ Enjoy the Outdoors — Gear Up Now!</h2>   <p style="font-size: 1.1rem;">Perfect weather to be outside! Check out our selection of <strong>picnic sets, walking shoes, and fitness accessories</strong> for your next outdoor adventure.</p>   <p style="font-size: 1.1rem;">Get <strong>free shipping</strong> on all outdoor gear this week.</p>   <a href="#" style="display:inline-block;padding:0.75rem 1.5rem;background:#2e7d32;color:white;border-radius:6px;text-decoration:none;margin-top:1rem;">Explore Outdoor Picks</a> </div>
```

## 冷天氣(Tag：cold)

寒冷天氣優惠方案的優惠方案文字

```html
<div class="offer-content" style="text-align: center; padding: 1rem;">   <img src="https://raw.githubusercontent.com/gbedekar489/gbedekar489.github.io/main/weather/pexels-romanp-16170.jpg"         alt="Winter clothing"         style="width: 100%; max-width: 400px; border-radius: 12px; margin-bottom: 1rem;">   <h2>Cold Weather, Hot Deals 🧤</h2>   <p>Stay warm in style with our exclusive <strong>25% off</strong> winter outerwear. From puffer jackets to wool scarves, find the perfect layers to beat the chill.</p>   <p><strong>Use code:</strong> <code>WINTER25</code> at checkout</p>   <p><em>Limited time offer. While supplies last.</em></p> </div>
```

### 建立集合

導覽至決策 — >目錄 — >集合 — >建立集合
為集合**天氣相關優惠**&#x200B;命名

使用規則產生器將這個集合中的這些優惠方案分組。

