# Guida rapida: scansione e unione in sicurezza

- **Panoramica e lingue**: [Panoramica in italiano](../readme/README.it.md) | [English Overview](../../README.md)
- **Guide**: **Guida rapida** | [Backup e recupero](recovery.md) | [Autorizzazioni e risoluzione dei problemi](permissions-troubleshooting.md) | [FAQ](faq.md)
- **Lingua / Language**: **Italiano** | [English](../en/quick-start.md)

Questa guida spiega come individuare, verificare e unire in sicurezza i contatti duplicati su iPhone utilizzando **ContactMerge+ Cleaner**.

ContactMerge+ Cleaner elabora i contatti direttamente sul dispositivo, non carica la rubrica sui server dello sviluppatore e non fornisce alcun servizio di backup su cloud dello sviluppatore. (La sincronizzazione dei contatti tramite iOS o account — come iCloud o Google — e i backup di sistema o del dispositivo sono meccanismi separati, regolati dalle impostazioni del proprio account e di iOS.) Le informazioni sul prodotto e il download sono disponibili sul [Sito ufficiale (in inglese)](https://contactmerge.app).

## Prima di iniziare

- **Creare un backup indipendente e datato (consigliato)**: L'esportazione di un file `.vcf` (vCard) è facoltativa — non è obbligatorio esportarne uno prima di procedere — ma è vivamente consigliato conservare un backup indipendente e datato, soprattutto prima della prima pulizia. Assicurarsi che il backup copra gli account effettivi in cui sono salvati i contatti e contenga le schede previste. La sincronizzazione dell'account (come iCloud o Google) non costituisce un backup indipendente, poiché le unioni possono propagarsi agli altri dispositivi collegati. Vedere [Backup, annullamento e cronologia di recupero](recovery.md) e [Backup Contacts Before Merge on iPhone (in inglese)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone).
- **Attendere il completamento di trasferimenti e sincronizzazioni iniziali**: Se di recente è stato configurato un nuovo iPhone, è stato usato Passa a iOS (`Move to iOS`) o è stato aggiunto un account e-mail o cloud, attendere il termine della sincronizzazione in background prima di scansionare e unire i contatti (attendere evita modifiche a metà sincronizzazione, pur non garantendo di per sé la rimozione dei duplicati già presenti).

## Procedura passo dopo passo per l'unione

1. **Concedere l'autorizzazione ai Contatti**: Consentire l'accesso ai Contatti quando richiesto da iOS. Se non compare alcuna richiesta o l'elenco appare incompleto, consultare [Autorizzazioni e risoluzione dei problemi](permissions-troubleshooting.md).
2. **Scansionare la rubrica**: Avviare una scansione in ContactMerge+ Cleaner per visualizzare i gruppi candidati di contatti duplicati.
3. **Aprire un gruppo ed esaminare l'anteprima**: Toccare un gruppo di duplicati, controllare l'anteprima di unione (`Merge Preview`) e scegliere quale scheda mantenere come contatto principale (scheda di base).
4. **Controllare le Note nell'app Contatti di Apple e verificare i campi prima di confermare**:
   - Le note importanti presenti sui contatti non principali (le altre schede che verranno unite) **non** vengono lette né copiate nel contatto principale e non potranno essere recuperate in seguito.
   - **Verificare le Note nell'app Contatti di Apple, non nell'anteprima**: ContactMerge+ Cleaner non può leggere le note dei contatti. Non dare mai per scontato che un contatto sia privo di note solo perché non ne compaiono nell'anteprima di ContactMerge+ Cleaner: aprire l'app **Contatti** di Apple per ispezionare quelle schede e copiare manualmente eventuali note importanti nel contatto principale prima dell'unione.
   - **Ricontrollare dopo consultazioni o modifiche esterne**: Se si esce da ContactMerge+ Cleaner per consultare o modificare schede nell'app **Contatti** di Apple, al rientro ricontrollare i candidati duplicati attuali e l'anteprima di unione prima di confermare. Non dare per scontato che un elenco di candidati o un'anteprima già aperta si aggiorni o avvii automaticamente una nuova scansione.
   - **Verificare l'identità e i campi previsti**: Confermare l'unione solo quando le schede appartengono senza dubbi alla stessa persona nella realtà e l'anteprima conserva i campi desiderati.

### Esempio: risultati della scansione e anteprima di unione

<img src="../../assets/scan-results-demo.png" alt="Demo su simulatore con interfaccia in inglese (schermata non localizzata in italiano, acquisita il 2026-11-03) dei risultati della scansione Duplicate Contacts con contatti fittizi che mostra Undo Last Contact Merge, Ready to merge e Needs review; schermate e diciture possono variare in base alla versione dell'app o di iOS" width="420">

*Risultati della scansione — Demo su simulatore con contatti fittizi (interfaccia in inglese, schermata non localizzata in italiano, acquisita il 2026-11-03). Schermate, layout e diciture possono variare in base alla versione dell'app installata o alla versione di iOS.*

<img src="../../assets/merge-preview-demo.png" alt="Demo su simulatore con interfaccia in inglese (schermata non localizzata in italiano, acquisita il 2026-11-03) di Merge Preview con contatti fittizi che mostra i motivi di corrispondenza, l'avviso Check and preserve notes in Contacts e la selezione del contatto principale mentre la seconda riga di contatto si trova sotto l'area di scorrimento visibile; schermate e diciture possono variare in base alla versione dell'app o di iOS" width="420">

*Anteprima di unione e selezione del contatto principale — Demo su simulatore con contatti fittizi (interfaccia in inglese, schermata non localizzata in italiano, acquisita il 2026-11-03; la seconda riga di contatto si trova sotto l'area di scorrimento visibile, quindi le due schede non sono visibili contemporaneamente). Schermate, layout e diciture possono variare in base alla versione dell'app installata o alla versione di iOS.*

## Comprendere le categorie dei gruppi: `Ready to merge` vs. `Needs review`

ContactMerge+ Cleaner suddivide i gruppi di duplicati candidati in due sezioni in base agli elementi di corrispondenza disponibili (questa documentazione illustra pratiche di revisione sicure, senza dichiarare soglie interne esatte di esecuzione o regole specifiche di normalizzazione):

- **`Ready to merge` (pronto per l'unione)**:
  - Ogni coppia di contatti nel gruppo ha superato controlli rigorosi basati su forti corrispondenze tra tutte le coppie.
  - **L'anteprima resta comunque obbligatoria**: condividere un nome o un numero di telefono non dimostra da solo che due schede rappresentino la stessa persona. Controllare sempre l'anteprima e verificare nell'app **Contatti** di Apple la presenza di eventuali note prima di confermare.
  - Idoneo all'unione in blocco nella versione Pro dopo la conferma dell'utente.
- **`Needs review` (da verificare)**:
  - Le schede presentano elementi più deboli o in conflitto — ad esempio un numero telefonico domestico o lavorativo condiviso, varianti del nome, date di compleanno discordanti o una sovrapposizione parziale.
  - La presenza in `Needs review` è una misura prudenziale di tutela e non un errore di scansione: differenze nel nome non indicano automaticamente due persone diverse, mentre numeri condivisi o nomi identici possono comunque appartenere a familiari o colleghi distinti.
  - Ogni gruppo deve essere esaminato e confermato singolarmente uno alla volta, e i gruppi `Needs review` non possono entrare nell'unione in blocco Pro. Se due schede rappresentano persone diverse, lasciarle separate senza unirle.

## Funzionalità Free vs. Pro

- **Free (versione gratuita)**:
  - Scansionare la rubrica e visualizzare tutti i gruppi di duplicati rilevati.
  - Unire un gruppo di duplicati alla volta, fino a un massimo di 3 contatti all'interno di quel gruppo (l'unione in blocco di più gruppi non è inclusa).
- **Pro**:
  - Sblocco una tantum su App Store senza abbonamento; Apple mostra direttamente il prezzo regionale previsto per il Paese o l'area geografica dell'account.
  - Sblocca l'unione per i gruppi con più di 3 contatti e l'unione in blocco dei gruppi `Ready to merge` dopo la conferma (i gruppi `Needs review` richiedono sempre un controllo manuale individuale).
  - Né la versione Free né la versione Pro promettono velocità di scansione specifiche o capacità illimitata della rubrica.
  - Per il ripristino dell'acquisto o la procedura di rimborso Apple, consultare le [FAQ](faq.md#q15) o contattare l'[Assistenza ufficiale (in inglese)](https://contactmerge.app/support).

## Guide correlate e assistenza

- [Backup, annullamento e cronologia di recupero](recovery.md)
- [Autorizzazioni e risoluzione dei problemi](permissions-troubleshooting.md)
- [Domande frequenti (FAQ)](faq.md)
- [How to Merge Contacts Safely (in inglese)](https://contactmerge.app/guides/merge-contacts-safely)
- [Backup Contacts Before Merge on iPhone (in inglese)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)
- [Assistenza ufficiale (in inglese)](https://contactmerge.app/support)
- [Informativa sulla privacy (in inglese)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Stato della documentazione

Verificato l'8 novembre 2026. Schermate, etichette e funzionamento possono variare in base alla versione dell'app installata e alla versione di iOS.
