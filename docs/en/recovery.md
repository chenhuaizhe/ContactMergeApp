# Backup, Undo, and Recovery History

- **Overview**: [English Overview](../../README.md) | [Deutsche Übersicht](../readme/README.de.md)
- **Guides**: [Quick Start](quick-start.md) | **Backup & Recovery** | [Permissions & Troubleshooting](permissions-troubleshooting.md)
- **Language / Sprache**: **English** | [Deutsch](../de/recovery.md)

This guide explains pre-merge backup options, how on-device undo and recovery work in **ContactMerge+ Cleaner**, and the exact limits of on-device recovery.

## Independent Backup Before Merging

- **Optional `.vcf` export**: Exporting a `.vcf` (vCard) file is optional—you do not have to export one before merging contacts in ContactMerge+ Cleaner.
- **Recommended before major cleanups**: Keeping an independent backup of your contacts before merging is strongly recommended, especially before your first cleanup. ContactMerge+ Cleaner does not provide its own cloud backup service or automatically export external backup files for you.
- **Further reading**: See [Backup Contacts Before Merge on iPhone](https://contactmerge.app/guides/backup-contacts-before-merge-iphone) and [How to Merge Contacts Safely](https://contactmerge.app/guides/merge-contacts-safely).

## Check and Save Contact Notes in Apple's Contacts App

Important Notes on non-primary contacts (the other cards that will be merged and deleted) are **not** read or copied to the primary contact during a merge. Before confirming any merge:

- **Inspect Notes in Apple's Contacts app, not in the preview**: ContactMerge+ Cleaner cannot read Contact Notes. Never assume a contact has no Notes just because none appear in the ContactMerge+ Cleaner preview—open Apple's **Contacts** app to check those cards and manually copy any important Notes into the primary contact (or another safe place) before merging.
- **Recheck after leaving the app to edit contacts**: If you switch out of ContactMerge+ Cleaner to view or edit contacts in Apple's Contacts app, return to ContactMerge+ Cleaner afterward and recheck the current duplicate candidates and merge preview before confirming. Do not assume an already-open candidate list or preview updates automatically.
- **Notes cannot be restored later**: Because ContactMerge+ Cleaner cannot read Notes, Notes from non-primary cards cannot be restored later through undo or `Recovery History`.

## Reversing Recent Changes in the App

ContactMerge+ Cleaner includes two on-device recovery features for recent actions:

- **`Undo Last Contact Merge` (most recent merge)**:
  - Targets only the single most recent merge.
  - **Verified screen location and caveats**: If you want to undo your most recent merge, open or return to the `Duplicate Contacts` scan results screen and look near the top of the screen, above the `Ready to merge` section, for the displayed `Undo Last Contact Merge` control.
  - **Version and verification limits**: Exact labels and screen layouts may vary by your installed app version or iOS version. This control location is verified from the dated `2026-11-03` English Release simulator screenshot rather than a live test of your installed version; this guide does not claim when the control is enabled in your session, that the undo action was tested end-to-end, or that it guarantees a complete reversal (and does not assume any specific confirmation prompt).
- **`Recovery History`**:
  - Uses an on-device recovery journal saved by the app when you merge or delete contacts.
  - Keeps **at most 3 merge records and at most 3 deletion records**.
  - Entries stay on the device for **about 30 days**; older entries or entries pushed past the 3-record limit for that action type cannot be restored.
  - **Unverified navigation path**: The entry point, screen navigation, and record-selection steps for `Recovery History` are not shown in the approved screenshots, so this guide cannot confirm the exact path for your installed app version. If you cannot locate `Recovery History` in your version of the app, please contact [Official Support](https://contactmerge.app/support).

## Important Limits of On-Device Recovery

Keep in mind what `Undo Last Contact Merge` and `Recovery History` do **not** provide:

- **Not a full system restore**: As shown in the app's own notice, Contact Notes cannot be read (so Notes from non-primary cards cannot be restored), and original system identifiers and links may not be restored.
- **Not unlimited undo**: `Recovery History` keeps at most 3 merge records and at most 3 deletion records for about 30 days on the device; older records beyond those limits cannot be restored.
- **No developer cloud backup; separate from account sync and system backups**:
  - Contact processing and the recovery journal stay on your device within the app; the developer does not provide a cloud backup service or upload your address book to developer servers.
  - **Account sync and iOS backups are separate**: iOS or account contact sync (such as iCloud or Google) and system or device backups are separate mechanisms controlled by your own account and iOS settings. Accordingly, these statements do **not** promise that a contact merge stays off iCloud/Google sync, and do **not** infer or promise whether system backups include or exclude app data.
  - Recovery is also not guaranteed beyond current app and device availability (for example, after uninstalling the app or losing or replacing your iPhone).
- **Conservative caution if contacts are edited later**: As conservative safety advice—rather than a verified hard block in the app—recovery cannot be guaranteed if affected contacts were edited or overwritten afterward (whether manually in Contacts, by another app, on another device, or through account sync). This guide does not claim the app always refuses recovery after later edits or state exact internal eligibility rules, but avoid editing merged contacts if you may still want to undo the merge.
- **Avoid risky manual repair attempts**: Do not repeatedly turn account sync off and on, delete mail or cloud accounts, or repeatedly reimport `.vcf` files to try to fix an unexpected merge result—doing so can multiply duplicates or overwrite contact details.

## Getting Support Safely

If you run into a question about recovery or cannot find a control in your version:

- Reach out through [Official Support](https://contactmerge.app/support).
- Share your iOS version, your ContactMerge+ Cleaner app version, and a plain description of what you expected vs. what happened.
- **Protect your privacy**: Never post personal contact details in public issues, and never upload contact lists or `.vcf` (vCard) files. Before sharing any screenshot, redact all names, phone numbers, email addresses, photos, street addresses, notes, and IDs—or use fabricated demo data only.

## Related Links

- [Quick Start: Scanning and Merging Safely](quick-start.md)
- [Permissions and Troubleshooting](permissions-troubleshooting.md)
- [Official Website](https://contactmerge.app)
- [Privacy Policy](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Documentation Status

Checked 8 Nov 2026. Screens, labels, and behavior may vary depending on your installed app version and iOS version.
