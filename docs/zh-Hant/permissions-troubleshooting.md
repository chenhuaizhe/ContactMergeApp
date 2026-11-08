# 權限設定與疑難排解

- **總覽與語言**：[繁體中文總覽](../readme/README.zh-Hant.md) | [英文總覽（English）](../../README.md) | [本指南英文版（English）](../en/permissions-troubleshooting.md)
- **操作指南**：[快速入門](quick-start.md) | [備份與復原](recovery.md) | **權限與疑難排解** | [常見問題（FAQ）](faq.md)

本指南涵蓋 iPhone 聯絡人取用權限設定、**ContactMerge+ Cleaner** 與 Apple 內建重複聯絡人功能的差異、同步帳號與換機移轉的安全處理方式、購買回復與退款常見疑問，以及如何安全地聯絡官方支援。

## iPhone 上的聯絡人取用權限

- **掃描與合併的必要條件**：ContactMerge+ Cleaner 需要聯絡人取用權限，才能在您的 iPhone 上尋找並合併重複聯絡人。所有聯絡人處理皆在您的裝置本機執行——您的通訊錄不會上傳至開發者伺服器，且開發者不提供雲端備份服務（此與由您自身設定控制的 iCloud／Google 聯絡人同步或 iOS 系統備份分屬不同機制）。
- **iOS 中的完整取用與限制取用**：依您的 iOS 版本而定，Apple 允許您在 iOS 系統設定中的隱私權與聯絡人權限頁面（英文介面路徑為 **Settings > Privacy & Security > Contacts**；實際選單名稱依 iOS 版本與系統語言顯示）控制應用程式可取用的聯絡人範圍，包括完整取用或僅限所選聯絡人的限制取用（請參閱 Apple 官方指南：[控制 iPhone 上「聯絡人」的取用權限（英文）](https://support.apple.com/guide/iphone/control-access-to-contacts-iph9536aa9a5/ios)）。
- **若無法執行掃描，或聯絡人顯示似乎不完整**：
  - 請先前往 iOS 系統設定檢查授予 ContactMerge+ Cleaner 的聯絡人權限等級。未完成授權或僅授予限制取用權限會影響本 App 可見的聯絡人範圍——這**不會**刪除您的聯絡人，但本 App 並不保證支援所有限制取用（部分選取）的操作流程。
  - 若檢查 iOS 系統設定後相關選項看似無法調整，或行為仍不如預期，請聯絡[官方支援（英文）](https://contactmerge.app/support)。
- **切勿採取的做法**：切勿為了排解權限問題而反覆開關帳號同步、移除帳號、刪除聯絡人，或重複匯入 `.vcf` 檔案。

## ContactMerge+ Cleaner 與 Apple 內建重複聯絡人工具的差異

Apple 內建的**「聯絡人」（`Contacts`）**App 提供原生的重複偵測與連結功能，其運作方式與 ContactMerge+ Cleaner 不同（請參閱 Apple 官方指南：[在 iPhone 上合併或隱藏重複的聯絡人（英文）](https://support.apple.com/guide/iphone/merge-or-hide-duplicate-contacts-iph2ab28320d/ios)）：

- **Apple「聯絡人」中的 `View Duplicates`（檢視重複項目）**：當系統偵測到可處理項目時，Apple 會在 `My Card`（我的名片）下方顯示 `View Duplicates` 提示，供使用者檢視與合併重複項目。若未出現 Apple 的 `View Duplicates` 橫幅提示——例如電話號碼使用了不同的國碼格式，或通訊錄聯絡人數量龐大時——請將此系統行為與 App 權限問題區分開來。本文件不宣稱 Apple 內部的偵測規則、不宣稱保證觸發的聯絡人數量門檻（例如 1,000 筆聯絡人）、不宣稱固定的等待時間，亦不提供一鍵「全部合併」的萬用解法。
- **連結／統一聯絡人與實際合併名片的差異**：在 Apple「聯絡人」App 中手動連結聯絡人（`Link Contacts`），只會將多張名片統一在單一檢視畫面中顯示，並不會合併底層的來源名片；此外，在統一聯絡人名片上所做的編輯，可能會同步至所連結的各個來源帳號。
- **ContactMerge+ Cleaner 的不同之處**：ContactMerge+ Cleaner 會在您的裝置本機執行掃描，並將候選項目區分為 `Ready to merge`（合併就緒）與 `Needs review`（需人工檢視），讓您先檢查合併預覽（同時先前往 Apple 內建**「聯絡人」（`Contacts`）**App 檢查 `Notes` 備註）。本 App 不承諾特定的掃描速度、通訊錄人數上限，亦不承諾自動修復先前已存在的通訊錄損壞。
- 相關官方網站指南：
  - [iOS「檢視重複項目」與國碼格式差異（英文）](https://contactmerge.app/guides/ios-view-duplicates-country-code)
  - [大型通訊錄未顯示「檢視重複項目」（英文）](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list)

## 換機移轉、帳號同步與避免誤刪聯絡人

設定新 iPhone、使用 `Move to iOS`（移轉到 iOS）、匯入聯絡人檔案，或同時連結多個帳號（如 iCloud 與 Google），常會讓跨帳號原有的舊重複項目浮現出來，這並不代表您的手機發生故障：

- **先等待初次同步完成並建立備份**：在判斷重複狀況前，請先等待裝置移轉或初次帳號同步完成（單靠等待不保證會自動消除重複，但能避免同步途中的資料變動造成混淆）。在進行任何變更前，請先確認聯絡人儲存在哪個帳號，並建立一份獨立且標註日期的備份。
- **謹慎檢視每一項變更**：請仔細檢查合併預覽（特別是 `Needs review` 群組），並先在 Apple 內建**「聯絡人」（`Contacts`）**App 中保留非主要聯絡人的 `Notes` 備註；若您曾離開本 App 前往外部檢視或編輯聯絡人，返回後請先重新核對目前的候選清單與預覽內容，再確認合併。
- **務必避免破壞性刪除操作**：從「聯絡人」移除整個帳號與刪除單筆聯絡人的運作機制不同，而刪除儲存在同步電子郵件或雲端帳號中的聯絡人，可能會在所有同步裝置上永久刪除這些資料（僅供風險背景參考，請參閱 Apple 的[在 iPhone「聯絡人」中加入或移除帳號（英文）](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios)與[刪除聯絡人注意事項（英文）](https://support.apple.com/en-us/111793)）。**切勿**將刪除來源聯絡人、點選 `"Delete from My iPhone"`（從我的 iPhone 刪除）、開關同步功能或反覆重新匯入 `.vcf` 檔案當作清理捷徑——若不確定該如何處理，請先暫停並向[官方支援（英文）](https://contactmerge.app/support)詢問。
- 官方情境指南：
  - [設定新 iPhone 後出現重複聯絡人（英文）](https://contactmerge.app/guides/duplicate-contacts-after-new-iphone)
  - [「移轉到 iOS」後出現重複聯絡人（英文）](https://contactmerge.app/guides/move-to-ios-duplicate-contacts)
  - [iCloud 同步後出現重複聯絡人（英文）](https://contactmerge.app/guides/icloud-duplicate-contacts-after-sync)
  - [在 iPhone 合併聯絡人前先備份（英文）](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)
  - [如何安全合併聯絡人（英文）](https://contactmerge.app/guides/merge-contacts-safely)

## Pro 專業版解鎖、回復購買與退款說明

- **一次性買斷解鎖（非訂閱制）**：Pro 為 App Store 一次性非消耗型購買項目，各地區價格由 Apple 直接顯示——請**勿**對本 App 套用取消訂閱的操作步驟。Pro 可解鎖包含超過 3 張聯絡人名片的群組合併，以及經確認後的 `Ready to merge` 群組批次合併（`Needs review` 群組仍維持逐組單獨檢視）。
- **回復 Pro 購買項目**：請確認您的 iPhone 已登入當初購買時所使用的**同一個 Apple Account**，並參閱 Apple 官方支援說明：[如果找不到或無法使用 App 內購買項目（英文）](https://support.apple.com/en-us/108096)。由於本文件未驗證 App 內回復購買按鈕的確切畫面路徑，我們不會猜測選單名稱、不建議重複購買 Pro，亦不保證自動回復成功——若無法順利回復，請聯絡[官方支援（英文）](https://contactmerge.app/support)或 Apple 支援。
- **退款申請**：App Store 的帳務由 Apple 處理，是否符合退款資格亦由 Apple 依國家或地區規定審核決定。部分購買項目可能符合退款條件，但**退款並非保證核准**。如有退款需求，請透過 Apple 官方流程於 [reportaproblem.apple.com（英文）](https://reportaproblem.apple.com) 提交申請（請參閱 Apple 官方說明：[為向 Apple 購買的 App 或內容申請退款（英文）](https://support.apple.com/en-us/118223)）；開發者並不保證退款申請獲准。

## 聯絡官方支援與保護個人隱私

- **客戶支援**：[官方支援（英文）](https://contactmerge.app/support)
- **建議提供的安全診斷資訊**：您的 ContactMerge+ Cleaner App 版本、iOS 版本、您預期的結果與實際觀察到的現象、該畫面屬於 Apple 系統控制項還是 ContactMerge+ Cleaner 內部畫面、涉及的帳號類型（例如 iCloud 或 Google，**請勿**提供您的電子郵件或帳號 ID），以及在相關情況下提供大略的聯絡人數量。
- **嚴格的隱私與個資遮蔽規範**：
  - 切勿在公開問題回報（Issue）中上傳私人聯絡人清單、`.vcf`（vCard）檔案、密碼、付款資訊或購買收據（如有任何帳務細節需求，請僅透過 Apple 官方安全管道，或於必要時透過適當的官方私密支援管道處理）。
  - 分享螢幕截圖前，請務必遮蔽所有真實姓名、電話號碼、電子郵件地址、照片、通訊地址、備註與各類識別碼——請盡可能改用虛構的示範資料。

## 相關連結

- [快速入門：安全掃描與合併聯絡人](quick-start.md)
- [備份、復原上次合併與復原紀錄](recovery.md)
- [常見問題（FAQ）](faq.md)
- [官方網站（英文）](https://contactmerge.app)
- [隱私權政策（英文）](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## 文件狀態

核對日期：2026 年 11 月 8 日。實際畫面、介面標籤與行為可能因您所安裝的 App 版本及 iOS 版本而異。
