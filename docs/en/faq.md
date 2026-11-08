# Frequently Asked Questions (FAQ)

- **Overview & Languages**: [English Overview](../../README.md)
- **Guides**: [Quick Start](quick-start.md) | [Backup & Recovery](recovery.md) | [Permissions & Troubleshooting](permissions-troubleshooting.md) | **FAQ**

Practical answers for using **ContactMerge+ Cleaner** safely on iPhone, noting verified behavior and version limits.

## Backups and Duplicate Matching (`q01`–`q06`)

<a id="q01"></a>
### 1. Do I need a `.vcf` backup before merging, or is `Recovery History` enough?

Exporting a `.vcf` file is optional—the app does not force an export before merging—but keeping an independent, dated backup before your first or largest cleanup is strongly recommended. `Recovery History` is only a limited on-device journal (at most 3 merge records and at most 3 deletion records for about 30 days), cannot restore non-primary Contact Notes, and has no developer cloud backup. Account sync (iCloud or Google) is not an independent backup because merges can sync across devices. Ensure your backup covers the actual account storing your contacts and contains expected records, and avoid repeated `.vcf` reimports or blind full-device restores. See [Backup & Recovery](recovery.md) and [Backup Contacts Before Merge on iPhone](https://contactmerge.app/guides/backup-contacts-before-merge-iphone).

<a id="q02"></a>
### 2. What does `Ready to merge` mean, and should I still preview it?

`Ready to merge` means every pair of cards in the group passed strict checks based on strong evidence across all pairs. Still open the preview before confirming: matching names or numbers alone do not prove two cards represent the same person, and the app cannot read Contact Notes. Select your primary card, check Apple's **Contacts** app for Notes on non-primary cards, verify expected fields in the preview, and then confirm (or include `Ready to merge` groups in a confirmed Pro batch merge). See [Quick Start](quick-start.md) and [How to Merge Contacts Safely](https://contactmerge.app/guides/merge-contacts-safely).

<a id="q03"></a>
### 3. Why is a group marked `Needs review`, and can I batch-merge it?

`Needs review` means weaker or conflicting evidence—such as a shared household number, different names, conflicting birthdays, or partial overlap. It is a safety check, not a scan error. `Needs review` groups require individual manual inspection and are not eligible for Pro batch merging; do not force uncertain records into a merge, and leave cards unmerged if unsure. See [Quick Start](quick-start.md).

<a id="q04"></a>
### 4. Should I merge when names differ—or when two cards have the exact same name?

Neither is automatic. Name differences (like a nickname vs. full name) do not automatically mean different people, while identical names can still belong to two different relatives or coworkers. These docs do not claim exact capitalization or text-normalization rules in runtime matching. In the preview, compare the details actually displayed there (such as names, phone numbers, and email addresses where present)—never assume a field or Note is empty on a contact card just because it is not shown in the preview. Open the original cards in Apple's **Contacts** app to check company/employer details, other additional identity fields, and any Notes to save; if you switch out to view or edit cards there, return and recheck the current candidates and preview before confirming (do not assume open views auto-refresh). See [Quick Start](quick-start.md).

<a id="q05"></a>
### 5. Two different people share a home or office phone number. What should I do?

Do **not** merge them. Family members sharing a landline, partners sharing an emergency number, or coworkers sharing a main reception line often appear as candidates—typically in `Needs review`. Merging combines separate people into one card. Leave different people unmerged and confirm only when every card represents the same person. See [Quick Start](quick-start.md).

<a id="q06"></a>
### 6. Why did conflicting birthdays flag a group for review?

Conflicting birthdays across cards (noted in historical 1.3.6 release and support records alongside name conflicts) are a practical cue to inspect manually rather than an exact published algorithm threshold. Different dates may indicate two relatives sharing contact info or a typo on an older card. Check both cards in the preview and Apple's **Contacts** app before deciding. See [Quick Start](quick-start.md).

## Accounts, Transfers, and Apple Contacts (`q07`–`q11`)

<a id="q07"></a>
### 7. How does the app work with iCloud or Google contact sync?

Contacts are processed locally on your iPhone with no upload to developer servers and no developer cloud backup. However, iCloud/Google sync and iOS system backups are separate mechanisms controlled by your settings, so confirmed merges can sync across connected devices. Never toggle sync off/on, remove accounts, tap "Delete from My iPhone," or delete synced source contacts to troubleshoot—deleting email/cloud contacts can permanently delete them across devices (see Apple's [account guide](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios) and [deletion warning](https://support.apple.com/en-us/111793)). Identify your account and back up first; if unsure, stop and contact [Official Support](https://contactmerge.app/support). See [iCloud Duplicate Contacts After Sync](https://contactmerge.app/guides/icloud-duplicate-contacts-after-sync).

<a id="q08"></a>
### 8. Why did duplicates appear after a new iPhone setup or Move to iOS?

Setting up a new iPhone, using Move to iOS, importing files, or connecting multiple accounts often exposes older duplicates across sources—it does not mean your phone is faulty or prove one guaranteed cause. Let migration and initial background sync finish before scanning (not guaranteed to clear duplicates alone, but avoids mid-sync changes), make an independent backup, then review previews in [Quick Start](quick-start.md). See [Duplicate Contacts After Setting Up a New iPhone](https://contactmerge.app/guides/duplicate-contacts-after-new-iphone) and [Move to iOS Duplicate Contacts](https://contactmerge.app/guides/move-to-ios-duplicate-contacts).

<a id="q09"></a>
### 9. Apple's `View Duplicates` is missing—how is ContactMerge+ Cleaner different?

In Apple's **Contacts** app, `View Duplicates` appears below `My Card` when available, while manual `Link Contacts` unifies the display view without merging underlying cards (and unified-card edits can propagate to source accounts; see Apple's [duplicate guide](https://support.apple.com/guide/iphone/merge-or-hide-duplicate-contacts-iph2ab28320d/ios)). Missing `View Duplicates` is separate from app permissions—there is no guaranteed 1,000-contact threshold, fixed wait time, or safe blanket "Merge All" fix. Grant Contacts access in ContactMerge+ Cleaner to scan locally and inspect previews. See [Permissions & Troubleshooting](permissions-troubleshooting.md).

<a id="q10"></a>
### 10. Can duplicates have the same number with and without a country code?

Yes—one card may store a local number while another adds a country prefix (like `+1`), which Apple's duplicate notice may not flag as an exact match. Without claiming exact phone-normalization rules, ContactMerge+ Cleaner lets you compare full numbers in the merge preview. Verify both belong to the same person and keep your expected format before confirming. See [iOS View Duplicates and Country Code Formatting](https://contactmerge.app/guides/ios-view-duplicates-country-code).

<a id="q11"></a>
### 11. Does ContactMerge+ Cleaner handle large contact lists?

You can scan large address books locally even when Apple's `View Duplicates` does not appear, reviewing results in `Ready to merge` and `Needs review`. However, the app does not promise specific scan speeds or unlimited capacity. Let background sync finish, create an independent dated backup, and test merging one group first. See [Permissions & Troubleshooting](permissions-troubleshooting.md) and [View Duplicates Missing on a Large Contact List](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list).

## Undo, Recovery History, and Contact Notes (`q12`–`q14`)

<a id="q12"></a>
### 12. Where is `Undo Last Contact Merge`, and what does it cover?

`Undo Last Contact Merge` targets only your single most recent merge. In the approved `2026-11-03` English Release simulator screenshot, it appears near the top of `Duplicate Contacts` scan results above `Ready to merge`. Because this is based on that dated simulator screenshot rather than a live test of your installed build, enabled state, labels, and prompts may vary, and it is not a full restore (non-primary Notes cannot be restored, and original system IDs/links may not return). See [Backup & Recovery](recovery.md).

<a id="q13"></a>
### 13. What are the limits of `Recovery History`, and how do I open it?

`Recovery History` saves **at most 3 merge records and at most 3 deletion records** for **about 30 days on your device** (separate caps, not 6 guaranteed records). Older or excess entries cannot be restored, nor is recovery guaranteed after app uninstall or device loss. **Unverified path**: its entry point and record-selection steps are not shown in approved screenshots, so we do not guess menu paths—contact [Official Support](https://contactmerge.app/support) for help on your version. See [Backup & Recovery](recovery.md).

<a id="q14"></a>
### 14. Why check Notes in Apple's Contacts app—and what else limits recovery?

ContactMerge+ Cleaner cannot read Contact Notes: non-primary Notes are **not** copied during merges or restorable via Undo or `Recovery History`. Missing Notes in the preview never means a card has no Notes—inspect and copy them in Apple's **Contacts** app first. After viewing or editing contacts externally, return and recheck current candidates and the preview (open views may not auto-refresh). System IDs/links may not restore, and as conservative caution, later contact edits or sync updates may prevent clean recovery. See [Backup & Recovery](recovery.md).

## Free vs. Pro, Purchases, and Support (`q15`–`q18`)

<a id="q15"></a>
### 15. What is included in Free vs. Pro?

**Free** includes scanning, viewing all candidate groups, and merging one group at a time with up to 3 contacts in that group (no multi-group batch merge). **Pro** is a one-time App Store unlock with **no subscription**, at the regional price shown by Apple. Pro unlocks groups larger than 3 contacts and batch merging for confirmed `Ready to merge` groups (`Needs review` stays one at a time). See [Quick Start](quick-start.md).

<a id="q16"></a>
### 16. How do I restore my Pro purchase?

Pro is a non-consumable purchase. Confirm your iPhone uses the **same Apple Account** as the original purchase and check Apple's guide: [If you can't find or use your in-app purchases](https://support.apple.com/en-us/108096). Because the exact in-app restore UI path is unverified here, we do not guess Settings/Upgrade labels, recommend buying again, or guarantee automatic restoration. If Pro remains locked, contact [Official Support](https://contactmerge.app/support) or Apple Support. See [Permissions & Troubleshooting](permissions-troubleshooting.md).

<a id="q17"></a>
### 17. How do Apple refunds work—and is there a subscription to cancel?

Pro is a one-time purchase, not a subscription—do not follow subscription-cancellation instructions for this app. Apple handles App Store billing and decides refund eligibility by country/region; **refunds are not guaranteed**. You can request a refund through Apple's official process at [reportaproblem.apple.com](https://reportaproblem.apple.com) (see Apple's [refund guide](https://support.apple.com/en-us/118223)), and the developer does not guarantee refund approval. See [Permissions & Troubleshooting](permissions-troubleshooting.md).

<a id="q18"></a>
### 18. How do I check permissions, protect privacy, and contact support safely?

Check iOS **Settings > Privacy & Security > Contacts** (see Apple's [Contacts access guide](https://support.apple.com/guide/iphone/control-access-to-contacts-iph9536aa9a5/ios)); limited access only restricts app visibility without deleting contacts, though every limited-access flow is not guaranteed. Processing is local with no upload to developer servers (separate from your iCloud/Google sync and iOS backups; see the [Privacy Policy](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)). For [Official Support](https://contactmerge.app/support), share app/iOS versions, Apple control vs. app screen, account type (no ID), approximate count, and expected vs. observed behavior—never post contact lists, `.vcf` files, real personal details, passwords, or payment receipts publicly. See [Permissions & Troubleshooting](permissions-troubleshooting.md).

## Documentation Status

Checked 8 Nov 2026. Screens, labels, and behavior may vary depending on your installed app version and iOS version.
