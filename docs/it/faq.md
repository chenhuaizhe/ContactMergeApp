# Domande frequenti (FAQ)

- **Panoramica e lingue**: [Panoramica in italiano](../readme/README.it.md) | [English Overview](../../README.md)
- **Guide**: [Guida rapida](quick-start.md) | [Backup e recupero](recovery.md) | [Autorizzazioni e risoluzione dei problemi](permissions-troubleshooting.md) | **FAQ**
- **Lingua / Language**: **Italiano** | [English](../en/faq.md)

Risposte pratiche per utilizzare **ContactMerge+ Cleaner** in sicurezza su iPhone, con indicazione dei comportamenti verificati e dei limiti legati alle versioni.

## Backup e rilevamento dei duplicati (`q01`–`q06`)

<a id="q01"></a>
### 1. È necessario un backup `.vcf` prima di unire i contatti o basta `Recovery History`?

L'esportazione di un file `.vcf` è facoltativa — l'app non impone un'esportazione prima dell'unione — ma conservare un backup indipendente e datato prima della prima pulizia o di interventi estesi è vivamente consigliato. `Recovery History` è soltanto un registro locale limitato sul dispositivo (al massimo 3 record di unione e al massimo 3 record di eliminazione per circa 30 giorni), non può recuperare le note dei contatti non principali e non dispone di alcun backup su cloud dello sviluppatore. La sincronizzazione dell'account (iCloud o Google) non costituisce un backup indipendente poiché le unioni possono propagarsi agli altri dispositivi collegati. Assicurarsi che il backup copra l'account effettivo in cui risiedono i contatti e contenga le schede attese, evitando reimportazioni ripetute di file `.vcf` o ripristini completi del dispositivo eseguiti alla cieca. Vedere [Backup e recupero](recovery.md) e [Backup Contacts Before Merge on iPhone (in inglese)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone).

<a id="q02"></a>
### 2. Cosa significa `Ready to merge` ed è comunque necessario controllare l'anteprima?

`Ready to merge` significa che ogni coppia di schede nel gruppo ha superato controlli rigorosi basati su corrispondenze solide tra tutte le coppie. È comunque indispensabile aprire l'anteprima prima di confermare: avere lo stesso nome o lo stesso numero non dimostra da solo che due schede appartengano alla stessa persona, e l'app non può leggere il campo delle note dei contatti. Selezionare la scheda principale, controllare nell'app **Contatti** di Apple eventuali note sulle schede non principali, verificare i campi attesi nell'anteprima e infine confermare (oppure includere i gruppi `Ready to merge` in un'unione in blocco Pro confermata). Vedere [Guida rapida](quick-start.md) e [How to Merge Contacts Safely (in inglese)](https://contactmerge.app/guides/merge-contacts-safely).

<a id="q03"></a>
### 3. Perché un gruppo è contrassegnato come `Needs review` e si può unire in blocco?

`Needs review` indica corrispondenze più deboli o in conflitto — come un numero fisso domestico condiviso, nomi diversi, date di compleanno discordanti o una sovrapposizione parziale. Si tratta di un controllo prudenziale di sicurezza e non di un errore di scansione. Esaminare e confermare i gruppi `Needs review` singolarmente uno alla volta: questi gruppi non possono entrare nell'unione in blocco Pro. In caso di dubbi, o se le schede riguardano persone diverse, lasciarle separate senza unirle. Vedere [Guida rapida](quick-start.md).

<a id="q04"></a>
### 4. Conviene unire i contatti quando i nomi sono diversi — o quando due schede hanno esattamente lo stesso nome?

Nessuno dei due casi è automatico. Differenze nel nome (come un soprannome rispetto al nome completo) non indicano automaticamente persone diverse, mentre nomi identici possono comunque appartenere a due parenti o colleghi distinti. Questa documentazione non dichiara regole esatte di gestione delle maiuscole o di normalizzazione del testo durante il confronto. Nell'anteprima, confrontare i dati effettivamente mostrati a schermo (come nomi, numeri di telefono e indirizzi e-mail, ove presenti) — senza mai presumere che un campo o una nota sia vuoto sulla scheda contatto solo perché non compare nell'anteprima. Aprire le schede originali nell'app **Contatti** di Apple per controllare azienda o datore di lavoro, altri dettagli identificativi aggiuntivi ed eventuali note da salvare; dopo aver consultato o modificato le schede all'esterno dell'app, tornare e ricontrollare i candidati attuali e l'anteprima prima di confermare (senza dare per scontato che le schermate aperte si aggiornino automaticamente). Vedere [Guida rapida](quick-start.md).

<a id="q05"></a>
### 5. Due persone diverse condividono lo stesso numero di casa o di ufficio: come procedere?

**Non** unirle. Familiari che condividono un telefono fisso, partner che indicano lo stesso recapito di emergenza o colleghi associati al numero del centralino compaiono spesso tra i candidati — di norma in `Needs review`. L'unione combinerebbe persone distinte in un'unica scheda. Lasciare separate le schede di persone diverse e confermare l'unione solo quando ogni scheda del gruppo rappresenta la stessa persona. Vedere [Guida rapida](quick-start.md).

<a id="q06"></a>
### 6. Perché date di compleanno in conflitto segnalano un gruppo da verificare?

Date di compleanno discordanti tra le schede (menzionate nei registri storici di rilascio e supporto della versione 1.3.6 insieme ai conflitti sul nome) costituiscono un segnale pratico per eseguire un controllo manuale, e non una soglia algoritmica pubblicata in modo esatto. Date diverse possono indicare due familiari che condividono un recapito oppure un errore di battitura su una scheda meno recente. Controllare entrambe le schede nell'anteprima e nell'app **Contatti** di Apple prima di decidere. Vedere [Guida rapida](quick-start.md).

## Account, trasferimenti e app Contatti di Apple (`q07`–`q11`)

<a id="q07"></a>
### 7. Come funziona l'app con la sincronizzazione dei contatti di iCloud o Google?

I contatti vengono elaborati localmente sull'iPhone senza caricamento sui server dello sviluppatore e senza alcun backup su cloud dello sviluppatore. Tuttavia, la sincronizzazione iCloud/Google e i backup di sistema di iOS sono meccanismi separati regolati dalle proprie impostazioni, per cui le unioni confermate possono sincronizzarsi sui dispositivi collegati. Non disattivare/riattivare mai la sincronizzazione, non rimuovere account, non toccare `"Delete from My iPhone"` e non eliminare i contatti di origine sincronizzati come tentativo di risoluzione: l'eliminazione di contatti da un account e-mail o cloud può cancellarli definitivamente su tutti i dispositivi (vedere la [guida Apple agli account (in inglese)](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios) e l'[avviso sull'eliminazione dei contatti (in inglese)](https://support.apple.com/en-us/111793)). Individuare prima l'account interessato ed eseguire un backup; in caso di dubbi, fermarsi e contattare l'[Assistenza ufficiale (in inglese)](https://contactmerge.app/support). Vedere [iCloud Duplicate Contacts After Sync (in inglese)](https://contactmerge.app/guides/icloud-duplicate-contacts-after-sync).

<a id="q08"></a>
### 8. Perché sono comparsi duplicati dopo la configurazione di un nuovo iPhone o con Passa a iOS (`Move to iOS`)?

La configurazione di un nuovo iPhone, l'utilizzo di Passa a iOS (`Move to iOS`), l'importazione di file o il collegamento di più account fanno spesso emergere duplicati preesistenti tra fonti diverse — ciò non significa che il telefono sia difettoso né dimostra un'unica causa garantita. Attendere il completamento della migrazione e della sincronizzazione iniziale in background prima di eseguire la scansione (attendere evita modifiche a metà sincronizzazione, pur non garantendo da solo la scomparsa dei duplicati), creare un backup indipendente e verificare le anteprime seguendo la [Guida rapida](quick-start.md). Vedere [Duplicate Contacts After Setting Up a New iPhone (in inglese)](https://contactmerge.app/guides/duplicate-contacts-after-new-iphone) e [Move to iOS Duplicate Contacts (in inglese)](https://contactmerge.app/guides/move-to-ios-duplicate-contacts).

<a id="q09"></a>
### 9. Manca la funzione `View Duplicates` di Apple: in cosa si differenzia ContactMerge+ Cleaner?

Nell'app **Contatti** di Apple, l'avviso `View Duplicates` compare sotto `My Card` quando disponibile, mentre il comando manuale `Link Contacts` unifica la visualizzazione in un'unica vista senza unire le schede sottostanti (e le modifiche apportate a una scheda unificata possono propagarsi agli account di origine; vedere la [guida Apple sui duplicati (in inglese)](https://support.apple.com/guide/iphone/merge-or-hide-duplicate-contacts-iph2ab28320d/ios)). L'assenza di `View Duplicates` è distinta dalle autorizzazioni dell'app: non esiste una soglia garantita di 1.000 contatti, un tempo fisso di attesa o una correzione sicura universale tramite `"Merge All"`. Concedere l'accesso ai Contatti in ContactMerge+ Cleaner per scansionare localmente la rubrica ed esaminare le anteprime. Vedere [Autorizzazioni e risoluzione dei problemi](permissions-troubleshooting.md).

<a id="q10"></a>
### 10. I duplicati possono avere lo stesso numero con e senza prefisso internazionale?

Sì: una scheda può memorizzare un numero in formato nazionale mentre un'altra include il prefisso internazionale (come `+39` o `+1`), caso che l'avviso duplicati di Apple potrebbe non segnalare come corrispondenza esatta. Senza dichiarare regole interne esatte di normalizzazione telefonica, ContactMerge+ Cleaner permette di confrontare i numeri completi nell'anteprima di unione. Verificare che entrambi appartengano alla stessa persona e mantengano il formato atteso prima di confermare. Vedere [iOS View Duplicates and Country Code Formatting (in inglese)](https://contactmerge.app/guides/ios-view-duplicates-country-code).

<a id="q11"></a>
### 11. ContactMerge+ Cleaner gestisce rubriche di grandi dimensioni?

È possibile scansionare localmente rubriche estese anche quando `View Duplicates` di Apple non compare, esaminando i risultati suddivisi tra `Ready to merge` e `Needs review`. Tuttavia, l'app non promette velocità di scansione specifiche né una capacità illimitata. Attendere la fine della sincronizzazione in background, creare un backup indipendente e datato e provare prima l'unione su un singolo gruppo. Vedere [Autorizzazioni e risoluzione dei problemi](permissions-troubleshooting.md) e [View Duplicates Missing on a Large Contact List (in inglese)](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list).

## Annullamento, cronologia di recupero e Note dei contatti (`q12`–`q14`)

<a id="q12"></a>
### 12. Dove si trova `Undo Last Contact Merge` e cosa copre?

`Undo Last Contact Merge` agisce esclusivamente sulla singola unione più recente. Nella schermata approvata del simulatore Release in inglese datata `2026-11-03`, compare nella parte superiore dei risultati di scansione `Duplicate Contacts`, sopra la sezione `Ready to merge`. Poiché questa indicazione si basa su quella schermata datata del simulatore e non su un test dal vivo della versione installata sul dispositivo, stato di attivazione, etichette e avvisi possono variare; inoltre non costituisce un ripristino completo (le note dei contatti non principali non possono essere recuperate e gli ID o i collegamenti di sistema originali potrebbero non tornare). Vedere [Backup e recupero](recovery.md).

<a id="q13"></a>
### 13. Quali sono i limiti di `Recovery History` e come si apre?

`Recovery History` conserva **al massimo 3 record di unione e al massimo 3 record di eliminazione** per **circa 30 giorni sul dispositivo** (limiti separati per tipologia, non 6 record garantiti). Le voci più vecchie o eccedenti il limite non sono recuperabili, e il recupero non è garantito dopo la disinstallazione dell'app o lo smarrimento del dispositivo. **Percorso non verificato**: il punto di accesso e i passaggi di selezione dei record non figurano nelle schermate approvate, pertanto non vengono ipotizzati percorsi di menu — contattare l'[Assistenza ufficiale (in inglese)](https://contactmerge.app/support) per ricevere indicazioni sulla versione in uso. Vedere [Backup e recupero](recovery.md).

<a id="q14"></a>
### 14. Perché controllare le Note nell'app Contatti di Apple — e quali altri limiti ha il recupero?

ContactMerge+ Cleaner non può leggere le note dei contatti: le note presenti sulle schede non principali **non** vengono copiate durante l'unione né possono essere recuperate tramite `Undo Last Contact Merge` o `Recovery History`. L'assenza di note nell'anteprima non significa mai che una scheda ne sia priva: controllarle e copiarle prima nell'app **Contatti** di Apple. Dopo aver consultato o modificato contatti all'esterno dell'app, tornare in ContactMerge+ Cleaner e ricontrollare i candidati attuali e l'anteprima (le schermate aperte potrebbero non aggiornarsi automaticamente). Gli ID e i collegamenti di sistema potrebbero non essere ripristinati e, in via prudenziale, modifiche successive ai contatti o aggiornamenti di sincronizzazione possono impedire un recupero pulito. Vedere [Backup e recupero](recovery.md).

## Versione gratuita (Free) vs. Pro, acquisti e assistenza (`q15`–`q18`)

<a id="q15"></a>
### 15. Cosa includono la versione gratuita (Free) e la versione Pro?

**Free** include la scansione della rubrica, la visualizzazione di tutti i gruppi candidati e l'unione di un gruppo alla volta fino a 3 contatti in quel gruppo (senza unione in blocco di più gruppi). **Pro** è uno sblocco una tantum su App Store **senza abbonamento**, al prezzo regionale mostrato direttamente da Apple. Pro sblocca i gruppi con più di 3 contatti e l'unione in blocco per i gruppi `Ready to merge` confermati (`Needs review` rimane sempre a controllo singolo). Vedere [Guida rapida](quick-start.md).

<a id="q16"></a>
### 16. Come si ripristina l'acquisto Pro?

Pro è un acquisto non consumabile. Verificare che sull'iPhone sia attivo lo **stesso Apple Account** usato per l'acquisto originale e consultare la guida di Apple: [If you can't find or use your in-app purchases (in inglese)](https://support.apple.com/en-us/108096). Poiché il percorso esatto dell'interfaccia di ripristino nell'app non è verificato in questa sede, non vengono ipotizzate etichette di menu (come `Settings` o `Upgrade`), non si consiglia un nuovo acquisto né si garantisce il ripristino automatico. Se Pro resta bloccato, contattare l'[Assistenza ufficiale (in inglese)](https://contactmerge.app/support) o il supporto Apple. Vedere [Autorizzazioni e risoluzione dei problemi](permissions-troubleshooting.md).

<a id="q17"></a>
### 17. Come funzionano i rimborsi Apple — e c'è un abbonamento da disdire?

Pro è un acquisto una tantum e non un abbonamento: non seguire istruzioni per l'annullamento degli abbonamenti per questa app. Apple gestisce la fatturazione dell'App Store e decide l'idoneità al rimborso in base al Paese o all'area geografica; **i rimborsi non sono garantiti**. Eventuali richieste di rimborso vanno presentate tramite la procedura ufficiale di Apple su [reportaproblem.apple.com (in inglese)](https://reportaproblem.apple.com) (vedere la [guida ai rimborsi di Apple (in inglese)](https://support.apple.com/en-us/118223)); lo sviluppatore non può garantire l'approvazione del rimborso. Vedere [Autorizzazioni e risoluzione dei problemi](permissions-troubleshooting.md).

<a id="q18"></a>
### 18. Come verificare le autorizzazioni, proteggere la privacy e contattare l'assistenza in sicurezza?

Controllare nelle impostazioni di iOS **Settings > Privacy & Security > Contacts** (vedere la [guida Apple sull'accesso ai Contatti (in inglese)](https://support.apple.com/guide/iphone/control-access-to-contacts-iph9536aa9a5/ios)); l'accesso limitato restringe soltanto la visibilità nell'app senza eliminare i contatti, anche se non è garantito il supporto per ogni flusso ad accesso limitato. L'elaborazione è locale senza caricamento sui server dello sviluppatore (distinta dalla sincronizzazione iCloud/Google e dai backup di iOS; vedere l'[Informativa sulla privacy (in inglese)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)). Per contattare l'[Assistenza ufficiale (in inglese)](https://contactmerge.app/support), indicare versione dell'app e di iOS, controllo di sistema Apple rispetto a schermata dell'app, tipo di account (senza ID), numero approssimativo di contatti e comportamento atteso rispetto a quello osservato — non pubblicare mai elenchi di contatti, file `.vcf`, dati personali reali, password, dati di pagamento o ricevute d'acquisto in segnalazioni pubbliche. Vedere [Autorizzazioni e risoluzione dei problemi](permissions-troubleshooting.md).

## Stato della documentazione

Verificato l'8 novembre 2026. Schermate, etichette e funzionamento possono variare in base alla versione dell'app installata e alla versione di iOS.
