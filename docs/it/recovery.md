# Backup, annullamento e cronologia di recupero

- **Panoramica e lingue**: [Panoramica in italiano](../readme/README.it.md) | [English Overview](../../README.md)
- **Guide**: [Guida rapida](quick-start.md) | **Backup e recupero** | [Autorizzazioni e risoluzione dei problemi](permissions-troubleshooting.md) | [FAQ](faq.md)
- **Lingua / Language**: **Italiano** | [English](../en/recovery.md)

Questa guida descrive le buone pratiche di backup prima dell'unione, il funzionamento dell'annullamento e del recupero sul dispositivo in **ContactMerge+ Cleaner** e i limiti importanti da conoscere prima di unire i contatti.

## Backup indipendente prima dell'unione

- **Esportazione `.vcf` facoltativa**: L'esportazione di un file `.vcf` (vCard) è facoltativa — ContactMerge+ Cleaner non obbliga a esportare un file prima di unire i contatti.
- **Backup indipendente e datato consigliato**: Conservare un backup indipendente e datato prima di procedere è vivamente consigliato, specialmente prima della prima pulizia o di un'unione in blocco. ContactMerge+ Cleaner non fornisce alcun servizio di backup su cloud dello sviluppatore né esporta automaticamente file di backup esterni.
- **Verificare cosa copre il backup**: Assicurarsi che il backup copra l'account di origine effettivo in cui si trovano i contatti (ad esempio iCloud o Google e non un account vuoto) e contenga il numero di schede e i dettagli attesi. La sincronizzazione dell'account non equivale a un backup indipendente, poiché le modifiche apportate durante la pulizia possono sincronizzarsi sugli altri dispositivi collegati.
- **Evitare tentativi di ripristino distruttivi**: Non reimportare ripetutamente file `.vcf` né eseguire alla cieca un ripristino completo del dispositivo per risolvere un singolo problema sui contatti — ciò può moltiplicare i duplicati o sovrascrivere modifiche più recenti.
- **Approfondimenti**: Consultare [Backup Contacts Before Merge on iPhone (in inglese)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone) e [How to Merge Contacts Safely (in inglese)](https://contactmerge.app/guides/merge-contacts-safely).

## Verificare e salvare le Note dei contatti nell'app Contatti di Apple

Le note importanti presenti sui contatti non principali (le altre schede che vengono unite nella scheda principale) **non** vengono lette né copiate durante un'unione. Prima di confermare qualsiasi unione:

- **Ispezionare le Note nell'app Contatti di Apple, non nell'anteprima**: ContactMerge+ Cleaner non può leggere le note dei contatti. Non dare mai per scontato che una scheda non contenga note solo perché non ne compaiono nell'anteprima di ContactMerge+ Cleaner: aprire l'app **Contatti** di Apple per controllare quelle schede e copiare manualmente eventuali note importanti nel contatto principale (o in un altro luogo sicuro) prima dell'unione.
- **Ricontrollare dopo essere usciti dall'app**: Se si passa all'app **Contatti** di Apple per visualizzare o modificare dei contatti, al rientro in ContactMerge+ Cleaner ricontrollare i candidati duplicati attuali e l'anteprima di unione prima di confermare. Non presupporre che un elenco di candidati o un'anteprima già aperta si aggiorni o avvii automaticamente una nuova scansione.
- **Le Note non possono essere recuperate in seguito**: Poiché ContactMerge+ Cleaner non può leggere il campo delle note, le note delle schede non principali non possono essere ripristinate successivamente tramite `Undo Last Contact Merge` o `Recovery History`.

## Annullare modifiche recenti nell'app

ContactMerge+ Cleaner include due funzioni di recupero locale sul dispositivo con precisi limiti di ambito:

- **`Undo Last Contact Merge` (ultima unione effettuata)**:
  - Riguarda esclusivamente la singola unione più recente.
  - **Posizione verificata nella schermata**: Per cercare il comando di annullamento dopo l'ultima unione, aprire o tornare alla schermata dei risultati di scansione `Duplicate Contacts` e controllare nella parte superiore della schermata, sopra la sezione `Ready to merge`, la voce `Undo Last Contact Merge`.
  - **Avvertenze su verifica e versioni**: Questa posizione del controllo è verificata sulla base della schermata del simulatore Release in inglese datata `2026-11-03`, e non tramite un test dal vivo sulla versione installata sul dispositivo dell'utente. Diciture e layout possono variare in base alla versione dell'app o di iOS; questa guida non dichiara quando il comando risulti attivo nella sessione specifica, né che l'annullamento completo sia stato testato dal vivo sulla build installata o che ogni proprietà sottostante del contatto venga ripristinata (e non presuppone una finestra di conferma specifica).
- **`Recovery History` (cronologia di recupero)**:
  - Utilizza un registro di recupero sul dispositivo salvato localmente dall'app sull'iPhone.
  - Conserva **al massimo 3 record di unione e al massimo 3 record di eliminazione** (si tratta di limiti separati per ciascun tipo di operazione, non della garanzia che siano disponibili 6 record in ogni momento).
  - Le voci restano sul dispositivo per **circa 30 giorni**; i record più vecchi o quelli che superano il limite di 3 voci per quel tipo di azione non possono essere recuperati.
  - **Percorso di navigazione non verificato**: Il punto di accesso, la navigazione tra le schermate e i passaggi di selezione dei record per `Recovery History` non sono mostrati nelle schermate approvate; pertanto questa guida indica il percorso di navigazione come non verificato anziché ipotizzare i nomi dei menu. Se non si riesce a individuare `Recovery History`, contattare l'[Assistenza ufficiale (in inglese)](https://contactmerge.app/support).

## Limiti importanti del recupero sul dispositivo

Tenere presente ciò che `Undo Last Contact Merge` e `Recovery History` **non** offrono:

- **Non sono un ripristino completo di sistema**: Le note dei contatti non principali non possono essere lette né recuperate, e gli identificatori di sistema e i collegamenti originali tra contatti potrebbero non essere ripristinati. Inoltre l'app non può riparare danni pregressi arbitrari alla rubrica causati da altri strumenti o importazioni.
- **Nessun backup su cloud dello sviluppatore; distinzione da sincronizzazione account e backup di sistema**:
  - L'elaborazione dei contatti e il registro di recupero rimangono sul dispositivo all'interno dell'app; lo sviluppatore non carica la rubrica sui propri server né fornisce un servizio di backup su cloud.
  - **Sincronizzazione dell'account e backup di iOS sono meccanismi separati**: La sincronizzazione dei contatti tramite iOS o account (come iCloud o Google) e i backup di sistema o del dispositivo sono meccanismi distinti regolati dalle impostazioni dell'account e di iOS dell'utente. Questa documentazione **non** promette che un'unione resti esclusa dalla sincronizzazione iCloud/Google e **non** formula garanzie sul fatto che i backup di sistema includano o escludano i dati dell'app.
  - Il recupero non è garantito in caso di disinstallazione dell'app o di smarrimento o sostituzione dell'iPhone.
- **Cautela prudenziale in caso di modifiche successive ai contatti**: Come indicazione prudenziale di sicurezza — e non come blocco rigido verificato nell'app — il recupero non può essere garantito se i contatti interessati sono stati successivamente modificati o sovrascritti tramite sincronizzazione (nell'app **Contatti** di Apple, in un'altra app, su un altro dispositivo o tramite sincronizzazione dell'account). Evitare di modificare i contatti uniti se si ritiene di voler ancora annullare quell'unione.
- **Non risolvere mai i problemi eliminando i contatti di origine o rimuovendo account**: L'eliminazione di contatti salvati in un account e-mail o cloud sincronizzato può cancellarli definitivamente su tutti i dispositivi collegati (vedere l'[avviso Apple sull'eliminazione dei contatti (in inglese)](https://support.apple.com/en-us/111793) e la [guida Apple alla gestione degli account (in inglese)](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios)). Non toccare `"Delete from My iPhone"`, non disattivare e riattivare la sincronizzazione dell'account e non rimuovere account per risolvere dubbi su un'unione: in caso di incertezza, fermarsi e contattare prima l'assistenza.

## Contattare l'assistenza in sicurezza

- Scrivere tramite l'[Assistenza ufficiale (in inglese)](https://contactmerge.app/support) indicando la versione dell'app ContactMerge+ Cleaner, la versione di iOS, se si sta osservando una schermata di Contatti di Apple o di ContactMerge+ Cleaner, il tipo di account interessato (come iCloud o Google, senza condividere l'ID dell'account) e il comportamento atteso rispetto a quello riscontrato.
- **Proteggere la privacy**: Non pubblicare mai elenchi di contatti, file `.vcf`, password, dati di pagamento o ricevute d'acquisto in segnalazioni pubbliche. Oscurare tutti i nomi reali, numeri di telefono, indirizzi e-mail, foto, indirizzi postali, note e ID prima di condividere qualsiasi schermata — oppure utilizzare esclusivamente dati dimostrativi fittizi.

## Link correlati

- [Guida rapida: scansione e unione in sicurezza](quick-start.md)
- [Autorizzazioni e risoluzione dei problemi](permissions-troubleshooting.md)
- [Domande frequenti (FAQ)](faq.md)
- [Sito ufficiale (in inglese)](https://contactmerge.app)
- [Informativa sulla privacy (in inglese)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Stato della documentazione

Verificato l'8 novembre 2026. Schermate, etichette e funzionamento possono variare in base alla versione dell'app installata e alla versione di iOS.
