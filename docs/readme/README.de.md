# ContactMerge+ Cleaner — Produktdokumentation & Support

Offizielle öffentliche Produktdokumentation und Bedienungsanleitungen für **ContactMerge+ Cleaner** auf dem iPhone. Dieses Repository enthält ausschließlich Nutzerdokumentation – es ist kein Quellcode-Repository der App.

ContactMerge+ Cleaner verarbeitet Kontakte auf Ihrem Gerät und lädt Ihr Adressbuch nicht auf Server des Entwicklers hoch. (Die Kontakt-Synchronisierung über iOS oder Konten – etwa iCloud oder Google – sowie System- oder Geräte-Backups sind separate Mechanismen, die über Ihre eigenen Konto- und iOS-Einstellungen gesteuert werden.)

- **Website**: [Offizielle Website (Englisch)](https://contactmerge.app)
- **App Store**: [Im App Store laden (Englisch)](https://apps.apple.com/us/app/contactmerge-contacts-cleaner/id6738980785)
- **Sprache / Language**: [English](../../README.md) | **Deutsch**

## Schnellstart in 4 Schritten

1. **Kontaktberechtigung erteilen**: Erlauben Sie den Zugriff auf Ihre Kontakte, sobald iOS danach fragt.
2. **Scannen**: Starten Sie einen Scan, um mögliche Duplikatgruppen auf Ihrem iPhone zu finden.
3. **Vorschau prüfen, Hauptkontakt wählen und Notizen in Kontakte prüfen**: Öffnen Sie eine einzelne Duplikatgruppe, prüfen Sie die Vorschau, wählen Sie den Hauptkontakt (Basiskarte) und sehen Sie in Apples **Kontakte**-App nach, ob wichtige Notizen gesichert werden müssen.
4. **Sorgfältig bestätigen**: Falls Sie die App zum Bearbeiten von Kontakten verlassen haben, prüfen Sie nach der Rückkehr zuerst erneut die aktuellen Duplikat-Vorschläge und die Vorschau. Bestätigen Sie nur, wenn die Karten eindeutig zu derselben Person gehören und alle erwarteten Felder erhalten bleiben.

<img src="../../assets/scan-results-demo.png" alt="Simulator-Demo der Scan-Ergebnisse (Duplicate Contacts) mit englischer Benutzeroberfläche, Undo Last Contact Merge sowie Ready to merge und Needs review für frei erfundene Beispielkontakte" width="420">

*Simulator-Demo mit frei erfundenen Beispielkontakten (englische Benutzeroberfläche, aufgenommen am 2026-11-03). Darstellung und Wortlaut können je nach App- oder iOS-Version abweichen.*

## Wichtige Sicherheitsgrenzen

- **`Ready to merge` vs. `Needs review`**:
  - `Ready to merge` (bereit zum Zusammenführen) bedeutet, dass jedes einzelne Kontaktpaar in der Gruppe strenge Übereinstimmungsprüfungen mit starken Hinweisen über alle Paare hinweg erfüllt. Prüfen Sie vor dem Bestätigen dennoch immer die Vorschau – gleiche Namen oder Telefonnummern beweisen nicht automatisch, dass zwei Karten zu derselben Person gehören.
  - `Needs review` (Überprüfung erforderlich) weist auf schwächere oder widersprüchliche Hinweise hin (z. B. eine geteilte Familiennummer, abweichende Namen oder nur teilweise übereinstimmende Angaben). Dies ist ein Sicherheitshinweis und nicht zwingend ein Fehler; prüfen Sie jede `Needs review`-Gruppe einzeln von Hand.
- **Notizen vor dem Zusammenführen in Apples Kontakte-App prüfen und sichern**:
  - Notizen (Notes) in den übrigen zusammengeführten Karten (sekundären Kontakten) werden **nicht** gelesen oder in den Hauptkontakt kopiert und lassen sich später nicht wiederherstellen.
  - Da ContactMerge+ Cleaner keine Notizen lesen kann, schließen Sie aus einer leeren Vorschau niemals darauf, dass keine Notizen vorhanden sind. Prüfen und kopieren Sie wichtige Notizen vor dem Zusammenführen direkt in Apples **Kontakte**-App; wenn Sie dort Kontakte bearbeiten, kehren Sie anschließend zu ContactMerge+ Cleaner zurück und kontrollieren Sie vor dem Bestätigen erneut die aktuellen Duplikat-Vorschläge und die Vorschau.
- **Rückgängigmachen und lokale Wiederherstellung**:
  - `Undo Last Contact Merge` bezieht sich auf die unmittelbar letzte Zusammenführung (Hinweise zur geprüften Bildschirmposition und zu Versionsunterschieden finden Sie in der [Anleitung zur Wiederherstellung](../de/recovery.md)).
  - `Recovery History` (Wiederherstellungsverlauf) ist ein lokal von der App gespeichertes Protokoll, das **höchstens 3 Zusammenführungs-Einträge und höchstens 3 Lösch-Einträge** für **etwa 30 Tage auf dem Gerät** aufbewahrt.
  - **Keine vollständige Systemwiederherstellung**: Kontaktnotizen können nicht gelesen werden (daher lassen sich Notizen aus sekundären Karten nicht wiederherstellen), und ursprüngliche Systemkennungen sowie Verknüpfungen werden möglicherweise nicht wiederhergestellt. Der Entwickler bietet kein Cloud-Backup an (unabhängig von Ihren eigenen Einstellungen für iCloud-/Google-Synchronisierung oder System-Backups). Als vorsorglicher Hinweis gilt: Eine Wiederherstellung ist nicht garantiert, wenn Kontakte später geändert werden oder wenn die App bzw. das Gerät nicht mehr verfügbar ist (etwa nach Deinstallation oder Geräteverlust). Alle Details finden Sie unter [Sicherung, Rückgängigmachen und Wiederherstellungsverlauf](../de/recovery.md).
- **Sicherung vor dem Zusammenführen**: Der Export einer `.vcf`-Datei ist optional – Sie müssen vorab keine Datei exportieren –, doch wird ein unabhängiges Backup empfohlen, besonders vor der ersten Bereinigung.

## Free vs. Pro

- **Free**: Kontakte scannen, alle Duplikatgruppen ansehen und jeweils eine einzelne Duplikatgruppe zusammenführen (bis zu 3 Kontakte innerhalb dieser Gruppe). Keine Stapelverarbeitung mehrerer Gruppen.
- **Pro**: Einmalige Freischaltung über den App Store ohne Abonnement; den Preis für Ihre Region zeigt Apple direkt an. Schaltet das vollständige Zusammenführen (auch für Gruppen mit mehr als 3 Kontakten) sowie die Stapelverarbeitung nach Bestätigung ausschließlich für `Ready to merge`-Gruppen frei. `Needs review`-Gruppen werden weiterhin einzeln geprüft.
- **Kauf- & Wiederherstellungs-Support**: Bei Fragen zu einem bestehenden Kauf oder zur Wiederherstellung von Pro wenden Sie sich an den [offiziellen Support (Englisch)](https://contactmerge.app/support).

## Bedienungsanleitungen

- [Schnellstart: Kontakte sicher prüfen und zusammenführen](../de/quick-start.md)
- [Sicherung, Rückgängigmachen und Wiederherstellungsverlauf](../de/recovery.md)
- [Berechtigungen und Fehlerbehebung](../de/permissions-troubleshooting.md)

## Offizieller Support & Datenschutz

- **Support**: [Offizieller Support (Englisch)](https://contactmerge.app/support)
- **Datenschutz**: [Datenschutzerklärung (Englisch)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)
- **Hinweis zum Datenschutz bei Rückfragen**: Teilen Sie keine privaten personenbezogenen Daten in öffentlichen Issues und laden Sie niemals Kontaktlisten oder `.vcf`-Dateien (vCards) hoch. Schwärzen Sie vor dem Teilen von Screenshots sämtliche Namen, Telefonnummern, E-Mail-Adressen, Fotos, Postanschriften, Notizen und Kennungen – verwenden Sie möglichst nur frei erfundene Beispieldaten.

## Dokumentationsstand

Geprüft am 8. Nov. 2026. Darstellung, Bezeichnungen und Verhalten können je nach installierter App-Version und iOS-Version abweichen.
