# Démarrage rapide : analyser et fusionner vos contacts en toute sécurité

- **Présentation et langues** : [Présentation en français](../readme/README.fr.md) | [English Overview](../../README.md)
- **Guides** : **Démarrage rapide** | [Sauvegarde et récupération](recovery.md) | [Autorisations et dépannage](permissions-troubleshooting.md) | [FAQ](faq.md)
- **Langue / Language** : **Français** | [English](../en/quick-start.md)

Ce guide explique comment rechercher, vérifier et fusionner des contacts en double sur votre iPhone avec **ContactMerge+ Cleaner**.

ContactMerge+ Cleaner traite vos contacts localement sur votre appareil, n'envoie pas votre carnet d'adresses vers des serveurs du développeur et ne fournit aucun service de sauvegarde cloud du développeur. (La synchronisation des contacts via iOS ou vos comptes — comme iCloud ou Google — ainsi que les sauvegardes système ou de l'appareil constituent des mécanismes distincts, régis par les réglages de vos propres comptes et d'iOS.) Les informations sur le produit et le téléchargement sont disponibles sur le [site officiel (en anglais)](https://contactmerge.app).

## Avant de commencer

- **Créer une sauvegarde indépendante et datée (recommandé)** : L'export d'un fichier `.vcf` (vCard) est facultatif — l'application ne vous oblige pas à en exporter un avant de fusionner —, mais il est vivement recommandé de conserver une sauvegarde indépendante et datée, en particulier avant votre premier nettoyage. Assurez-vous que cette sauvegarde couvre bien les comptes où se trouvent réellement vos contacts et qu'elle contient les fiches attendues. La synchronisation de compte (comme iCloud ou Google) ne remplace pas une sauvegarde indépendante, car les fusions peuvent se répercuter sur vos autres appareils connectés. Consultez [Sauvegarde, annulation et historique de récupération](recovery.md) ainsi que le guide [Backup Contacts Before Merge on iPhone (en anglais)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone).
- **Laisser se terminer les transferts et synchronisations initiales** : Si vous venez de configurer un nouvel iPhone, d'utiliser Migrer vers iOS (`Move to iOS`) ou d'ajouter un compte de messagerie ou cloud, patientez jusqu'à la fin complète de la synchronisation en arrière-plan avant d'analyser et de fusionner (attendre évite d'intervenir en plein milieu d'une synchronisation, même si cela ne garantit pas en soi la disparition des doublons existants).

## Procédure de fusion étape par étape

1. **Autoriser l'accès aux contacts** : Accordez l'autorisation d'accès aux contacts lorsque iOS vous y invite. Si aucune invite n'apparaît ou si la liste semble incomplète, consultez [Autorisations et dépannage](permissions-troubleshooting.md).
2. **Analyser votre carnet d'adresses** : Lancez une analyse dans ContactMerge+ Cleaner pour afficher les groupes de doublons proposés.
3. **Ouvrir un groupe et examiner l'aperçu** : Touchez un groupe de doublons, inspectez l'aperçu de fusion (`Merge Preview`) et choisissez la fiche qui doit être conservée comme contact principal (fiche de base).
4. **Vérifier les notes dans l'app Contacts d'Apple et contrôler les champs avant de confirmer** :
   - Les notes (`Notes`) importantes présentes sur les fiches secondaires (les autres fiches qui seront fusionnées) ne sont **ni** lues **ni** copiées vers le contact principal, et ne pourront pas être récupérées ultérieurement.
   - **Vérifier les notes dans l'app Contacts d'Apple, et non dans l'aperçu** : ContactMerge+ Cleaner ne peut pas lire les notes des contacts. Ne concluez jamais à l'absence de notes sur une fiche simplement parce qu'aucune n'apparaît dans l'aperçu de ContactMerge+ Cleaner — ouvrez l'app **Contacts** d'Apple pour inspecter ces fiches et copiez manuellement toute note importante dans le contact principal avant de fusionner.
   - **Revérifier après toute consultation ou modification externe** : Si vous quittez ContactMerge+ Cleaner pour consulter ou modifier des fiches dans l'app **Contacts** d'Apple, revenez ensuite dans l'application et revérifiez les doublons proposés ainsi que l'aperçu de fusion avant de confirmer. Ne supposez pas qu'une liste de candidats ou un aperçu déjà ouvert s'actualise ou relance une analyse automatiquement.
   - **Contrôler l'identité et les champs attendus** : Confirmez la fusion uniquement lorsque les fiches correspondent sans ambiguïté à la même personne dans la vie réelle et que l'aperçu conserve les champs souhaités.

### Exemple : résultats d'analyse et aperçu de fusion

<img src="../../assets/scan-results-demo.png" alt="Démo sur simulateur avec interface en anglais (capture non localisée en français, prise le 2026-11-03) des résultats d'analyse Duplicate Contacts avec des contacts fictifs montrant Undo Last Contact Merge, Ready to merge et Needs review ; les écrans et libellés peuvent varier selon la version de l'application ou d'iOS" width="420">

*Résultats d'analyse — Démo sur simulateur avec des contacts fictifs (interface en anglais — capture non localisée en français — prise le 2026-11-03). Les écrans, la disposition et les libellés peuvent varier selon la version installée de l'application ou votre version d'iOS.*

<img src="../../assets/merge-preview-demo.png" alt="Démo sur simulateur avec interface en anglais (capture non localisée en français, prise le 2026-11-03) de l'écran Merge Preview avec des contacts fictifs montrant les motifs de rapprochement, l'avertissement Check and preserve notes in Contacts et le choix du contact principal, tandis que la deuxième ligne de contact se trouve sous la zone visible de défilement ; les écrans et libellés peuvent varier selon la version de l'application ou d'iOS" width="420">

*Aperçu de fusion et choix du contact principal — Démo sur simulateur avec des contacts fictifs (interface en anglais — capture non localisée en français — prise le 2026-11-03 ; la deuxième ligne de contact se situe sous la zone visible de défilement, de sorte que les deux fiches ne sont pas visibles simultanément). Les écrans, la disposition et les libellés peuvent varier selon la version installée de l'application ou votre version d'iOS.*

## Comprendre le classement des groupes : `Ready to merge` vs `Needs review`

ContactMerge+ Cleaner répartit les groupes de doublons potentiels en deux sections selon les indices de concordance disponibles (cette documentation décrit de bonnes pratiques de vérification et ne revendique aucun seuil interne exact d'exécution ni aucune règle précise de normalisation) :

- **`Ready to merge` (prêt à fusionner)** :
  - Chaque paire de fiches du groupe a satisfait à des vérifications strictes fondées sur des indices solides entre toutes les paires.
  - **L'aperçu reste indispensable** : partager un nom ou un numéro de téléphone ne prouve pas, à soi seul, que deux fiches désignent la même personne. Examinez toujours l'aperçu et vérifiez la présence éventuelle de notes dans l'app **Contacts** d'Apple avant de confirmer.
  - Éligible à la fusion par lots dans la version Pro après votre confirmation.
- **`Needs review` (à vérifier)** :
  - Les fiches présentent des indices plus faibles ou contradictoires — par exemple un numéro de téléphone domestique ou professionnel partagé, des variantes de nom, des dates d'anniversaire divergentes ou un recoupement partiel.
  - Le classement dans `Needs review` constitue un garde-fou prudent et non une erreur d'analyse : une différence de nom ne signifie pas automatiquement qu'il s'agit de deux personnes distinctes, tandis qu'un numéro partagé ou un nom identique peut tout à fait appartenir à deux membres d'une même famille ou à deux collègues.
  - Chaque groupe doit être inspecté et confirmé manuellement, un par un. Les groupes `Needs review` ne sont jamais inclus dans les fusions par lots, et aucun réglage ne permet de forcer des groupes ambigus à passer en fusion groupée. Si deux fiches représentent des personnes différentes, laissez-les séparées.

## Fonctionnalités Free vs Pro

- **Free (version gratuite)** :
  - Analyser le carnet d'adresses et consulter l'ensemble des groupes de doublons détectés.
  - Fusionner un groupe de doublons à la fois, comportant jusqu'à 3 contacts dans ce groupe (la fusion par lots de plusieurs groupes n'est pas incluse).
- **Pro** :
  - Déblocage unique via l'App Store, sans abonnement ; Apple affiche directement le prix régional correspondant à votre boutique.
  - Débloque la fusion des groupes de plus de 3 contacts ainsi que la fusion par lots des groupes `Ready to merge` après confirmation (les groupes `Needs review` requièrent toujours un examen manuel individuel).
  - Ni la version Free ni la version Pro ne promettent une vitesse d'analyse déterminée ou une capacité illimitée de carnet d'adresses.
  - Pour la restauration d'un achat ou les règles de remboursement d'Apple, consultez la [FAQ](faq.md#q15) ou contactez l'[assistance officielle (en anglais)](https://contactmerge.app/support).

## Guides associés et assistance

- [Sauvegarde, annulation et historique de récupération](recovery.md)
- [Autorisations et dépannage](permissions-troubleshooting.md)
- [Foire aux questions (FAQ)](faq.md)
- [How to Merge Contacts Safely (en anglais)](https://contactmerge.app/guides/merge-contacts-safely)
- [Backup Contacts Before Merge on iPhone (en anglais)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)
- [Assistance officielle (en anglais)](https://contactmerge.app/support)
- [Politique de confidentialité (en anglais)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## État de la documentation

Vérifié le 8 novembre 2026. Les écrans, intitulés et comportements peuvent varier selon la version installée de l'application et votre version d'iOS.
