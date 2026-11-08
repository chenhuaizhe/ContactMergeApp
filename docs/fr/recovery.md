# Sauvegarde, annulation et historique de récupération

- **Présentation et langues** : [Présentation en français](../readme/README.fr.md) | [English Overview](../../README.md)
- **Guides** : [Démarrage rapide](quick-start.md) | **Sauvegarde et récupération** | [Autorisations et dépannage](permissions-troubleshooting.md) | [FAQ](faq.md)
- **Langue / Language** : **Français** | [English](../en/recovery.md)

Ce guide présente les bonnes pratiques de sauvegarde avant une fusion, le fonctionnement de l'annulation et de la récupération locales dans **ContactMerge+ Cleaner**, ainsi que les limites à connaître avant de fusionner des contacts.

## Sauvegarde indépendante avant de fusionner

- **Export `.vcf` facultatif** : L'export d'un fichier `.vcf` (vCard) est facultatif — ContactMerge+ Cleaner ne vous impose pas d'exporter un fichier avant de procéder à une fusion.
- **Sauvegarde indépendante et datée recommandée** : Conserver une sauvegarde indépendante et datée avant de fusionner est vivement conseillé, surtout avant un premier nettoyage ou une fusion par lots. Le développeur ne fournit aucun service de sauvegarde cloud, et ContactMerge+ Cleaner n'exporte pas automatiquement de fichiers de sauvegarde externes.
- **Vérifier le périmètre de votre sauvegarde** : Assurez-vous que votre sauvegarde couvre bien le compte source qui héberge réellement vos contacts (par exemple iCloud ou Google, et non un compte vide) et qu'elle contient le nombre de fiches ainsi que les détails attendus. La synchronisation de compte ne constitue pas une sauvegarde indépendante, car les modifications effectuées lors du nettoyage peuvent se synchroniser sur vos autres appareils connectés.
- **Éviter les tentatives de restauration destructrices** : Ne réimportez pas à répétition des fichiers `.vcf` et n'effectuez pas une restauration complète de l'appareil à l'aveugle pour corriger un simple problème de contacts — vous risqueriez de multiplier les doublons ou d'écraser des modifications récentes.
- **Pour aller plus loin** : Consultez [Backup Contacts Before Merge on iPhone (en anglais)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone) et [How to Merge Contacts Safely (en anglais)](https://contactmerge.app/guides/merge-contacts-safely).

## Vérifier et conserver les notes dans l'app Contacts d'Apple

Les notes (`Notes`) importantes présentes sur les fiches secondaires (les autres fiches fusionnées dans le contact principal) ne sont **ni** lues **ni** copiées lors d'une fusion. Avant de confirmer toute fusion :

- **Inspecter les notes dans l'app Contacts d'Apple, et non dans l'aperçu** : ContactMerge+ Cleaner ne peut pas lire les notes des contacts. Ne supposez jamais qu'une fiche est dépourvue de notes simplement parce qu'aucune n'apparaît dans l'aperçu de ContactMerge+ Cleaner — ouvrez l'app **Contacts** d'Apple pour vérifier ces fiches et copiez manuellement toute note importante dans le contact principal (ou en lieu sûr) avant de fusionner.
- **Revérifier après avoir quitté l'application** : Si vous quittez ContactMerge+ Cleaner pour consulter ou modifier des fiches dans l'app **Contacts** d'Apple, revenez ensuite dans l'application et revérifiez les doublons proposés ainsi que l'aperçu de fusion avant de confirmer. Ne supposez pas qu'une liste de candidats ou un aperçu déjà ouvert s'actualise ou déclenche automatiquement une nouvelle analyse.
- **Impossible de récupérer les notes ultérieurement** : Comme ContactMerge+ Cleaner ne peut pas lire les notes, celles des fiches secondaires ne peuvent être rétablies ni via `Undo Last Contact Merge` ni via `Recovery History`.

## Annuler ou récupérer des modifications récentes dans l'application

ContactMerge+ Cleaner propose deux fonctions de récupération locale sur l'appareil, dont la portée est strictement délimitée :

- **`Undo Last Contact Merge` (annuler la dernière fusion)** :
  - Vise exclusivement la toute dernière fusion individuelle effectuée.
  - **Emplacement vérifié à l'écran** : Pour rechercher cette commande d'annulation après votre dernière fusion, ouvrez l'écran des résultats d'analyse `Duplicate Contacts` (ou revenez-y) et regardez en haut de l'écran, au-dessus de la section `Ready to merge`, où figure `Undo Last Contact Merge`.
  - **Réserves de vérification et de version** : Cet emplacement est vérifié d'après la capture sur simulateur de la version anglaise Release datée du `2026-11-03`, et non à partir d'un test en conditions réelles sur votre version installée. Les intitulés et la disposition peuvent varier selon la version de l'application ou d'iOS ; ce guide ne garantit pas à quel moment la commande est active au cours de votre session, n'affirme pas que l'annulation de bout en bout a été testée en direct sur votre version, ne promet pas l'inversion de chaque propriété sous-jacente du contact et ne présume d'aucune boîte de dialogue de confirmation particulière.
- **`Recovery History` (historique de récupération)** :
  - S'appuie sur un journal de récupération enregistré localement par l'application sur votre iPhone.
  - Conserve **au maximum 3 enregistrements de fusion et au maximum 3 enregistrements de suppression** (il s'agit de plafonds distincts par type d'opération, et non d'une garantie que 6 enregistrements soient disponibles à tout moment).
  - Les entrées demeurent sur l'appareil pendant **environ 30 jours** ; les entrées plus anciennes ou celles qui dépassent le plafond de 3 enregistrements pour ce type d'action ne peuvent plus être récupérées.
  - **Chemin de navigation non vérifié** : Le point d'entrée, le chemin de navigation à l'écran et les étapes de sélection d'un enregistrement pour `Recovery History` ne figurent pas dans les captures d'écran approuvées ; ce guide signale donc le chemin d'accès actuel comme non vérifié plutôt que de deviner des intitulés de menu pour votre version installée. Si vous ne trouvez pas `Recovery History`, veuillez contacter l'[assistance officielle (en anglais)](https://contactmerge.app/support).

## Limites importantes de la récupération sur l'appareil

Gardez à l'esprit ce que `Undo Last Contact Merge` et `Recovery History` ne permettent **pas** :

- **Pas une restauration complète du système** : Les notes des fiches secondaires ne peuvent ni être lues ni être récupérées, et les identifiants système ainsi que les liens de contacts d'origine peuvent ne pas être rétablis. L'application ne garantit pas non plus la réparation de dommages antérieurs arbitraires causés à votre carnet d'adresses par d'autres outils ou importations.
- **Aucune sauvegarde cloud du développeur ; séparation vis-à-vis de la synchronisation et des sauvegardes système** :
  - Le traitement des contacts et le journal de récupération restent localement dans l'application sur votre iPhone ; le développeur n'envoie pas votre carnet d'adresses vers ses serveurs et ne fournit aucun service de sauvegarde cloud.
  - **La synchronisation de compte et les sauvegardes iOS sont indépendantes** : la synchronisation des contacts via iOS ou un compte (comme iCloud ou Google) et les sauvegardes système ou de l'appareil sont des mécanismes séparés, gérés par vos propres réglages de compte et d'iOS. Cette documentation ne promet **pas** qu'une fusion restera à l'écart de la synchronisation iCloud/Google, et ne prend **aucun** engagement quant à l'inclusion ou à l'exclusion des données de l'application dans les sauvegardes système.
  - La récupération n'est pas garantie si vous désinstallez l'application, ou si vous perdez ou remplacez votre iPhone.
- **Prudence en cas de modification ultérieure des contacts** : À titre de précaution — et non comme un blocage strict vérifié dans l'application —, la récupération ne peut pas être garantie si les fiches concernées ont été modifiées ou écrasées par synchronisation entre-temps (dans l'app **Contacts** d'Apple, une autre application, sur un autre appareil ou via la synchronisation de compte). Évitez de modifier des fiches fusionnées tant que vous envisagez encore d'annuler cette fusion.
- **Ne jamais dépanner en supprimant des contacts sources ou en retirant des comptes** : La suppression de contacts hébergés sur un compte de messagerie ou cloud synchronisé peut les effacer définitivement sur l'ensemble de vos appareils (voir l'[avertissement d'Apple sur la suppression de contacts (en anglais)](https://support.apple.com/en-us/111793) et le [guide Apple de gestion des comptes (en anglais)](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios)). Ne touchez pas `"Delete from My iPhone"`, ne désactivez/réactivez pas la synchronisation d'un compte et ne retirez pas de compte pour tenter de résoudre un problème de fusion — en cas de doute, arrêtez-vous et contactez d'abord l'assistance.

## Contacter l'assistance en toute sécurité

- Écrivez à l'[assistance officielle (en anglais)](https://contactmerge.app/support) en précisant votre version de ContactMerge+ Cleaner, votre version d'iOS, si vous observez un écran de l'app **Contacts** d'Apple ou de ContactMerge+ Cleaner, le type de compte concerné (par exemple iCloud ou Google, sans communiquer l'identifiant du compte), ainsi que le comportement attendu par rapport à ce qui s'est produit.
- **Protéger votre vie privée** : Ne publiez jamais de listes de contacts, de fichiers `.vcf`, de mots de passe, d'informations de paiement ni de reçus d'achat dans des signalements publics. Masquez tous les vrais noms, numéros de téléphone, adresses e-mail, photos, adresses postales, notes et identifiants avant de transmettre une capture d'écran — ou utilisez exclusivement des données fictives de démonstration.

## Liens utiles

- [Démarrage rapide : analyser et fusionner vos contacts en toute sécurité](quick-start.md)
- [Autorisations et dépannage](permissions-troubleshooting.md)
- [Foire aux questions (FAQ)](faq.md)
- [Site officiel (en anglais)](https://contactmerge.app)
- [Politique de confidentialité (en anglais)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## État de la documentation

Vérifié le 8 novembre 2026. Les écrans, intitulés et comportements peuvent varier selon la version installée de l'application et votre version d'iOS.
