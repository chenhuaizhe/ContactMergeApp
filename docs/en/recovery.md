# Backup, Undo, and Recovery History

- **Overview & Languages**: [English Overview](../../README.md)
- **Guides**: [Quick Start](quick-start.md) | **Backup & Recovery** | [Permissions & Troubleshooting](permissions-troubleshooting.md) | [FAQ](faq.md)

This guide explains pre-merge backup practices, how on-device undo and recovery work in **ContactMerge+ Cleaner**, and the limits you should know before merging contacts.

## Independent Backup Before Merging

- **Optional `.vcf` export**: Exporting a `.vcf` (vCard) file is optional—ContactMerge+ Cleaner does not force you to export a file before merging.
- **Recommended independent dated backup**: Keeping an independent, dated backup before merging is strongly recommended, especially before your first cleanup or a batch merge. ContactMerge+ Cleaner does not provide a developer cloud backup service or automatically export external backup files.
- **Check what your backup covers**: Make sure your backup covers the actual source account holding your contacts (such as iCloud or Google rather than an empty account) and contains the contact count and details you expect. Account sync is not an independent backup because changes made during cleanup can sync to your other connected devices.
- **Avoid destructive restore attempts**: Do not repeatedly reimport `.vcf` files or perform a blind full-device restore to fix a small contact issue—doing so can multiply duplicates or overwrite newer edits.
- **Further reading**: See [Backup Contacts Before Merge on iPhone](https://contactmerge.app/guides/backup-contacts-before-merge-iphone) and [How to Merge Contacts Safely](https://contactmerge.app/guides/merge-contacts-safely).

## Check and Save Contact Notes in Apple's Contacts App

Important Notes on non-primary contacts (the other cards merged into the primary card) are **not** read or copied during a merge. Before confirming any merge:

- **Inspect Notes in Apple's Contacts app, not in the preview**: ContactMerge+ Cleaner cannot read Contact Notes. Never assume a contact has no Notes just because none appear in the ContactMerge+ Cleaner preview—open Apple's **Contacts** app to check those cards and manually copy any important Notes into the primary contact (or another safe place) before merging.
- **Recheck after leaving the app**: If you switch out of ContactMerge+ Cleaner to view or edit contacts in Apple's Contacts app, return afterward and recheck the current duplicate candidates and merge preview before confirming. Do not assume an already-open candidate list or preview refreshes or triggers a rescan automatically.
- **Notes cannot be restored later**: Because ContactMerge+ Cleaner cannot read Notes, Notes from non-primary cards cannot be restored later through `Undo Last Contact Merge` or `Recovery History`.

## Reversing Recent Changes in the App

ContactMerge+ Cleaner includes two on-device recovery features with strict scope limits:

- **`Undo Last Contact Merge` (most recent merge)**:
  - Targets only the single most recent merge.
  - **Verified screen location**: To look for undo after your latest merge, open or return to the `Duplicate Contacts` scan results screen and check near the top of the screen, above the `Ready to merge` section, for `Undo Last Contact Merge`.
  - **Verification and version caveats**: This control location is verified from the dated `2026-11-03` English Release simulator screenshot rather than a live test of your installed version. Screen wording and layout may vary by app or iOS version, and this guide does not claim when the control is enabled in your session, that end-to-end reversal was live-tested on your build, or that every underlying contact property is reversed (nor does it assume a specific confirmation prompt).
- **`Recovery History`**:
  - Uses an on-device recovery journal saved by the app on your iPhone.
  - Keeps **at most 3 merge records and at most 3 deletion records** (these are separate per-type caps, not a guarantee that 6 records are available at any time).
  - Entries remain on the device for **about 30 days**; older entries or entries pushed past the 3-record cap for that action type cannot be restored.
  - **Unverified navigation path**: The entry point, screen navigation, and record-selection steps for `Recovery History` are not shown in the approved screenshots, so this guide marks the current navigation path as unverified rather than guessing menu labels for your installed app version. If you cannot locate `Recovery History`, please contact [Official Support](https://contactmerge.app/support).

## Important Limits of On-Device Recovery

Keep in mind what `Undo Last Contact Merge` and `Recovery History` do **not** provide:

- **Not a full system restore**: Contact Notes cannot be read or restored from non-primary cards, and original system identifiers and contact links may not be restored. The app also cannot repair arbitrary earlier address-book damage caused by other tools or imports.
- **No developer cloud backup; separate from account sync and system backups**:
  - Contact processing and the recovery journal stay on your device within the app; the developer does not upload your address book to developer servers or provide a cloud backup service.
  - **Account sync and iOS backups are separate**: iOS or account contact sync (such as iCloud or Google) and system or device backups are separate mechanisms controlled by your own account and iOS settings. These docs do **not** promise that a merge stays off iCloud/Google sync, and do **not** promise whether system backups include or exclude app data.
  - Recovery is not guaranteed if you uninstall the app or lose or replace your iPhone.
- **Conservative caution if contacts are edited later**: As conservative safety advice—not a verified hard block in the app—recovery cannot be guaranteed if affected contacts were edited or synced over afterward (in Apple's Contacts app, another app, on another device, or via account sync). Avoid editing merged contacts if you may still want to undo that merge.
- **Never troubleshoot by deleting source contacts or removing accounts**: Deleting contacts stored in a synced email or cloud account can permanently delete them across your devices (see Apple's [contact deletion warning](https://support.apple.com/en-us/111793) and [account management guide](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios)). Do not tap "Delete from My iPhone," toggle account sync off and on, or remove accounts to troubleshoot a merge—if you are unsure, stop and contact support first.

## Getting Support Safely

- Reach out through [Official Support](https://contactmerge.app/support) with your ContactMerge+ Cleaner app version, iOS version, whether you are looking at an Apple Contacts screen or a ContactMerge+ Cleaner screen, relevant account type (such as iCloud or Google, without sharing your account ID), and what you expected vs. what happened.
- **Protect your privacy**: Never post contact lists, `.vcf` files, passwords, payment details, or purchase receipts in public issues. Redact all real names, phone numbers, email addresses, photos, street addresses, notes, and IDs before sharing any screenshot—or use fabricated demo data only.

## Related Links

- [Quick Start: Scanning and Merging Safely](quick-start.md)
- [Permissions and Troubleshooting](permissions-troubleshooting.md)
- [Frequently Asked Questions (FAQ)](faq.md)
- [Official Website](https://contactmerge.app)
- [Privacy Policy](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Documentation Status

Checked 8 Nov 2026. Screens, labels, and behavior may vary depending on your installed app version and iOS version.
