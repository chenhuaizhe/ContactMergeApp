# Foire aux questions (FAQ)

- **Présentation et langues** : [Présentation en français](../readme/README.fr.md) | [English Overview](../../README.md)
- **Guides** : [Démarrage rapide](quick-start.md) | [Sauvegarde et récupération](recovery.md) | [Autorisations et dépannage](permissions-troubleshooting.md) | **FAQ**
- **Langue / Language** : **Français** | [English](../en/faq.md)

Réponses pratiques pour utiliser **ContactMerge+ Cleaner** en toute sécurité sur iPhone, avec rappel des comportements vérifiés et des limites liées aux versions.

## Sauvegardes et détection des doublons (`q01`–`q06`)

<a id="q01"></a>
### 1. Faut-il créer une sauvegarde `.vcf` avant de fusionner, ou `Recovery History` suffit-il ?

L'export d'un fichier `.vcf` est facultatif — l'application n'impose aucun export avant une fusion —, mais conserver une sauvegarde indépendante et datée avant votre premier nettoyage ou une opération importante est vivement recommandé. `Recovery History` n'est qu'un journal local limité sur l'appareil (au maximum 3 enregistrements de fusion et au maximum 3 enregistrements de suppression pendant environ 30 jours), ne peut pas rétablir les notes des fiches secondaires et ne repose sur aucune sauvegarde cloud du développeur. La synchronisation de compte (iCloud ou Google) ne remplace pas une sauvegarde indépendante, car les fusions peuvent se répercuter sur vos autres appareils. Vérifiez que votre sauvegarde couvre bien le compte où sont stockés vos contacts ainsi que les fiches attendues, et évitez les réimportations répétées de fichiers `.vcf` ou les restaurations complètes de l'appareil à l'aveugle. Consultez [Sauvegarde et récupération](recovery.md) et [Backup Contacts Before Merge on iPhone (en anglais)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone).

<a id="q02"></a>
### 2. Que signifie `Ready to merge`, et dois-je quand même vérifier l'aperçu ?

`Ready to merge` (prêt à fusionner) indique que chaque paire de fiches au sein du groupe a passé des contrôles stricts appuyés sur des indices solides entre toutes les paires. Ouvrez malgré tout l'aperçu de fusion (`Merge Preview`) avant de confirmer : un nom ou un numéro identique ne suffit pas, à lui seul, à prouver que deux fiches désignent la même personne, et l'application ne peut pas lire les notes des contacts. Sélectionnez votre fiche principale, vérifiez dans l'app **Contacts** d'Apple si les fiches secondaires contiennent des notes à conserver, contrôlez les champs attendus dans l'aperçu, puis confirmez (ou incluez les groupes `Ready to merge` dans une fusion par lots Pro confirmée). Voir [Démarrage rapide](quick-start.md) et [How to Merge Contacts Safely (en anglais)](https://contactmerge.app/guides/merge-contacts-safely).

<a id="q03"></a>
### 3. Pourquoi un groupe est-il classé dans `Needs review`, et puis-je le fusionner par lots ?

`Needs review` (à vérifier) signale des indices plus faibles ou contradictoires — par exemple un numéro fixe du foyer partagé, des noms différents, des dates d'anniversaire divergentes ou un recoupement partiel. Il s'agit d'un contrôle de sécurité et non d'une erreur d'analyse. Les groupes `Needs review` requièrent un examen manuel individuel et ne sont pas éligibles à la fusion par lots Pro : ne forcez pas la fusion de fiches incertaines et, en cas de doute, laissez les fiches séparées. Voir [Démarrage rapide](quick-start.md).

<a id="q04"></a>
### 4. Faut-il fusionner lorsque les noms diffèrent — ou lorsque deux fiches portent exactement le même nom ?

Rien n'est automatique dans un cas comme dans l'autre. Une différence de nom (comme un diminutif face au nom complet) n'implique pas forcément deux personnes distinctes, tandis que deux fiches portant exactement le même nom peuvent appartenir à deux proches ou collègues homonymes. Cette documentation ne revendique aucune règle exacte de casse ou de normalisation de texte lors du rapprochement. Dans l'aperçu, comparez les informations qui y sont effectivement affichées (telles que les noms, numéros de téléphone et adresses e-mail lorsqu'ils sont présents) — ne supposez jamais qu'un champ ou une note est vide sur la fiche contact simplement parce qu'il n'apparaît pas dans l'aperçu. Ouvrez les fiches d'origine dans l'app **Contacts** d'Apple pour vérifier l'entreprise ou l'employeur, d'autres détails d'identité complémentaires ainsi que les notes à conserver ; si vous quittez l'application pour consulter ou modifier des fiches, revenez et revérifiez les candidats actuels ainsi que l'aperçu avant de confirmer (ne présumez pas que les vues ouvertes s'actualisent automatiquement). Voir [Démarrage rapide](quick-start.md).

<a id="q05"></a>
### 5. Deux personnes différentes partagent un numéro de domicile ou de bureau. Que faire ?

Ne les fusionnez **pas**. Des membres d'une même famille partageant une ligne fixe, des conjoints partageant un numéro d'urgence ou des collègues partageant un standard apparaissent souvent parmi les candidats — généralement sous `Needs review`. Une fusion regrouperait deux personnes distinctes sur une seule fiche. Laissez ces fiches séparées et ne confirmez que lorsque chaque fiche du groupe représente bien la même personne. Voir [Démarrage rapide](quick-start.md).

<a id="q06"></a>
### 6. Pourquoi des dates d'anniversaire contradictoires signalent-elles un groupe à vérifier ?

Des dates d'anniversaire divergentes d'une fiche à l'autre (mentionnées dans l'historique des notes de version 1.3.6 et d'assistance aux côtés des conflits de noms) constituent un repère concret invitant à une vérification manuelle, et non un seuil d'algorithme publié au détail près. Des dates différentes peuvent révéler deux proches partageant des coordonnées ou une erreur de saisie ancienne. Examinez les deux fiches dans l'aperçu ainsi que dans l'app **Contacts** d'Apple avant de décider. Voir [Démarrage rapide](quick-start.md).

## Comptes, transferts et app Contacts d'Apple (`q07`–`q11`)

<a id="q07"></a>
### 7. Comment l'application fonctionne-t-elle avec la synchronisation iCloud ou Google ?

Les contacts sont traités localement sur votre iPhone : votre carnet d'adresses n'est pas envoyé vers des serveurs du développeur et il n'existe aucun service de sauvegarde cloud du développeur. Toutefois, la synchronisation iCloud/Google et les sauvegardes système iOS restent des mécanismes indépendants gérés par vos réglages ; les fusions confirmées peuvent donc se synchroniser sur vos appareils connectés. Ne coupez/réactivez jamais la synchronisation, ne retirez aucun compte, ne touchez pas `"Delete from My iPhone"` et ne supprimez jamais de contacts sources synchronisés pour dépanner — supprimer des contacts d'un compte mail ou cloud peut les effacer définitivement sur tous vos appareils (voir le [guide des comptes d'Apple (en anglais)](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios) et l'[avertissement d'Apple sur la suppression (en anglais)](https://support.apple.com/en-us/111793)). Identifiez d'abord votre compte et faites une sauvegarde ; en cas de doute, arrêtez-vous et contactez l'[assistance officielle (en anglais)](https://contactmerge.app/support). Voir [iCloud Duplicate Contacts After Sync (en anglais)](https://contactmerge.app/guides/icloud-duplicate-contacts-after-sync).

<a id="q08"></a>
### 8. Pourquoi des doublons sont-ils apparus après la configuration d'un nouvel iPhone ou Migrer vers iOS ?

Configurer un nouvel iPhone, utiliser Migrer vers iOS (`Move to iOS`), importer des fichiers ou connecter plusieurs comptes met souvent en évidence d'anciens doublons présents entre différentes sources — cela ne signifie pas que votre téléphone présente un défaut et ne prouve pas une cause unique garantie. Laissez la migration et la synchronisation initiale en arrière-plan se terminer avant d'analyser (cela ne suffit pas nécessairement à éliminer les doublons, mais évite des changements en cours de synchronisation), créez une sauvegarde indépendante, puis examinez les aperçus selon le [Démarrage rapide](quick-start.md). Consultez [Duplicate Contacts After Setting Up a New iPhone (en anglais)](https://contactmerge.app/guides/duplicate-contacts-after-new-iphone) et [Move to iOS Duplicate Contacts (en anglais)](https://contactmerge.app/guides/move-to-ios-duplicate-contacts).

<a id="q09"></a>
### 9. La mention `View Duplicates` d'Apple n'apparaît pas — en quoi ContactMerge+ Cleaner diffère-t-il ?

Dans l'app **Contacts** d'Apple, `View Duplicates` s'affiche sous `My Card` lorsqu'elle est disponible, tandis que la liaison manuelle `Link Contacts` unifie l'affichage sans fusionner les fiches sources sous-jacentes (et les modifications d'une fiche unifiée peuvent se propager aux comptes sources ; voir le [guide d'Apple sur les doublons (en anglais)](https://support.apple.com/guide/iphone/merge-or-hide-duplicate-contacts-iph2ab28320d/ios)). L'absence de `View Duplicates` est indépendante des autorisations de l'application — il n'existe ni seuil garanti de 1 000 contacts, ni temps d'attente fixe, ni solution sûre consistant à tout fusionner d'un bloc. Autorisez l'accès aux contacts dans ContactMerge+ Cleaner pour lancer une analyse locale et vérifier chaque aperçu. Voir [Autorisations et dépannage](permissions-troubleshooting.md).

<a id="q10"></a>
### 10. Deux doublons peuvent-ils avoir le même numéro avec et sans indicatif international ?

Oui : une fiche peut enregistrer un numéro au format national tandis qu'une autre inclut un indicatif pays (comme `+33` ou `+1`), ce que la détection intégrée d'Apple ne signale pas toujours comme une correspondance exacte. Sans revendiquer de règles précises de normalisation téléphonique, ContactMerge+ Cleaner vous permet de comparer les numéros complets dans l'aperçu de fusion (`Merge Preview`). Vérifiez que les deux fiches concernent bien la même personne et qu'elles conservent le format souhaité avant de confirmer. Voir [iOS View Duplicates and Country Code Formatting (en anglais)](https://contactmerge.app/guides/ios-view-duplicates-country-code).

<a id="q11"></a>
### 11. ContactMerge+ Cleaner prend-il en charge les grands carnets d'adresses ?

Vous pouvez analyser localement un carnet d'adresses volumineux même lorsque `View Duplicates` d'Apple ne s'affiche pas, en examinant les résultats répartis entre `Ready to merge` et `Needs review`. En revanche, l'application ne promet ni vitesse d'analyse particulière ni capacité illimitée. Laissez d'abord la synchronisation en arrière-plan s'achever, créez une sauvegarde indépendante et datée, puis testez la fusion sur un seul groupe avant d'aller plus loin. Voir [Autorisations et dépannage](permissions-troubleshooting.md) et [View Duplicates Missing on a Large Contact List (en anglais)](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list).

## Annulation, historique de récupération et notes de contacts (`q12`–`q14`)

<a id="q12"></a>
### 12. Où se trouve `Undo Last Contact Merge`, et que couvre cette annulation ?

`Undo Last Contact Merge` (annuler la dernière fusion de contacts) porte uniquement sur la toute dernière fusion individuelle effectuée. Sur la capture approuvée du simulateur Release en anglais datée du `2026-11-03`, cette commande apparaît en haut de l'écran des résultats `Duplicate Contacts`, au-dessus de `Ready to merge`. Comme cette indication repose sur cette capture datée et non sur un test en direct de votre version installée, l'état d'activation, les libellés et les messages peuvent varier, et il ne s'agit pas d'une restauration complète (les notes des fiches secondaires ne peuvent pas être récupérées et les identifiants ou liens système d'origine peuvent ne pas revenir). Voir [Sauvegarde et récupération](recovery.md).

<a id="q13"></a>
### 13. Quelles sont les limites de `Recovery History`, et comment y accéder ?

`Recovery History` (historique de récupération) enregistre **au maximum 3 enregistrements de fusion et au maximum 3 enregistrements de suppression** pendant **environ 30 jours sur votre appareil** (plafonds séparés, et non 6 enregistrements garantis). Les entrées plus anciennes ou au-delà du plafond ne peuvent pas être récupérées, et aucune récupération n'est garantie après désinstallation de l'application ou perte de l'appareil. **Chemin non vérifié** : son point d'entrée et les étapes de sélection d'un enregistrement ne figurent pas dans les captures approuvées ; nous ne devinons donc aucun chemin de menu — contactez l'[assistance officielle (en anglais)](https://contactmerge.app/support) pour obtenir de l'aide sur votre version. Voir [Sauvegarde et récupération](recovery.md).

<a id="q14"></a>
### 14. Pourquoi vérifier les notes dans l'app Contacts d'Apple — et quelles autres limites s'appliquent à la récupération ?

ContactMerge+ Cleaner ne peut pas lire les notes des contacts (`Notes`) : celles des fiches secondaires ne sont **pas** copiées lors des fusions et ne peuvent être rétablies ni via `Undo Last Contact Merge` ni via `Recovery History`. L'absence de notes dans l'aperçu ne signifie jamais qu'une fiche n'en contient pas — inspectez-les et copiez-les d'abord dans l'app **Contacts** d'Apple. Après avoir consulté ou modifié des fiches en dehors de l'application, revenez et revérifiez les candidats actuels ainsi que l'aperçu (les vues ouvertes peuvent ne pas s'actualiser automatiquement). Les identifiants et liens système peuvent ne pas être rétablis et, par précaution, des modifications ou synchronisations ultérieures peuvent empêcher une récupération propre. Voir [Sauvegarde et récupération](recovery.md).

## Free vs Pro, achats et assistance (`q15`–`q18`)

<a id="q15"></a>
### 15. Quelle est la différence entre la version gratuite (Free) et Pro ?

La version **Free** permet d'analyser votre carnet d'adresses, d'afficher tous les groupes de candidats et de fusionner un groupe à la fois comprenant jusqu'à 3 contacts dans ce groupe (sans fusion par lots multi-groupes). **Pro** est un déblocage unique sur l'App Store, **sans abonnement**, au tarif régional affiché par Apple. Pro débloque les groupes de plus de 3 contacts ainsi que la fusion par lots des groupes `Ready to merge` confirmés (les groupes `Needs review` restent examinés un par un). Voir [Démarrage rapide](quick-start.md).

<a id="q16"></a>
### 16. Comment restaurer mon achat Pro ?

Pro est un achat intégré non consommable. Vérifiez que votre iPhone utilise le **même compte Apple** que lors de l'achat initial et consultez le guide d'Apple : [If you can't find or use your in-app purchases (en anglais)](https://support.apple.com/en-us/108096). Comme le chemin exact du bouton de restauration dans l'interface de l'application n'est pas vérifié ici, nous ne devinons pas les intitulés de menu (`Settings` / `Upgrade`), ne conseillons pas de racheter Pro et ne garantissons pas une restauration automatique. Si Pro demeure verrouillé, contactez l'[assistance officielle (en anglais)](https://contactmerge.app/support) ou l'assistance Apple. Voir [Autorisations et dépannage](permissions-troubleshooting.md).

<a id="q17"></a>
### 17. Comment fonctionnent les remboursements Apple — et y a-t-il un abonnement à résilier ?

Pro est un achat unique et non un abonnement — ne suivez pas les instructions de résiliation d'abonnement pour cette application. Apple gère la facturation de l'App Store et décide de l'éligibilité au remboursement selon le pays ou la région ; **les remboursements ne sont pas garantis**. Vous pouvez déposer une demande via la procédure officielle d'Apple sur [reportaproblem.apple.com (en anglais)](https://reportaproblem.apple.com) (voir le [guide de remboursement d'Apple (en anglais)](https://support.apple.com/en-us/118223)) ; le développeur ne garantit pas son approbation. Voir [Autorisations et dépannage](permissions-troubleshooting.md).

<a id="q18"></a>
### 18. Comment vérifier les autorisations, protéger ma vie privée et contacter l'assistance en toute sécurité ?

Vérifiez dans iOS `Settings > Privacy & Security > Contacts` (voir le [guide d'Apple sur l'accès aux contacts (en anglais)](https://support.apple.com/guide/iphone/control-access-to-contacts-iph9536aa9a5/ios)) ; un accès limité restreint uniquement la visibilité dans l'application sans supprimer vos fiches, bien que tous les flux d'accès limité ne soient pas garantis. Le traitement est local, sans envoi vers des serveurs du développeur (indépendamment de votre synchronisation iCloud/Google et de vos sauvegardes iOS ; voir la [Politique de confidentialité (en anglais)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)). Pour l'[assistance officielle (en anglais)](https://contactmerge.app/support), indiquez vos versions de l'application et d'iOS, s'il s'agit d'un réglage Apple ou d'un écran de l'application, le type de compte (sans identifiant de compte), un nombre approximatif de contacts et le comportement attendu par rapport à celui constaté — ne publiez jamais de listes de contacts, fichiers `.vcf`, données personnelles réelles, mots de passe ou reçus de paiement publiquement. Voir [Autorisations et dépannage](permissions-troubleshooting.md).

## État de la documentation

Vérifié le 8 novembre 2026. Les écrans, intitulés et comportements peuvent varier selon la version installée de l'application et votre version d'iOS.
