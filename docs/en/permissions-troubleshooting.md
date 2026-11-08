# Permissions and Troubleshooting

- **Overview & Languages**: [English Overview](../../README.md)
- **Guides**: [Quick Start](quick-start.md) | [Backup & Recovery](recovery.md) | **Permissions & Troubleshooting** | [FAQ](faq.md)

This guide covers iPhone Contacts permission settings, how **ContactMerge+ Cleaner** differs from Apple's built-in duplicate features, safe handling of synced accounts and phone transfers, purchase and refund questions, and how to contact support safely.

## Contacts Permission on iPhone

- **Required for scanning and merging**: ContactMerge+ Cleaner needs Contacts access so it can find and merge duplicates on your iPhone. Contact processing happens locally on your device—your address book is not uploaded to developer servers, and the developer does not provide a cloud backup service (separate from any iCloud/Google contact sync or iOS system backups controlled by your own settings).
- **Full vs. limited access in iOS**: Depending on your iOS version, Apple lets you control which contacts an app can access—including full access or limited access to selected contacts—under iOS **Settings > Privacy & Security > Contacts** (see Apple's guide: [Control access to Contacts on iPhone](https://support.apple.com/guide/iphone/control-access-to-contacts-iph9536aa9a5/ios)).
- **If scanning is blocked or contacts appear missing**:
  - Check the Contacts permission level granted to ContactMerge+ Cleaner in iOS Settings. Incomplete or limited access can restrict which contacts the app can see—it does **not** delete your contacts, though the app is not guaranteed to support every limited-access workflow.
  - If the setting looks unavailable or still behaves unexpectedly after checking iOS Settings, contact [Official Support](https://contactmerge.app/support).
- **What not to do**: Never toggle account sync off and on, remove accounts, delete contacts, or reimport `.vcf` files to troubleshoot permissions.

## ContactMerge+ Cleaner vs. Apple's Built-In Duplicate Tools

Apple's **Contacts** app includes built-in duplicate and linking features that work differently from ContactMerge+ Cleaner (see Apple's guide: [Merge or hide duplicate contacts on iPhone](https://support.apple.com/guide/iphone/merge-or-hide-duplicate-contacts-iph2ab28320d/ios)):

- **`View Duplicates` in Apple Contacts**: When available, Apple shows a `View Duplicates` notice below `My Card` for reviewing and merging detected duplicates. If Apple's `View Duplicates` banner does not appear—such as when numbers use different country-code formats or in some large address books—distinguish that system behavior from an app permission issue. These docs do not claim Apple's internal detection rules, a guaranteed contact-count threshold (such as 1,000 contacts), a fixed waiting time, or a blanket "Merge All" fix.
- **Linked / unified contacts vs. merged cards**: Manually linking contacts in Apple's Contacts app unifies how cards display in a single view without merging the underlying source cards, and edits made on a unified card can propagate to the connected accounts.
- **How ContactMerge+ Cleaner differs**: ContactMerge+ Cleaner scans on your device and separates candidates into `Ready to merge` and `Needs review` so you can inspect a merge preview first (while checking Apple's **Contacts** app for Notes). It does not promise specific scan speeds, contact-list size limits, or automatic repair of prior address-book damage.
- Related official web guides:
  - [iOS View Duplicates and Country Code Formatting](https://contactmerge.app/guides/ios-view-duplicates-country-code)
  - [View Duplicates Missing on a Large Contact List](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list)

## Migration, Account Sync, and Avoiding Accidental Deletion

Setting up a new iPhone, using Move to iOS, importing files, or connecting multiple accounts (such as iCloud and Google) often exposes older duplicates across accounts without meaning your device is faulty:

- **Finish initial sync and back up first**: Wait until device migration or initial account syncing finishes before judging duplicates (not guaranteed to remove duplicates by itself, but prevents mid-sync confusion). Identify which account holds your contacts and make an independent dated backup before changing anything.
- **Review carefully**: Inspect merge previews (especially `Needs review` groups) and save any non-primary Contact Notes in Apple's **Contacts** app first; if you leave the app to view or edit contacts, return and recheck the current candidates and preview before confirming.
- **Mandatory deletion avoidance**: Removing an account from Contacts behaves differently from deleting individual contacts, and deleting contacts from a synced email or cloud account can permanently delete them across all synced devices (for background context only, see Apple's [Add or remove accounts in Contacts on iPhone](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios) and [contact deletion notice](https://support.apple.com/en-us/111793)). **Do not** delete source contacts, tap "Delete from My iPhone," toggle sync off/on, or repeatedly reimport `.vcf` files as a cleanup shortcut—if unsure, stop and ask [Official Support](https://contactmerge.app/support).
- Official scenario guides:
  - [Duplicate Contacts After Setting Up a New iPhone](https://contactmerge.app/guides/duplicate-contacts-after-new-iphone)
  - [Move to iOS Duplicate Contacts](https://contactmerge.app/guides/move-to-ios-duplicate-contacts)
  - [iCloud Duplicate Contacts After Sync](https://contactmerge.app/guides/icloud-duplicate-contacts-after-sync)
  - [Backup Contacts Before Merge on iPhone](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)
  - [How to Merge Contacts Safely](https://contactmerge.app/guides/merge-contacts-safely)

## Pro Unlock, Restoring Purchases, and Refunds

- **One-time unlock (not a subscription)**: Pro is a one-time App Store non-consumable purchase with regional pricing shown by Apple—do **not** follow subscription-cancellation steps for this app. It unlocks groups larger than 3 contacts and batch merging for confirmed `Ready to merge` groups (`Needs review` stays one at a time).
- **Restoring Pro**: Make sure your iPhone is signed in with the **same Apple Account** used for the original purchase and review Apple's official guide: [If you can't find or use your in-app purchases](https://support.apple.com/en-us/108096). Because the exact in-app restore button path is unverified in these docs, we do not guess menu names, recommend buying Pro again, or guarantee automatic restoration—if restoring fails, contact [Official Support](https://contactmerge.app/support) or Apple Support.
- **Refund requests**: Apple handles App Store billing and decides refund eligibility by country or region. Some purchases may be eligible for a refund, and you can request one through Apple's official process at [reportaproblem.apple.com](https://reportaproblem.apple.com) (see Apple's [Request a refund for apps or content that you bought from Apple](https://support.apple.com/en-us/118223)); **refunds are not guaranteed**, and the developer does not guarantee refund approval.

## Contacting Support & Protecting Your Privacy

- **Support**: [Official Support](https://contactmerge.app/support)
- **Helpful, safe details to share**: Your ContactMerge+ Cleaner app version, iOS version, what you expected vs. what you observed, whether the screen is an Apple system control or inside ContactMerge+ Cleaner, the account type involved (e.g., iCloud or Google, **without** your email or account ID), and an approximate contact count if relevant.
- **Strict privacy & redaction rules**:
  - Never upload private contact lists, `.vcf` (vCard) files, passwords, payment details, or purchase receipts in public issues (handle any billing specifics only through Apple's official secure channels or an appropriate private official support channel when needed).
  - Redact all real names, phone numbers, email addresses, photos, street addresses, notes, and IDs before sharing screenshots—use fabricated demo data whenever possible.

## Related Links

- [Quick Start: Scanning and Merging Safely](quick-start.md)
- [Backup, Undo, and Recovery History](recovery.md)
- [Frequently Asked Questions (FAQ)](faq.md)
- [Official Website](https://contactmerge.app)
- [Privacy Policy](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Documentation Status

Checked 8 Nov 2026. Screens, labels, and behavior may vary depending on your installed app version and iOS version.
