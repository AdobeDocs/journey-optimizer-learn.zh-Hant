---
title: 設定和啟動
description: 在Adobe Journey Optimizer (AJO)和Adobe Experience Platform (AEP)中設定行動裝置頻道、整合行動應用程式，並確保行銷活動執行的整備。
feature: Overview
role: Developer, Admin
level: Beginner, Intermediate
hide: true
index: false
last-substantial-update: 2025-08-22T00:00:00Z
exl-id: d8ffe406-b54b-455f-bd41-7d1fef0a4714
source-git-commit: eed29b23e46480725b6ed786911758283b25ad16
workflow-type: tm+mt
source-wordcount: '2106'
ht-degree: 18%

---


# 設定和啟動

針對&#x200B;**管理員**&#x200B;和&#x200B;**行動應用程式開發人員**，本節說明如何在Adobe Journey Optimizer中設定和啟動行動與網路頻道。 內容涵蓋先決條件、許可權和平台支援，然後引導您建立應用程式專屬設定。

>[!IMPORTANT]
>
> 若您為Journey Optimizer和Experience Platform的新手，請參加此課程： [Adobe Journey Optimizer智慧型歷程啟用的工程師資料](https://experienceleague.adobe.com/en/courses/ajo-engineer-data-for-intelligent-journey-activation){target="_blank"}，以熟悉Journey Optimizer的核心概念資料管理
>


## Adobe Journey Optimizer中的行動裝置功能

瞭解Adobe Journey Optimizer為開發人員、行銷人員和產品團隊提供的行動裝置功能，包括推送訊息、應用程式內訊息和內容個人化。

>[!VIDEO](https://video.tv.adobe.com/v/342103?quality=12&learn=on){transcript=true}


## 管道設定

### 行動推送和應用程式內

Journey Optimizer中的行動實作從應用程式中的&#x200B;**Adobe Experience Platform Mobile SDK**&#x200B;整合開始。 SDK是資料收集以及與Adobe Experience Platform (AEP)及其應用程式(例如Adobe Journey Optimizer (AJO))互動的必要元件。

#### 什麼是Mobile SDK：

行動SDK：

- 收集應用程式事件（熒幕檢視、點選、購買、生命週期事件等）並傳送至&#x200B;**Adobe Experience Platform Edge Network**。
- 管理&#x200B;**身分**&#x200B;和&#x200B;**同意**，讓Journey Optimizer可以安全地建立及使用客戶設定檔。
- 註冊並更新&#x200B;**推播權杖**，並將&#x200B;**推播和應用程式內追蹤事件**&#x200B;傳送回Adobe Experience Platform。
- 與&#x200B;**[Journey Optimizer行動擴充功能](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer)**&#x200B;整合，所以訊息可以端對端傳送、轉譯及測量。

若未將行動SDK整合至您的應用程式中，Journey Optimizer就無法可靠地：

- 傳遞及追蹤行動推播和應用程式內訊息。
- 呈現和追蹤內容卡。
- 使用即時應用程式內行為來觸發歷程並個人化體驗。

#### 新實施的引導式管道設定

若是新的行動應用程式內和推送實作，建議從引導式頻道設定開始。 它可降低資料串流設定錯誤或缺少擴充功能的風險，並逐步引導您使用Assurance完成SDK驗證。

>[!PREREQUISITES]
>
>請確定您擁有：
>
> - 為您的組織布建的&#x200B;**Adobe Journey Optimizer** (AJO)。
> - 使用[資料收集和Journey Optimizer許可權](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/guided-setup/set-mobile-config#:~:text=Required%20permissions)存取Adobe Experience Platform。
> - AJO中的管理員許可權，用於管道和組態設定。
> - 存取行動應用程式的原始碼(iOS、Android或跨平台架構)。
> - 您的應用程式已啟用必要的作業系統層級功能（例如推送許可權、通知服務擴充功能、背景模式）。
> - 如果您使用現有的組態選項，請確定您使用[目前的Adobe Experience Platform Mobile SDK版本](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}


>[!VIDEO](https://video.tv.adobe.com/v/3433053/?learn=on)

如需詳細資訊，請參閱[開始使用引導式頻道設定](https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/guided-setup/set-mobile-config.html?lang=zh-Hant){target="_blank"}


#### 手動設定推播通道

以下指南會逐步引導您瞭解如何手動設定並有效使用推播通知所需的一切，從瞭解資料流程、與Firebase和Apple推播通知服務(APN)等服務整合，到設定行動應用程式和測試通知。

<!-- CARDS
* https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs
{title = Push notification data flow and components}
{description = Learn how to setup and understand key services and workflows involved with push notifications in Journey Optimizer.}
{image = https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/media_1f6e99fa57e318230d92f5dde619c450690b5d27a.png?width=2000&format=webply&optimize=medium}
{target = _blank}

* https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-configuration
{image = https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/media_1134ddf9b0f7d39bb365d4884a1d603fd4aa5bbdf.png?width=2000&format=webply&optimize=medium}
{target = _blank}
* https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/overview 
{target = _blank}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Push notification data flow and components">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs" title="推播通知資料流程和元件" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/media_1f6e99fa57e318230d92f5dde619c450690b5d27a.png?width=400&format=webply&optimize=medium" alt="推播通知資料流程和元件"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs" target="_blank" rel="referrer" title="推播通知資料流程和元件">推播通知資料流程和元件</a>
                    </p>
                    <p class="is-size-6">瞭解如何設定並瞭解Journey Optimizer中推播通知的相關關鍵服務和工作流程。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">深入了解</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Push notification configuration">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-configuration" title="推播通知設定" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/media_1134ddf9b0f7d39bb365d4884a1d603fd4aa5bbdf.png?width=400&format=webply&optimize=medium" alt="推播通知設定"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-configuration" target="_blank" rel="referrer" title="推播通知設定">推播通知設定</a>
                    </p>
                    <p class="is-size-6">瞭解如何使用Journey Optimizer設定您的環境以傳送推播通知</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-configuration" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">深入了解</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Implement Adobe Experience Cloud in mobile apps tutorial">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/overview" title="在行動應用程式教學課程中實作Adobe Experience Cloud" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/overview./media_1c75750ec1be623e56a379ca69ef6c495799e52a5.png?width=400&format=png&optimize=medium" alt="在行動應用程式教學課程中實作Adobe Experience Cloud"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/overview" target="_blank" rel="referrer" title="在行動應用程式教學課程中實作Adobe Experience Cloud">在行動應用程式教學課程中實作 Adobe Experience Cloud</a>
                    </p>
                    <p class="is-size-6">瞭解如何實作Adobe Experience Cloud行動應用程式。 本教學課程將指導您在一個範例Swift或Android應用程式中實施Experience Cloud應用程式。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/overview" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">深入了解</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

### 其他資源


<!-- CARDS
* https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk
{target = _blank}
* https://developer.adobe.com/client-sdks/home/base/assurance
{target = _blank}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Get the Adobe Experience Platform Mobile SDK">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk" title="取得Adobe Experience Platform Mobile SDK" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://developer.adobe.com/shared/images/adobe-social-share.png" alt="取得Adobe Experience Platform Mobile SDK"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk" target="_blank" rel="referrer" title="取得Adobe Experience Platform Mobile SDK">取得Adobe Experience Platform Mobile SDK</a>
                    </p>
                    <p class="is-size-6">說明如何在應用程式中安裝Adobe Experience Platform Mobile SDK的指南。</p>
                </div>
                <a href="https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">深入了解</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe Experience Platform Assurance overview">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/client-sdks/home/base/assurance" title="Adobe Experience Platform Assurance概觀" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://developer.adobe.com/shared/images/adobe-social-share.png" alt="Adobe Experience Platform Assurance概觀"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/client-sdks/home/base/assurance" target="_blank" rel="referrer" title="Adobe Experience Platform Assurance概觀">Adobe Experience Platform Assurance概觀</a>
                    </p>
                    <p class="is-size-6">Adobe Experience Platform Assurance行動擴充功能的概觀。</p>
                </div>
                <a href="https://developer.adobe.com/client-sdks/home/base/assurance" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">深入了解</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

#### 行動SDK整備檢查清單

將應用程式傳遞給行銷人員之前，請在&#x200B;**[Assurance](https://developer.adobe.com/client-sdks/home/base/assurance/){target="_blank"}**&#x200B;中確認：

>[!SUCCESS]
> 
> [ 已載入]核心SDK + Journey Optimizer擴充功能，\
> [ ]事件在正確的資料流和資料集上流動，\
> [ ]所有重要事件上皆有身分和同意，\
> [ 已追蹤]個推播權杖和互動，並且\
> [ ]至少已顯示一個測試應用程式內訊息或內容卡，並記錄為曝光數。


### 內容卡片

<!-- CARDS
* https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/content-card-lp
{title = Configure content cards support in Mobile SDK}
{description = Learn how to integrate content cards in your mobile application using Messaging SDK.}
{target = _blank}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Configure content cards support in Mobile SDK">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/content-card-lp" title="在 Mobile SDK 中設定內容卡支援" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/content-card-lp./media_17623afb1c5e280b7fb6861b4003d0ef8f8bea24d.jpg?width=400&format=jpg&optimize=medium" alt="在 Mobile SDK 中設定內容卡支援"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/content-card-lp" target="_blank" rel="referrer" title="在 Mobile SDK 中設定內容卡支援">在行動SDK中設定內容卡支援</a>
                    </p>
                    <p class="is-size-6">瞭解如何使用傳訊SDK將內容卡整合到您的行動應用程式中。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/content-card-lp" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">深入了解</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

### WhatsApp

瞭解如何設定&#x200B;**WhatsApp頻道**：

<!-- CARDS
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/whatsapp-channel/set-up-whatsapp-channel
{target = _blank}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Set up the WhatsApp channel">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/whatsapp-channel/set-up-whatsapp-channel" title="設定 WhatsApp 頻道" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3470268/?format=jpeg&nocache=1765241811878" alt="設定 WhatsApp 頻道"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/whatsapp-channel/set-up-whatsapp-channel" target="_blank" rel="referrer" title="設定 WhatsApp 頻道">設定 WhatsApp 頻道</a>
                    </p>
                    <p class="is-size-6">本教學課程將引導您在 Adobe Journey Optimizer 中設定 WhatsApp 頻道，以實現即時業務訊息傳送。</p>
                </div>
                <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/whatsapp-channel/set-up-whatsapp-channel" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

### SMS/MMS/RCS

使用標準提供者（Twilio、Synch或Infobip）或自訂SMS提供者設定&#x200B;**SMS/MMS/RCS頻道**：

<!-- CARDS
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-sms-channel
{target = _blank}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-custom-sms-provider
{description = Learn how to configure custom SMS providers in Journey Optimizer, set up API credentials and webhooks, manage opt-in/opt-out keywords, and launch personalized campaigns.}
{target = _blank}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-mms-api-credentials-and-channel-surfaces
{target = _blank}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-rcs
{target = _blank}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Configure SMS API credentials and channel surfaces">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-sms-channel" title="設定簡訊 API 認證及頻道介面" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3413355?format=jpeg&nocache=1765241812951" alt="設定簡訊 API 認證及頻道介面"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-sms-channel" target="_blank" rel="referrer" title="設定簡訊 API 認證及頻道介面">設定SMS API認證和頻道介面</a>
                    </p>
                    <p class="is-size-6">瞭解如何將 Journey Optimizer 連線至 SMS 服務提供者，以及如何建立簡訊頻道介面。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-sms-channel" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Configure a custom SMS provider">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-custom-sms-provider" title="設定自訂簡訊提供者" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3431625/?format=jpeg&nocache=1765241812924" alt="設定自訂簡訊提供者"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-custom-sms-provider" target="_blank" rel="referrer" title="設定自訂簡訊提供者">設定自訂 SMS 提供者</a>
                    </p>
                    <p class="is-size-6">瞭解如何在Journey Optimizer中設定自訂簡訊提供者、設定API憑證和Webhook、管理選擇加入/選擇退出關鍵字，以及啟動個人化行銷活動。</p>
                </div>
                <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-custom-sms-provider" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Configure MMS API credentials and channel surfaces">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-mms-api-credentials-and-channel-surfaces" title="設定多媒體簡訊 API 憑證及頻道介面" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3428872/?format=jpeg&nocache=1765241812943" alt="設定多媒體簡訊 API 憑證及頻道介面"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-mms-api-credentials-and-channel-surfaces" target="_blank" rel="referrer" title="設定多媒體簡訊 API 憑證及頻道介面">設定簡訊 API 憑證及管道表面</a>
                    </p>
                    <p class="is-size-6">瞭解如何將 Journey Optimizer 連線至多媒體簡訊服務提供者，以及如何建立多媒體簡訊頻道介面。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-mms-api-credentials-and-channel-surfaces" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Set up RCS in Journey Optimizer">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-rcs" title="在 Journey Optimizer 中設定 RCS" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3464755/?format=jpeg&nocache=1765241812927" alt="在 Journey Optimizer 中設定 RCS"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-rcs" target="_blank" rel="referrer" title="在 Journey Optimizer 中設定 RCS">在 Journey Optimizer 中設定 RCS</a>
                    </p>
                    <p class="is-size-6">瞭解如何使用自訂簡訊供應商，就能在 Adobe Journey Optimizer 中設定、傳送品牌化互動式 RCS 訊息。本教學課程會逐步引導您設定 API 認證、Webhook 和道設定，然後建立歷程，以便提供豐富、個人化的傳訊體驗，全都可以透過原生傳訊應用程式完成。</p>
                </div>
                <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-rcs" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## 確保遵守隱私權法規和平台指引。

<!-- CARDS
* https://experienceleague.adobe.com/en/docs/journey-optimizer/using/privacy/privacy-landing-page{image=../mobile-learning-hub/assets/privacy.webp}{title = Privacy Features in Adobe Journey Optimizer}{description = Learn how to process privacy requests, audit user actions, manage consent, apply governance rules, and leverage advanced security options like Customer Managed Keys.}
{target = _blank}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/data-governance-framework
{target = _blank}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/classify-data-using-lables
{cta = Watch}
{target = _blank}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/create-data-usage-policies
{target = _blank}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Privacy Features in Adobe Journey Optimizer">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/privacy/privacy-landing-page" title="Adobe Journey Optimizer 中的隱私功能" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../mobile-learning-hub/assets/privacy.webp" alt="Adobe Journey Optimizer 中的隱私功能"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        Adobe Journey Optimizer中的<a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/privacy/privacy-landing-page" target="_blank" rel="referrer" title="Adobe Journey Optimizer 中的隱私功能">隱私權功能</a>
                    </p>
                    <p class="is-size-6">瞭解如何處理隱私權請求、稽核使用者動作、管理同意、套用治理規則，以及運用進階安全性選項，例如客戶自控金鑰。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/privacy/privacy-landing-page" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">深入了解</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Data Governance Framework Overview">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/data-governance-framework" title="資料治理框架概觀" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/29708/?format=jpeg&nocache=1765241813815" alt="資料治理框架概觀"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/data-governance-framework" target="_blank" rel="referrer" title="資料治理框架概觀">資料治理框架概觀</a>
                    </p>
                    <p class="is-size-6">了解 Adobe Experience Platform 的控管功能。</p>
                </div>
                <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/data-governance-framework" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Classify data using labels">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/classify-data-using-lables" title="使用標籤進行資料分類" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/29709?format=jpeg&nocache=1765241813814" alt="使用標籤進行資料分類"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/classify-data-using-lables" target="_blank" rel="referrer" title="使用標籤進行資料分類">使用標籤進行資料分類</a>
                    </p>
                    <p class="is-size-6">了解如何在您的結構描述和資料集套用標籤。</p>
                </div>
                <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/classify-data-using-lables" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Create Data Usage Policies">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/create-data-usage-policies" title="建立資料使用原則" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/32977/?format=jpeg&nocache=1765241813810" alt="建立資料使用原則"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/create-data-usage-policies" target="_blank" rel="referrer" title="建立資料使用原則">建立資料使用原則</a>
                    </p>
                    <p class="is-size-6">學習如何建立和管理資料使用原則。</p>
                </div>
                <a href="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/create-data-usage-policies" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">觀看</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->


## 常見的實作陷阱和避免方式

大部分行動問題產生於&#x200B;**SDK或資料收集設定**，而非Journey Optimizer歷程或行銷活動本身。 使用下表找出問題，然後展開對應的區段以取得詳細資料。

### 陷阱總覽

| # | 問題/症狀 | 常見陷阱 | 修正一覽 |
|---|----------------------------------------------|-----------------------------------------------------|------------------------------------------|
| 1 | 引導式管道設定失敗；無流量或流量低 | [SDK版本或擴充功能未對齊](#1-sdk-versions-and-extensions-not-aligned-with-channel-requirements) | 更新SDK/擴充功能版本；在Assurance中驗證 |
| 2 | 追蹤批次失敗；AEP發生錯誤 | [資料串流或資料集設定錯誤](#2-misconfigured-datastreams-or-datasets) | 將事件對應到事件資料集，將設定檔對應到設定檔資料集 |
| 3 | 歷程不會引發；奇怪的個人化 | [缺少身分或同意/不一致](#3-missing-or-inconsistent-identity-and-consent) | 實作Edge身分與同意；在Assurance中驗證 |
| 4 | 無推播傳遞或在報表中開啟 | [推播權杖註冊或追蹤中斷](#4-push-token-registration-and-tracking-not-wired-correctly) | 透過SDK修正權杖註冊和互動追蹤 |
| 5 | 即使使用中行銷活動，仍沒有應用程式內曝光數 | [應用程式內訊息或內容卡未顯示](#5-in-app-messages-or-content-cards-not-displaying) | 檢查傳訊擴充功能、觸發器和Assurance決策回應 |

### 每個陷阱的詳細指引

開啟與您的症狀相符的陷阱，以檢視要檢查什麼以及如何加以修正。

+++ &#x200B;1. SDK版本和擴充功能不符合通道要求
**您將注意到的事項**

- 推播或應用程式內活動無法連線至裝置。
- 引導式管道設定或管道驗證失敗。
- Assurance會顯示遺失的Journey Optimizer、Edge或身分副檔名。

**檢查內容**

- 您是否使用引導式頻道設定所需的最低&#x200B;**行動核心**&#x200B;和&#x200B;**Journey Optimizer**&#x200B;擴充功能版本？
- 在&#x200B;**Assurance**&#x200B;中，在擴充功能和事件底下：
   - 您看到預期的擴充功能已載入嗎？
   - 事件是否會傳送至Edge Network並進行確認？

**如何修正**

- 升級至支援的行動SDK和Journey Optimizer擴充功能版本。
- 重建應用程式、重新連線至Assurance，然後重新執行引導式頻道設定。

請參閱：[設定行動裝置和網頁](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/configuration/guided-setup/set-mobile-config){target="_blank"}

+++

+++ 2.資料串流或資料集設定錯誤
**您將注意到的事項**

- Platform資料集中的事件或推播追蹤批次失敗。
- 資料擷取錯誤（例如「事件不支援更新」）。
- 推播或應用程式內報表顯示很少或沒有追蹤。

**檢查內容**

- 有人變更為Journey Optimizer追蹤建立的&#x200B;**系統結構描述或資料集**&#x200B;嗎？
- 在您的&#x200B;**資料流**&#x200B;中：
   - 體驗事件是否對應至&#x200B;**事件資料集**？
   - 設定檔屬性是否對應至&#x200B;**設定檔資料集**？

**如何修正**

- 請勿編輯AJO建立的系統資料集/結構描述。
- 更正資料流對應(事件→事件資料集、設定檔→設定檔資料集)。
- 偏好使用引導式管道設定或紀錄的資料流步驟，而非臨時變更。

請參閱： Adobe Journey Optimizer中的[推播通知流程](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs){target="_blank"}

+++

+++ 3.遺失或不一致的身分和同意
**您將注意到的事項**

- 應用程式使用者的歷程未如預期觸發。
- Personalization不符合使用者在其他頻道中的行為。
- 事件會出現在Experience Platform中，但設定檔看起來是分散的。

**檢查內容**

- Edge Network **的**&#x200B;身分識別是否已實作並傳送穩定的主要ID （例如，登入識別碼）？
- 當偏好設定變更時，**Edge Network的同意**&#x200B;是否已實作和更新？
- 在&#x200B;**Assurance**&#x200B;中：
   - 傳出事件是否包含同意值？
   - 它們是否包含一致的ECID和您的主要ID？

**如何修正**

- 在應用程式中實作或修正Edge Network **的**&#x200B;身分識別。
- 實作Edge Network **的**&#x200B;同意，並將其連線到您應用程式的同意UI。
- 在Assurance中重新測試，直到身分和同意出現在所有相關事件上為止。

請參閱：[Platform Mobile SDK實作的實作同意](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/consent){target="_blank"}

+++

+++ 4.推播權杖註冊和追蹤未正確佈線
**您將注意到的事項**

- 即使行銷活動或歷程執行，使用者仍不會收到推播通知。
- 推播報表不會顯示開啟、關閉或互動。

**檢查內容**

- 應用程式是否會使用Journey Optimizer擴充功能註冊推送代號：
   - 第一次安裝時？
   - 每次應用程式更新後？
   - 作業系統每次都會重新整理Token？
- 當使用者開啟或關閉通知時，您會在Assurance中看到追蹤事件嗎？

**如何修正**

- 新增或修正程式碼：
   - 建立或重新整理權杖時，請透過Journey Optimizer行動擴充功能註冊權杖。
   - 透過行動SDK傳送推播互動事件（開啟、關閉、自訂動作）。
- 使用Assurance確認註冊和追蹤事件如預期般引發。

請參閱： Adobe Journey Optimizer中的[推播通知流程](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs){target="_blank"}

+++

+++ 5.應用程式內訊息或內容卡未顯示
**您將注意到的事項**

- 即使促銷活動或歷程有效，應用程式內訊息或內容卡片也絕不會顯示。
- 報表顯示0次曝光。

**檢查內容**

- **Journey Optimizer行動傳訊/應用程式內擴充功能**&#x200B;和&#x200B;**傳訊SDK**&#x200B;是否已安裝並在應用程式中註冊？
- 在您的&#x200B;**標籤**&#x200B;設定中：
   - 您是否有規則可在正確的事件（例如熒幕檢視或自訂事件）上觸發請求？
- 在&#x200B;**Assurance**&#x200B;中：
   - 當這些事件引發時，您會看到應用程式內或內容卡決策請求發出嗎？
   - 您看到來自Edge Network的回應嗎？

**如何修正**

- 安裝並註冊必要的傳訊擴充功能。
- 新增或修正觸發目標事件（畫面、自訂事件）上決策的規則。
- 對於內容卡片，請確定：
   - 透過傳訊SDK API擷取卡片。
   - 在您的UI中呈現它們。
   - 透過SDK追蹤互動。

請參閱：
- [建立並傳送應用程式內訊息](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/experience-cloud/journey-optimizer/journey-optimizer-inapp){target="_blank"}
- [在行動SDK中設定內容卡支援](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/content-card-lp){target="_blank"}

+++

## 其他資源

- [在行動裝置上使用以CDN為基礎的使用者端個人化(ODD)，以加快個人化速度（部落格）](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/using-cdn-based-client-side-personalization-odd-on-mobile-for/ba-p/761626){target="_blank"}
- [下一層級行動應用程式參與度和成長率（高峰會工作階段）的秘密](https://business.adobe.com/summit/2025/sessions/the-secret-to-nextlevel-mobile-app-engagement-s603.html)
