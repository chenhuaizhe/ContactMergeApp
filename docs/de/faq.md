# Häufig gestellte Fragen (FAQ)

- **Übersicht & Sprachen**: [Deutsche Übersicht](../readme/README.de.md) | [English Overview](../../README.md)
- **Anleitungen**: [Schnellstart](quick-start.md) | [Sicherung & Wiederherstellung](recovery.md) | [Berechtigungen & Fehlerbehebung](permissions-troubleshooting.md) | **FAQ**
- **Sprache / Language**: **Deutsch** | [English](../en/faq.md)

Praxisnahe Antworten für die sichere Nutzung von **ContactMerge+ Cleaner** auf dem iPhone – mit geprüftem Verhalten und bekannten Versionsgrenzen.

## Sicherungen und Duplikaterkennung (`q01`–`q06`)

<a id="q01"></a>
### 1. Benötige ich vor dem Zusammenführen ein `.vcf`-Backup oder reicht `Recovery History` aus?

Der `.vcf`-Export ist optional – die App erzwingt vorab keinen Export –, doch wird vor Ihrer ersten oder größten Bereinigung eine unabhängige, datierte Sicherung dringend empfohlen. `Recovery History` (Wiederherstellungsverlauf) ist nur ein begrenztes lokales Geräteprotokoll (höchstens 3 Zusammenführungs-Einträge und höchstens 3 Lösch-Einträge für etwa 30 Tage), stellt Kontaktnotizen nicht-primärer Karten nicht wieder her und bietet keinen Cloud-Backup-Dienst des Entwicklers. Kontosynchronisierung (iCloud oder Google) ist kein unabhängiges Backup, da Zusammenführungen geräteübergreifend synchronisieren können. Ihre Sicherung muss das tatsächliche Kontaktkonto und die erwarteten Einträge abdecken; vermeiden Sie wiederholte `.vcf`-Neuimporte oder blinde Komplett-Wiederherstellungen des Geräts. Siehe [Sicherung & Wiederherstellung](recovery.md) und [Backup Contacts Before Merge on iPhone (Englisch)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone).

<a id="q02"></a>
### 2. Was bedeutet `Ready to merge`, und sollte ich trotzdem die Vorschau prüfen?

`Ready to merge` (bereit zum Zusammenführen) bedeutet, dass jedes Kartenpaar der Gruppe strenge Prüfungen mit starken Hinweisen über alle Paare hinweg bestanden hat. Öffnen Sie vor dem Bestätigen dennoch stets die Vorschau (`Merge Preview`): Gleiche Namen oder Nummern allein beweisen nicht dieselbe Person, und die App kann Kontaktnotizen nicht lesen. Wählen Sie Ihre Hauptkarte, prüfen Sie in Apples **Kontakte**-App etwaige Notizen nicht-primärer Karten, kontrollieren Sie die erwarteten Felder in der Vorschau und bestätigen Sie erst dann (oder beziehen Sie `Ready to merge`-Gruppen nach Bestätigung in die Pro-Stapelverarbeitung ein). Siehe [Schnellstart](quick-start.md) und [How to Merge Contacts Safely (Englisch)](https://contactmerge.app/guides/merge-contacts-safely).

<a id="q03"></a>
### 3. Warum ist eine Gruppe als `Needs review` markiert, und kann ich sie per Stapelverarbeitung zusammenführen?

`Needs review` (Überprüfung erforderlich) steht für schwächere oder widersprüchliche Hinweise – etwa eine geteilte Haushaltsnummer, abweichende Namen, widersprüchliche Geburtstage oder Teilüberschneidungen. Das ist eine Sicherheitsvorkehrung, kein Scan-Fehler. `Needs review`-Gruppen erfordern eine manuelle Einzelprüfung und sind von der Pro-Stapelverarbeitung ausgeschlossen – erzwingen Sie bei unsicheren Einträgen keine Zusammenführung und lassen Sie Karten im Zweifel getrennt. Siehe [Schnellstart](quick-start.md).

<a id="q04"></a>
### 4. Sollte ich zusammenführen, wenn sich Namen unterscheiden – oder wenn zwei Karten exakt denselben Namen tragen?

Keines von beidem gilt automatisch. Namensunterschiede (z. B. Spitzname vs. voller Name) bedeuten nicht automatisch verschiedene Personen, während identische Namen dennoch zu verschiedenen Verwandten oder Mitarbeitenden gehören können. Diese Dokumentation beansprucht keine exakten Laufzeitregeln zu Groß-/Kleinschreibung oder Textnormalisierung. Vergleichen Sie in der Vorschau die dort tatsächlich angezeigten Angaben (etwa Namen, Telefonnummern und E-Mail-Adressen, sofern vorhanden) – gehen Sie niemals davon aus, dass ein Feld oder eine Notiz auf der Kontaktkarte leer ist, nur weil es in der Vorschau nicht erscheint. Öffnen Sie die Originalkarten in Apples **Kontakte**-App, um Firmen-/Arbeitgeberangaben, weitere identitätsrelevante Details sowie zu sichernde Notizen zu prüfen; kehren Sie nach externem Ansehen oder Bearbeiten zurück und prüfen Sie die aktuellen Vorschläge sowie die Vorschau vor dem Bestätigen erneut (gehen Sie nicht von einer automatischen Aktualisierung geöffneter Ansichten aus). Siehe [Schnellstart](quick-start.md).

<a id="q05"></a>
### 5. Zwei verschiedene Personen teilen sich eine Festnetz- oder Bürotelefonnummer. Was sollte ich tun?

Führen Sie sie **nicht** zusammen. Familienmitglieder mit gemeinsamem Festnetzanschluss, Partner mit derselben Notfallnummer oder Kolleginnen und Kollegen mit zentraler Empfangsnummer erscheinen oft als Vorschläge – meist unter `Needs review`. Ein Zusammenführen vereint verschiedene Personen in einer Karte. Lassen Sie verschiedene Personen getrennt und bestätigen Sie nur, wenn jede Karte dieselbe Person darstellt. Siehe [Schnellstart](quick-start.md).

<a id="q06"></a>
### 6. Warum hat ein Konflikt bei Geburtstagen eine Gruppe zur Überprüfung markiert?

Widersprüchliche Geburtstage zwischen Karten (in historischen Release- und Support-Notizen zu Version 1.3.6 neben Namenskonflikten erwähnt) sind ein praktischer Hinweis für eine manuelle Prüfung, kein exakt veröffentlichter Algorithmus-Schwellenwert. Abweichende Daten können auf zwei Verwandte mit geteilten Kontaktdaten oder auf einen Tippfehler einer älteren Karte hindeuten. Prüfen Sie beide Karten vorab in der Vorschau und in Apples **Kontakte**-App. Siehe [Schnellstart](quick-start.md).

## Konten, Übertragungen und Apple Kontakte (`q07`–`q11`)

<a id="q07"></a>
### 7. Wie arbeitet die App mit der iCloud- oder Google-Kontaktsynchronisierung zusammen?

Kontakte werden lokal auf Ihrem iPhone verarbeitet – es erfolgt kein Upload auf Entwickler-Server und es gibt keinen Cloud-Backup-Dienst des Entwicklers. iCloud-/Google-Synchronisierung und iOS-System-Backups sind jedoch separate, über Ihre Einstellungen gesteuerte Mechanismen, sodass bestätigte Zusammenführungen auf verbundene Geräte synchronisieren können. Schalten Sie zur Fehlerbehebung niemals die Synchronisierung aus/ein, entfernen Sie keine Konten, tippen Sie nicht auf `"Delete from My iPhone"` (vom iPhone löschen) und löschen Sie keine synchronisierten Quellkontakte – das Löschen von E-Mail-/Cloud-Kontakten kann diese geräteübergreifend dauerhaft entfernen (siehe Apples [Anleitung zur Kontoverwaltung (Englisch)](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios) und [Löschwarnung (Englisch)](https://support.apple.com/en-us/111793)). Ermitteln Sie zuerst Ihr Konto und sichern Sie es; halten Sie im Zweifel inne und kontaktieren Sie den [offiziellen Support (Englisch)](https://contactmerge.app/support). Siehe [Doppelte Kontakte nach iCloud-Synchronisierung](https://contactmerge.app/de/guides/icloud-duplicate-contacts-after-sync).

<a id="q08"></a>
### 8. Warum sind nach dem Einrichten eines neuen iPhones oder nach „Auf iOS übertragen“ (Move to iOS) Duplikate aufgetaucht?

Das Einrichten eines neuen iPhones, „Auf iOS übertragen“ (Move to iOS), Dateiimporte oder mehrere verbundene Konten legen oft ältere Duplikate über verschiedene Quellen hinweg offen – das bedeutet weder ein defektes Gerät noch eine einzelne garantierte Ursache. Warten Sie vor dem Scannen das Ende von Übertragung und erster Hintergrundsynchronisierung ab (beseitigt Duplikate nicht garantiert allein, vermeidet aber Änderungen mitten im Abgleich), erstellen Sie eine unabhängige Sicherung und prüfen Sie dann die Vorschauen laut [Schnellstart](quick-start.md). Siehe [Doppelte Kontakte nach dem Einrichten eines neuen iPhones](https://contactmerge.app/de/guides/duplicate-contacts-after-new-iphone) und [Doppelte Kontakte nach Wechsel mit „Auf iOS übertragen“ (Move to iOS)](https://contactmerge.app/de/guides/move-to-ios-duplicate-contacts).

<a id="q09"></a>
### 9. Apples `View Duplicates` fehlt – worin unterscheidet sich ContactMerge+ Cleaner?

In Apples **Kontakte**-App erscheint `View Duplicates` (Duplikate anzeigen), sofern verfügbar, unterhalb von `My Card` (eigene Karte), während manuelles `Link Contacts` nur die Anzeige vereinheitlicht, ohne die zugrunde liegenden Karten zusammenzuführen (Änderungen an einer vereinheitlichten Karte können an Quellkonten übertragen werden; siehe Apples [Duplikat-Anleitung (Englisch)](https://support.apple.com/guide/iphone/merge-or-hide-duplicate-contacts-iph2ab28320d/ios)). Fehlendes `View Duplicates` ist getrennt von App-Berechtigungen – es gibt keinen garantierten 1.000-Kontakte-Schwellenwert, keine feste Wartezeit und keine sichere pauschale „Alle zusammenführen“-Lösung (`Merge All`). Erteilen Sie ContactMerge+ Cleaner Kontaktzugriff, um lokal zu scannen und Vorschauen zu prüfen. Siehe [Berechtigungen & Fehlerbehebung](permissions-troubleshooting.md).

<a id="q10"></a>
### 10. Können Duplikate dieselbe Telefonnummer einmal mit und einmal ohne Ländervorwahl enthalten?

Ja – eine Karte speichert eventuell eine lokale Nummer, während eine andere eine Ländervorwahl ergänzt (etwa `+49` oder `+1`), was Apples Duplikathinweis nicht immer als exakten Treffer markiert. Ohne exakte Regeln zur Rufnummernnormalisierung zu beanspruchen, lässt ContactMerge+ Cleaner Sie die vollständigen Nummern in der Vorschau vergleichen. Prüfen Sie vor dem Bestätigen, ob beide zur selben Person gehören und Ihr gewünschtes Format erhalten bleibt. Siehe [iOS View Duplicates and Country Code Formatting (Englisch)](https://contactmerge.app/guides/ios-view-duplicates-country-code).

<a id="q11"></a>
### 11. Kann ContactMerge+ Cleaner auch große Kontaktlisten verarbeiten?

Sie können große Adressbücher lokal scannen – auch wenn Apples `View Duplicates` ausbleibt – und Ergebnisse unter `Ready to merge` sowie `Needs review` prüfen. Die App verspricht jedoch weder bestimmte Scangeschwindigkeiten noch unbegrenzte Kapazität. Lassen Sie die Hintergrundsynchronisierung abschließen, erstellen Sie eine unabhängige, datierte Sicherung und testen Sie zunächst eine einzelne Gruppe. Siehe [Berechtigungen & Fehlerbehebung](permissions-troubleshooting.md) und [View Duplicates Missing on a Large Contact List (Englisch)](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list).

## Rückgängigmachen, Wiederherstellungsverlauf und Kontaktnotizen (`q12`–`q14`)

<a id="q12"></a>
### 12. Wo befindet sich `Undo Last Contact Merge`, und was deckt die Funktion ab?

`Undo Last Contact Merge` (letzte Kontaktzusammenführung rückgängig machen) gilt nur für Ihre einzelne, unmittelbar letzte Zusammenführung. Im freigegebenen englischen Release-Simulator-Screenshot vom `2026-11-03` steht die Option oben in den Scan-Ergebnissen unter `Duplicate Contacts` oberhalb von `Ready to merge`. Da dies auf jenem datierten Simulator-Screenshot statt einem Live-Test Ihrer installierten Version beruht, können Aktivierungsstatus, Beschriftungen und Abfragen abweichen; zudem ist es keine vollständige Systemwiederherstellung (Notizen nicht-primärer Karten sind nicht wiederherstellbar, und ursprüngliche System-IDs/Verknüpfungen kehren eventuell nicht zurück). Siehe [Sicherung & Wiederherstellung](recovery.md).

<a id="q13"></a>
### 13. Welche Grenzen gelten für `Recovery History`, und wie öffne ich den Verlauf?

`Recovery History` (Wiederherstellungsverlauf) speichert **höchstens 3 Zusammenführungs-Einträge und höchstens 3 Lösch-Einträge** für **etwa 30 Tage auf Ihrem Gerät** (getrennte Obergrenzen, keine 6 garantierten Einträge). Ältere oder überschüssige Einträge sind nicht wiederherstellbar; nach App-Deinstallation oder Geräteverlust ist ebenfalls keine Wiederherstellung garantiert. **Nicht verifizierter Pfad**: Einstiegspunkt und Eintragsauswahl sind in den freigegebenen Screenshots nicht sichtbar, weshalb wir keine Menüpfade erraten – wenden Sie sich für Ihre Version an den [offiziellen Support (Englisch)](https://contactmerge.app/support). Siehe [Sicherung & Wiederherstellung](recovery.md).

<a id="q14"></a>
### 14. Warum muss ich Notizen in Apples Kontakte-App prüfen – und was schränkt die Wiederherstellung sonst noch ein?

ContactMerge+ Cleaner kann Kontaktnotizen nicht lesen: Notizen nicht-primärer Karten werden beim Zusammenführen **nicht** kopiert und sind weder über `Undo Last Contact Merge` noch über `Recovery History` wiederherstellbar. Fehlende Notizen in der Vorschau heißen niemals, dass eine Karte keine Notizen hat – prüfen und kopieren Sie diese vorab in Apples **Kontakte**-App. Kehren Sie nach externem Ansehen oder Bearbeiten zurück und prüfen Sie Vorschläge sowie Vorschau erneut (geöffnete Ansichten aktualisieren sich eventuell nicht automatisch). System-IDs/Verknüpfungen kehren möglicherweise nicht zurück, und als vorsorglicher Hinweis können spätere Bearbeitungen oder Synchronisierungs-Updates eine saubere Wiederherstellung verhindern. Siehe [Sicherung & Wiederherstellung](recovery.md).

## Free vs. Pro, Käufe und Support (`q15`–`q18`)

<a id="q15"></a>
### 15. Was ist in Free im Vergleich zu Pro enthalten?

**Free** umfasst Scannen, Ansehen aller vorgeschlagenen Gruppen sowie das Zusammenführen jeweils einer einzelnen Gruppe mit bis zu 3 Kontakten (keine Stapelverarbeitung mehrerer Gruppen). **Pro** ist eine einmalige Freischaltung im App Store **ohne Abonnement** zum von Apple angezeigten regionalen Preis. Pro schaltet Gruppen mit mehr als 3 Kontakten sowie die Stapelverarbeitung für bestätigte `Ready to merge`-Gruppen frei (`Needs review` bleibt einzeln zu prüfen). Siehe [Schnellstart](quick-start.md).

<a id="q16"></a>
### 16. Wie stelle ich meinen Pro-Kauf wieder her?

Pro ist ein nicht verbrauchbarer Kauf (Non-Consumable). Prüfen Sie, ob Ihr iPhone **denselben Apple Account** wie beim ursprünglichen Kauf nutzt, und lesen Sie Apples Anleitung: [If you can't find or use your in-app purchases (Englisch)](https://support.apple.com/en-us/108096). Da der genaue Wiederherstellungspfad in der App hier nicht verifiziert ist, erraten wir keine `Settings`-/Upgrade-Beschriftungen, empfehlen keinen Neukauf und garantieren keine automatische Wiederherstellung. Bleibt Pro gesperrt, kontaktieren Sie den [offiziellen Support (Englisch)](https://contactmerge.app/support) oder den Apple Support. Siehe [Berechtigungen & Fehlerbehebung](permissions-troubleshooting.md).

<a id="q17"></a>
### 17. Wie funktionieren Apple-Rückerstattungen – und gibt es ein Abonnement, das ich kündigen muss?

Pro ist ein Einmalkauf, kein Abonnement – folgen Sie für diese App keinen Anleitungen zur Abo-Kündigung. Apple wickelt die App-Store-Abrechnung ab und entscheidet je nach Land/Region über die Erstattungsfähigkeit; **Rückerstattungen sind nicht garantiert**. Sie können eine Rückerstattung über Apples offizielles Verfahren unter [reportaproblem.apple.com (Englisch)](https://reportaproblem.apple.com) beantragen (siehe Apples [Anleitung zu Rückerstattungen (Englisch)](https://support.apple.com/en-us/118223)); der Entwickler garantiert keine Genehmigung. Siehe [Berechtigungen & Fehlerbehebung](permissions-troubleshooting.md).

<a id="q18"></a>
### 18. Wie prüfe ich Berechtigungen, schütze meine Daten und kontaktiere sicher den Support?

Prüfen Sie in den iOS-Einstellungen Datenschutz & Sicherheit unter Kontakte (englischer Pfad `Settings > Privacy & Security > Contacts`; siehe Apples [Anleitung zum Kontaktzugriff (Englisch)](https://support.apple.com/guide/iphone/control-access-to-contacts-iph9536aa9a5/ios)); eingeschränkter Zugriff begrenzt nur die Sichtbarkeit für die App, ohne Kontakte zu löschen, wobei nicht jeder Ablauf mit eingeschränktem Zugriff garantiert wird. Die Verarbeitung erfolgt lokal ohne Upload auf Entwickler-Server (getrennt von iCloud-/Google-Synchronisierung und iOS-Backups; siehe [Datenschutzerklärung (Englisch)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)). Nennen Sie beim [offiziellen Support (Englisch)](https://contactmerge.app/support) App-/iOS-Version, Apple-Systemelement vs. App-Bildschirm, Kontotyp (ohne ID), ungefähre Kontaktanzahl sowie erwartetes vs. beobachtetes Verhalten – teilen Sie niemals Kontaktlisten, `.vcf`-Dateien, echte persönliche Daten, Passwörter oder Kaufbelege öffentlich. Siehe [Berechtigungen & Fehlerbehebung](permissions-troubleshooting.md).

## Dokumentationsstand

Geprüft am 8. Nov. 2026. Bildschirme, Bezeichnungen und Verhalten können je nach installierter App-Version und iOS-Version abweichen.
