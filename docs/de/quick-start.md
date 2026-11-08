# Schnellstart: Kontakte sicher prüfen und zusammenführen

- **Übersicht**: [Deutsche Übersicht](../readme/README.de.md) | [English Overview](../../README.md)
- **Anleitungen**: **Schnellstart** | [Sicherung & Wiederherstellung](recovery.md) | [Berechtigungen & Fehlerbehebung](permissions-troubleshooting.md)
- **Sprache / Language**: **Deutsch** | [English](../en/quick-start.md)

Diese Anleitung zeigt, wie Sie doppelte Kontakte auf Ihrem iPhone mit **ContactMerge+ Cleaner** finden, prüfen und sicher zusammenführen.

ContactMerge+ Cleaner verarbeitet Ihre Kontakte auf Ihrem Gerät und lädt Ihr Adressbuch nicht auf Server des Entwicklers hoch. (Die Kontakt-Synchronisierung über iOS oder Konten – etwa iCloud oder Google – sowie System- oder Geräte-Backups sind separate Mechanismen, die über Ihre eigenen Konto- und iOS-Einstellungen gesteuert werden.) Produktinformationen und Downloads finden Sie auf der [offiziellen Website (Englisch)](https://contactmerge.app).

## Vor dem Start

- **Unabhängige Sicherung anlegen (empfohlen)**: Der Export einer `.vcf`-Datei ist optional – Sie müssen vor dem Zusammenführen keine Datei exportieren –, doch wird ein unabhängiges Backup empfohlen, besonders vor der ersten Bereinigung. ContactMerge+ Cleaner bietet keinen eigenen Cloud-Backup-Dienst an und exportiert keine externen Sicherungsdateien automatisch für Sie (unabhängig von System-Backups oder Kontosynchronisierungen in Ihren iOS-Einstellungen). Weitere Details finden Sie unter [Sicherung, Rückgängigmachen und Wiederherstellungsverlauf](recovery.md) sowie im Leitfaden [Backup Contacts Before Merge on iPhone (Englisch)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone).
- **Laufende Synchronisierungen abwarten**: Wenn Sie kürzlich ein neues iPhone eingerichtet, Daten von einem anderen Telefon übertragen oder eine Kontosynchronisierung eingeschaltet haben, warten Sie vor dem Zusammenführen ab, bis die Hintergrundsynchronisierung abgeschlossen ist.

## Schritt-für-Schritt-Ablauf

1. **Kontaktberechtigung erteilen**: Erlauben Sie den Zugriff auf Kontakte, sobald iOS danach fragt. Falls keine Abfrage erscheint oder der Zugriff zuvor deaktiviert wurde, lesen Sie [Berechtigungen und Fehlerbehebung](permissions-troubleshooting.md).
2. **Adressbuch scannen**: Starten Sie in ContactMerge+ Cleaner einen Scan, um mögliche Duplikatgruppen anzuzeigen.
3. **Einzelne Gruppe öffnen und Vorschau prüfen**: Tippen Sie auf eine Duplikatgruppe, prüfen Sie die Zusammenführungsvorschau und wählen Sie aus, welche Karte als Hauptkontakt (Basiskarte) erhalten bleiben soll.
4. **Notizen in Apples Kontakte-App prüfen und Felder vor dem Bestätigen kontrollieren**:
   - Wichtige Notizen (Notes) in den übrigen zusammengeführten und anschließend gelöschten Karten (sekundären Kontakten) werden **nicht** gelesen oder in den Hauptkontakt kopiert und lassen sich später nicht wiederherstellen.
   - **Notizen in Apples Kontakte-App prüfen, nicht in der Vorschau**: ContactMerge+ Cleaner kann Kontaktnotizen nicht lesen. Schließen Sie niemals daraus, dass in der Vorschau von ContactMerge+ Cleaner keine Notizen erscheinen, auf das Fehlen von Notizen – öffnen Sie vor dem Zusammenführen Apples **Kontakte**-App, um wichtige Notizen dort einzusehen und manuell zu sichern.
   - **Nach externen Änderungen erneut prüfen**: Wenn Sie ContactMerge+ Cleaner verlassen, um Kontakte in Apples Kontakte-App anzusehen oder zu bearbeiten, kehren Sie danach zu ContactMerge+ Cleaner zurück und kontrollieren Sie vor dem Bestätigen erneut die aktuellen Duplikat-Vorschläge und die Zusammenführungsvorschau. Gehen Sie nicht davon aus, dass sich eine bereits geöffnete Vorschlagsliste oder Vorschau automatisch aktualisiert.
   - **Erwartete Felder kontrollieren**: Gehen Sie nicht davon aus, dass in jedem Fall alle Felder automatisch übernommen werden. Bestätigen Sie nur, wenn die Karten eindeutig zu derselben Person gehören und die Vorschau die gewünschten Felder zeigt.

### Beispielansichten: Scan-Ergebnisse und Zusammenführungsvorschau

<img src="../../assets/scan-results-demo.png" alt="Simulator-Demo der Scan-Ergebnisse (Duplicate Contacts) mit englischer Benutzeroberfläche, Undo Last Contact Merge sowie Ready to merge und Needs review für frei erfundene Beispielkontakte" width="420">

*Scan-Ergebnisse – Simulator-Demo mit frei erfundenen Beispielkontakten (englische Benutzeroberfläche, aufgenommen am 2026-11-03). Darstellung und Wortlaut können je nach App- oder iOS-Version abweichen.*

<img src="../../assets/merge-preview-demo.png" alt="Simulator-Demo der Zusammenführungsvorschau (Merge Preview) mit englischer Benutzeroberfläche, Hinweis zum Prüfen von Notizen in Contacts und Auswahl des Hauptkontakts für einen fiktiven Kontakt" width="420">

*Zusammenführungsvorschau und Auswahl des Hauptkontakts – Simulator-Demo mit frei erfundenen Beispielkontakten (englische Benutzeroberfläche, aufgenommen am 2026-11-03; weitere Kontaktzeilen liegen unterhalb des sichtbaren Bildausschnitts). Darstellung und Wortlaut können je nach App- oder iOS-Version abweichen.*

## Gruppenstatus verstehen: `Ready to merge` vs. `Needs review`

ContactMerge+ Cleaner ordnet mögliche Duplikatgruppen anhand der vorliegenden Übereinstimmungshinweise in zwei Bereiche ein (die englischen Originalbezeichnungen bleiben hier zur Orientierung erhalten):

- **`Ready to merge` (bereit zum Zusammenführen)**:
  - Jedes einzelne Kontaktpaar in der Gruppe erfüllt strenge Übereinstimmungsprüfungen mit starken Hinweisen über alle Paare hinweg.
  - **Vorschau bleibt erforderlich**: Ein gleicher Name oder eine gleiche Telefonnummer garantiert nicht automatisch, dass zwei Karten im Alltag dieselbe Person betreffen. Prüfen Sie vor dem Bestätigen stets die Vorschau (und in Apples Kontakte-App eventuelle Notizen).
  - Nach Ihrer Bestätigung für die Stapelverarbeitung in Pro freigegeben.
- **`Needs review` (Überprüfung erforderlich)**:
  - Die Karten weisen schwächere oder widersprüchliche Hinweise auf – etwa eine geteilte Familien- oder Festnetznummer, unterschiedliche Namen oder nur teilweise übereinstimmende Kontaktdaten.
  - `Needs review` bedeutet nicht zwangsläufig einen Erkennungsfehler, sondern dient als vorsorglicher Schutz, damit Sie prüfen können, ob es sich tatsächlich um verschiedene Personen handelt.
  - Jede Gruppe muss einzeln von Hand geprüft und bestätigt werden. `Needs review`-Gruppen werden niemals in eine Stapelverarbeitung einbezogen.

## Funktionsumfang: Free vs. Pro

- **Free**:
  - Adressbuch scannen und alle erkannten Duplikatgruppen ansehen.
  - Jeweils eine einzelne Duplikatgruppe zusammenführen, mit bis zu 3 Kontakten innerhalb dieser Gruppe.
  - Keine Stapelverarbeitung mehrerer Gruppen.
- **Pro**:
  - Einmalige Freischaltung über den App Store ohne Abonnement. Den genauen Preis zeigt Apple für Ihre Region an.
  - Schaltet das vollständige Zusammenführen (auch für Gruppen mit mehr als 3 Kontakten) sowie die Stapelverarbeitung nach Bestätigung ausschließlich für `Ready to merge`-Gruppen frei.
  - `Needs review`-Gruppen erfordern weiterhin eine manuelle Einzelprüfung und Bestätigung.
  - Bei Fragen zur Abrechnung oder zur Wiederherstellung eines früheren Pro-Kaufs wenden Sie sich bitte an den [offiziellen Support (Englisch)](https://contactmerge.app/support).

## Weiterführende offizielle Leitfäden

- [How to Merge Contacts Safely (Englisch)](https://contactmerge.app/guides/merge-contacts-safely)
- [Backup Contacts Before Merge on iPhone (Englisch)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)
- [Offizieller Support (Englisch)](https://contactmerge.app/support)
- [Datenschutzerklärung (Englisch)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Dokumentationsstand

Geprüft am 8. Nov. 2026. Darstellung, Bezeichnungen und Verhalten können je nach installierter App-Version und iOS-Version abweichen.
