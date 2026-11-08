# ContactMerge+ Cleaner — 產品說明文件與支援指南

本儲存庫提供 iPhone 應用程式 **ContactMerge+ Cleaner** 的官方公開產品說明文件與支援指南。此處僅包含使用者說明文件，並非應用程式原始碼儲存庫。

ContactMerge+ Cleaner 會在您的 iPhone 本機處理聯絡人資料，不會將您的通訊錄上傳至開發者伺服器，且開發者不提供雲端備份服務。（iOS 或帳號聯絡人同步——例如 iCloud 或 Google——以及系統或裝置備份屬於獨立運作的機制，由您自身的帳號與 iOS 設定控制。）

- **官方網站**：[官方網站（英文）](https://contactmerge.app)
- **App Store**：[於 App Store 下載（英文頁面）](https://apps.apple.com/us/app/contactmerge-contacts-cleaner/id6738980785)
- **客戶支援**：[官方支援（英文）](https://contactmerge.app/support)
- **語言版本**：[English](../../README.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Italiano](README.it.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [日本語](README.ja.md) | [한국어](README.ko.md) | [简体中文](README.zh-Hans.md) | [**繁體中文**](README.zh-Hant.md)

## 快速入門 4 步驟

1. **建立備份並授予聯絡人權限**：進行大規模清理前，建議先保留一份獨立且標註日期的備份（可選用 `.vcf` 匯出），等待手機移轉或初次帳號同步完成，並在 iOS 詢問時允許取用聯絡人。
2. **掃描（Scan）**：執行掃描，找出 iPhone 上可能重複的聯絡人群組。
3. **檢視預覽、選擇主要聯絡人，並在「聯絡人」App 檢查備註（`Notes`）**：點開單一重複群組，檢視合併預覽畫面，選擇要保留為基底名片的主要聯絡人（Primary contact），並開啟 Apple 內建的**「聯絡人」（`Contacts`）**App 檢查是否有需要保留的重要備註（`Notes`）。
4. **返回重新核對並謹慎確認**：若您曾切換至 Apple「聯絡人」App 檢視或編輯聯絡人，返回本 App 後請先重新核對目前的重複候選清單與預覽內容。僅在確認各張名片確實屬於同一人，且預覽保留了預期欄位時才確認合併。

<img src="../../assets/scan-results-demo.png" alt="2026-11-03 擷取之英文介面模擬器示範畫面：以虛構聯絡人展示 Duplicate Contacts 掃描結果，顯示 Undo Last Contact Merge、Ready to merge 與 Needs review；實際畫面與文字可能因 App 或 iOS 版本而異" width="420">

*使用虛構聯絡人的模擬器示範畫面（英文介面，擷取於 2026-11-03）。實際畫面、版面配置與文字可能因您安裝的 App 版本或 iOS 版本而異。*

## 關鍵安全限制與注意事項

- **`Ready to merge` 與 `Needs review` 分類說明**：
  - `Ready to merge`（合併就緒）代表該群組內的**每一對**聯絡人名片皆具備明確比對證據，並通過嚴格檢查。即便如此，確認前仍請務必檢視合併預覽——僅有相同姓名或相同電話號碼，並不足以證明兩張名片屬於同一人。
  - `Needs review`（需人工檢視）代表比對證據較弱或存在衝突（例如共用家庭電話、姓名不同、生日衝突或僅部分資訊重疊）。這是保護資料的安全機制而非掃描錯誤；請逐組單獨人工檢視 `Needs review` 群組，切勿合併代表不同人物的名片。
- **合併前請先在 Apple「聯絡人」App 檢查並保留備註（`Notes`）**：
  - 非主要聯絡人（將併入主名片的其他名片）上的 `Notes`（備註欄位）**不會**被讀取或複製到主要聯絡人，合併後也無法復原。
  - 由於 ContactMerge+ Cleaner 無法讀取 `Notes`，切勿因為合併預覽中沒有顯示備註，就假設該名片沒有備註。合併前請直接開啟 Apple 內建的**「聯絡人」（`Contacts`）**App 檢查並複製重要備註；若您曾在該處檢視或編輯聯絡人，返回 ContactMerge+ Cleaner 後請先重新核對目前的重複候選項目與預覽再確認（請勿假設已開啟的畫面會自動重新整理）。
- **復原上次合併與裝置端復原紀錄**：
  - `Undo Last Contact Merge`（復原上一次聯絡人合併）僅針對最近一次完成的單筆合併（已驗證的畫面位置與版本注意事項請參閱[備份、復原上次合併與復原紀錄](../zh-Hant/recovery.md)）。
  - `Recovery History`（復原紀錄）是 App 儲存在裝置端的復原日誌，在裝置上**最多保留 3 筆合併紀錄與最多 3 筆刪除紀錄**，保存期限**約 30 天**（其在 App 內的確切導覽路徑於本文件中屬未驗證項目；詳見[復原指南](../zh-Hant/recovery.md)）。
  - **並非完整系統還原**：非主要名片的聯絡人 `Notes` 無法復原，且原本的系統識別碼與聯絡人連結可能無法還原。開發者不提供雲端備份服務（這與您自身的 iCloud／Google 同步或 iOS 系統備份分屬不同機制，因此合併結果可能會同步至您連結的帳號）。基於保守安全原則，若聯絡人事後經過編輯、解除安裝 App 或遺失裝置，皆不保證能夠復原。
- **獨立備份與帳號安全**：匯出 `.vcf` 檔案為選用操作，但建議在首次清理前先建立涵蓋實際聯絡人帳號、且標註日期的獨立備份（帳號同步不等於獨立備份）。切勿為了排錯而刪除來源聯絡人、點選 `"Delete from My iPhone"`（從我的 iPhone 刪除），或切換開關／移除帳號。

## 免費版（Free）與專業版（Pro）

- **Free（免費版）**：可掃描通訊錄、檢視所有重複群組，並每次單獨合併 1 個重複群組（該群組內最多 3 張聯絡人名片），不包含多群組批次合併。
- **Pro（專業版）**：App Store 一次性買斷解鎖，無訂閱制；各地區價格由 Apple 直接顯示。解鎖包含超過 3 張聯絡人名片的群組合併，以及經確認後的 `Ready to merge` 群組批次合併（`Needs review` 群組仍一律須逐組人工檢視）。
- **回復購買與帳務退款**：若需在同一個 Apple Account 上回復既有的 Pro 購買項目，或了解 Apple 的退款流程（透過 Apple 官方入口 [reportaproblem.apple.com（英文）](https://reportaproblem.apple.com) 處理，是否符合資格由 Apple 決定且不保證核准，開發者亦無法保證退款獲准），請參閱[常見問題（FAQ）](../zh-Hant/faq.md#q16)或聯絡[官方支援（英文）](https://contactmerge.app/support)。

## 操作指南

- [快速入門：安全掃描與合併聯絡人](../zh-Hant/quick-start.md)
- [備份、復原上次合併與復原紀錄](../zh-Hant/recovery.md)
- [權限設定與疑難排解](../zh-Hant/permissions-troubleshooting.md)
- [常見問題（FAQ）](../zh-Hant/faq.md)

## 官方支援與隱私權保護

- **客戶支援**：[官方支援（英文）](https://contactmerge.app/support)
- **隱私權政策**：[隱私權政策（英文）](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)
- **隱私與個資遮蔽提醒**：切勿在公開問題回報（Issue）中分享私人聯絡人清單、`.vcf`（vCard）檔案、密碼、付款資訊或購買收據。分享任何螢幕截圖前，請務必遮蔽所有真實姓名、電話號碼、電子郵件地址、照片、通訊地址、備註與帳號 ID——請盡可能改用虛構的示範資料。

## 文件狀態

核對日期：2026 年 11 月 8 日。實際畫面、介面標籤與行為可能因您所安裝的 App 版本及 iOS 版本而異。
