# Sicherung, Rückgängigmachen und Wiederherstellungsverlauf

- **Übersicht & Sprachen**: [Deutsche Übersicht](../readme/README.de.md) | [English Overview](../../README.md)
- **Anleitungen**: [Schnellstart](quick-start.md) | **Sicherung & Wiederherstellung** | [Berechtigungen & Fehlerbehebung](permissions-troubleshooting.md) | [FAQ](faq.md)
- **Sprache / Language**: **Deutsch** | [English](../en/recovery.md)

Diese Anleitung erläutert empfehlenswerte Sicherungen vor dem Zusammenführen, die Funktionsweise der lokalen Rückgängig- und Wiederherstellungsfunktionen auf dem Gerät in **ContactMerge+ Cleaner** sowie die Grenzen, die Sie vor dem Zusammenführen von Kontakten kennen sollten.

## Unabhängige Sicherung vor dem Zusammenführen

- **Optionaler `.vcf`-Export**: Der Export einer `.vcf`-Datei (vCard) ist optional – ContactMerge+ Cleaner zwingt Sie vor dem Zusammenführen nicht zum Exportieren einer Datei.
- **Empfohlene unabhängige, datierte Sicherung**: Eine unabhängige, mit Datum versehene Sicherung vor dem Zusammenführen wird dringend empfohlen, insbesondere vor Ihrer ersten Bereinigung oder einer Stapelzusammenführung. ContactMerge+ Cleaner bietet keinen Cloud-Backup-Dienst des Entwicklers an und exportiert keine externen Sicherungsdateien automatisch.
- **Prüfen, was Ihre Sicherung abdeckt**: Stellen Sie sicher, dass Ihre Sicherung das tatsächliche Quellkonto umfasst, in dem Ihre Kontakte gespeichert sind (etwa iCloud oder Google statt eines leeren Kontos), und die erwartete Kontaktanzahl sowie die erwarteten Details enthält. Eine Kontosynchronisierung ist kein unabhängiges Backup, da bei der Bereinigung vorgenommene Änderungen auf Ihre anderen verbundenen Geräte synchronisiert werden können.
- **Destruktive Wiederherstellungsversuche vermeiden**: Importieren Sie `.vcf`-Dateien nicht wiederholt neu und führen Sie keine blinde vollständige Gerätewiederherstellung durch, um ein kleines Kontaktproblem zu beheben – dies kann Duplikate vervielfachen oder neuere Änderungen überschreiben.
- **Weiterführende Lektüre**: Siehe [Backup Contacts Before Merge on iPhone (Englisch)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone) und [How to Merge Contacts Safely (Englisch)](https://contactmerge.app/guides/merge-contacts-safely).

## Kontaktnotizen in Apples Kontakte-App prüfen und sichern

Wichtige Notizen (Notes) in nicht-primären Kontakten (den übrigen Karten, die in die Hauptkarte zusammengeführt werden) werden beim Zusammenführen **nicht** gelesen oder kopiert. Beachten Sie vor dem Bestätigen jeder Zusammenführung:

- **Notizen in Apples Kontakte-App prüfen, nicht in der Vorschau**: ContactMerge+ Cleaner kann Kontaktnotizen nicht lesen. Schließen Sie aus fehlenden Notizen in der Vorschau von ContactMerge+ Cleaner niemals darauf, dass ein Kontakt keine Notizen enthält – öffnen Sie vor dem Zusammenführen Apples **Kontakte**-App, prüfen Sie die betreffenden Karten dort und kopieren Sie wichtige Notizen manuell in den Hauptkontakt (oder an einen anderen sicheren Ort).
- **Nach dem Verlassen der App erneut prüfen**: Wenn Sie ContactMerge+ Cleaner verlassen, um Kontakte in Apples **Kontakte**-App anzusehen oder zu bearbeiten, kehren Sie anschließend zurück und prüfen Sie vor dem Bestätigen erneut die aktuellen Duplikat-Vorschläge und die Zusammenführungsvorschau. Gehen Sie nicht davon aus, dass sich eine bereits geöffnete Vorschlagsliste oder Vorschau automatisch aktualisiert oder automatisch einen neuen Scan auslöst.
- **Notizen können später nicht wiederhergestellt werden**: Da ContactMerge+ Cleaner keine Notizen lesen kann, lassen sich Notizen aus nicht-primären Karten später weder über `Undo Last Contact Merge` noch über `Recovery History` wiederherstellen.

## Kürzliche Änderungen in der App rückgängig machen

ContactMerge+ Cleaner enthält zwei lokale Wiederherstellungsfunktionen auf dem Gerät mit klar abgegrenztem Umfang (die englischen Originalbezeichnungen bleiben zur Orientierung erhalten):

- **`Undo Last Contact Merge` (unmittelbar letzte Zusammenführung)**:
  - Bezieht sich ausschließlich auf die einzelne, unmittelbar letzte Zusammenführung.
  - **Geprüfte Bildschirmposition**: Um nach Ihrer letzten Zusammenführung nach der Rückgängig-Option zu suchen, öffnen Sie die Scan-Ergebnisseite `Duplicate Contacts` (oder kehren Sie dorthin zurück) und prüfen Sie den oberen Bildschirmbereich oberhalb des Abschnitts `Ready to merge` auf das Bedienelement `Undo Last Contact Merge`.
  - **Prüf- und Versionsvorbehalte**: Diese Positionsangabe wurde anhand des datierten englischen Release-Simulator-Screenshots vom `2026-11-03` geprüft und nicht durch einen Live-Test Ihrer installierten Version. Wortlaut und Layout können je nach App- oder iOS-Version abweichen; diese Anleitung erhebt keinen Anspruch darauf, wann das Bedienelement in Ihrer Sitzung aktiv geschaltet ist, dass eine Ende-zu-Ende-Rücknahme auf Ihrem Build live getestet wurde oder dass jede zugrunde liegende Kontakteigenschaft rückgängig gemacht wird (und setzt auch keinen bestimmten Bestätigungsdialog voraus).
- **`Recovery History` (Wiederherstellungsverlauf)**:
  - Nutzt ein lokales Wiederherstellungsprotokoll, das von der App auf Ihrem iPhone gespeichert wird.
  - Bewahrt **höchstens 3 Zusammenführungs-Einträge und höchstens 3 Lösch-Einträge** auf (dies sind getrennte Obergrenzen je Aktionstyp und keine Garantie dafür, dass jederzeit 6 Einträge verfügbar sind).
  - Einträge bleiben **etwa 30 Tage auf dem Gerät** erhalten; ältere Einträge oder Einträge, die über die 3-Einträge-Grenze des jeweiligen Aktionstyps hinausgeschoben wurden, können nicht wiederhergestellt werden.
  - **Nicht verifizierter Navigationspfad**: Der Einstiegspunkt, die Bildschirmnavigation und die Schritte zur Auswahl einzelner Einträge für `Recovery History` sind in den freigegebenen Screenshots nicht abgebildet. Daher kennzeichnet diese Anleitung den aktuellen Navigationspfad ausdrücklich als nicht verifiziert, anstatt Menübezeichnungen für Ihre installierte App-Version zu erraten. Wenn Sie `Recovery History` nicht finden können, wenden Sie sich bitte an den [offiziellen Support (Englisch)](https://contactmerge.app/support).

## Wichtige Grenzen der lokalen Wiederherstellung

Beachten Sie, was `Undo Last Contact Merge` und `Recovery History` **nicht** leisten:

- **Keine vollständige Systemwiederherstellung**: Kontaktnotizen aus nicht-primären Karten können weder gelesen noch wiederhergestellt werden, und ursprüngliche Systemkennungen sowie Kontaktverknüpfungen werden möglicherweise nicht wiederhergestellt. Zudem kann die App keine beliebigen früheren Schäden im Adressbuch reparieren, die durch andere Werkzeuge oder Importe entstanden sind.
- **Kein Cloud-Backup des Entwicklers; getrennt von Kontosynchronisierung und System-Backups**:
  - Kontaktverarbeitung und Wiederherstellungsprotokoll verbleiben innerhalb der App auf Ihrem Gerät; der Entwickler lädt Ihr Adressbuch nicht auf Entwickler-Server hoch und bietet keinen Cloud-Backup-Dienst an.
  - **Kontosynchronisierung und iOS-Backups sind getrennt**: Die Kontakt-Synchronisierung über iOS oder Konten (wie iCloud oder Google) sowie System- oder Geräte-Backups sind separate Mechanismen, die über Ihre eigenen Konto- und iOS-Einstellungen gesteuert werden. Diese Dokumentation verspricht **nicht**, dass eine Zusammenführung von der iCloud-/Google-Synchronisierung ausgenommen bleibt, und trifft **keine** Zusage darüber, ob System-Backups App-Daten einschließen oder ausschließen.
  - Eine Wiederherstellung ist nicht garantiert, wenn Sie die App deinstallieren oder Ihr iPhone verlieren bzw. ersetzen.
- **Vorsorglicher Hinweis bei späteren Kontaktänderungen**: Als vorsorgliche Sicherheitsempfehlung – nicht als nachgewiesene harte Sperre in der App – kann eine Wiederherstellung nicht garantiert werden, wenn betroffene Kontakte nachträglich bearbeitet oder per Synchronisierung überschrieben wurden (in Apples **Kontakte**-App, einer anderen App, auf einem anderen Gerät oder über die Kontosynchronisierung). Vermeiden Sie das Bearbeiten zusammengeführter Kontakte, solange Sie diese Zusammenführung eventuell noch rückgängig machen möchten.
- **Fehler niemals durch Löschen von Quellkontakten oder Entfernen von Konten beheben**: Das Löschen von Kontakten, die in einem synchronisierten E-Mail- oder Cloud-Konto gespeichert sind, kann diese geräteübergreifend dauerhaft löschen (siehe Apples [Warnhinweis zum Löschen von Kontakten (Englisch)](https://support.apple.com/en-us/111793) und [Anleitung zur Kontoverwaltung (Englisch)](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios)). Tippen Sie nicht auf `"Delete from My iPhone"` (vom iPhone löschen), schalten Sie die Kontosynchronisierung nicht aus und wieder ein und entfernen Sie keine Konten, um ein Problem beim Zusammenführen zu beheben – wenn Sie unsicher sind, brechen Sie ab und kontaktieren Sie zuerst den Support.

## Sicher Support anfordern

- Wenden Sie sich über den [offiziellen Support (Englisch)](https://contactmerge.app/support) an uns und nennen Sie Ihre App-Version von ContactMerge+ Cleaner, Ihre iOS-Version, ob Sie auf eine Ansicht von Apple Kontakte oder von ContactMerge+ Cleaner schauen, den relevanten Kontotyp (etwa iCloud oder Google, ohne Ihre Konto-ID zu teilen) sowie was Sie erwartet haben im Vergleich zu dem, was passiert ist.
- **Schützen Sie Ihre Privatsphäre**: Veröffentlichen Sie niemals Kontaktlisten, `.vcf`-Dateien, Passwörter, Zahlungsdaten oder Kaufbelege in öffentlichen Issues. Schwärzen Sie alle echten Namen, Telefonnummern, E-Mail-Adressen, Fotos, Postanschriften, Notizen und IDs, bevor Sie einen Screenshot teilen – oder verwenden Sie ausschließlich frei erfundene Beispieldaten.

## Verwandte Links

- [Schnellstart: Kontakte sicher scannen und zusammenführen](quick-start.md)
- [Berechtigungen und Fehlerbehebung](permissions-troubleshooting.md)
- [Häufig gestellte Fragen (FAQ)](faq.md)
- [Offizielle Website (Englisch)](https://contactmerge.app)
- [Datenschutzerklärung (Englisch)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Dokumentationsstand

Geprüft am 8. Nov. 2026. Bildschirme, Bezeichnungen und Verhalten können je nach installierter App-Version und iOS-Version abweichen.
