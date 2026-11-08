# Berechtigungen und Fehlerbehebung

- **Übersicht**: [Deutsche Übersicht](../readme/README.de.md) | [English Overview](../../README.md)
- **Anleitungen**: [Schnellstart](quick-start.md) | [Sicherung & Wiederherstellung](recovery.md) | **Berechtigungen & Fehlerbehebung**
- **Sprache / Language**: **Deutsch** | [English](../en/permissions-troubleshooting.md)

Diese Anleitung beantwortet Fragen zur Kontaktberechtigung auf dem iPhone, zum Unterschied zwischen **ContactMerge+ Cleaner** und Apples integrierter Duplikaterkennung, zu Vorsichtsmaßnahmen nach Gerätewechsel oder Synchronisierung sowie zum sicheren Kontakt mit dem Support.

## Kontaktberechtigung auf dem iPhone

- **Für die Nutzung erforderlich**: ContactMerge+ Cleaner benötigt Zugriff auf Ihre Kontakte, um Duplikate auf Ihrem Gerät zu scannen und zusammenzuführen. Ihr Adressbuch wird auf Ihrem Gerät verarbeitet und nicht auf Entwickler-Server hochgeladen (unabhängig von einer über Ihre eigenen Konto- und iOS-Einstellungen gesteuerten iCloud-/Google-Synchronisierung oder von System-Backups).
- **Vollzugriff vs. eingeschränkter Zugriff**: Je nach iOS-Version zeigt iOS möglicherweise Optionen für vollen oder eingeschränkten Kontaktzugriff an.
- **Was Sie prüfen sollten, wenn der Scan blockiert oder unvollständig ist**:
  - Prüfen Sie die Kontaktberechtigung für ContactMerge+ Cleaner in den iOS-Einstellungen.
  - Falls die Berechtigungsoption dort nicht verfügbar ist, blockiert wirkt oder sich weiterhin unerwartet verhält, wenden Sie sich mit Ihrer iOS-Version, der App-Version sowie einer kurzen Beschreibung des erwarteten und des beobachteten Verhaltens an den [offiziellen Support (Englisch)](https://contactmerge.app/support).
- **Was Sie vermeiden sollten**: Schalten Sie die Kontosynchronisierung nicht wiederholt aus und ein, löschen Sie keine Konten und importieren Sie keine `.vcf`-Dateien erneut, um Berechtigungsprobleme zu lösen. Solche Schritte beheben keine App-Berechtigungen und können zusätzliche Duplikate oder Datenverlust verursachen.

## Unterschied zu Apples „Duplikate anzeigen / zusammenführen“

Apples integrierte Funktion **Duplikate anzeigen / zusammenführen** (View Duplicates / Merge Duplicates) in der iOS-Kontakte-App ist unabhängig von ContactMerge+ Cleaner:

- Apples Systemfunktion bietet eine integrierte Prüfung und Zusammenführung von Duplikaten und kann exakte Duplikate anzeigen, zeigt Duplikate jedoch nicht garantiert an, wenn Telefonnummern unterschiedliche Ländervorwahl-Formate nutzen oder wenn das Adressbuch sehr groß ist.
- ContactMerge+ Cleaner prüft auf Ihrem Gerät und sortiert Vorschläge in `Ready to merge` (bereit zum Zusammenführen) und `Needs review` (Überprüfung erforderlich), damit Sie jede Zusammenführung vorab in der Vorschau prüfen können. ContactMerge+ Cleaner verspricht jedoch keine bestimmten Scangeschwindigkeiten, Obergrenzen für Kontaktlisten oder eine automatische Reparatur früherer Schäden im Adressbuch.
- Weiterführende offizielle Leitfäden:
  - [iOS View Duplicates and Country Code Formatting (Englisch)](https://contactmerge.app/guides/ios-view-duplicates-country-code)
  - [View Duplicates Missing on a Large Contact List (Englisch)](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list)

## Duplikate nach Gerätewechsel und Synchronisierung

Doppelte Kontakte entstehen häufig direkt nach dem Einrichten eines neuen iPhones, beim Wechsel von Android (Move to iOS) oder bei der Synchronisierung mit iCloud- und E-Mail-Konten. Beachten Sie folgende Vorsichtsmaßnahmen:

- Warten Sie ab, bis die Datenübertragung oder die Hintergrundsynchronisierung vollständig abgeschlossen ist, bevor Sie scannen und zusammenführen.
- Legen Sie vor der ersten Bereinigung eine unabhängige Sicherung an, prüfen Sie die Vorschau sorgfältig (besonders bei `Needs review`-Gruppen) und sehen Sie vor dem Bestätigen in Apples **Kontakte**-App nach, um wichtige Notizen aus sekundären Karten manuell zu sichern (falls Sie Kontakte dort bearbeiten, prüfen Sie nach der Rückkehr vor dem Bestätigen erneut die aktuellen Duplikat-Vorschläge und die Vorschau).
- Schalten Sie iCloud- oder Kontosynchronisierungen nicht wiederholt aus und ein, entfernen Sie keine Konten und importieren Sie `.vcf`-Dateien nicht mehrfach neu, um Synchronisierungsduplikate zu beseitigen.
- Offizielle Szenario-Leitfäden:
  - [Doppelte Kontakte nach dem Einrichten eines neuen iPhones](https://contactmerge.app/de/guides/duplicate-contacts-after-new-iphone)
  - [Doppelte Kontakte nach Wechsel mit „Auf iOS übertragen“ (Move to iOS)](https://contactmerge.app/de/guides/move-to-ios-duplicate-contacts)
  - [Doppelte Kontakte nach iCloud-Synchronisierung](https://contactmerge.app/de/guides/icloud-duplicate-contacts-after-sync)
  - [Backup Contacts Before Merge on iPhone (Englisch)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)
  - [How to Merge Contacts Safely (Englisch)](https://contactmerge.app/guides/merge-contacts-safely)

## Fragen zur Pro-Freischaltung und zu Käufen

Pro ist eine einmalige Freischaltung im App Store (kein Abonnement); den Preis zeigt Apple für Ihre Region an. Pro schaltet das vollständige Zusammenführen über das Free-Limit (1 Gruppe mit bis zu 3 Kontakten) hinaus sowie die Stapelverarbeitung nach Bestätigung für `Ready to merge`-Gruppen frei (`Needs review`-Gruppen bleiben weiterhin einzeln zu prüfen).

Wenn Sie Hilfe bei der Freischaltung oder der Wiederherstellung eines Pro-Kaufs benötigen, wenden Sie sich an den [offiziellen Support (Englisch)](https://contactmerge.app/support).

## Support kontaktieren & Datenschutz wahren

- **Support**: [Offizieller Support (Englisch)](https://contactmerge.app/support)
- **Hilfreiche Angaben**: Ihre iOS-Version, Ihre installierte App-Version von ContactMerge+ Cleaner sowie was Sie erwartet haben im Vergleich zu dem, was Sie beobachtet haben.
- **Strikte Datenschutzregeln**:
  - Veröffentlichen Sie keine privaten personenbezogenen Angaben in öffentlichen Issues.
  - Laden Sie niemals Kontaktlisten oder `.vcf`-Dateien (vCards) hoch.
  - Schwärzen Sie vor dem Teilen von Screenshots alle Namen, Telefonnummern, E-Mail-Adressen, Fotos, Postanschriften, Notizen und Kennungen – verwenden Sie möglichst ausschließlich frei erfundene Beispieldaten.

## Verwandte Links

- [Schnellstart: Kontakte sicher prüfen und zusammenführen](quick-start.md)
- [Sicherung, Rückgängigmachen und Wiederherstellungsverlauf](recovery.md)
- [Offizielle Website (Englisch)](https://contactmerge.app)
- [Datenschutzerklärung (Englisch)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Dokumentationsstand

Geprüft am 8. Nov. 2026. Darstellung, Bezeichnungen und Verhalten können je nach installierter App-Version und iOS-Version abweichen.
