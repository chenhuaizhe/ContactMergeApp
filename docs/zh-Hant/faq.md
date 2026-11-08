# 常見問題（FAQ）

- **總覽與語言**：[繁體中文總覽](../readme/README.zh-Hant.md) | [英文總覽（English）](../../README.md) | [本指南英文版（English）](../en/faq.md)
- **操作指南**：[快速入門](quick-start.md) | [備份與復原](recovery.md) | [權限與疑難排解](permissions-troubleshooting.md) | **常見問題（FAQ）**

本頁整理在 iPhone 上安全使用 **ContactMerge+ Cleaner** 的實務解答，並清楚標示已驗證的產品行為與版本限制。

## 備份與重複聯絡人比對（`q01`–`q06`）

<a id="q01"></a>
### 1. 合併前一定要先匯出 `.vcf` 備份嗎？只靠 `Recovery History` 足夠嗎？

匯出 `.vcf` 檔案屬於選用操作——App 不會在合併前強制要求您匯出——但強烈建議您在進行第一次清理或大規模合併前，先保留一份獨立且標註日期的備份。`Recovery History`（復原紀錄）僅是容量有限的裝置端日誌（在裝置上最多保留 3 筆合併紀錄與最多 3 筆刪除紀錄，保存約 30 天），無法復原非主要聯絡人的 `Notes`（備註欄位），也沒有開發者雲端備份。此外，帳號同步（如 iCloud 或 Google）不等於獨立備份，因為合併結果可能會同步至其他連線裝置。請確認您的備份涵蓋實際儲存聯絡人的帳號並包含預期紀錄，同時避免重複匯入 `.vcf` 檔案或盲目執行整機回復。詳情請參閱[備份與復原](recovery.md)以及[在 iPhone 合併聯絡人前先備份（英文）](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)。

<a id="q02"></a>
### 2. `Ready to merge` 代表什麼意思？我還需要點開預覽檢查嗎？

`Ready to merge`（合併就緒）代表該群組內的**每一對**聯絡人名片皆具備明確比對證據，並通過嚴格檢查。即便如此，確認前仍請務必開啟預覽畫面檢查：僅憑相同姓名或相同電話號碼，並不足以證明兩張名片代表現實中的同一人，且本 App 無法讀取聯絡人的 `Notes`（備註欄位）。請先選好主要聯絡人名片，前往 Apple 內建的**「聯絡人」（`Contacts`）**App 檢查非主要名片上是否有重要備註，並在預覽中核對預期保留的欄位後再確認合併（或將已確認的 `Ready to merge` 群組納入 Pro 專業版批次合併）。詳情請參閱[快速入門](quick-start.md)與[如何安全合併聯絡人（英文）](https://contactmerge.app/guides/merge-contacts-safely)。

<a id="q03"></a>
### 3. 為什麼群組會被標示為 `Needs review`？可以將它批次合併嗎？

`Needs review`（需人工檢視）代表名片之間的比對證據較弱或存在衝突——例如共用家庭電話號碼、姓名不同、生日衝突或僅有部分欄位重疊。這是一項安全保護機制，並非掃描錯誤。請逐組單獨人工檢視並確認 `Needs review` 群組；您無法將證據模糊的群組強制納入 Pro 批次合併。若無法確定是否為同一人，或名片屬於不同人，請保持不合併。詳情請參閱[快速入門](quick-start.md)。

<a id="q04"></a>
### 4. 姓名不同時應該合併嗎？如果兩張名片姓名完全相同呢？

這兩種情況都不應直接自動合併。姓名有所差異（例如暱稱與本名、英文名與中文名）不代表一定是不同人；反之，姓名完全相同的兩張名片，仍可能分屬同名同姓的親友或同事。本文件不宣稱執行期比對中精確的大小寫或文字正規化演算法規則。在預覽畫面中，請比對該處實際顯示的資訊（例如有資料時顯示的姓名、電話號碼與電子郵件地址）——切勿因為某個欄位或備註未出現在預覽中，就假設原始名片上該欄位為空白。請在 Apple 內建的**「聯絡人」（`Contacts`）**App 中開啟原始名片，檢查公司／任職單位、其他補充身分細節及需要保留的 `Notes` 備註；若您曾切換至該處檢視或編輯名片，返回後請先重新核對目前的候選清單與預覽內容再確認合併（請勿假設已開啟的畫面會自動重新整理）。詳情請參閱[快速入門](quick-start.md)。

<a id="q05"></a>
### 5. 兩位不同的人共用同一個住家或公司電話號碼，該怎麼處理？

請**切勿**將他們合併。共用住宅電話（市話）的家庭成員、填寫相同緊急聯絡電話的伴侶，或共用公司總機代表號的同事，常會被列為重複候選項目——通常會出現在 `Needs review` 區塊中。一旦執行合併，兩位不同人物的資料就會被併入同一張名片。請將代表不同人物的名片保持不合併，僅在群組內每一張名片都確實代表同一人時才確認合併。詳情請參閱[快速入門](quick-start.md)。

<a id="q06"></a>
### 6. 為什麼生日衝突會讓群組被標記為需要人工檢視？

名片之間出現不同的生日日期（歷史 1.3.6 版本紀錄與支援紀錄中曾與姓名衝突一併提及），是提醒您進行人工檢視的實用線索，而非本文件所宣稱的固定公開演算法門檻。不同的生日可能代表共用聯絡資訊的兩位家人，也可能是舊名片上曾輸入錯誤的日期。決定是否合併前，請先在預覽畫面與 Apple 內建的**「聯絡人」（`Contacts`）**App 中核對兩張名片的內容。詳情請參閱[快速入門](quick-start.md)。

## 帳號同步、換機移轉與 Apple 內建「聯絡人」（`q07`–`q11`）

<a id="q07"></a>
### 7. 這款 App 如何與 iCloud 或 Google 聯絡人同步搭配運作？

聯絡人資料會在您的 iPhone 本機處理，不會上傳至開發者伺服器，亦無開發者雲端備份。不過，iCloud／Google 帳號同步與 iOS 系統備份屬於由您自身設定控制的獨立機制，因此已確認的合併結果可能會同步至其他連線裝置。切勿為了排錯而反覆開關同步功能、移除帳號、點選 `"Delete from My iPhone"`（從我的 iPhone 刪除），或刪除已同步的來源聯絡人——刪除電子郵件或雲端帳號中的聯絡人，可能會在所有同步裝置上造成永久刪除（請參閱 Apple 的[帳號管理指南（英文）](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios)與[刪除聯絡人風險提醒（英文）](https://support.apple.com/en-us/111793)）。變更資料前請先確認聯絡人所屬帳號並建立備份；若有不確定之處，請先暫停並聯絡[官方支援（英文）](https://contactmerge.app/support)。另請參閱[iCloud 同步後出現重複聯絡人（英文）](https://contactmerge.app/guides/icloud-duplicate-contacts-after-sync)。

<a id="q08"></a>
### 8. 為什麼設定新 iPhone 或使用 `Move to iOS` 後會出現重複聯絡人？

設定新 iPhone、使用 `Move to iOS`（移轉到 iOS）、匯入聯絡人檔案或同時連結多個帳號，常會使跨來源原有的舊重複項目顯現出來——這並不代表您的手機有問題，也不代表單一必然原因。請先等待資料移轉與初次背景同步完成後再執行掃描（單靠等待不保證會自動清除重複，但可避免同步途中的資料變動），接著建立一份獨立備份，並依照[快速入門](quick-start.md)檢視合併預覽。詳情請參閱[設定新 iPhone 後出現重複聯絡人（英文）](https://contactmerge.app/guides/duplicate-contacts-after-new-iphone)與[「移轉到 iOS」後出現重複聯絡人（英文）](https://contactmerge.app/guides/move-to-ios-duplicate-contacts)。

<a id="q09"></a>
### 9. Apple 內建的 `View Duplicates` 沒有顯示——ContactMerge+ Cleaner 有何不同？

在 Apple 內建的**「聯絡人」（`Contacts`）**App 中，當系統判定可用時，會在 `My Card`（我的名片）下方顯示 `View Duplicates`（檢視重複項目）；而手動使用 `Link Contacts`（連結聯絡人）僅會統一顯示畫面，並不會合併底層來源名片（且在統一名片上所做的編輯可能會同步至所連結的來源帳號；請參閱 Apple 的[重複聯絡人處理指南（英文）](https://support.apple.com/guide/iphone/merge-or-hide-duplicate-contacts-iph2ab28320d/ios)）。系統未顯示 `View Duplicates` 與本 App 的取用權限分屬不同問題——並不存在保證觸發的 1,000 筆聯絡人門檻、固定等待時間或安全的「全部合併」通則。您可以在 ContactMerge+ Cleaner 中授予聯絡人權限，進行本機掃描並逐一檢查合併預覽。詳情請參閱[權限與疑難排解](permissions-troubleshooting.md)。

<a id="q10"></a>
### 10. 同一支電話號碼一張有國碼、一張沒有國碼，也會產生重複名片嗎？

會的——例如一張名片儲存本地號碼，另一張則加上國碼前綴（如 `+1`），Apple 內建的重複提示不一定會將其視為完全相符的項目。在不宣稱精確電話號碼正規化演算法規則的前提下，ContactMerge+ Cleaner 能讓您在合併預覽畫面中直接比對完整電話號碼。確認合併前，請核實兩組號碼確實屬於同一人，並確認預覽保留了您預期的號碼格式。詳情請參閱[iOS「檢視重複項目」與國碼格式差異（英文）](https://contactmerge.app/guides/ios-view-duplicates-country-code)。

<a id="q11"></a>
### 11. ContactMerge+ Cleaner 可以處理大型通訊錄嗎？

即使通訊錄規模較大且未出現 Apple 的 `View Duplicates` 提示，您仍可在裝置本機執行掃描，並在 `Ready to merge` 與 `Needs review` 分類中檢視結果。不過，本 App 不承諾特定的掃描速度或無限的通訊錄容量上限。建議先等待背景同步完成，建立一份獨立且標註日期的備份，並先測試合併單一群組以確認結果符合預期。詳情請參閱[權限與疑難排解](permissions-troubleshooting.md)與[大型通訊錄未顯示「檢視重複項目」（英文）](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list)。

## 復原上次合併、`Recovery History` 與聯絡人備註（`q12`–`q14`）

<a id="q12"></a>
### 12. `Undo Last Contact Merge` 在哪個位置？它的復原範圍為何？

`Undo Last Contact Merge`（復原上一次聯絡人合併）僅針對您最近完成的單筆合併。在經核准的 `2026-11-03` 英文 Release 模擬器示範截圖中，該控制項位於 `Duplicate Contacts`（重複聯絡人）掃描結果畫面頂端附近、`Ready to merge` 區塊上方。由於此資訊係根據該張特定日期的模擬器截圖，而非針對您實際安裝版本的實機測試，因此按鈕的啟用狀態、標籤文字與提示視窗可能因版本而異；同時它並非完整系統還原（非主要名片的 `Notes` 備註無法復原，且原本的系統識別碼與連結可能無法還原）。詳情請參閱[備份與復原](recovery.md)。

<a id="q13"></a>
### 13. `Recovery History` 有哪些限制？該如何開啟？

`Recovery History`（復原紀錄）在您的裝置上**最多保留 3 筆合併紀錄與最多 3 筆刪除紀錄**，保存期限**約 30 天**（兩類紀錄分開計算上限，並非保證隨時有 6 筆可用紀錄）。超過保存期限或超出該類型 3 筆上限的舊紀錄無法復原；解除安裝 App 或遺失裝置後亦不保證能夠復原。**路徑未驗證**：核准的截圖中未包含 `Recovery History` 的入口位置與紀錄選取步驟，因此我們不會臆測選單路徑——若在您安裝的版本中需要協助尋找，請聯絡[官方支援（英文）](https://contactmerge.app/support)。詳情請參閱[備份與復原](recovery.md)。

<a id="q14"></a>
### 14. 為什麼一定要到 Apple「聯絡人」App 檢查 `Notes`（備註）？還有哪些因素會限制復原？

ContactMerge+ Cleaner 無法讀取聯絡人的 `Notes` 欄位：非主要名片上的備註在合併時**不會**被複製，事後也無法透過 `Undo Last Contact Merge` 或 `Recovery History` 復原。合併預覽中沒有顯示備註，絕不代表該名片沒有備註——合併前請務必先到 Apple 內建的**「聯絡人」（`Contacts`）**App 檢查並手動複製重要備註。在外部檢視或編輯聯絡人後，返回本 App 時請重新核對目前的候選清單與預覽（已開啟的畫面不一定會自動重新整理）。此外，系統識別碼與聯絡人連結可能無法還原；基於保守安全提醒，合併後若對聯絡人進行編輯或發生同步更新，亦可能導致無法完整復原。詳情請參閱[備份與復原](recovery.md)。

## 免費版與 Pro 專業版、購買回復與客戶支援（`q15`–`q18`）

<a id="q15"></a>
### 15. 免費版（Free）與專業版（Pro）分別包含哪些功能？

**Free（免費版）**支援掃描通訊錄、檢視所有重複候選群組，並每次單獨合併 1 個群組，且該群組內最多包含 3 張聯絡人名片（不包含跨群組批次合併）。**Pro（專業版）**為 App Store 一次性買斷解鎖，**無訂閱制**，售價依 Apple 在您所在地區顯示的金額為準。Pro 可解鎖包含超過 3 張聯絡人名片的群組合併，以及經確認後的 `Ready to merge` 群組批次合併（`Needs review` 群組仍維持逐組單獨檢視）。詳情請參閱[快速入門](quick-start.md)。

<a id="q16"></a>
### 16. 如何回復已購買的 Pro 專業版？

Pro 屬於非消耗型購買項目。請先確認您的 iPhone 已登入當初購買時使用的**同一個 Apple Account**，並參閱 Apple 官方指南：[如果找不到或無法使用 App 內購買項目（英文）](https://support.apple.com/en-us/108096)。由於本文件未驗證 App 內回復購買按鈕的確切介面路徑，我們不會猜測「設定」或「升級」等選單標籤、不建議重複購買，亦不保證自動回復成功。若 Pro 仍處於鎖定狀態，請聯絡[官方支援（英文）](https://contactmerge.app/support)或 Apple 支援。詳情請參閱[權限與疑難排解](permissions-troubleshooting.md)。

<a id="q17"></a>
### 17. Apple 退款流程如何運作？是否有訂閱需要取消？

Pro 為一次性購買項目而非訂閱制——請勿對本 App 執行取消訂閱的操作步驟。所有 App Store 帳務均由 Apple 處理，是否符合退款資格亦由 Apple 依國家或地區規定決定；**退款並非保證核准**。如需申請退款，請直接透過 Apple 官方入口 [reportaproblem.apple.com（英文）](https://reportaproblem.apple.com) 提交（請參閱 Apple 的[退款申請說明（英文）](https://support.apple.com/en-us/118223)）；開發者無法保證退款申請獲准。詳情請參閱[權限與疑難排解](permissions-troubleshooting.md)。

<a id="q18"></a>
### 18. 如何檢查聯絡人權限、保護個人隱私並安全地聯絡官方支援？

請前往 iOS 系統設定中的隱私權與聯絡人權限頁面檢查設定（英文介面為 **Settings > Privacy & Security > Contacts**；請參閱 Apple 的[聯絡人取用權限指南（英文）](https://support.apple.com/guide/iphone/control-access-to-contacts-iph9536aa9a5/ios)）；限制取用只會影響 App 可見的聯絡人範圍而不會刪除聯絡人，但本 App 不保證支援每一種限制取用流程。聯絡人資料皆於本機處理，不會上傳至開發者伺服器（與您的 iCloud／Google 同步及 iOS 備份分屬不同機制；請參閱[隱私權政策（英文）](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)）。聯絡[官方支援（英文）](https://contactmerge.app/support)時，請提供 App 版本、iOS 版本、畫面屬於 Apple 系統控制項或本 App 畫面、帳號類型（勿附帳號 ID）、大略聯絡人數量，以及預期與實際觀察到的現象——切勿在公開場合張貼聯絡人清單、`.vcf` 檔案、真實個人資料、密碼或購買收據。詳情請參閱[權限與疑難排解](permissions-troubleshooting.md)。

## 文件狀態

核對日期：2026 年 11 月 8 日。實際畫面、介面標籤與行為可能因您所安裝的 App 版本及 iOS 版本而異。
