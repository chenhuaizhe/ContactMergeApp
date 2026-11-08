# Berechtigungen und Fehlerbehebung

- **Übersicht & Sprachen**: [Deutsche Übersicht](../readme/README.de.md) | [English Overview](../../README.md)
- **Anleitungen**: [Schnellstart](quick-start.md) | [Sicherung & Wiederherstellung](recovery.md) | **Berechtigungen & Fehlerbehebung** | [FAQ](faq.md)
- **Sprache / Language**: **Deutsch** | [English](../en/permissions-troubleshooting.md)

Diese Anleitung behandelt die Einstellungen zur Kontaktberechtigung auf dem iPhone, die Unterschiede zwischen **ContactMerge+ Cleaner** und Apples integrierten Duplikat-Funktionen, den sicheren Umgang mit synchronisierten Konten und Telefonübertragungen, Fragen zu Kauf und Rückerstattung sowie die sichere Kontaktaufnahme mit dem Support.

## Kontaktberechtigung auf dem iPhone

- **Erforderlich zum Scannen und Zusammenführen**: ContactMerge+ Cleaner benötigt Zugriff auf Ihre Kontakte, um Duplikate auf Ihrem iPhone zu finden und zusammenzuführen. Die Kontaktverarbeitung erfolgt lokal auf Ihrem Gerät – Ihr Adressbuch wird nicht auf Entwickler-Server hochgeladen, und der Entwickler bietet keinen Cloud-Backup-Dienst an (getrennt von einer über Ihre eigenen Einstellungen gesteuerten iCloud-/Google-Kontosynchronisierung oder von iOS-System-Backups).
- **Vollzugriff vs. eingeschränkter Zugriff in iOS**: Je nach Ihrer iOS-Version können Sie in den iOS-Einstellungen im Bereich für Datenschutz & Sicherheit unter Kontakte (englischer Systempfad `Settings > Privacy & Security > Contacts`) steuern, auf welche Kontakte eine App zugreifen darf – einschließlich Vollzugriff oder eingeschränktem Zugriff auf ausgewählte Kontakte (siehe Apples Anleitung: [Control access to Contacts on iPhone (Englisch)](https://support.apple.com/guide/iphone/control-access-to-contacts-iph9536aa9a5/ios)).
- **Wenn der Scan blockiert ist oder Kontakte zu fehlen scheinen**:
  - Prüfen Sie in den iOS-Einstellungen die für ContactMerge+ Cleaner gewährte Kontaktberechtigungsstufe. Ein unvollständiger oder eingeschränkter Zugriff kann begrenzen, welche Kontakte die App sehen kann – er löscht Ihre Kontakte **nicht**, allerdings ist nicht garantiert, dass die App jeden Ablauf mit eingeschränktem Zugriff unterstützt.
  - Wenn die Einstellung nicht verfügbar wirkt oder sich auch nach Prüfung der iOS-Einstellungen unerwartet verhält, wenden Sie sich an den [offiziellen Support (Englisch)](https://contactmerge.app/support).
- **Was Sie nicht tun sollten**: Schalten Sie niemals die Kontosynchronisierung aus und wieder ein, entfernen Sie keine Konten, löschen Sie keine Kontakte und importieren Sie keine `.vcf`-Dateien erneut, um Berechtigungsprobleme zu beheben.

## ContactMerge+ Cleaner im Vergleich zu Apples integrierten Duplikat-Werkzeugen

Apples **Kontakte**-App verfügt über eigene Funktionen zum Erkennen und Verknüpfen von Duplikaten, die anders arbeiten als ContactMerge+ Cleaner (siehe Apples Anleitung: [Merge or hide duplicate contacts on iPhone (Englisch)](https://support.apple.com/guide/iphone/merge-or-hide-duplicate-contacts-iph2ab28320d/ios)):

- **`View Duplicates` in Apple Kontakte**: Wenn verfügbar, blendet Apple unterhalb Ihrer eigenen Karte (`My Card`) einen Hinweis `View Duplicates` (Duplikate anzeigen) ein, über den erkannte Duplikate geprüft und zusammengeführt werden können. Erscheint Apples Hinweis `View Duplicates` nicht – etwa wenn Nummern unterschiedliche Ländervorwahl-Formate verwenden oder in manchen großen Adressbüchern –, unterscheiden Sie dieses Systemverhalten bitte von einem Berechtigungsproblem der App. Diese Dokumentation erhebt keinen Anspruch auf Apples interne Erkennungsregeln, einen garantierten Schwellenwert für die Kontaktanzahl (wie etwa 1.000 Kontakte), eine feste Wartezeit oder eine pauschale „Alle zusammenführen“-Lösung (`Merge All`).
- **Verknüpfte / vereinheitlichte Kontakte vs. zusammengeführte Karten**: Das manuelle Verknüpfen von Kontakten (`Link Contacts`) in Apples **Kontakte**-App fasst lediglich zusammen, wie Karten in einer gemeinsamen Ansicht dargestellt werden, ohne die zugrunde liegenden Quellkarten zusammenzuführen; Änderungen an einer vereinheitlichten Karte können jedoch an die verbundenen Konten weitergegeben werden.
- **Wie sich ContactMerge+ Cleaner unterscheidet**: ContactMerge+ Cleaner scannt lokal auf Ihrem Gerät und trennt Vorschläge in `Ready to merge` (bereit zum Zusammenführen) und `Needs review` (Überprüfung erforderlich), sodass Sie vorab eine Zusammenführungsvorschau prüfen können (während Sie Notizen in Apples **Kontakte**-App kontrollieren). Die App verspricht keine bestimmten Scangeschwindigkeiten, Größenlimits für Kontaktlisten oder eine automatische Reparatur früherer Schäden im Adressbuch.
- Weiterführende offizielle Web-Leitfäden:
  - [iOS View Duplicates and Country Code Formatting (Englisch)](https://contactmerge.app/guides/ios-view-duplicates-country-code)
  - [View Duplicates Missing on a Large Contact List (Englisch)](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list)

## Gerätewechsel, Kontosynchronisierung und Vermeidung versehentlicher Löschungen

Das Einrichten eines neuen iPhones, die Nutzung von „Auf iOS übertragen“ (Move to iOS), Dateiimporte oder das Verbinden mehrerer Konten (wie iCloud und Google) legt häufig ältere, kontenübergreifende Duplikate offen, ohne dass Ihr Gerät fehlerhaft ist:

- **Zuerst Erstsynchronisierung abwarten und Sicherung anlegen**: Warten Sie ab, bis der Geräteumzug oder die erste Kontosynchronisierung abgeschlossen ist, bevor Sie Duplikate beurteilen (dies beseitigt Duplikate nicht garantiert von selbst, vermeidet aber Verwirrung während laufender Synchronisierung). Prüfen Sie, welches Konto Ihre Kontakte hält, und erstellen Sie eine unabhängige, datierte Sicherung, bevor Sie etwas ändern.
- **Sorgfältig prüfen**: Kontrollieren Sie die Zusammenführungsvorschau (insbesondere bei `Needs review`-Gruppen) und sichern Sie etwaige Kontaktnotizen nicht-primärer Karten vorab in Apples **Kontakte**-App; wenn Sie die App zum Ansehen oder Bearbeiten von Kontakten verlassen, kehren Sie zurück und prüfen Sie vor dem Bestätigen erneut die aktuellen Vorschläge und die Vorschau.
- **Zwingende Vermeidung von Löschaktionen**: Das Entfernen eines Kontos aus der Kontakte-App verhält sich anders als das Löschen einzelner Kontakte, und das Löschen von Kontakten aus einem synchronisierten E-Mail- oder Cloud-Konto kann diese auf allen synchronisierten Geräten dauerhaft löschen (nur als Hintergrundinformation siehe Apples [Add or remove accounts in Contacts on iPhone (Englisch)](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios) und den [Hinweis zum Löschen von Kontakten (Englisch)](https://support.apple.com/en-us/111793)). Löschen Sie **keine** Quellkontakte, tippen Sie **nicht** auf `"Delete from My iPhone"` (vom iPhone löschen), schalten Sie die Synchronisierung nicht aus/ein und importieren Sie `.vcf`-Dateien nicht wiederholt neu als vermeintliche Abkürzung – wenn Sie unsicher sind, halten Sie inne und fragen Sie den [offiziellen Support (Englisch)](https://contactmerge.app/support).
- Offizielle Szenario-Leitfäden:
  - [Doppelte Kontakte nach dem Einrichten eines neuen iPhones](https://contactmerge.app/de/guides/duplicate-contacts-after-new-iphone)
  - [Doppelte Kontakte nach Wechsel mit „Auf iOS übertragen“ (Move to iOS)](https://contactmerge.app/de/guides/move-to-ios-duplicate-contacts)
  - [Doppelte Kontakte nach iCloud-Synchronisierung](https://contactmerge.app/de/guides/icloud-duplicate-contacts-after-sync)
  - [Backup Contacts Before Merge on iPhone (Englisch)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)
  - [How to Merge Contacts Safely (Englisch)](https://contactmerge.app/guides/merge-contacts-safely)

## Pro-Freischaltung, Käufe wiederherstellen und Rückerstattungen

- **Einmalige Freischaltung (kein Abonnement)**: Pro ist ein einmaliger, nicht verbrauchbarer Kauf (Non-Consumable) im App Store mit regionaler Preisanzeige durch Apple – befolgen Sie für diese App **keine** Anleitungen zum Kündigen eines Abonnements. Pro schaltet Gruppen mit mehr als 3 Kontakten sowie die Stapelverarbeitung für bestätigte `Ready to merge`-Gruppen frei (`Needs review` bleibt weiterhin einzeln zu prüfen).
- **Pro wiederherstellen**: Vergewissern Sie sich, dass Ihr iPhone mit **demselben Apple Account** angemeldet ist, der beim ursprünglichen Kauf verwendet wurde, und lesen Sie Apples offizielle Anleitung: [If you can't find or use your in-app purchases (Englisch)](https://support.apple.com/en-us/108096). Da der genaue Pfad zur Wiederherstellungsschaltfläche innerhalb der App in dieser Dokumentation nicht verifiziert ist, erraten wir keine Menübezeichnungen, empfehlen keinen erneuten Kauf von Pro und garantieren keine automatische Wiederherstellung – schlägt die Wiederherstellung fehl, wenden Sie sich bitte an den [offiziellen Support (Englisch)](https://contactmerge.app/support) oder an den Apple Support.
- **Rückerstattungsanträge**: Apple wickelt die Abrechnung im App Store ab und entscheidet je nach Land oder Region über die Berechtigung zu einer Rückerstattung. Manche Käufe kommen möglicherweise für eine Rückerstattung infrage, die Sie über Apples offizielles Verfahren unter [reportaproblem.apple.com (Englisch)](https://reportaproblem.apple.com) beantragen können (siehe Apples [Request a refund for apps or content that you bought from Apple (Englisch)](https://support.apple.com/en-us/118223)); **Rückerstattungen sind nicht garantiert**, und der Entwickler garantiert keine Genehmigung.

## Support kontaktieren & Privatsphäre schützen

- **Support**: [Offizieller Support (Englisch)](https://contactmerge.app/support)
- **Hilfreiche, sichere Angaben**: Ihre ContactMerge+ Cleaner App-Version, Ihre iOS-Version, was Sie erwartet haben im Vergleich zu dem, was Sie beobachtet haben, ob es sich bei der Ansicht um ein Apple-Systemelement oder einen Bildschirm innerhalb von ContactMerge+ Cleaner handelt, der beteiligte Kontotyp (z. B. iCloud oder Google, **ohne** Ihre E-Mail-Adresse oder Konto-ID) sowie bei Bedarf eine ungefähre Kontaktanzahl.
- **Strikte Datenschutz- & Schwärzungsregeln**:
  - Laden Sie niemals private Kontaktlisten, `.vcf`-Dateien (vCards), Passwörter, Zahlungsdaten oder Kaufbelege in öffentlichen Issues hoch (klären Sie etwaige Abrechnungsdetails ausschließlich über Apples offizielle sichere Kanäle oder bei Bedarf über einen geeigneten privaten offiziellen Support-Kanal).
  - Schwärzen Sie sämtliche echten Namen, Telefonnummern, E-Mail-Adressen, Fotos, Postanschriften, Notizen und IDs vor dem Teilen von Screenshots – verwenden Sie nach Möglichkeit frei erfundene Beispieldaten.

## Verwandte Links

- [Schnellstart: Kontakte sicher scannen und zusammenführen](quick-start.md)
- [Sicherung, Rückgängigmachen und Wiederherstellungsverlauf](recovery.md)
- [Häufig gestellte Fragen (FAQ)](faq.md)
- [Offizielle Website (Englisch)](https://contactmerge.app)
- [Datenschutzerklärung (Englisch)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Dokumentationsstand

Geprüft am 8. Nov. 2026. Bildschirme, Bezeichnungen und Verhalten können je nach installierter App-Version und iOS-Version abweichen.
