# Sicherung, Rückgängigmachen und Wiederherstellungsverlauf

- **Übersicht**: [Deutsche Übersicht](../readme/README.de.md) | [English Overview](../../README.md)
- **Anleitungen**: [Schnellstart](quick-start.md) | **Sicherung & Wiederherstellung** | [Berechtigungen & Fehlerbehebung](permissions-troubleshooting.md)
- **Sprache / Language**: **Deutsch** | [English](../en/recovery.md)

Diese Anleitung erklärt sinnvolle Sicherungen vor dem Zusammenführen, die Funktionsweise der lokalen Rückgängig- und Wiederherstellungsfunktionen in **ContactMerge+ Cleaner** sowie deren genaue Grenzen.

## Unabhängige Sicherung vor dem Zusammenführen

- **Optionaler `.vcf`-Export**: Der Export einer `.vcf`-Datei (vCard) ist optional – Sie müssen vor dem Zusammenführen in ContactMerge+ Cleaner keine Datei exportieren.
- **Empfohlen vor größeren Bereinigungen**: Es wird dringend empfohlen, vor dem Zusammenführen – besonders vor Ihrer ersten Bereinigung – eine unabhängige Sicherung Ihrer Kontakte anzulegen. ContactMerge+ Cleaner bietet keinen eigenen Cloud-Backup-Dienst an und exportiert keine externen Sicherungsdateien automatisch für Sie.
- **Weiterführende Informationen**: Lesen Sie hierzu [Backup Contacts Before Merge on iPhone (Englisch)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone) und [How to Merge Contacts Safely (Englisch)](https://contactmerge.app/guides/merge-contacts-safely).

## Kontaktnotizen vorab in Apples Kontakte-App prüfen und sichern

Wichtige Notizen (Notes) in den übrigen zusammengeführten und anschließend gelöschten Karten (sekundären Kontakten) werden beim Zusammenführen **nicht** gelesen oder in den Hauptkontakt kopiert. Beachten Sie daher vor jeder Bestätigung:

- **Notizen in Apples Kontakte-App prüfen, nicht in der Vorschau**: ContactMerge+ Cleaner kann Kontaktnotizen nicht lesen. Schließen Sie niemals aus einer Vorschau ohne sichtbare Notizen darauf, dass ein Kontakt keine Notizen enthält – öffnen Sie vor dem Zusammenführen Apples **Kontakte**-App, prüfen Sie die betroffenen Karten dort und kopieren Sie wichtige Notizen manuell in den Hauptkontakt (oder an einen anderen sicheren Ort).
- **Nach dem Wechsel zum Bearbeiten erneut prüfen**: Wenn Sie ContactMerge+ Cleaner verlassen, um Kontakte in Apples Kontakte-App anzusehen oder zu bearbeiten, kehren Sie danach zu ContactMerge+ Cleaner zurück und kontrollieren Sie vor dem Bestätigen erneut die aktuellen Duplikat-Vorschläge und die Zusammenführungsvorschau. Gehen Sie nicht davon aus, dass sich eine bereits geöffnete Vorschlagsliste oder Vorschau automatisch aktualisiert.
- **Keine spätere Wiederherstellung von Notizen**: Da ContactMerge+ Cleaner keine Notizen lesen kann, lassen sich Notizen aus sekundären Karten später weder über die Rückgängig-Funktion noch über `Recovery History` wiederherstellen.

## Letzte Änderungen in der App rückgängig machen

ContactMerge+ Cleaner bietet zwei lokale Funktionen auf dem Gerät für kürzlich ausgeführte Aktionen (die englischen Originalbezeichnungen bleiben zur Orientierung erhalten):

- **`Undo Last Contact Merge` (letzte Zusammenführung)**:
  - Bezieht sich ausschließlich auf die unmittelbar letzte einzelne Zusammenführung.
  - **Geprüfte Bildschirmposition und Hinweise**: Wenn Sie Ihre letzte Zusammenführung rückgängig machen möchten, öffnen Sie die Scan-Ergebnisseite `Duplicate Contacts` (oder kehren Sie dorthin zurück) und suchen Sie im oberen Bildschirmbereich oberhalb des Abschnitts `Ready to merge` nach dem angezeigten Bedienelement `Undo Last Contact Merge`.
  - **Versions- und Prüfgrenzen**: Genaue Bezeichnungen und Bildschirmlayouts können je nach installierter App- oder iOS-Version abweichen. Diese Positionsangabe stammt aus dem datierten englischen Release-Simulator-Screenshot vom `2026-11-03` und nicht aus einem Live-Test Ihrer installierten Version; diese Anleitung macht keine Zusage darüber, wann das Element in Ihrer Sitzung aktiv geschaltet ist, ob der Vorgang Ende-zu-Ende getestet wurde oder ob eine vollständige Rücknahme garantiert ist (und setzt auch keinen bestimmten Bestätigungsdialog voraus).
- **`Recovery History` (Wiederherstellungsverlauf)**:
  - Nutzt ein lokales Wiederherstellungsprotokoll, das die App beim Zusammenführen oder Löschen von Kontakten auf dem Gerät speichert.
  - Bewahrt **höchstens 3 Zusammenführungs-Einträge und höchstens 3 Lösch-Einträge** auf.
  - Einträge bleiben **etwa 30 Tage auf dem Gerät** gespeichert; ältere Einträge oder Einträge, die über das jeweilige 3-Einträge-Limit hinausgehen, können nicht wiederhergestellt werden.
  - **Nicht verifizierter Navigationspfad**: Der Einstiegspunkt, die Menüführung und die Schritte zur Auswahl einzelner Einträge für `Recovery History` sind auf den freigegebenen Screenshots nicht abgebildet, sodass diese Anleitung den genauen Pfad für Ihre installierte App-Version nicht bestätigen kann. Falls Sie `Recovery History` in Ihrer App-Version nicht finden können, wenden Sie sich bitte an den [offiziellen Support (Englisch)](https://contactmerge.app/support).

## Wichtige Grenzen der lokalen Wiederherstellung

Bitte beachten Sie, was `Undo Last Contact Merge` und `Recovery History` **nicht** bieten:

- **Keine vollständige Systemwiederherstellung**: Wie im Hinweis der App selbst angegeben, können Kontaktnotizen nicht gelesen werden (daher lassen sich Notizen aus sekundären Karten nicht wiederherstellen), und ursprüngliche Systemkennungen sowie Verknüpfungen werden möglicherweise nicht wiederhergestellt.
- **Keine unbegrenzte Rückgängig-Funktion**: `Recovery History` bewahrt höchstens 3 Zusammenführungs-Einträge und höchstens 3 Lösch-Einträge für etwa 30 Tage auf dem Gerät auf; ältere Einträge außerhalb dieser Grenzen können nicht wiederhergestellt werden.
- **Kein Cloud-Backup des Entwicklers; getrennt von Kontosynchronisierung und System-Backups**:
  - Kontaktverarbeitung und Wiederherstellungsprotokoll bleiben innerhalb der App auf Ihrem Gerät; der Entwickler bietet keinen Cloud-Backup-Dienst an und lädt Ihr Adressbuch nicht auf Entwickler-Server hoch.
  - **Kontosynchronisierung und iOS-Backups sind getrennt**: Die Kontakt-Synchronisierung über iOS oder Konten (z. B. iCloud oder Google) sowie System- oder Geräte-Backups sind separate Mechanismen, die über Ihre eigenen Konto- und iOS-Einstellungen gesteuert werden. Diese Aussagen versprechen daher **nicht**, dass eine Kontaktzusammenführung von der iCloud-/Google-Synchronisierung ausgenommen bleibt, und treffen **keine** Aussage oder Zusage darüber, ob System-Backups App-Daten einschließen oder ausschließen.
  - Über die aktuelle Verfügbarkeit der App und des Geräts hinaus (etwa nach Deinstallation der App oder bei Verlust bzw. Wechsel Ihres iPhones) ist eine Wiederherstellung ebenfalls nicht garantiert.
- **Vorsorglicher Sicherheitshinweis bei späteren Bearbeitungen**: Als vorsorgliche Sicherheitsregel – und nicht als nachgewiesene harte Sperre in der App – kann eine Wiederherstellung nicht garantiert werden, wenn betroffene Kontakte nachträglich bearbeitet oder überschrieben wurden (sei es manuell in der Kontakte-App, durch eine andere App, auf einem anderen Gerät oder über eine Kontosynchronisierung). Diese Anleitung behauptet nicht, dass die App eine Wiederherstellung nach späteren Änderungen stets verweigert, und nennt keine internen Prüfregeln; vermeiden Sie jedoch Änderungen an zusammengeführten Kontakten, solange Sie die Zusammenführung eventuell noch rückgängig machen möchten.
- **Riskante manuelle Reparaturversuche vermeiden**: Schalten Sie die Kontosynchronisierung nicht wiederholt aus und ein, löschen Sie keine E-Mail- oder Cloud-Konten und importieren Sie `.vcf`-Dateien nicht mehrfach neu, um ein unerwartetes Ergebnis zu korrigieren – dies kann Duplikate vervielfachen oder Kontaktdaten überschreiben.

## Sicher Support anfordern

Wenn Sie Fragen zur Wiederherstellung haben oder ein Bedienelement in Ihrer Version nicht finden:

- Wenden Sie sich an den [offiziellen Support (Englisch)](https://contactmerge.app/support).
- Nennen Sie Ihre iOS-Version, Ihre installierte App-Version von ContactMerge+ Cleaner sowie kurz, was Sie erwartet haben und was stattdessen passiert ist.
- **Datenschutz beachten**: Teilen Sie keine privaten Kontaktdaten in öffentlichen Issues und laden Sie niemals Kontaktlisten oder `.vcf`-Dateien (vCards) hoch. Schwärzen Sie auf Screenshots vor dem Teilen alle Namen, Telefonnummern, E-Mail-Adressen, Fotos, Postanschriften, Notizen und Kennungen – oder nutzen Sie ausschließlich frei erfundene Beispieldaten.

## Verwandte Links

- [Schnellstart: Kontakte sicher prüfen und zusammenführen](quick-start.md)
- [Berechtigungen und Fehlerbehebung](permissions-troubleshooting.md)
- [Offizielle Website (Englisch)](https://contactmerge.app)
- [Datenschutzerklärung (Englisch)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Dokumentationsstand

Geprüft am 8. Nov. 2026. Darstellung, Bezeichnungen und Verhalten können je nach installierter App-Version und iOS-Version abweichen.
