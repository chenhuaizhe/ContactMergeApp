# Quick Start: Scanning and Merging Safely

- **Overview & Languages**: [English Overview](../../README.md)
- **Guides**: **Quick Start** | [Backup & Recovery](recovery.md) | [Permissions & Troubleshooting](permissions-troubleshooting.md) | [FAQ](faq.md)

This guide shows how to find, check, and merge duplicate contacts on your iPhone using **ContactMerge+ Cleaner**.

ContactMerge+ Cleaner processes your contacts on your device, does not upload your address book to developer servers, and does not provide a developer cloud backup service. (iOS or account contact sync—such as iCloud or Google—and system or device backups are separate mechanisms controlled by your own account and iOS settings.) Product information and downloads are available on the [Official Website](https://contactmerge.app).

## Before You Begin

- **Create an independent dated backup (recommended)**: Exporting a `.vcf` (vCard) file is optional—you do not have to export one before merging—but keeping an independent dated backup is strongly recommended, especially before your first cleanup. Make sure your backup covers the actual accounts holding your contacts and contains the records you expect. Account sync (such as iCloud or Google) is not an independent backup because merges can sync across connected devices. See [Backup, Undo, and Recovery History](recovery.md) and [Backup Contacts Before Merge on iPhone](https://contactmerge.app/guides/backup-contacts-before-merge-iphone).
- **Let transfers and initial syncs finish**: If you recently set up a new iPhone, used Move to iOS, or added an email or cloud account, wait until background syncing finishes before scanning and merging (waiting avoids mid-sync changes, though it is not guaranteed to remove existing duplicates on its own).

## Step-by-Step Merging Workflow

1. **Grant Contacts permission**: Allow Contacts access when iOS asks. If no prompt appears or visibility looks incomplete, see [Permissions and Troubleshooting](permissions-troubleshooting.md).
2. **Scan your address book**: Run a scan in ContactMerge+ Cleaner to view candidate duplicate groups.
3. **Open one group and preview**: Tap a duplicate group, inspect the merge preview, and choose which contact card should stay as the primary contact (base card).
4. **Check Notes in Apple's Contacts app and verify fields before confirming**:
   - Important Notes on non-primary contacts (the other cards that will be merged) are **not** read or copied to the primary contact, and cannot be restored later.
   - **Check Notes in Apple's Contacts app, not in the preview**: ContactMerge+ Cleaner cannot read Contact Notes. Never assume a contact has no Notes just because none appear in the ContactMerge+ Cleaner preview—open Apple's **Contacts** app to inspect those cards and copy any important Notes into the primary contact before merging.
   - **Recheck after external viewing or edits**: If you leave ContactMerge+ Cleaner to view or edit contacts in Apple's Contacts app, return afterward and recheck the current duplicate candidates and merge preview before confirming. Do not assume an already-open candidate list or preview refreshes or rescans automatically.
   - **Verify identity and expected fields**: Confirm the merge only when the cards clearly belong to the same person in real life and the preview keeps the fields you expect.

### Example: Scan Results and Merge Preview

<img src="../../assets/scan-results-demo.png" alt="English UI simulator demo (captured 2026-11-03) of Duplicate Contacts scan results with fictional contacts showing Undo Last Contact Merge, Ready to merge, and Needs review; screens and wording may differ by app or iOS version" width="420">

*Scan results — Simulator demo with fictional contacts (English UI, captured 2026-11-03). Screens, layout, and wording may differ by installed app version or iOS version.*

<img src="../../assets/merge-preview-demo.png" alt="English UI simulator demo (captured 2026-11-03) of Merge Preview with fictional contacts showing match reasons, Check and preserve notes in Contacts warning, and primary contact selection while the second contact row is below the visible scroll area; screens and wording may differ by app or iOS version" width="420">

*Merge preview and primary contact selection — Simulator demo with fictional contacts (English UI, captured 2026-11-03; the second contact row appears below the visible scroll area so both cards are not visible at once). Screens, layout, and wording may differ by installed app version or iOS version.*

## Understanding Group Labels: `Ready to merge` vs. `Needs review`

ContactMerge+ Cleaner sorts candidate duplicate groups into two sections based on the available matching evidence (these docs describe safe review habits rather than claiming exact internal runtime thresholds or normalization rules):

- **`Ready to merge`**:
  - Every pair of contacts in the group passed strict matching checks based on strong evidence across all pairs.
  - **Preview is still required**: Sharing a name or phone number alone does not prove two cards represent the same person. Always inspect the preview and check Apple's **Contacts** app for Notes before confirming.
  - Eligible for Pro batch merging after your confirmation.
- **`Needs review`**:
  - Cards have weaker or conflicting evidence—for example, a shared household or workplace phone number, name variations, conflicting birthdays, or partial overlap.
  - Seeing `Needs review` is a conservative safeguard rather than a scan error: name differences do not automatically mean two different people, while shared numbers or matching names can still belong to different family members or coworkers.
  - Must be inspected and confirmed manually one group at a time. `Needs review` groups are never included in batch merges, and there is no setting to force ambiguous groups into batch merging. If two cards represent different people, leave them unmerged.

## Free vs. Pro Capabilities

- **Free**:
  - Scan and view all detected duplicate groups.
  - Merge one duplicate group at a time, with up to 3 contacts inside that group (multi-group batch merging is not included).
- **Pro**:
  - One-time App Store unlock with no subscription; Apple displays the regional price for your storefront.
  - Unlocks merging for groups larger than 3 contacts and batch merging for `Ready to merge` groups after confirmation (`Needs review` groups still require manual, one-at-a-time review).
  - Neither tier claims specific scan speeds or unlimited contact-list capacity.
  - For purchase restoration or Apple refund rules, see the [FAQ](faq.md#q15) or contact [Official Support](https://contactmerge.app/support).

## Related Guides & Support

- [Backup, Undo, and Recovery History](recovery.md)
- [Permissions and Troubleshooting](permissions-troubleshooting.md)
- [Frequently Asked Questions (FAQ)](faq.md)
- [How to Merge Contacts Safely](https://contactmerge.app/guides/merge-contacts-safely)
- [Backup Contacts Before Merge on iPhone](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)
- [Official Support](https://contactmerge.app/support)
- [Privacy Policy](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Documentation Status

Checked 8 Nov 2026. Screens, labels, and behavior may vary depending on your installed app version and iOS version.
