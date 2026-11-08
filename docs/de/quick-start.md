# Schnellstart: Kontakte sicher scannen und zusammenführen

- **Übersicht & Sprachen**: [Deutsche Übersicht](../readme/README.de.md) | [English Overview](../../README.md)
- **Anleitungen**: **Schnellstart** | [Sicherung & Wiederherstellung](recovery.md) | [Berechtigungen & Fehlerbehebung](permissions-troubleshooting.md) | [FAQ](faq.md)
- **Sprache / Language**: **Deutsch** | [English](../en/quick-start.md)

Diese Anleitung zeigt, wie Sie doppelte Kontakte auf Ihrem iPhone mit **ContactMerge+ Cleaner** finden, prüfen und sicher zusammenführen.

ContactMerge+ Cleaner verarbeitet Ihre Kontakte lokal auf Ihrem Gerät, lädt Ihr Adressbuch nicht auf Server des Entwicklers hoch und bietet keinen Cloud-Backup-Dienst des Entwicklers an. (Die Kontakt-Synchronisierung über iOS oder Konten – etwa iCloud oder Google – sowie System- oder Geräte-Backups sind separate Mechanismen, die über Ihre eigenen Konto- und iOS-Einstellungen gesteuert werden.) Produktinformationen und Downloads finden Sie auf der [offiziellen Website (Englisch)](https://contactmerge.app).

## Vor dem Start

- **Unabhängige, datierte Sicherung anlegen (empfohlen)**: Der Export einer `.vcf`-Datei (vCard) ist optional – Sie müssen vor dem Zusammenführen keine Datei exportieren –, doch wird eine unabhängige, datierte Sicherung dringend empfohlen, besonders vor Ihrer ersten Bereinigung. Stellen Sie sicher, dass Ihre Sicherung die tatsächlichen Konten abdeckt, in denen Ihre Kontakte gespeichert sind, und die erwarteten Einträge enthält. Eine Kontosynchronisierung (etwa über iCloud oder Google) ist kein unabhängiges Backup, da Zusammenführungen auf verbundene Geräte synchronisiert werden können. Weitere Hinweise finden Sie unter [Sicherung, Rückgängigmachen und Wiederherstellungsverlauf](recovery.md) sowie im Leitfaden [Backup Contacts Before Merge on iPhone (Englisch)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone).
- **Übertragungen und Erstsynchronisierungen abwarten**: Wenn Sie kürzlich ein neues iPhone eingerichtet, „Auf iOS übertragen“ (Move to iOS) genutzt oder ein E-Mail- bzw. Cloud-Konto hinzugefügt haben, warten Sie vor dem Scannen und Zusammenführen ab, bis die Hintergrundsynchronisierung vollständig abgeschlossen ist (Abwarten vermeidet Änderungen mitten während der Synchronisierung, garantiert für sich genommen jedoch nicht, dass bestehende Duplikate verschwinden).

## Schritt-für-Schritt-Ablauf beim Zusammenführen

1. **Kontaktberechtigung erteilen**: Erlauben Sie den Kontaktzugriff, sobald iOS danach fragt. Falls keine Abfrage erscheint oder die Sichtbarkeit unvollständig wirkt, lesen Sie [Berechtigungen und Fehlerbehebung](permissions-troubleshooting.md).
2. **Adressbuch scannen**: Starten Sie in ContactMerge+ Cleaner einen Scan, um mögliche Duplikatgruppen anzuzeigen.
3. **Einzelne Gruppe öffnen und Vorschau prüfen**: Tippen Sie auf eine Duplikatgruppe, prüfen Sie die Zusammenführungsvorschau (`Merge Preview`) und wählen Sie aus, welche Kontaktkarte als Hauptkontakt (Basiskarte) erhalten bleiben soll.
4. **Notizen in Apples Kontakte-App prüfen und Felder vor dem Bestätigen kontrollieren**:
   - Wichtige Notizen (Notes) in nicht-primären Kontakten (den übrigen Karten, die zusammengeführt werden) werden **nicht** gelesen oder in den Hauptkontakt kopiert und lassen sich später nicht wiederherstellen.
   - **Notizen in Apples Kontakte-App prüfen, nicht in der Vorschau**: ContactMerge+ Cleaner kann Kontaktnotizen nicht lesen. Schließen Sie aus fehlenden Notizen in der Vorschau von ContactMerge+ Cleaner niemals darauf, dass ein Kontakt keine Notizen enthält – öffnen Sie vor dem Zusammenführen Apples **Kontakte**-App, um diese Karten dort zu prüfen und wichtige Notizen manuell in den Hauptkontakt zu kopieren.
   - **Nach externem Ansehen oder Bearbeiten erneut prüfen**: Wenn Sie ContactMerge+ Cleaner verlassen, um Kontakte in Apples **Kontakte**-App anzusehen oder zu bearbeiten, kehren Sie danach zurück und prüfen Sie vor dem Bestätigen erneut die aktuellen Duplikat-Vorschläge und die Zusammenführungsvorschau. Gehen Sie nicht davon aus, dass sich eine bereits geöffnete Vorschlagsliste oder Vorschau automatisch aktualisiert oder automatisch einen neuen Scan auslöst.
   - **Identität und erwartete Felder kontrollieren**: Bestätigen Sie die Zusammenführung nur dann, wenn die Karten im Alltag eindeutig zu derselben Person gehören und die Vorschau die von Ihnen erwarteten Felder beibehält.

### Beispiel: Scan-Ergebnisse und Zusammenführungsvorschau

<img src="../../assets/scan-results-demo.png" alt="Simulator-Demo mit englischer Benutzeroberfläche (kein deutschsprachiger Screenshot, aufgenommen am 2026-11-03) der Scan-Ergebnisse unter Duplicate Contacts mit frei erfundenen Beispielkontakten sowie Undo Last Contact Merge, Ready to merge und Needs review; Bildschirme und Wortlaut können je nach App- oder iOS-Version abweichen" width="420">

*Scan-Ergebnisse – Simulator-Demo mit frei erfundenen Beispielkontakten (englische Benutzeroberfläche – kein deutschsprachiger Screenshot –, aufgenommen am 2026-11-03). Bildschirme, Layout und Wortlaut können je nach installierter App-Version oder iOS-Version abweichen.*

<img src="../../assets/merge-preview-demo.png" alt="Simulator-Demo mit englischer Benutzeroberfläche (kein deutschsprachiger Screenshot, aufgenommen am 2026-11-03) der Zusammenführungsvorschau unter Merge Preview mit frei erfundenen Beispielkontakten, Übereinstimmungsgründen, dem Warnhinweis Check and preserve notes in Contacts und der Auswahl des Hauptkontakts, während die zweite Kontaktzeile unterhalb des sichtbaren Scrollbereichs liegt; Bildschirme und Wortlaut können je nach App- oder iOS-Version abweichen" width="420">

*Zusammenführungsvorschau und Auswahl des Hauptkontakts – Simulator-Demo mit frei erfundenen Beispielkontakten (englische Benutzeroberfläche – kein deutschsprachiger Screenshot –, aufgenommen am 2026-11-03; die zweite Kontaktzeile liegt unterhalb des sichtbaren Scrollbereichs, sodass nicht beide Karten gleichzeitig zu sehen sind). Bildschirme, Layout und Wortlaut können je nach installierter App-Version oder iOS-Version abweichen.*

## Gruppenbezeichnungen verstehen: `Ready to merge` vs. `Needs review`

ContactMerge+ Cleaner ordnet mögliche Duplikatgruppen anhand der vorliegenden Übereinstimmungshinweise in zwei Bereiche ein (diese Dokumentation beschreibt sichere Prüfgewohnheiten und erhebt keinen Anspruch auf genaue interne Laufzeit-Schwellenwerte oder Normalisierungsregeln; die englischen Originalbezeichnungen der App bleiben zur Orientierung erhalten):

- **`Ready to merge` (bereit zum Zusammenführen)**:
  - Jedes einzelne Kontaktpaar in der Gruppe hat strenge Übereinstimmungsprüfungen auf Basis starker Hinweise über alle Paare hinweg bestanden.
  - **Vorschau bleibt erforderlich**: Ein gleicher Name oder eine gleiche Telefonnummer allein beweist nicht, dass zwei Karten für dieselbe Person stehen. Prüfen Sie vor dem Bestätigen stets die Vorschau und sehen Sie in Apples **Kontakte**-App nach eventuellen Notizen.
  - Nach Ihrer Bestätigung für die Stapelverarbeitung in Pro freigegeben.
- **`Needs review` (Überprüfung erforderlich)**:
  - Die Karten weisen schwächere oder widersprüchliche Hinweise auf – beispielsweise eine gemeinsam genutzte Haushalts- oder Bürotelefonnummer, Namensvarianten, widersprüchliche Geburtstage oder teilweise Überschneidungen.
  - Die Einstufung als `Needs review` ist eine vorsorgliche Sicherheitsmaßnahme und kein Scan-Fehler: Namensunterschiede bedeuten nicht automatisch zwei verschiedene Personen, während geteilte Telefonnummern oder identische Namen dennoch zu verschiedenen Familienmitgliedern oder Kolleginnen und Kollegen gehören können.
  - Jede Gruppe muss einzeln von Hand geprüft und bestätigt werden. `Needs review`-Gruppen werden niemals in Stapelzusammenführungen einbezogen, und es gibt keine Einstellung, mit der sich mehrdeutige Gruppen in die Stapelverarbeitung zwingen lassen. Wenn zwei Karten verschiedene Personen darstellen, lassen Sie sie getrennt.

## Funktionsumfang: Free vs. Pro

- **Free**:
  - Adressbuch scannen und alle erkannten Duplikatgruppen ansehen.
  - Jeweils eine einzelne Duplikatgruppe zusammenführen, mit bis zu 3 Kontakten innerhalb dieser Gruppe (eine Stapelverarbeitung mehrerer Gruppen ist nicht enthalten).
- **Pro**:
  - Einmalige Freischaltung über den App Store ohne Abonnement; Apple zeigt den regionalen Preis für Ihren Storefront-Bereich direkt an.
  - Schaltet das Zusammenführen für Gruppen mit mehr als 3 Kontakten sowie die Stapelverarbeitung für `Ready to merge`-Gruppen nach Bestätigung frei (`Needs review`-Gruppen erfordern weiterhin eine manuelle Einzelprüfung).
  - Keine der beiden Stufen verspricht bestimmte Scangeschwindigkeiten oder eine unbegrenzte Kontaktlisten-Kapazität.
  - Hinweise zur Wiederherstellung eines Kaufs oder zu Apples Rückerstattungsregeln finden Sie in den [FAQ](faq.md#q15) oder beim [offiziellen Support (Englisch)](https://contactmerge.app/support).

## Weiterführende Anleitungen & Support

- [Sicherung, Rückgängigmachen und Wiederherstellungsverlauf](recovery.md)
- [Berechtigungen und Fehlerbehebung](permissions-troubleshooting.md)
- [Häufig gestellte Fragen (FAQ)](faq.md)
- [How to Merge Contacts Safely (Englisch)](https://contactmerge.app/guides/merge-contacts-safely)
- [Backup Contacts Before Merge on iPhone (Englisch)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)
- [Offizieller Support (Englisch)](https://contactmerge.app/support)
- [Datenschutzerklärung (Englisch)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Dokumentationsstand

Geprüft am 8. Nov. 2026. Bildschirme, Bezeichnungen und Verhalten können je nach installierter App-Version und iOS-Version abweichen.
