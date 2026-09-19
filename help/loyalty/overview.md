---
title: 開始使用Journey Optimizer Loyalty
description: 瞭解如何加入Adobe Journey Optimizer Loyalty、設定挑戰、套用和顯示挑戰並分析其效能。
topic: Get Started
role: User
level: Beginner
doc-type: Tutorial
jira: KT-21773
last-substantial-update: '2026-07-28T00:00:00.000Z'
autotag-review: '2026-08-25T19:43:05.657Z'
TQID: 'https://experienceleague.adobe.com/k0YmuHe8wolVlL-fbnh0lPOyPiF5avG4ewbZm-b-cDM'
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
    internal-label: Use cases
subfeature_v2:
  - id: d48edf2f-7bae-4df0-a9d4-7cabfb867d23
    internal-label: Loyalty challenges
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 522d7abb4e436bd72f1c528a033ea5f3f267fe21
workflow-type: tm+mt
source-wordcount: '1658'
ht-degree: 42%
---

# 開始使用Journey Optimizer Loyalty

您可以透過忠誠度挑戰建立吸引人、遊戲化的忠誠度方案，推動客戶行為及深化品牌關係。 建立挑戰以獎勵客戶的特定行動，從購買和撰寫評論，到參與社群媒體和反向連結朋友。

## 熟客率簡介

本節介紹Journey Optimizer Loyalty，涵蓋其內容、在Adobe Journey Optimizer中的地位以及從設定到分析的挑戰生命週期。

<!--
CARDS

* https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/loyalty/introduction/discover-journey-optimizer-loyalty
  {description = Understand what Journey Optimizer Loyalty is, where it sits under AJO, and the challenge lifecycle.}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/loyalty/introduction/understand-loyalty-challenge-concepts
    {decription = Before you build anything in Adobe Journey Optimizer Loyalty, it helps to understand what a loyalty challenge is and the few pieces it's made of.}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Discover Journey Optimizer Loyalty">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/loyalty/introduction/discover-journey-optimizer-loyalty" title="探索Journey Optimizer Loyalty" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3496441/?format=jpeg&nocache=1789775328538" alt="探索Journey Optimizer Loyalty"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/loyalty/introduction/discover-journey-optimizer-loyalty" target="_blank" rel="referrer" title="探索Journey Optimizer Loyalty">探索Journey Optimizer Loyalty</a>
                    </p>
                    <p class="is-size-6">瞭解Journey Optimizer Loyalty是什麼、它在AJO之下的位置以及挑戰生命週期。</p>
                </div>
                <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/loyalty/introduction/discover-journey-optimizer-loyalty" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Understand loyalty challenge concepts">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/loyalty/introduction/understand-loyalty-challenge-concepts" title="瞭解忠誠度挑戰概念" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://cdn.experienceleague.adobe.com/thumb/exl-cards/slideshow.png" alt="瞭解忠誠度挑戰概念"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/loyalty/introduction/understand-loyalty-challenge-concepts" target="_blank" rel="referrer" title="瞭解忠誠度挑戰概念">瞭解忠誠度挑戰概念</a>
                    </p>
                    <p class="is-size-6">瞭解Journey Optimizer Loyalty背後的核心概念和辭彙。 您會瞭解忠誠度挑戰的成因（挑戰、工作和獎勵），以及各個部分如何組合，因此在下個單元中建構之前，您會擁有所需的思維模式。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/loyalty/introduction/understand-loyalty-challenge-concepts" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">了解更多</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## 設定忠誠度

本節說明開始建立挑戰之前所需的一次性設定。


<!--
CARDS

* ./set-up-loyalty/set-up-a-loyalty-reward-provider.md
  {description = Learn how to set up a reward provider, create reward definitions, and configure reward payloads so Adobe Journey Optimizer can issue loyalty rewards through your external rewards system.}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Set up a loyalty reward provider">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./set-up-loyalty/set-up-a-loyalty-reward-provider.md" title="設定忠誠度獎勵提供者" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3497346/?format=jpeg&nocache=1789775329089" alt="設定忠誠度獎勵提供者"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./set-up-loyalty/set-up-a-loyalty-reward-provider.md" target="_blank" rel="referrer" title="設定忠誠度獎勵提供者">設定忠誠獎勵提供者</a>
                    </p>
                    <p class="is-size-6">瞭解如何設定獎勵提供者、建立獎勵定義及設定獎勵裝載，以便Adobe Journey Optimizer可透過您的外部獎勵系統發出忠誠度獎勵。</p>
                </div>
                <a href="./set-up-loyalty/set-up-a-loyalty-reward-provider.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## 設定您的挑戰

本節將逐步引導您建立和設定端對端的忠誠度挑戰，包括其型別、結構和排程、任務和獎勵。


<!--
CARDS

* ./configure-your-challenge/set-up-a-loyalty-challenge.md
  {description = Learn how to set up a loyalty challenge by selecting the right challenge type, configuring audiences and schedules, defining participation rules, and controlling how progress is tracked and rewarded.}
* ./configure-your-challenge/create-tasks.md
  {description = Learn how to set up tasks: purchase & spend, quantities, eligible items & exclusions, and reuse.}
* ./configure-your-challenge/configure-rewards.md
  {description = Learn how to configure rewards: provider, milestone vs. completion delivery, reward types & coupons.}
* ./configure-your-challenge/create-a-challenge-and-get-insights-with-cx-enterprise-coworker.md
  {description = Learn how to use CX Enterprise Coworker to create, configure, and launch loyalty challenges using natural language, including audiences, rewards, schedules, and automated journey setup.}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Set up a loyalty challenge">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./configure-your-challenge/set-up-a-loyalty-challenge.md" title="設定忠誠度挑戰" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3496471/?format=jpeg&nocache=1789775329289" alt="設定忠誠度挑戰"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./configure-your-challenge/set-up-a-loyalty-challenge.md" target="_blank" rel="referrer" title="設定忠誠度挑戰">設定忠誠度挑戰</a>
                    </p>
                    <p class="is-size-6">瞭解如何選取正確的挑戰型別、設定對象和時程表、定義參與規則，並控制如何追蹤和獎勵進度，以設定忠誠度挑戰。</p>
                </div>
                <a href="./configure-your-challenge/set-up-a-loyalty-challenge.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Create tasks for your loyalty challenge">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./configure-your-challenge/create-tasks.md" title="建立您的忠誠度挑戰任務" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3496442/?format=jpeg&nocache=1789775329314" alt="建立您的忠誠度挑戰任務"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./configure-your-challenge/create-tasks.md" target="_blank" rel="referrer" title="建立您的忠誠度挑戰任務">為您的熟客方案挑戰建立任務</a>
                    </p>
                    <p class="is-size-6">瞭解如何設定任務：購買和支出、數量、合格專案和排除專案，以及重複使用。</p>
                </div>
                <a href="./configure-your-challenge/create-tasks.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Configure rewards">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./configure-your-challenge/configure-rewards.md" title="設定獎勵" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3496481/?format=jpeg&nocache=1789775329305" alt="設定獎勵"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./configure-your-challenge/configure-rewards.md" target="_blank" rel="referrer" title="設定獎勵">設定獎勵</a>
                    </p>
                    <p class="is-size-6">瞭解如何設定獎勵：提供者、里程碑與完成傳遞、獎勵型別與優惠券。</p>
                </div>
                <a href="./configure-your-challenge/configure-rewards.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Create a loyalty challenge and surface insights with CX Enterprise Coworker">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./configure-your-challenge/create-a-challenge-and-get-insights-with-cx-enterprise-coworker.md" title="使用CX Enterprise Coworker建立忠誠度挑戰並呈現深入分析" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3496528/?format=jpeg&nocache=1789775329297" alt="使用CX Enterprise Coworker建立忠誠度挑戰並呈現深入分析"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./configure-your-challenge/create-a-challenge-and-get-insights-with-cx-enterprise-coworker.md" target="_blank" rel="referrer" title="使用CX Enterprise Coworker建立忠誠度挑戰並呈現深入分析">使用CX Enterprise Coworker建立忠誠度挑戰並呈現深入分析</a>
                    </p>
                    <p class="is-size-6">瞭解如何使用CX Enterprise Coworker使用自然語言來建立、設定和啟動忠誠度挑戰，包括受眾、獎勵、時間表和自動化歷程設定。</p>
                </div>
                <a href="./configure-your-challenge/create-a-challenge-and-get-insights-with-cx-enterprise-coworker.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## 套用並顯示您的挑戰

本節說明如何使用內容卡和程式碼型體驗來向客戶挑戰。

<!--
CARDS

* ./apply-and-display-your-challenge/build-a-challenge-content-card.md
  {description = Learn how to build a challenge content card / code-based experience, covering opt-in and dynamic progress across the opt-in, progress, and completed stages, plus rewards and channel configuration.}
* ./apply-and-display-your-challenge/display-challenge-content-using-code-based-experience-channel.md
  {description = Learn how to use code-based experiences to promote loyalty challenges, display challenge progress, and deliver personalized content within your app using HTML or JSON.}
* ./apply-and-display-your-challenge/personalize-content-with-challenge-attributes-using-custom-actions.md
  {description = Learn how to retrieve challenge data with a custom action and use it to dynamically personalize content cards and code-based experiences based on each member's challenge progress and rewards.}
* ./apply-and-display-your-challenge/set-up-lifecycle-messaging-for-your-challenge.md
  {description = Learn how to configure multi-channel messaging for every stage of a loyalty challenge, from invitations and engagement messages to completion and reward notifications.}
* ./apply-and-display-your-challenge/publish-a-challenge-and-generate-a-journey.md
  {description = Learn how to publish a challenge and automatically generate a journey. Discover how challenge communications are translated into journey orchestration, review the generated journey structure, and customize it with additional conditions, decisioning, or optimization logic.}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Build a challenge content card">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./apply-and-display-your-challenge/build-a-challenge-content-card.md" title="建立挑戰內容卡" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3496529/?format=jpeg&nocache=1789775329771" alt="建立挑戰內容卡"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./apply-and-display-your-challenge/build-a-challenge-content-card.md" target="_blank" rel="referrer" title="建立挑戰內容卡">建立挑戰內容卡</a>
                    </p>
                    <p class="is-size-6">瞭解如何建置挑戰內容卡/程式碼型體驗，涵蓋選擇加入、進度和完成階段的動態進度，以及獎勵和管道設定。</p>
                </div>
                <a href="./apply-and-display-your-challenge/build-a-challenge-content-card.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Display challenge content using the code-based experience channel">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./apply-and-display-your-challenge/display-challenge-content-using-code-based-experience-channel.md" title="使用程式碼型體驗管道顯示挑戰內容" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3497465/?format=jpeg&nocache=1789775329764" alt="使用程式碼型體驗管道顯示挑戰內容"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./apply-and-display-your-challenge/display-challenge-content-using-code-based-experience-channel.md" target="_blank" rel="referrer" title="使用程式碼型體驗管道顯示挑戰內容">使用程式碼式體驗通道顯示挑戰內容</a>
                    </p>
                    <p class="is-size-6">瞭解如何使用程式碼型體驗來促進忠誠度挑戰、顯示挑戰進度，以及使用HTML或JSON在應用程式內提供個人化內容。</p>
                </div>
                <a href="./apply-and-display-your-challenge/display-challenge-content-using-code-based-experience-channel.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Personalize content with challenge attributes using custom actions">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./apply-and-display-your-challenge/personalize-content-with-challenge-attributes-using-custom-actions.md" title="使用自訂動作利用挑戰屬性個人化內容" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3503375/?format=jpeg&nocache=1789775329782" alt="使用自訂動作利用挑戰屬性個人化內容"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./apply-and-display-your-challenge/personalize-content-with-challenge-attributes-using-custom-actions.md" target="_blank" rel="referrer" title="使用自訂動作利用挑戰屬性個人化內容">使用自訂動作以挑戰屬性個人化內容</a>
                    </p>
                    <p class="is-size-6">瞭解如何使用自訂動作擷取挑戰資料，並用於根據每位成員的挑戰進度和獎勵，動態地個人化內容卡和程式碼型體驗。</p>
                </div>
                <a href="./apply-and-display-your-challenge/personalize-content-with-challenge-attributes-using-custom-actions.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Set up lifecycle messaging for your challenge">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./apply-and-display-your-challenge/set-up-lifecycle-messaging-for-your-challenge.md" title="針對您的挑戰設定生命週期訊息" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3497455/?format=jpeg&nocache=1789775329756" alt="針對您的挑戰設定生命週期訊息"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./apply-and-display-your-challenge/set-up-lifecycle-messaging-for-your-challenge.md" target="_blank" rel="referrer" title="針對您的挑戰設定生命週期訊息">設定您挑戰的生命週期訊息</a>
                    </p>
                    <p class="is-size-6">瞭解如何針對忠誠度挑戰的每個階段設定多管道訊息，從邀請和參與訊息到完成和獎勵通知。</p>
                </div>
                <a href="./apply-and-display-your-challenge/set-up-lifecycle-messaging-for-your-challenge.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Publish a challenge and generate a journey">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./apply-and-display-your-challenge/publish-a-challenge-and-generate-a-journey.md" title="發佈挑戰並產生歷程" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3498577/?format=jpeg&nocache=1789775329777" alt="發佈挑戰並產生歷程"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./apply-and-display-your-challenge/publish-a-challenge-and-generate-a-journey.md" target="_blank" rel="referrer" title="發佈挑戰並產生歷程">發佈挑戰並產生歷程</a>
                    </p>
                    <p class="is-size-6">瞭解如何發佈挑戰並自動產生歷程。 探索如何將挑戰通訊轉換為歷程協調、檢閱產生的歷程結構，並使用其他條件、決策或最佳化邏輯來自訂它。</p>
                </div>
                <a href="./apply-and-display-your-challenge/publish-a-challenge-and-generate-a-journey.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## 分析和報告

本節說明如何衡量忠誠度挑戰上線後的成效。

<!--
CARDS

* ./analyze-and-report/measure-performance-with-challenge-reports.md
  {description = Learn how to use challenge reports and performance dashboards to measure participation, completion rates, revenue attribution, and overall loyalty program performance.}
* ./analyze-and-report/analyze-loyalty-performance-using-loyalty-insights-dashboard.md
  {description = Explore the Loyalty Insights dashboard and learn how AI-generated insights help you identify significant changes in loyalty program performance, prioritize findings based on business KPIs, and take action on the metrics that matter most.}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Measure challenge performance with challenge reports">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./analyze-and-report/measure-performance-with-challenge-reports.md" title="使用挑戰報告測量挑戰效能" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3497534/?format=jpeg&nocache=1789775330174" alt="使用挑戰報告測量挑戰效能"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./analyze-and-report/measure-performance-with-challenge-reports.md" target="_blank" rel="referrer" title="使用挑戰報告測量挑戰效能">使用挑戰報告測量挑戰效能</a>
                    </p>
                    <p class="is-size-6">瞭解如何使用挑戰報表和績效儀表板來測量參與率、完成率、收入歸因和整體忠誠計畫績效。</p>
                </div>
                <a href="./analyze-and-report/measure-performance-with-challenge-reports.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Analyze loyalty performance with the insights dashboard">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./analyze-and-report/analyze-loyalty-performance-using-loyalty-insights-dashboard.md" title="使用見解儀表板分析熟客績效" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3502413/?format=jpeg&nocache=1789775330183" alt="使用見解儀表板分析熟客績效"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./analyze-and-report/analyze-loyalty-performance-using-loyalty-insights-dashboard.md" target="_blank" rel="referrer" title="使用見解儀表板分析熟客績效">使用見解儀表板分析熟客績效</a>
                    </p>
                    <p class="is-size-6">探索「忠誠度深入分析」儀表板，瞭解AI產生的深入分析如何協助您識別忠誠度計畫績效的重大變更、根據業務KPI排定結果的優先順序，以及對最重要的量度採取行動。</p>
                </div>
                <a href="./analyze-and-report/analyze-loyalty-performance-using-loyalty-insights-dashboard.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->
