# ContactMerge+ Cleaner — Produktdokumentation & Support

Offizielle öffentliche Produktdokumentation und Bedienungsanleitungen für **ContactMerge+ Cleaner** auf dem iPhone. Dieses Repository enthält ausschließlich Nutzerdokumentation – es ist kein Quellcode-Repository der App.

ContactMerge+ Cleaner verarbeitet Kontakte lokal auf Ihrem Gerät, lädt Ihr Adressbuch nicht auf Server des Entwicklers hoch, und der Entwickler bietet keinen Cloud-Backup-Dienst an. (Die Kontakt-Synchronisierung über iOS oder Konten – etwa iCloud oder Google – sowie System- oder Geräte-Backups sind separate Mechanismen, die über Ihre eigenen Konto- und iOS-Einstellungen gesteuert werden.)

- **Website**: [Offizielle Website (Englisch)](https://contactmerge.app)
- **App Store**: [Im App Store laden (Englisch)](https://apps.apple.com/us/app/contactmerge-contacts-cleaner/id6738980785)
- **Support**: [Offizieller Support (Englisch)](https://contactmerge.app/support)
- **Sprachen**: [English](../../README.md) | **Deutsch** | [Français](README.fr.md) | [Italiano](README.it.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [日本語](README.ja.md) | [한국어](README.ko.md) | [简体中文](README.zh-Hans.md) | [繁體中文](README.zh-Hant.md)

## Schnellstart in 4 Schritten

1. **Sicherung anlegen und Kontaktberechtigung erteilen**: Bewahren Sie vor größeren Bereinigungen eine unabhängige, datierte Sicherung auf (optionaler `.vcf`-Export), warten Sie ab, bis eine Telefonübertragung oder Erstsynchronisierung vollständig abgeschlossen ist, und erlauben Sie den Kontaktzugriff, sobald iOS danach fragt.
2. **Scannen**: Starten Sie einen Scan, um mögliche Duplikatgruppen auf Ihrem iPhone zu finden.
3. **Vorschau prüfen, Hauptkontakt wählen und Notizen in der Kontakte-App prüfen**: Öffnen Sie eine einzelne Duplikatgruppe, prüfen Sie die Zusammenführungsvorschau (`Merge Preview`), wählen Sie den Hauptkontakt (Basiskarte) aus und sehen Sie in Apples **Kontakte**-App nach, ob dort Notizen vorhanden sind, die Sie sichern möchten.
4. **Erneut prüfen und sorgfältig bestätigen**: Falls Sie die App verlassen haben, um Kontakte in Apples **Kontakte**-App anzusehen oder zu bearbeiten, kehren Sie zurück und prüfen Sie zuerst erneut die aktuellen Duplikat-Vorschläge und die Vorschau. Bestätigen Sie nur, wenn die Karten eindeutig zu derselben Person gehören und die Vorschau Ihre erwarteten Felder beibehält.

<img src="../../assets/scan-results-demo.png" alt="Simulator-Demo mit englischer Benutzeroberfläche (kein deutschsprachiger Screenshot, aufgenommen am 2026-11-03) der Scan-Ergebnisse unter Duplicate Contacts mit frei erfundenen Beispielkontakten sowie Undo Last Contact Merge, Ready to merge und Needs review; Bildschirme und Wortlaut können je nach App- oder iOS-Version abweichen" width="420">

*Simulator-Demo mit frei erfundenen Beispielkontakten (englische Benutzeroberfläche – kein deutschsprachiger Screenshot –, aufgenommen am 2026-11-03). Bildschirme, Layout und Wortlaut können je nach installierter App-Version oder iOS-Version abweichen.*

## Wichtige Sicherheitsgrenzen

- **`Ready to merge` vs. `Needs review`**:
  - `Ready to merge` (bereit zum Zusammenführen) bedeutet, dass jedes einzelne Kontaktpaar in der Gruppe strenge Übereinstimmungsprüfungen auf Basis starker Hinweise über alle Paare hinweg bestanden hat. Prüfen Sie vor dem Bestätigen dennoch immer die Vorschau – gleiche Namen oder Telefonnummern allein beweisen nicht, dass zwei Karten zu derselben Person gehören.
  - `Needs review` (Überprüfung erforderlich) weist auf schwächere oder widersprüchliche Hinweise hin (etwa eine geteilte Familiennummer, unterschiedliche Namen, widersprüchliche Geburtstage oder teilweise Überschneidungen). Dies ist eine Sicherheitsvorkehrung und kein Fehler; prüfen Sie jede `Needs review`-Gruppe einzeln von Hand und führen Sie niemals Karten zusammen, die verschiedene Personen darstellen.
- **Notizen vor dem Zusammenführen in Apples Kontakte-App prüfen und sichern**:
  - Notizen (Notes) in nicht-primären Kontakten (den übrigen Karten, die zusammengeführt werden) werden **nicht** gelesen oder in den Hauptkontakt kopiert und lassen sich später nicht wiederherstellen.
  - Da ContactMerge+ Cleaner keine Notizen lesen kann, schließen Sie aus fehlenden Notizen in der Zusammenführungsvorschau niemals darauf, dass ein Kontakt keine Notizen enthält. Prüfen und kopieren Sie wichtige Notizen vor dem Zusammenführen direkt in Apples **Kontakte**-App; wenn Sie Kontakte dort ansehen oder bearbeiten, kehren Sie anschließend zu ContactMerge+ Cleaner zurück und prüfen Sie vor dem Bestätigen erneut die aktuellen Duplikat-Vorschläge und die Vorschau (gehen Sie nicht davon aus, dass sich geöffnete Ansichten automatisch aktualisieren).
- **Rückgängigmachen und lokale Wiederherstellung auf dem Gerät**:
  - `Undo Last Contact Merge` (letzte Kontaktzusammenführung rückgängig machen) bezieht sich ausschließlich auf die unmittelbar letzte einzelne Zusammenführung (Hinweise zur geprüften Bildschirmposition und zu Versionsvorbehalten finden Sie unter [Sicherung, Rückgängigmachen und Wiederherstellungsverlauf](../de/recovery.md)).
  - `Recovery History` (Wiederherstellungsverlauf) ist ein lokal von der App auf dem Gerät gespeichertes Wiederherstellungsprotokoll, das **höchstens 3 Zusammenführungs-Einträge und höchstens 3 Lösch-Einträge** für **etwa 30 Tage auf dem Gerät** aufbewahrt (der genaue Navigationspfad innerhalb der App ist in dieser Dokumentation nicht verifiziert; siehe [Anleitung zur Wiederherstellung](../de/recovery.md)).
  - **Keine vollständige Systemwiederherstellung**: Kontaktnotizen aus nicht-primären Karten können nicht wiederhergestellt werden, und ursprüngliche Systemkennungen sowie Verknüpfungen werden möglicherweise nicht wiederhergestellt. Der Entwickler bietet keinen Cloud-Backup-Dienst an (getrennt von Ihrer eigenen iCloud-/Google-Synchronisierung oder Ihren iOS-System-Backups, sodass Zusammenführungen über Ihre Konten synchronisiert werden können). Als vorsorgliche Sicherheitsmaßnahme gilt: Eine Wiederherstellung ist nach späteren Kontaktänderungen, einer Deinstallation der App oder einem Geräteverlust nicht garantiert.
- **Unabhängige Sicherung & Kontosicherheit**: Der Export einer `.vcf`-Datei ist optional, doch wird vor Ihrer ersten Bereinigung eine unabhängige, datierte Sicherung empfohlen, die Ihre tatsächlichen Kontaktkonten abdeckt (eine Kontosynchronisierung ist kein unabhängiges Backup). Löschen Sie zur Fehlerbehebung niemals Quellkontakte, tippen Sie nicht auf `"Delete from My iPhone"` (vom iPhone löschen) und schalten Sie Konten nicht aus/ein oder entfernen Sie diese nicht.

## Free vs. Pro

- **Free**: Kontakte scannen, alle Duplikatgruppen ansehen und jeweils eine einzelne Duplikatgruppe zusammenführen (bis zu 3 Kontakte innerhalb dieser Gruppe). Eine Stapelverarbeitung mehrerer Gruppen ist nicht enthalten.
- **Pro**: Einmalige Freischaltung über den App Store ohne Abonnement; den regionalen Preis zeigt Apple direkt an. Schaltet Gruppen mit mehr als 3 Kontakten sowie die Stapelverarbeitung für `Ready to merge`-Gruppen nach Bestätigung frei (`Needs review`-Gruppen werden stets einzeln geprüft).
- **Kauf wiederherstellen & Abrechnung**: Informationen zum Wiederherstellen eines bestehenden Pro-Kaufs über denselben Apple Account oder zu Apples Rückerstattungsverfahren (abgewickelt durch Apple über [reportaproblem.apple.com (Englisch)](https://reportaproblem.apple.com), Anspruch nicht garantiert) finden Sie in den [FAQ](../de/faq.md#q16) oder beim [offiziellen Support (Englisch)](https://contactmerge.app/support).

## Bedienungsanleitungen

- [Schnellstart: Kontakte sicher scannen und zusammenführen](../de/quick-start.md)
- [Sicherung, Rückgängigmachen und Wiederherstellungsverlauf](../de/recovery.md)
- [Berechtigungen und Fehlerbehebung](../de/permissions-troubleshooting.md)
- [Häufig gestellte Fragen (FAQ)](../de/faq.md)

## Offizieller Support & Datenschutz

- **Support**: [Offizieller Support (Englisch)](https://contactmerge.app/support)
- **Datenschutz**: [Datenschutzerklärung (Englisch)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)
- **Datenschutz- & Schwärzungshinweis**: Teilen Sie niemals private Kontaktlisten, `.vcf`-Dateien (vCards), Passwörter, Zahlungsdaten oder Kaufbelege in öffentlichen Issues. Schwärzen Sie vor dem Teilen eines Screenshots sämtliche echten Namen, Telefonnummern, E-Mail-Adressen, Fotos, Postanschriften, Notizen und Konto-IDs – verwenden Sie nach Möglichkeit frei erfundene Beispieldaten.

## Dokumentationsstand

Geprüft am 8. Nov. 2026. Bildschirme, Bezeichnungen und Verhalten können je nach installierter App-Version und iOS-Version abweichen.
