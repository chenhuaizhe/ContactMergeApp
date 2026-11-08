# ContactMerge+ Cleaner — Product Documentation & Support

Official public product documentation and support guides for **ContactMerge+ Cleaner** on iPhone. This repository contains user documentation only—it is not an app source code repository.

ContactMerge+ Cleaner processes contacts on your device and does not upload your address book to developer servers, and the developer does not provide a cloud backup service. (iOS or account contact sync—such as iCloud or Google—and system or device backups are separate mechanisms controlled by your own account and iOS settings.)

- **Website**: [Official Website](https://contactmerge.app)
- **App Store**: [Download on the App Store](https://apps.apple.com/us/app/contactmerge-contacts-cleaner/id6738980785)
- **Support**: [Official Support](https://contactmerge.app/support)
- **Languages**: **English** | [Deutsch](docs/readme/README.de.md) | [Français](docs/readme/README.fr.md) | [Italiano](docs/readme/README.it.md) | [Español](docs/readme/README.es.md) | [Português (Brasil)](docs/readme/README.pt-BR.md) | [日本語](docs/readme/README.ja.md) | [한국어](docs/readme/README.ko.md) | [简体中文](docs/readme/README.zh-Hans.md) | [繁體中文](docs/readme/README.zh-Hant.md)

## 4-Step Quick Start

1. **Back up and grant Contacts permission**: Keep an independent dated backup before major cleanups (optional `.vcf` export), let any phone transfer or initial sync finish, and allow Contacts access when iOS prompts you.
2. **Scan**: Run a scan to find possible duplicate groups on your iPhone.
3. **Preview, choose primary, and check Notes in Contacts**: Open one duplicate group, review the merge preview, pick the primary contact to keep as the base card, and inspect Apple's **Contacts** app for any Notes you want to save.
4. **Recheck and confirm carefully**: If you switched out to view or edit contacts in Apple's Contacts app, return and recheck the current duplicate candidates and preview first. Confirm only when the cards clearly belong to the same person and the preview keeps your expected fields.

<img src="assets/scan-results-demo.png" alt="English UI simulator demo (captured 2026-11-03) of Duplicate Contacts scan results with fictional contacts showing Undo Last Contact Merge, Ready to merge, and Needs review; screens and wording may differ by app or iOS version" width="420">

*Simulator demo with fictional contacts (English UI, captured 2026-11-03). Screens, layout, and wording may differ by installed app version or iOS version.*

## Key Safety Limits

- **`Ready to merge` vs. `Needs review`**:
  - `Ready to merge` means every pair of contacts in the group passed strict matching checks based on strong evidence across all pairs. Even so, always check the preview before confirming—shared names or phone numbers alone do not prove two cards belong to the same person.
  - `Needs review` means weaker or conflicting evidence (such as a shared family phone number, different names, conflicting birthdays, or partial overlap). It is a safety safeguard rather than an error; inspect each `Needs review` group manually one at a time, and never merge cards representing different people.
- **Check and save Notes in Apple's Contacts app before merging**:
  - Notes on non-primary contacts (the other cards being merged) are **not** read or copied to the primary contact, and cannot be restored later.
  - Because ContactMerge+ Cleaner cannot read Notes, never assume a contact has no Notes just because none appear in the merge preview. Inspect and copy important Notes directly in Apple's **Contacts** app before merging; if you view or edit contacts there, return to ContactMerge+ Cleaner and recheck the current duplicate candidates and preview before confirming (do not assume open views refresh automatically).
- **Undo and on-device recovery**:
  - `Undo Last Contact Merge` targets the single most recent merge (see [Backup, Undo, and Recovery History](docs/en/recovery.md) for verified screen location and version caveats).
  - `Recovery History` is an on-device recovery journal saved by the app that keeps **at most 3 merge records and at most 3 deletion records** for **about 30 days on the device** (its exact in-app navigation path is unverified in these docs; see the [Recovery Guide](docs/en/recovery.md)).
  - **Not a full system restore**: Contact Notes from non-primary cards cannot be restored, and original system identifiers and links may not be restored. The developer does not provide a cloud backup service (separate from your own iCloud/Google sync or iOS system backups, so merges may sync across your accounts). As a conservative precaution, recovery is not guaranteed after later contact edits, app uninstallation, or device loss.
- **Independent backup & account safety**: Exporting a `.vcf` file is optional, but keeping an independent dated backup that covers your actual contact accounts is recommended before your first cleanup (account sync is not an independent backup). Never delete source contacts, tap "Delete from My iPhone," or toggle/remove accounts as a troubleshooting step.

## Free vs. Pro

- **Free**: Scan your contacts, view all duplicate groups, and merge one duplicate group at a time (up to 3 contacts within that group). Multi-group batch merging is not included.
- **Pro**: One-time App Store unlock with no subscription; regional pricing is shown directly by Apple. Unlocks groups larger than 3 contacts and batch merging for `Ready to merge` groups after confirmation (`Needs review` groups are always reviewed one at a time).
- **Purchase Restore & Billing**: For restoring an existing Pro purchase on the same Apple Account or understanding Apple's refund process (handled by Apple via [reportaproblem.apple.com](https://reportaproblem.apple.com), eligibility not guaranteed), see the [FAQ](docs/en/faq.md#q16) or contact [Official Support](https://contactmerge.app/support).

## Operating Guides

- [Quick Start: Scanning and Merging Safely](docs/en/quick-start.md)
- [Backup, Undo, and Recovery History](docs/en/recovery.md)
- [Permissions and Troubleshooting](docs/en/permissions-troubleshooting.md)
- [Frequently Asked Questions (FAQ)](docs/en/faq.md)

## Official Support & Privacy

- **Support**: [Official Support](https://contactmerge.app/support)
- **Privacy**: [Privacy Policy](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)
- **Privacy & Redaction Notice**: Never share private contact lists, `.vcf` (vCard) files, passwords, payment details, or purchase receipts in public issues. Redact all real names, phone numbers, email addresses, photos, street addresses, notes, and account IDs before sharing any screenshot—use fabricated demo data whenever possible.

## Documentation Status

Checked 8 Nov 2026. Screens, labels, and behavior may vary depending on your installed app version and iOS version.
