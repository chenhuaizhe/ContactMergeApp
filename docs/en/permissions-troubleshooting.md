# Permissions and Troubleshooting

- **Overview**: [English Overview](../../README.md) | [Deutsche Übersicht](../readme/README.de.md)
- **Guides**: [Quick Start](quick-start.md) | [Backup & Recovery](recovery.md) | **Permissions & Troubleshooting**
- **Language / Sprache**: **English** | [Deutsch](../de/permissions-troubleshooting.md)

This guide covers Contacts permission questions on iPhone, how **ContactMerge+ Cleaner** differs from Apple's built-in duplicate tools, safety steps after phone transfers or account sync, and how to contact support safely.

## Contacts Permission on iPhone

- **Required to use the app**: ContactMerge+ Cleaner needs Contacts access to scan and merge duplicates on your device. Your address book is processed on your device and is not uploaded to developer servers (separate from any iCloud/Google contact sync or system backups controlled by your own account and iOS settings).
- **Full vs. limited access**: Depending on your iOS version, iOS may show full or limited Contacts access options.
- **What to check if scanning is blocked or incomplete**:
  - Check the Contacts permission for ContactMerge+ Cleaner in iOS Settings.
  - If the permission setting is unavailable, appears stuck, or still behaves unexpectedly after checking iOS Settings, contact [Official Support](https://contactmerge.app/support) with your iOS version, app version, and what you expected vs. what happened.
- **What not to do**: Do not repeatedly turn account sync off and on, delete accounts, or reimport `.vcf` files to try to fix permissions. Those steps do not fix app permissions and can create extra duplicates or data loss.

## ContactMerge+ Cleaner vs. Apple View Duplicates / Merge Duplicates

Apple's built-in **View Duplicates / Merge Duplicates** feature in the iOS Contacts app is separate from ContactMerge+ Cleaner:

- Apple's built-in tool offers duplicate review and merging and may show exact duplicates, but it is not guaranteed to show duplicates when phone numbers use different country-code formats or when you have a large address book.
- ContactMerge+ Cleaner scans on your device and separates candidate groups into `Ready to merge` and `Needs review` so you can check a preview before confirming. However, ContactMerge+ Cleaner does not promise specific scan speeds, contact-list size limits, or automatic repair of earlier address book damage.
- Related official guides:
  - [iOS View Duplicates and Country Code Formatting](https://contactmerge.app/guides/ios-view-duplicates-country-code)
  - [View Duplicates Missing on a Large Contact List](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list)

## Migration and Sync Duplicate Scenarios

Duplicates often appear right after setting up a new iPhone, transferring from Android, or syncing iCloud and email accounts. Follow these precautions:

- Wait until phone migration or background account syncing finishes completely before scanning and merging.
- Create an independent backup before your first cleanup, review merge previews carefully (especially `Needs review` groups), and check Apple's **Contacts** app to copy any important Notes from non-primary cards before confirming (if you edit contacts there, return and recheck the current duplicate candidates and preview before confirming).
- Avoid repeatedly turning iCloud or account sync off and on, removing accounts, or reimporting `.vcf` files to clear sync duplicates.
- Official scenario guides:
  - [Duplicate Contacts After Setting Up a New iPhone](https://contactmerge.app/guides/duplicate-contacts-after-new-iphone)
  - [Move to iOS Duplicate Contacts](https://contactmerge.app/guides/move-to-ios-duplicate-contacts)
  - [iCloud Duplicate Contacts After Sync](https://contactmerge.app/guides/icloud-duplicate-contacts-after-sync)
  - [Backup Contacts Before Merge on iPhone](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)
  - [How to Merge Contacts Safely](https://contactmerge.app/guides/merge-contacts-safely)

## Pro Unlock & Purchase Questions

Pro is a one-time App Store unlock (no subscription), with regional pricing shown by Apple. It unlocks full merging beyond the Free 3-contact single-group limit and enables batch merging for `Ready to merge` groups after confirmation (`Needs review` groups remain manual, one at a time).

If you need help unlocking or restoring a Pro purchase, contact [Official Support](https://contactmerge.app/support).

## Contacting Support & Protecting Your Privacy

- **Support**: [Official Support](https://contactmerge.app/support)
- **Helpful details to include**: Your iOS version, your ContactMerge+ Cleaner app version, and what you expected to happen versus what you observed.
- **Strict privacy rules**:
  - Do not post private personal information in public issues.
  - Never upload contact lists or `.vcf` (vCard) files.
  - Redact all names, phone numbers, email addresses, photos, street addresses, notes, and IDs before sharing any screenshot—use fabricated demo data whenever possible.

## Related Links

- [Quick Start: Scanning and Merging Safely](quick-start.md)
- [Backup, Undo, and Recovery History](recovery.md)
- [Official Website](https://contactmerge.app)
- [Privacy Policy](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Documentation Status

Checked 8 Nov 2026. Screens, labels, and behavior may vary depending on your installed app version and iOS version.
