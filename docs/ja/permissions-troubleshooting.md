# アクセス権限とトラブルシューティング

- **概要と言語**: [日本語版トップ](../readme/README.ja.md) | [English Overview](../../README.md)
- **ガイド**: [クイックスタート](quick-start.md) | [バックアップと復元](recovery.md) | **アクセス権限とトラブルシューティング** | [FAQ](faq.md)
- **言語 / Language**: **日本語** | [English](../en/permissions-troubleshooting.md)

このガイドでは、iPhone の連絡先アクセス権限の設定、**ContactMerge+ Cleaner** と Apple 標準の重複管理機能との違い、同期アカウントや機種変更時の安全な取り扱い、購入の復元や返金に関するご案内、およびプライバシーを守りながらサポートへ連絡する方法を説明します。

## iPhone での連絡先アクセス権限

- **スキャンと統合に必要です**: ContactMerge+ Cleaner が iPhone 上で重複を検出して統合するには、連絡先へのアクセス権限が必要です。連絡先の処理は端末内でローカルに行われ、アドレス帳が開発者のサーバーへアップロードされることはなく、開発者によるクラウドバックアップサービスも提供していません（ご自身の設定で管理される iCloud／Google の連絡先同期や iOS システムバックアップとは別の仕組みです）。
- **iOS におけるフルアクセスと制限付きアクセス**: お使いの iOS バージョンによっては、アプリに許可する連絡先の範囲（フルアクセス、または選択した連絡先のみの制限付きアクセスなど）を iOS の設定内にあるプライバシーとセキュリティの連絡先設定（英語表記参考：**Settings > Privacy & Security > Contacts**）で管理できます（Apple 公式ガイド [Control access to Contacts on iPhone（英語）](https://support.apple.com/guide/iphone/control-access-to-contacts-iph9536aa9a5/ios) をご参照ください）。
- **スキャンがブロックされる場合や連絡先が一部しか表示されない場合**:
  - iOS の設定で ContactMerge+ Cleaner に付与されている連絡先アクセス権限のレベルを確認してください。アクセスが不完全または制限付きになっていると、アプリから参照できる連絡先が制限される場合がありますが、それによって連絡先自体が**削除されるわけではありません**（なお、あらゆる制限付きアクセスの利用パターンへの完全な対応を保証するものではありません）。
  - iOS の設定を確認しても項目が利用できない場合や、想定外の動作が続く場合は、[公式サポート（英語）](https://contactmerge.app/support)までお問い合わせください。
- **行ってはいけない操作**: 権限に関するトラブル対処として、アカウント同期のオフ／オン切り替え、アカウントの削除、連絡先の削除、または `.vcf` ファイルの再インポートを決して行わないでください。

## ContactMerge+ Cleaner と Apple 標準の重複管理機能との違い

Apple の**連絡先**（Contacts）アプリには標準の重複検出およびリンク機能がありますが、ContactMerge+ Cleaner とは仕組みが異なります（Apple 公式ガイド [Merge or hide duplicate contacts on iPhone（英語）](https://support.apple.com/guide/iphone/merge-or-hide-duplicate-contacts-iph2ab28320d/ios) をご参照ください）。

- **Apple「連絡先」アプリの `View Duplicates`**: 利用可能な場合、Apple の連絡先アプリでは `My Card`（マイカード）の下に重複を確認・統合するための `View Duplicates`（重複項目を表示する案内）が表示されます。国番号の表記形式が異なる場合や件数の多いアドレス帳などで Apple 側の `View Duplicates` バナーが表示されない場合は、そのシステム側の挙動とアプリのアクセス権限の問題を切り分けて考えてください。本ドキュメントは、Apple 内部の検出ルール、保証された連絡先件数の閾値（1,000件など）、一定の待機時間、または一律の「すべて統合」による解決を主張するものではありません。
- **リンク／統一表示された連絡先とカードの統合の違い**: Apple の**連絡先**アプリで連絡先を手動でリンク（`Link Contacts`）すると、元のソースカード自体は統合されないまま1つの統一画面にまとめて表示されます。なお、統一カード上で行った編集は接続された元のアカウントへ反映される場合があります。
- **ContactMerge+ Cleaner の特徴と範囲**: ContactMerge+ Cleaner は端末内でスキャンを行い、候補を `Ready to merge` と `Needs review` に分けて統合プレビューを事前確認できるようにします（メモ欄については Apple の**連絡先**アプリで確認します）。特定のスキャン速度や処理可能な連絡先件数の保証、あるいは過去のアドレス帳破損の自動修復を約束するものではありません。
- 関連する公式ウェブガイド:
  - [iOS View Duplicates and Country Code Formatting（英語）](https://contactmerge.app/guides/ios-view-duplicates-country-code)
  - [View Duplicates Missing on a Large Contact List（英語）](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list)

## データ移行、アカウント同期、誤削除の防止

新しい iPhone の設定、`Move to iOS`（iOSに移行）の使用、ファイルのインポート、または複数アカウント（iCloud と Google など）の接続を行うと、以前から各アカウント間に存在していた重複が表面化することがありますが、これは端末の不具合を意味するものではありません。

- **まず初回同期の完了を待ち、バックアップを作成する**: 重複を判断する前に、データ移行や初回のアカウント同期が完了するまで待ってください（待つだけで重複が解消される保証はありませんが、同期途中の混乱を防げます）。連絡先がどのアカウントに保存されているかを確認し、変更を加える前に独立した日付付きバックアップを作成してください。
- **慎重に確認する**: 統合プレビュー（特に `Needs review` のグループ）を丁寧に確認し、メイン以外のカードにあるメモは先に Apple の**連絡先**アプリで保存してください。連絡先の閲覧・編集のためにアプリを離れた場合は、ContactMerge+ Cleaner に戻ってから現在の重複候補とプレビューを再確認したうえで確定してください。
- **削除操作の厳禁**: 連絡先設定からアカウントを削除する操作は個別の連絡先削除とは挙動が異なり、同期中のメールアカウントやクラウドアカウントから連絡先を削除すると、同期されているすべての端末から連絡先が完全に消去されるおそれがあります（背景知識として、Apple の [Add or remove accounts in Contacts on iPhone（英語）](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios) および[連絡先削除に関する注意（英語）](https://support.apple.com/en-us/111793)をご参照ください）。整理の近道として元の連絡先を削除したり、`"Delete from My iPhone"`（iPhoneから削除）をタップしたり、同期のオフ／オンを切り替えたり、`.vcf` ファイルの再インポートを繰り返したり**しないでください**。判断に迷う場合は操作を止め、[公式サポート（英語）](https://contactmerge.app/support)へご相談ください。
- 公式シナリオ別ガイド:
  - [Duplicate Contacts After Setting Up a New iPhone（英語）](https://contactmerge.app/guides/duplicate-contacts-after-new-iphone)
  - [Move to iOS Duplicate Contacts（英語）](https://contactmerge.app/guides/move-to-ios-duplicate-contacts)
  - [iCloud Duplicate Contacts After Sync（英語）](https://contactmerge.app/guides/icloud-duplicate-contacts-after-sync)
  - [Backup Contacts Before Merge on iPhone（英語）](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)
  - [How to Merge Contacts Safely（英語）](https://contactmerge.app/guides/merge-contacts-safely)

## Pro の機能解放、購入の復元、返金について

- **買い切り型の機能解放（サブスクリプションではありません）**: Pro は App Store での1回払いの非消耗型アプリ内課金であり、地域ごとの価格は Apple によって表示されます。本アプリに対してサブスクリプション（定期購読）の解約手順を行う必要はありません。Pro により、4件以上（3件超）の連絡先を含むグループの統合と、確認後の `Ready to merge` グループの一括統合が利用可能になります（`Needs review` は引き続き1グループずつの確認となります）。
- **Pro 購入の復元**: 購入時と**同じ Apple Account** で iPhone にサインインしていることを確認し、Apple の公式ガイド [If you can't find or use your in-app purchases（英語）](https://support.apple.com/en-us/108096) をご確認ください。アプリ内の正確な復元ボタンの経路は本ドキュメントでは未確認であるため、メニュー名を推測したり、Pro の再購入を勧めたり、自動復元を保証したりすることはしていません。復元できない場合は、[公式サポート（英語）](https://contactmerge.app/support)または Apple サポートへお問い合わせください。
- **返金の申請**: App Store の請求および返金の判断は Apple が行います。一部の購入は返金の対象となる場合がありますが、国や地域ごとの条件に基づき Apple が対象可否を決定するため、**返金が保証されるものではありません**。返金の申請は Apple の公式手続きである [reportaproblem.apple.com（英語）](https://reportaproblem.apple.com) を通じて行ってください（Apple の [Request a refund for apps or content that you bought from Apple（英語）](https://support.apple.com/en-us/118223) をご参照ください）。開発者側で返金の承認を保証することはできません。

## サポートへの連絡とプライバシー保護

- **サポート窓口**: [公式サポート（英語）](https://contactmerge.app/support)
- **安全にお知らせいただきたい情報**: ContactMerge+ Cleaner のアプリバージョン、iOS バージョン、期待していた動作と実際の挙動、確認している画面が Apple のシステム側か ContactMerge+ Cleaner 内か、関係するアカウント種別（iCloud や Google など。**メールアドレスやアカウント ID は記載しないでください**）、および必要に応じておおよその連絡先件数。
- **厳格なプライバシー保護とマスク処理のルール**:
  - 公開の Issue などに個人の連絡先リスト、`.vcf`（vCard）ファイル、パスワード、お支払い情報、購入時の領収書を決してアップロードしないでください（請求に関する個別情報は、必要な場合に限り Apple の公式な安全な窓口または適切な非公開の公式サポート窓口でのみ扱ってください）。
  - スクリーンショットを共有する際は、実名、電話番号、メールアドレス、写真、住所、メモ、各種 ID をすべて黒塗り（マスク処理）し、可能な限り架空のデモデータをご使用ください。

## 関連リンク

- [クイックスタート：安全なスキャンと連絡先の統合](quick-start.md)
- [バックアップ、取り消し、復元履歴](recovery.md)
- [よくある質問（FAQ）](faq.md)
- [公式ウェブサイト（英語）](https://contactmerge.app)
- [プライバシーポリシー（英語）](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## ドキュメントの確認状況

2026年11月8日確認。インストールされているアプリのバージョンおよび iOS のバージョンによって、画面、表示ラベル、動作が異なる場合があります。
