# ContactMerge+ Cleaner — Product Documentation & Support

Official public product documentation and support guides for **ContactMerge+ Cleaner** on iPhone. This repository contains user documentation only—it is not an app source code repository.

ContactMerge+ Cleaner processes contacts on your device and does not upload your address book to developer servers. (iOS or account contact sync—such as iCloud or Google—and system or device backups are separate mechanisms controlled by your own account and iOS settings.)

- **Website**: [Official Website](https://contactmerge.app)
- **App Store**: [Download on the App Store](https://apps.apple.com/us/app/contactmerge-contacts-cleaner/id6738980785)
- **Language / Sprache**: **English** | [Deutsch](docs/readme/README.de.md)

## 4-Step Quick Start

1. **Grant Contacts permission**: Allow Contacts access when iOS asks.
2. **Scan**: Run a scan to find possible duplicate groups on your iPhone.
3. **Preview, choose primary, and check Notes in Contacts**: Open one duplicate group, review the merge preview, pick the primary contact to keep as the base card, and check Apple's **Contacts** app for any Notes you want to save.
4. **Confirm carefully**: If you left the app to edit contacts, return and recheck the current duplicate candidates and preview first. Confirm only when the cards clearly belong to the same person and the preview keeps your expected fields.

<img src="assets/scan-results-demo.png" alt="Simulator demo of Duplicate Contacts scan results in English UI showing Undo Last Contact Merge, Ready to merge, and Needs review groups with fictional contacts" width="420">

*Simulator demo with fictional contacts (English UI, captured 2026-11-03). Screens and wording may differ by app or iOS version.*

## Key Safety Limits

- **`Ready to merge` vs. `Needs review`**:
  - `Ready to merge` means every pair of contacts in the group passed strict matching checks based on strong evidence across all pairs. Even so, always check the preview before confirming—shared names or phone numbers do not automatically prove two cards belong to the same person.
  - `Needs review` means weaker or conflicting evidence (such as a shared family phone number, different names, or partial overlap). This is a safety check rather than necessarily an error; inspect each `Needs review` group manually one at a time.
- **Check and save Notes in Apple's Contacts app before merging**:
  - Notes on non-primary contacts (the other cards being merged) are **not** read or copied to the primary contact, and cannot be restored later.
  - Because ContactMerge+ Cleaner cannot read Notes, never assume a contact has no Notes just because none appear in the merge preview. Inspect and copy important Notes directly in Apple's **Contacts** app before merging; if you edit contacts there, return to ContactMerge+ Cleaner and recheck the current duplicate candidates and preview before confirming.
- **Undo and on-device recovery**:
  - `Undo Last Contact Merge` targets the single most recent merge (see the [Recovery Guide](docs/en/recovery.md) for verified screen location and version caveats).
  - `Recovery History` is an on-device recovery log saved by the app that keeps **at most 3 merge records and at most 3 deletion records** for **about 30 days on the device**.
  - **Not a full system restore**: Contact Notes cannot be read (so Notes from non-primary cards cannot be restored), and original system identifiers and links may not be restored. The developer does not provide cloud backup (separate from your own iCloud/Google sync or system backup settings). As a conservative precaution, recovery is not guaranteed if contacts are edited later, or beyond current app and device availability (such as after uninstalling the app or losing your iPhone). See [Backup, Undo, and Recovery History](docs/en/recovery.md) for full details.
- **Pre-merge backup**: Exporting a `.vcf` file is optional—you do not have to export one before merging—but keeping an independent backup is recommended, especially before your first cleanup.

## Free vs. Pro

- **Free**: Scan your contacts, view all duplicate groups, and merge one duplicate group at a time (up to 3 contacts within that group). Multi-group batch merging is not included.
- **Pro**: One-time App Store unlock with no subscription; the regional price is shown directly by Apple. Unlocks full merging (including groups larger than 3 contacts) and batch merging for `Ready to merge` groups after confirmation. `Needs review` groups are still reviewed one at a time.
- **Billing & Purchase Support**: For help with an existing purchase or restoring Pro access, contact [Official Support](https://contactmerge.app/support).

## Operating Guides

- [Quick Start: Scanning and Merging Safely](docs/en/quick-start.md)
- [Backup, Undo, and Recovery History](docs/en/recovery.md)
- [Permissions and Troubleshooting](docs/en/permissions-troubleshooting.md)

## Official Support & Privacy

- **Support**: [Official Support](https://contactmerge.app/support)
- **Privacy**: [Privacy Policy](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)
- **Privacy & Redaction Notice**: Do not share private personal details in public issues, and never upload contact lists or `.vcf` (vCard) files. Redact all names, phone numbers, email addresses, photos, street addresses, notes, and IDs before sharing any screenshot—use fabricated demo data whenever possible.

## Documentation Status

Checked 8 Nov 2026. Screens, labels, and behavior may vary depending on your installed app version and iOS version.
