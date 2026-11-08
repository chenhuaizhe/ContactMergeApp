# ContactMerge+ Cleaner — Documentazione del prodotto e assistenza

Documentazione pubblica ufficiale del prodotto e guide di supporto per **ContactMerge+ Cleaner** su iPhone. Questo repository contiene esclusivamente documentazione per gli utenti — non è un repository del codice sorgente dell'applicazione.

ContactMerge+ Cleaner elabora i contatti direttamente sul dispositivo, non carica la rubrica sui server dello sviluppatore e lo sviluppatore non fornisce alcun servizio di backup su cloud. (La sincronizzazione dei contatti tramite iOS o account — come iCloud o Google — e i backup di sistema o del dispositivo sono meccanismi separati, regolati dalle impostazioni del proprio account e di iOS.)

- **Sito web**: [Sito ufficiale (in inglese)](https://contactmerge.app)
- **App Store**: [Scarica su App Store (in inglese)](https://apps.apple.com/us/app/contactmerge-contacts-cleaner/id6738980785)
- **Assistenza**: [Assistenza ufficiale (in inglese)](https://contactmerge.app/support)
- **Lingue**: [English](../../README.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | **Italiano** | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [日本語](README.ja.md) | [한국어](README.ko.md) | [简体中文](README.zh-Hans.md) | [繁體中文](README.zh-Hant.md)

## Avvio rapido in 4 passaggi

1. **Eseguire un backup e concedere l'autorizzazione ai Contatti**: Conservare un backup indipendente e datato prima di pulizie importanti (esportazione `.vcf` facoltativa), attendere il completamento di eventuali trasferimenti del telefono o sincronizzazioni iniziali e consentire l'accesso ai Contatti quando richiesto da iOS.
2. **Scansionare**: Avviare una scansione per individuare i possibili gruppi di duplicati sull'iPhone.
3. **Controllare l'anteprima, scegliere il contatto principale e verificare le Note nell'app Contatti**: Aprire un singolo gruppo di duplicati, esaminare l'anteprima di unione (`Merge Preview`), selezionare il contatto principale da mantenere come scheda di base e controllare nell'app **Contatti** di Apple eventuali note (`Notes`) da salvare.
4. **Ricontrollare e confermare con attenzione**: Se si è passati all'app **Contatti** di Apple per consultare o modificare dei contatti, tornare in ContactMerge+ Cleaner e ricontrollare prima i candidati duplicati attuali e l'anteprima. Confermare solo quando le schede appartengono chiaramente alla stessa persona e l'anteprima mantiene i campi desiderati.

<img src="../../assets/scan-results-demo.png" alt="Demo su simulatore con interfaccia in inglese (schermata non localizzata in italiano, acquisita il 2026-11-03) dei risultati della scansione Duplicate Contacts con contatti fittizi che mostra Undo Last Contact Merge, Ready to merge e Needs review; schermate e diciture possono variare in base alla versione dell'app o di iOS" width="420">

*Demo su simulatore con contatti fittizi (interfaccia in inglese, schermata non localizzata in italiano, acquisita il 2026-11-03). Schermate, layout e diciture possono variare in base alla versione dell'app installata o alla versione di iOS.*

## Limiti di sicurezza fondamentali

- **`Ready to merge` vs. `Needs review`**:
  - `Ready to merge` (pronto per l'unione) indica che ogni coppia di contatti nel gruppo ha superato controlli rigorosi basati su corrispondenze solide tra tutte le coppie. È comunque necessario esaminare sempre l'anteprima prima di confermare: la sola condivisione del nome o del numero di telefono non dimostra che due schede appartengano alla stessa persona.
  - `Needs review` (da verificare) segnala elementi più deboli o discordanti (come un numero di telefono familiare condiviso, nomi diversi, date di compleanno in conflitto o sovrapposizioni parziali). Si tratta di una misura di sicurezza e non di un errore di scansione: esaminare ogni gruppo `Needs review` manualmente, uno alla volta, senza mai unire schede che rappresentano persone diverse.
- **Verificare e salvare le Note nell'app Contatti di Apple prima di unire**:
  - Le note presenti sui contatti non principali (le altre schede che vengono unite) **non** vengono lette né copiate nel contatto principale e non possono essere recuperate in seguito.
  - Poiché ContactMerge+ Cleaner non può leggere il campo delle note, non dare mai per scontato che una scheda sia priva di note solo perché non ne compaiono nell'anteprima di unione. Controllare e copiare le note importanti direttamente nell'app **Contatti** di Apple prima dell'unione; dopo aver consultato o modificato schede in quell'app, tornare in ContactMerge+ Cleaner e ricontrollare i candidati duplicati attuali e l'anteprima prima di confermare (non presupporre che le schermate già aperte si aggiornino automaticamente).
- **Annullamento e recupero sul dispositivo**:
  - `Undo Last Contact Merge` (annulla l'ultima unione di contatti) agisce esclusivamente sulla singola unione più recente (vedere [Backup, annullamento e cronologia di recupero](../it/recovery.md) per la posizione verificata nella schermata e le avvertenze sulle versioni).
  - `Recovery History` (cronologia di recupero) è un registro di recupero salvato localmente dall'app che conserva **al massimo 3 record di unione e al massimo 3 record di eliminazione** per **circa 30 giorni sul dispositivo** (il percorso esatto di navigazione nell'app non è verificato in questa documentazione; vedere [Backup, annullamento e cronologia di recupero](../it/recovery.md)).
  - **Non è un ripristino completo di sistema**: Le note delle schede non principali non possono essere recuperate e gli identificatori di sistema e i collegamenti originali potrebbero non essere ripristinati. Lo sviluppatore non fornisce un servizio di backup su cloud (distinto dalla sincronizzazione iCloud/Google o dai backup di sistema iOS dell'utente, per cui le unioni possono sincronizzarsi tra gli account collegati). In via prudenziale, il recupero non è garantito dopo successive modifiche ai contatti, la disinstallazione dell'app o lo smarrimento del dispositivo.
- **Backup indipendente e sicurezza degli account**: L'esportazione di un file `.vcf` è facoltativa, ma prima della prima pulizia è consigliabile conservare un backup indipendente e datato che copra gli account effettivi in cui risiedono i contatti (la sincronizzazione dell'account non costituisce un backup indipendente). Non eliminare mai i contatti di origine, non toccare `"Delete from My iPhone"` e non disattivare/riattivare o rimuovere account come tentativo di risoluzione dei problemi.

## Versione gratuita (Free) vs. Pro

- **Free**: Consente di scansionare i contatti, visualizzare tutti i gruppi di duplicati e unire un gruppo di duplicati alla volta (fino a 3 contatti all'interno di quel gruppo). L'unione in blocco di più gruppi non è inclusa.
- **Pro**: Sblocco una tantum su App Store senza abbonamento; il prezzo regionale viene mostrato direttamente da Apple. Sblocca i gruppi con più di 3 contatti e l'unione in blocco dei gruppi `Ready to merge` dopo la conferma (i gruppi `Needs review` vanno sempre esaminati singolarmente uno alla volta).
- **Ripristino dell'acquisto e fatturazione**: Per ripristinare un acquisto Pro esistente sullo stesso Apple Account o comprendere la procedura ufficiale di rimborso di Apple (gestita tramite [reportaproblem.apple.com (in inglese)](https://reportaproblem.apple.com); l'idoneità è decisa da Apple, i rimborsi non sono garantiti e lo sviluppatore non può garantirne l'approvazione), consultare le [FAQ](../it/faq.md#q16) o contattare l'[Assistenza ufficiale (in inglese)](https://contactmerge.app/support).

## Guide operative

- [Guida rapida: scansione e unione in sicurezza](../it/quick-start.md)
- [Backup, annullamento e cronologia di recupero](../it/recovery.md)
- [Autorizzazioni e risoluzione dei problemi](../it/permissions-troubleshooting.md)
- [Domande frequenti (FAQ)](../it/faq.md)

## Assistenza ufficiale e privacy

- **Assistenza**: [Assistenza ufficiale (in inglese)](https://contactmerge.app/support)
- **Privacy**: [Informativa sulla privacy (in inglese)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)
- **Avviso su privacy e oscuramento dei dati**: Non condividere mai elenchi di contatti privati, file `.vcf` (vCard), password, dati di pagamento o ricevute d'acquisto in segnalazioni pubbliche. Oscurare tutti i nomi reali, numeri di telefono, indirizzi e-mail, foto, indirizzi postali, note e ID account prima di inviare qualsiasi schermata — utilizzare dati dimostrativi fittizi ogni volta che è possibile.

## Stato della documentazione

Verificato l'8 novembre 2026. Schermate, etichette e funzionamento possono variare in base alla versione dell'app installata e alla versione di iOS.
