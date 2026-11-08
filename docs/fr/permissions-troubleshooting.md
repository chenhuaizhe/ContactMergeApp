# Autorisations et dépannage

- **Présentation et langues** : [Présentation en français](../readme/README.fr.md) | [English Overview](../../README.md)
- **Guides** : [Démarrage rapide](quick-start.md) | [Sauvegarde et récupération](recovery.md) | **Autorisations et dépannage** | [FAQ](faq.md)
- **Langue / Language** : **Français** | [English](../en/permissions-troubleshooting.md)

Ce guide aborde les réglages d'autorisation d'accès aux contacts sur iPhone, les différences entre **ContactMerge+ Cleaner** et les outils intégrés de l'app **Contacts** d'Apple, les précautions à prendre avec les comptes synchronisés et les transferts de téléphone, les questions d'achat et de remboursement, ainsi que la manière de contacter l'assistance en protégeant vos données.

## Autorisation d'accès aux contacts sur iPhone

- **Indispensable pour analyser et fusionner** : ContactMerge+ Cleaner a besoin d'accéder à vos contacts afin de détecter et de fusionner les doublons sur votre iPhone. Le traitement s'effectue localement sur votre appareil — votre carnet d'adresses n'est pas envoyé vers des serveurs du développeur, et le développeur ne propose aucun service de sauvegarde cloud (indépendamment de toute synchronisation iCloud/Google ou sauvegarde système iOS régie par vos propres réglages).
- **Accès complet ou accès limité dans iOS** : Selon votre version d'iOS, Apple vous permet de choisir à quels contacts une application peut accéder — accès complet ou accès limité à certains contacts sélectionnés — dans les réglages de confidentialité d'iOS (`Settings > Privacy & Security > Contacts` ; voir le guide d'Apple : [Control access to Contacts on iPhone (en anglais)](https://support.apple.com/guide/iphone/control-access-to-contacts-iph9536aa9a5/ios)).
- **Si l'analyse est bloquée ou si des contacts semblent manquer** :
  - Vérifiez le niveau d'accès aux contacts accordé à ContactMerge+ Cleaner dans les réglages d'iOS. Un accès incomplet ou limité peut restreindre les fiches visibles par l'application — cela ne **supprime** pas vos contacts, mais la prise en charge de tous les scénarios d'accès limité n'est pas garantie.
  - Si le réglage paraît indisponible ou continue de se comporter de façon inattendue après vérification dans iOS, contactez l'[assistance officielle (en anglais)](https://contactmerge.app/support).
- **À ne jamais faire** : Ne désactivez/réactivez jamais la synchronisation d'un compte, ne retirez aucun compte, ne supprimez pas de contacts et ne réimportez pas de fichiers `.vcf` pour dépanner un problème d'autorisation.

## ContactMerge+ Cleaner vs les outils de doublons intégrés d'Apple

L'app **Contacts** d'Apple comporte ses propres fonctions de détection de doublons et de liaison de fiches, dont le fonctionnement diffère de celui de ContactMerge+ Cleaner (voir le guide d'Apple : [Merge or hide duplicate contacts on iPhone (en anglais)](https://support.apple.com/guide/iphone/merge-or-hide-duplicate-contacts-iph2ab28320d/ios)) :

- **`View Duplicates` dans l'app Contacts d'Apple** : Lorsqu'elle est disponible, l'app d'Apple affiche une mention `View Duplicates` sous votre fiche personnelle (`My Card`) pour examiner et fusionner les doublons détectés. Si cette bannière d'Apple n'apparaît pas — par exemple lorsque des numéros utilisent des formats d'indicatif international différents ou dans certains carnets d'adresses volumineux —, distinguez bien ce comportement du système d'un éventuel problème d'autorisation de l'application. Cette documentation ne formule aucune affirmation quant aux règles internes de détection d'Apple, à un seuil garanti de nombre de contacts (tel que 1 000 fiches), à un délai d'attente fixe ou à une solution globale de type « tout fusionner ».
- **Contacts liés / fiche unifiée vs fiches fusionnées** : Lier manuellement des contacts (`Link Contacts`) dans l'app **Contacts** d'Apple regroupe leur affichage au sein d'une vue unifiée sans fusionner les fiches sources sous-jacentes, et les modifications apportées à une fiche unifiée peuvent se répercuter sur les comptes connectés.
- **Ce qui distingue ContactMerge+ Cleaner** : ContactMerge+ Cleaner effectue une analyse locale sur votre iPhone et classe les candidats entre `Ready to merge` et `Needs review` afin que vous puissiez inspecter un aperçu de fusion au préalable (tout en vérifiant les notes dans l'app **Contacts** d'Apple). L'application ne promet ni vitesse d'analyse déterminée, ni capacité garantie de carnet d'adresses, ni réparation automatique de dommages antérieurs du carnet d'adresses.
- Guides web officiels associés :
  - [iOS View Duplicates and Country Code Formatting (en anglais)](https://contactmerge.app/guides/ios-view-duplicates-country-code)
  - [View Duplicates Missing on a Large Contact List (en anglais)](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list)

## Migration, synchronisation de comptes et prévention des suppressions accidentelles

La configuration d'un nouvel iPhone, l'utilisation de Migrer vers iOS (`Move to iOS`), l'importation de fichiers ou la connexion de plusieurs comptes (tels qu'iCloud et Google) révèlent souvent d'anciens doublons répartis entre plusieurs sources, sans que cela signifie que votre téléphone est défectueux :

- **Attendre la fin de la synchronisation initiale et sauvegarder d'abord** : Patientez jusqu'à l'achèvement de la migration de l'appareil ou de la synchronisation initiale des comptes avant d'évaluer vos doublons (cela ne suffit pas forcément à éliminer les doublons, mais évite toute confusion en cours de synchronisation). Identifiez le compte qui héberge vos contacts et créez une sauvegarde indépendante et datée avant toute modification.
- **Vérifier soigneusement avant de fusionner** : Inspectez les aperçus de fusion (en particulier les groupes `Needs review`) et sauvegardez d'abord dans l'app **Contacts** d'Apple toute note présente sur les fiches secondaires ; si vous quittez l'application pour consulter ou modifier des contacts, revenez et revérifiez les candidats actuels ainsi que l'aperçu avant de confirmer.
- **Prévention impérative de toute suppression** : Retirer un compte de l'app Contacts n'a pas le même effet que supprimer des fiches individuelles, et supprimer des contacts issus d'un compte de messagerie ou cloud synchronisé peut entraîner leur suppression définitive sur tous vos appareils synchronisés (à titre purement informatif, consultez les pages Apple [Add or remove accounts in Contacts on iPhone (en anglais)](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios) et l'[avertissement d'Apple sur la suppression de contacts (en anglais)](https://support.apple.com/en-us/111793)). Ne supprimez **jamais** vos contacts sources, ne touchez pas `"Delete from My iPhone"`, ne coupez/réactivez pas la synchronisation et ne réimportez pas à répétition des fichiers `.vcf` pour gagner du temps — en cas d'hésitation, arrêtez-vous et sollicitez l'[assistance officielle (en anglais)](https://contactmerge.app/support).
- Guides officiels par scénario :
  - [Duplicate Contacts After Setting Up a New iPhone (en anglais)](https://contactmerge.app/guides/duplicate-contacts-after-new-iphone)
  - [Move to iOS Duplicate Contacts (en anglais)](https://contactmerge.app/guides/move-to-ios-duplicate-contacts)
  - [iCloud Duplicate Contacts After Sync (en anglais)](https://contactmerge.app/guides/icloud-duplicate-contacts-after-sync)
  - [Backup Contacts Before Merge on iPhone (en anglais)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)
  - [How to Merge Contacts Safely (en anglais)](https://contactmerge.app/guides/merge-contacts-safely)

## Déblocage Pro, restauration d'achats et remboursements

- **Déblocage unique (sans abonnement)** : Pro est un achat intégré unique non consommable sur l'App Store, dont le prix régional est affiché par Apple — ne suivez **pas** de procédure de résiliation d'abonnement pour cette application. Il débloque les groupes de plus de 3 contacts ainsi que la fusion par lots des groupes `Ready to merge` confirmés (les groupes `Needs review` restent traités un par un).
- **Restaurer un achat Pro** : Vérifiez que votre iPhone est connecté au **même compte Apple** que celui utilisé lors de l'achat initial et consultez le guide officiel d'Apple : [If you can't find or use your in-app purchases (en anglais)](https://support.apple.com/en-us/108096). Comme l'emplacement exact du bouton de restauration dans l'application n'est pas vérifié dans cette documentation, nous ne devinons pas d'intitulés de menu, ne recommandons pas de racheter Pro et ne garantissons pas une restauration automatique — si la restauration échoue, contactez l'[assistance officielle (en anglais)](https://contactmerge.app/support) ou l'assistance Apple.
- **Demandes de remboursement** : Apple gère la facturation de l'App Store et détermine l'éligibilité au remboursement selon le pays ou la région. Certains achats peuvent donner lieu à un remboursement, que vous pouvez demander via la procédure officielle d'Apple sur [reportaproblem.apple.com (en anglais)](https://reportaproblem.apple.com) (voir le guide d'Apple [Request a refund for apps or content that you bought from Apple (en anglais)](https://support.apple.com/en-us/118223)) ; **les remboursements ne sont pas garantis**, et le développeur ne garantit pas leur approbation.

## Contacter l'assistance et protéger votre confidentialité

- **Assistance** : [Assistance officielle (en anglais)](https://contactmerge.app/support)
- **Informations utiles et sûres à communiquer** : Votre version de ContactMerge+ Cleaner, votre version d'iOS, le résultat attendu par rapport à ce que vous avez constaté, si l'écran concerné est un réglage système Apple ou un écran interne à ContactMerge+ Cleaner, le type de compte impliqué (par exemple iCloud ou Google, **sans** votre adresse e-mail ni votre identifiant de compte) et, si utile, un ordre de grandeur du nombre de contacts.
- **Règles strictes de confidentialité et de masquage** :
  - N'envoyez jamais de listes de contacts privées, de fichiers `.vcf` (vCard), de mots de passe, de données de paiement ni de reçus d'achat dans des signalements publics (traitez tout élément de facturation uniquement via les canaux officiels sécurisés d'Apple ou un canal privé approprié de l'assistance officielle si nécessaire).
  - Masquez systématiquement les vrais noms, numéros de téléphone, adresses e-mail, photos, adresses postales, notes et identifiants avant de partager une capture d'écran — privilégiez chaque fois que possible des données fictives de démonstration.

## Liens utiles

- [Démarrage rapide : analyser et fusionner vos contacts en toute sécurité](quick-start.md)
- [Sauvegarde, annulation et historique de récupération](recovery.md)
- [Foire aux questions (FAQ)](faq.md)
- [Site officiel (en anglais)](https://contactmerge.app)
- [Politique de confidentialité (en anglais)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## État de la documentation

Vérifié le 8 novembre 2026. Les écrans, intitulés et comportements peuvent varier selon la version installée de l'application et votre version d'iOS.
