# 備份、復原上次合併與復原紀錄

- **總覽與語言**：[繁體中文總覽](../readme/README.zh-Hant.md) | [英文總覽（English）](../../README.md) | [本指南英文版（English）](../en/recovery.md)
- **操作指南**：[快速入門](quick-start.md) | **備份與復原** | [權限與疑難排解](permissions-troubleshooting.md) | [常見問題（FAQ）](faq.md)

本指南說明合併聯絡人前的備份建議、**ContactMerge+ Cleaner** 裝置端復原功能的運作方式，以及您在合併前應了解的重要限制。

## 合併前的獨立備份建議

- **選用的 `.vcf` 匯出功能**：匯出 `.vcf`（vCard）檔案屬於選用操作——ContactMerge+ Cleaner 不會強制要求您在合併前先匯出檔案。
- **建議建立獨立且標註日期的備份**：強烈建議在合併前（特別是首次清理或執行批次合併前）保留一份獨立且標註日期的備份。ContactMerge+ Cleaner 不提供開發者雲端備份服務，也不會自動匯出外部備份檔案。
- **確認備份涵蓋的範圍**：請確認您的備份涵蓋實際儲存聯絡人的來源帳號（例如 iCloud 或 Google，而非沒有資料的帳號），且包含預期的聯絡人數量與詳細內容。帳號同步不等於獨立備份，因為清理過程中所做的變更可能會同步到您的其他連線裝置。
- **避免破壞性的還原操作**：請勿為了處理小範圍的聯絡人問題而反覆重新匯入 `.vcf` 檔案，或盲目執行整機回復——這麼做可能會讓重複名片倍增，或覆蓋近期修改過的聯絡人資料。
- **延伸閱讀**：請參閱[在 iPhone 合併聯絡人前先備份（英文）](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)與[如何安全合併聯絡人（英文）](https://contactmerge.app/guides/merge-contacts-safely)。

## 在 Apple「聯絡人」App 檢查並保留聯絡人備註（`Notes`）

合併過程中，非主要聯絡人（併入主要名片的其他名片）上的重要 `Notes`（備註欄位）**不會**被讀取或複製。在確認任何合併之前：

- **請在 Apple「聯絡人」App 中檢查備註，而非依賴預覽畫面**：ContactMerge+ Cleaner 無法讀取聯絡人的 `Notes` 欄位。切勿因為 ContactMerge+ Cleaner 預覽畫面沒有顯示備註，就假設該聯絡人沒有備註——合併前請開啟 Apple 內建的**「聯絡人」（`Contacts`）**App 檢查各張名片，並手動將任何重要備註複製到主要聯絡人（或其他安全位置）。
- **離開本 App 後返回請重新核對**：若您切換離開 ContactMerge+ Cleaner 前往 Apple「聯絡人」App 檢視或編輯聯絡人，返回後請先重新核對目前的重複候選清單與合併預覽，再確認合併。請勿假設原先已開啟的候選清單或預覽畫面會自動重新整理或自動觸發重新掃描。
- **備註無法在事後復原**：由於 ContactMerge+ Cleaner 無法讀取 `Notes`，非主要聯絡人名片上的備註事後無法透過 `Undo Last Contact Merge` 或 `Recovery History` 復原。

## 在 App 內復原近期變更

ContactMerge+ Cleaner 內建兩項具有嚴格範圍限制的裝置端復原功能：

- **`Undo Last Contact Merge`（復原最近一次合併）**：
  - 僅針對最新完成的**單筆**聯絡人合併。
  - **已驗證的畫面位置**：完成最近一次合併後若需尋找復原控制項，請開啟或返回 `Duplicate Contacts`（重複聯絡人掃描結果）畫面，查看畫面頂端附近、`Ready to merge` 區塊上方的 `Undo Last Contact Merge`。
  - **驗證範圍與版本注意事項**：此控制項位置係依據日期為 `2026-11-03` 的英文 Release 模擬器示範截圖確認，並非針對您裝置上實際安裝版本的實機測試。畫面文字與版面配置可能隨 App 或 iOS 版本而異；本指南不宣稱該控制項在您的操作階段何時處於啟用狀態、不宣稱已在您的安裝版本上實機驗證完整端對端還原、不保證每個底層聯絡人屬性皆能完全還原，亦不預設特定的確認提示視窗。
- **`Recovery History`（復原紀錄）**：
  - 使用 App 儲存在您 iPhone 本機上的裝置端復原日誌（recovery journal）。
  - **最多保留 3 筆合併紀錄與最多 3 筆刪除紀錄**（此為兩種操作類型各自獨立的上限，並非保證任何時候皆有 6 筆紀錄可供使用）。
  - 紀錄會在裝置上保留**約 30 天**；超過約 30 天，或因超出該操作類型 3 筆上限而被替換掉的舊紀錄，皆無法復原。
  - **導覽路徑未驗證**：核准使用的截圖中並未展示 `Recovery History` 的入口位置、畫面切換方式與紀錄選取步驟，因此本指南將目前的導覽路徑明確標示為未驗證，而不臆測您所安裝 App 版本中的選單名稱。若您無法找到 `Recovery History`，請聯絡[官方支援（英文）](https://contactmerge.app/support)。

## 裝置端復原功能的重要限制

請留意 `Undo Last Contact Merge` 與 `Recovery History` **無法提供**以下保障：

- **並非完整系統還原**：無法從非主要聯絡人名片讀取或復原 `Notes`（備註），且原本的系統識別碼（system identifiers）與聯絡人連結（links）可能無法還原。此外，本 App 亦不保證能修復先前由其他工具或匯入操作所造成的任意通訊錄損壞。
- **無開發者雲端備份；與帳號同步及系統備份各自獨立**：
  - 聯絡人處理與復原日誌僅保留在您裝置上的 App 內；開發者不會將您的通訊錄上傳至開發者伺服器，亦不提供雲端備份服務。
  - **帳號同步與 iOS 備份屬於獨立機制**：iOS 或帳號聯絡人同步（如 iCloud 或 Google）以及系統或裝置備份，均由您自身的帳號與 iOS 設定獨立控制。本文件**不保證**合併結果不會同步至 iCloud／Google，亦**不保證**系統備份是否包含或排除本 App 資料。
  - 若您解除安裝 App，或遺失、更換 iPhone，則不保證仍能復原。
- **聯絡人事後若經修改的保守安全提醒**：基於保守安全考量（並非宣稱 App 內設有已驗證的硬性阻擋條件），若受影響的聯絡人在合併後曾被編輯或遭同步更新覆蓋（無論是在 Apple「聯絡人」App、其他應用程式、其他裝置上或透過帳號同步），皆無法保證能順利復原。若您仍可能希望復原某次合併，請暫勿手動編輯該筆已合併的聯絡人。
- **切勿以刪除來源聯絡人或移除帳號來排錯**：刪除儲存在同步電子郵件或雲端帳號中的聯絡人，可能會在您的所有裝置上永久刪除這些資料（僅供了解風險背景，切勿照著移除帳號或刪除資料：請參閱 Apple 的[刪除聯絡人風險提醒（英文）](https://support.apple.com/en-us/111793)與[管理聯絡人帳號指南（英文）](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios)）。請勿點選 `"Delete from My iPhone"`（從我的 iPhone 刪除）、反覆開關帳號同步或移除帳號來排解合併問題——若有不確定之處，請先暫停並聯絡客戶支援。

## 安全取得官方支援

- 請透過[官方支援（英文）](https://contactmerge.app/support)與我們聯絡，並提供您的 ContactMerge+ Cleaner App 版本、iOS 版本、您目前查看的是 Apple「聯絡人」畫面還是 ContactMerge+ Cleaner 畫面、相關帳號類型（如 iCloud 或 Google，請勿提供您的帳號 ID），以及您預期的結果與實際發生的情況。
- **保護個人隱私**：切勿在公開問題回報（Issue）中張貼聯絡人清單、`.vcf` 檔案、密碼、付款資訊或購買收據。分享任何截圖前，請務必遮蔽所有真實姓名、電話號碼、電子郵件地址、照片、通訊地址、備註與各類識別碼——或僅使用虛構的示範資料。

## 相關連結

- [快速入門：安全掃描與合併聯絡人](quick-start.md)
- [權限設定與疑難排解](permissions-troubleshooting.md)
- [常見問題（FAQ）](faq.md)
- [官方網站（英文）](https://contactmerge.app)
- [隱私權政策（英文）](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## 文件狀態

核對日期：2026 年 11 月 8 日。實際畫面、介面標籤與行為可能因您所安裝的 App 版本及 iOS 版本而異。
