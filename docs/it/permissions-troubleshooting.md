# Autorizzazioni e risoluzione dei problemi

- **Panoramica e lingue**: [Panoramica in italiano](../readme/README.it.md) | [English Overview](../../README.md)
- **Guide**: [Guida rapida](quick-start.md) | [Backup e recupero](recovery.md) | **Autorizzazioni e risoluzione dei problemi** | [FAQ](faq.md)
- **Lingua / Language**: **Italiano** | [English](../en/permissions-troubleshooting.md)

Questa guida illustra le impostazioni di autorizzazione per i Contatti su iPhone, le differenze tra **ContactMerge+ Cleaner** e gli strumenti integrati di Apple per i duplicati, la gestione sicura degli account sincronizzati e dei trasferimenti di telefono, le domande su acquisti e rimborsi e come contattare l'assistenza in sicurezza.

## Autorizzazione di accesso ai Contatti su iPhone

- **Necessaria per scansione e unione**: ContactMerge+ Cleaner richiede l'accesso ai Contatti per poter individuare e unire i duplicati sull'iPhone. L'elaborazione dei contatti avviene localmente sul dispositivo — la rubrica non viene caricata sui server dello sviluppatore e lo sviluppatore non fornisce alcun servizio di backup su cloud (distinto da eventuali sincronizzazioni dei contatti iCloud/Google o backup di sistema iOS regolati dalle proprie impostazioni).
- **Accesso completo vs. limitato in iOS**: A seconda della versione di iOS, Apple consente di stabilire a quali contatti può accedere un'app — incluso l'accesso completo o l'accesso limitato a contatti selezionati — nelle impostazioni di sistema per la privacy (**Settings > Privacy & Security > Contacts**; vedere la guida Apple: [Control access to Contacts on iPhone (in inglese)](https://support.apple.com/guide/iphone/control-access-to-contacts-iph9536aa9a5/ios)).
- **Se la scansione è bloccata o sembrano mancare dei contatti**:
  - Controllare nelle impostazioni di iOS il livello di autorizzazione ai Contatti concesso a ContactMerge+ Cleaner. Un accesso incompleto o limitato può restringere i contatti visibili all'app — **non** elimina i contatti, anche se non è garantito che l'app supporti ogni flusso di lavoro ad accesso limitato.
  - Se l'opzione non appare disponibile o il comportamento resta imprevisto dopo aver verificato le impostazioni di iOS, contattare l'[Assistenza ufficiale (in inglese)](https://contactmerge.app/support).
- **Cosa non fare**: Non disattivare e riattivare mai la sincronizzazione degli account, non rimuovere account, non eliminare contatti e non reimportare file `.vcf` per tentare di risolvere problemi di autorizzazione.

## ContactMerge+ Cleaner rispetto agli strumenti integrati di Apple per i duplicati

L'app **Contatti** di Apple integra funzioni per i duplicati e il collegamento delle schede che operano in modo diverso da ContactMerge+ Cleaner (vedere la guida Apple: [Merge or hide duplicate contacts on iPhone (in inglese)](https://support.apple.com/guide/iphone/merge-or-hide-duplicate-contacts-iph2ab28320d/ios)):

- **`View Duplicates` nell'app Contatti di Apple**: Quando disponibile, Apple mostra un avviso `View Duplicates` sotto `My Card` (la scheda personale) per rivedere e unire i duplicati rilevati. Se il banner `View Duplicates` di Apple non compare — ad esempio quando i numeri utilizzano formati diversi di prefisso internazionale o in alcune rubriche molto ampie — occorre distinguere questo comportamento di sistema da un problema di autorizzazione dell'app. Questa documentazione non dichiara le regole interne di rilevamento di Apple, né una soglia garantita di numero di contatti (come 1.000 contatti), un tempo fisso di attesa o una soluzione universale tramite `"Merge All"`.
- **Contatti collegati / scheda unificata vs. schede unite**: Il collegamento manuale dei contatti (`Link Contacts`) nell'app **Contatti** di Apple unifica la visualizzazione delle schede in un'unica vista senza unire le schede di origine sottostanti, e le modifiche effettuate su una scheda unificata possono propagarsi agli account collegati.
- **Come si differenzia ContactMerge+ Cleaner**: ContactMerge+ Cleaner esegue la scansione sul dispositivo e separa i candidati in `Ready to merge` e `Needs review`, consentendo di ispezionare prima un'anteprima di unione (verificando al contempo le note nell'app **Contatti** di Apple). Non promette velocità di scansione specifiche, capacità garantite sulle dimensioni della rubrica né la riparazione automatica di danni pregressi alla rubrica.
- Guide web ufficiali correlate:
  - [iOS View Duplicates and Country Code Formatting (in inglese)](https://contactmerge.app/guides/ios-view-duplicates-country-code)
  - [View Duplicates Missing on a Large Contact List (in inglese)](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list)

## Migrazione, sincronizzazione degli account e prevenzione di eliminazioni accidentali

La configurazione di un nuovo iPhone, l'uso di Passa a iOS (`Move to iOS`), l'importazione di file o il collegamento di più account (come iCloud e Google) fanno spesso emergere vecchi duplicati presenti tra diverse fonti, senza che ciò indichi un difetto del dispositivo:

- **Completare la sincronizzazione iniziale ed eseguire prima un backup**: Attendere che la migrazione del dispositivo o la sincronizzazione iniziale degli account sia terminata prima di valutare i duplicati (ciò non garantisce di per sé l'eliminazione dei duplicati, ma evita confusione a metà sincronizzazione). Individuare quale account ospita i contatti e creare un backup indipendente e datato prima di apportare qualsiasi modifica.
- **Verificare con cura**: Esaminare le anteprime di unione (soprattutto i gruppi `Needs review`) e salvare prima eventuali note dei contatti non principali nell'app **Contatti** di Apple; se si esce dall'app per visualizzare o modificare contatti, al ritorno ricontrollare i candidati attuali e l'anteprima prima di confermare.
- **Prevenzione obbligatoria delle eliminazioni**: Rimuovere un account da Contatti ha un effetto diverso rispetto all'eliminazione di singoli contatti, ed eliminare contatti da un account e-mail o cloud sincronizzato può cancellarli in modo permanente su tutti i dispositivi sincronizzati (solo per contesto informativo, vedere la guida Apple [Add or remove accounts in Contacts on iPhone (in inglese)](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios) e l'[avviso Apple sull'eliminazione dei contatti (in inglese)](https://support.apple.com/en-us/111793)). **Non** eliminare i contatti di origine, non toccare `"Delete from My iPhone"`, non disattivare/riattivare la sincronizzazione e non reimportare ripetutamente file `.vcf` come scorciatoia di pulizia — in caso di dubbi, interrompere l'operazione e rivolgersi all'[Assistenza ufficiale (in inglese)](https://contactmerge.app/support).
- Guide ufficiali per scenari specifici:
  - [Duplicate Contacts After Setting Up a New iPhone (in inglese)](https://contactmerge.app/guides/duplicate-contacts-after-new-iphone)
  - [Move to iOS Duplicate Contacts (in inglese)](https://contactmerge.app/guides/move-to-ios-duplicate-contacts)
  - [iCloud Duplicate Contacts After Sync (in inglese)](https://contactmerge.app/guides/icloud-duplicate-contacts-after-sync)
  - [Backup Contacts Before Merge on iPhone (in inglese)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)
  - [How to Merge Contacts Safely (in inglese)](https://contactmerge.app/guides/merge-contacts-safely)

## Sblocco Pro, ripristino degli acquisti e rimborsi

- **Sblocco una tantum (nessun abbonamento)**: Pro è un acquisto non consumabile una tantum su App Store con prezzo regionale mostrato da Apple — **non** seguire procedure di disdetta degli abbonamenti per questa app. Sblocca i gruppi con più di 3 contatti e l'unione in blocco per i gruppi `Ready to merge` confermati (`Needs review` resta sempre a revisione singola).
- **Ripristino di Pro**: Assicurarsi che sull'iPhone sia stato effettuato l'accesso con lo **stesso Apple Account** usato per l'acquisto originale e consultare la guida ufficiale di Apple: [If you can't find or use your in-app purchases (in inglese)](https://support.apple.com/en-us/108096). Poiché il percorso esatto del pulsante di ripristino all'interno dell'app non è verificato in questa documentazione, non vengono ipotizzati nomi di menu, non si consiglia di acquistare nuovamente Pro né si garantisce il ripristino automatico — se il ripristino non riesce, contattare l'[Assistenza ufficiale (in inglese)](https://contactmerge.app/support) o il supporto Apple.
- **Richieste di rimborso**: La fatturazione dell'App Store e le decisioni sull'idoneità ai rimborsi (che può variare per Paese o area geografica) spettano ad Apple; alcuni acquisti possono risultare idonei, ma **i rimborsi non sono garantiti**. Le richieste di rimborso utilizzano la procedura ufficiale di Apple tramite [reportaproblem.apple.com (in inglese)](https://reportaproblem.apple.com) (vedere [Request a refund for apps or content that you bought from Apple (in inglese)](https://support.apple.com/en-us/118223)), e lo sviluppatore non può garantire l'approvazione del rimborso.

## Contattare l'assistenza e proteggere la privacy

- **Assistenza**: [Assistenza ufficiale (in inglese)](https://contactmerge.app/support)
- **Dettagli utili e sicuri da comunicare**: Versione dell'app ContactMerge+ Cleaner, versione di iOS, comportamento atteso rispetto a quello osservato, indicazione se la schermata riguarda un controllo di sistema Apple o ContactMerge+ Cleaner, tipo di account coinvolto (ad es. iCloud o Google, **senza** indirizzo e-mail o ID account) e numero approssimativo di contatti se pertinente.
- **Regole rigorose di privacy e oscuramento dei dati**:
  - Non caricare mai elenchi di contatti privati, file `.vcf` (vCard), password, dati di pagamento o ricevute d'acquisto in segnalazioni pubbliche (gestire eventuali dettagli di fatturazione esclusivamente tramite i canali ufficiali sicuri di Apple o un appropriato canale privato di assistenza ufficiale quando necessario).
  - Oscurare tutti i nomi reali, numeri di telefono, indirizzi e-mail, foto, indirizzi postali, note e ID prima di condividere schermate — utilizzare dati dimostrativi fittizi ogni volta che è possibile.

## Link correlati

- [Guida rapida: scansione e unione in sicurezza](quick-start.md)
- [Backup, annullamento e cronologia di recupero](recovery.md)
- [Domande frequenti (FAQ)](faq.md)
- [Sito ufficiale (in inglese)](https://contactmerge.app)
- [Informativa sulla privacy (in inglese)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Stato della documentazione

Verificato l'8 novembre 2026. Schermate, etichette e funzionamento possono variare in base alla versione dell'app installata e alla versione di iOS.
