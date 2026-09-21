---
source-git-commit: 084d4d9457db32e30855cd6466439b1de96f2b68
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 3%
---
# 即時動態

## 這是什麼

**已上線的活動**&#x200B;可讓您提供即時、持續性的更新，讓客戶在活動進行時瞭解最新資訊，例如正在準備訂單、運送中或正在路上的行程。 系統不會為每次更新傳送新通知，而是會建立單一上線活動，然後隨著活動發展而更新及結束，讓客戶的鎖定畫面或通知陰影與正在發生的情況保持同步。

Adobe Journey Optimizer支援兩個主要行動平台上的即時活動：

* **[iOS Live活動](/help/channels/ios-live-activities.md)** — iPhone鎖定畫面和動態島上的豐富即時更新。
* **[Android即時更新](/help/channels/android-live-updates.md)** — Android通知陰影中的即時、持續更新。

若要設定Mobile SDK並使用API來啟動、更新及結束客戶歷程中的即時體驗，請參閱[設定即時活動](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/channels/live-activity/configure-live-activity/mobile-live-configuration-sdk){target="_blank"}。

## 使用案例

當您需要以下動作時，選擇已上線活動作為您偏好的管道：

| # | 優點 | 原因 | 使用案例範例 |
|---|---------|-----|-------------------|
| 1 | 進行中的進度總覽 | 更新會直接顯示在鎖定畫面或Dynamic Island /通知陰影上，使用者無需開啟應用程式 | <ul><li>食物配送追蹤</li><li>叫車服務狀態</li><li>即時運動分數</li></ul> |
| 2 | 減少通知疲勞 | 已更新單一活動，而非引發重複的推播通知 | <ul><li>訂單準備與傳遞階段</li><li>航班登機與登機口更新</li></ul> |
| 3 | 時間關鍵、短期的內容 | 適用於具有明確開始和結束時間的活動 | <ul><li>路邊取車倒計時</li><li>鍛鍊或計時器工作階段</li></ul> |
| 4 | 原生、可檢視的UI | 使用作業系統原生表面（動態島、鎖定熒幕、通知陰影）以獲得高可見度、低摩擦的體驗 | <ul><li>套件追蹤</li><li>佇列或等待時間更新</li></ul> |

## 當&#x200B;*不*&#x200B;使用已上線活動時

* 對於沒有明確結尾的長期執行或未結束狀態 — 在基礎處理完成時結束活動。
* 針對促銷或行銷內容 — 請改用推播通知、應用程式內訊息或內容卡。
* 當更新節奏非常快時 — 頻繁的更新會被作業系統限制，或者讓使用者感到嘈雜。
* 如果您的應用程式不支援iOS Live活動或Android Live更新所需的最低作業系統版本。
