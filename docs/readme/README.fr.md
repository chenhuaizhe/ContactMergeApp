# ContactMerge+ Cleaner — Documentation produit et assistance

Documentation produit publique officielle et guides d'utilisation pour **ContactMerge+ Cleaner** sur iPhone. Ce dépôt contient uniquement de la documentation destinée aux utilisateurs — il ne s'agit pas d'un dépôt du code source de l'application.

ContactMerge+ Cleaner traite vos contacts localement sur votre appareil, n'envoie pas votre carnet d'adresses vers des serveurs du développeur, et le développeur ne fournit aucun service de sauvegarde cloud. (La synchronisation des contacts via iOS ou vos comptes — comme iCloud ou Google — ainsi que les sauvegardes système ou de l'appareil constituent des mécanismes distincts, régis par les réglages de vos propres comptes et d'iOS.)

- **Site web** : [Site officiel (en anglais)](https://contactmerge.app)
- **App Store** : [Télécharger dans l'App Store (en anglais)](https://apps.apple.com/us/app/contactmerge-contacts-cleaner/id6738980785)
- **Assistance** : [Assistance officielle (en anglais)](https://contactmerge.app/support)
- **Langues** : [English](../../README.md) | [Deutsch](README.de.md) | **Français** | [Italiano](README.it.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [日本語](README.ja.md) | [한국어](README.ko.md) | [简体中文](README.zh-Hans.md) | [繁體中文](README.zh-Hant.md)

## Démarrage rapide en 4 étapes

1. **Sauvegarder vos contacts et autoriser l'accès** : Conservez une sauvegarde indépendante et datée avant tout nettoyage important (export `.vcf` facultatif), laissez se terminer tout transfert de téléphone ou toute synchronisation initiale, puis autorisez l'accès aux contacts lorsque iOS vous le demande.
2. **Analyser** : Lancez une analyse dans ContactMerge+ Cleaner pour repérer les groupes de doublons potentiels sur votre iPhone.
3. **Prévisualiser, choisir la fiche principale et vérifier les notes dans l'app Contacts d'Apple** : Ouvrez un groupe de doublons, examinez l'aperçu de fusion (`Merge Preview`), sélectionnez le contact principal à conserver comme fiche de base, puis consultez l'app **Contacts** d'Apple afin d'y vérifier et sauvegarder les éventuelles notes (`Notes`).
4. **Revérifier avant de confirmer** : Si vous avez quitté l'application pour consulter ou modifier des fiches dans l'app **Contacts** d'Apple, revenez dans ContactMerge+ Cleaner et revérifiez d'abord les doublons proposés ainsi que l'aperçu en cours. Ne confirmez la fusion que si les fiches désignent clairement la même personne et que l'aperçu conserve les champs attendus.

<img src="../../assets/scan-results-demo.png" alt="Démo sur simulateur avec interface en anglais (capture non localisée en français, prise le 2026-11-03) de l'écran Duplicate Contacts avec des contacts fictifs montrant Undo Last Contact Merge, Ready to merge et Needs review ; les écrans et libellés peuvent varier selon la version de l'application ou d'iOS" width="420">

*Démo sur simulateur avec des contacts fictifs (interface en anglais — capture non localisée en français — prise le 2026-11-03). Les écrans, la disposition et les libellés peuvent varier selon la version installée de l'application ou votre version d'iOS.*

## Limites de sécurité essentielles

- **`Ready to merge` vs `Needs review`** :
  - `Ready to merge` (prêt à fusionner) signifie que chaque paire de fiches du groupe a satisfait à des contrôles stricts reposant sur des indices concordants entre toutes les paires. Vérifiez néanmoins toujours l'aperçu avant de confirmer : un même nom ou un même numéro de téléphone ne suffit pas, à lui seul, à prouver qu'il s'agit de la même personne.
  - `Needs review` (à vérifier) signale des indices plus faibles ou contradictoires (par exemple un numéro fixe familial partagé, des noms différents, des dates d'anniversaire divergentes ou un recoupement partiel). Il s'agit d'une mesure de prudence et non d'une erreur d'analyse : examinez chaque groupe `Needs review` manuellement, un par un, et ne fusionnez jamais des fiches correspondant à des personnes distinctes.
- **Vérifier et enregistrer les notes dans l'app Contacts d'Apple avant toute fusion** :
  - Les notes (`Notes`) figurant sur les fiches secondaires (les autres fiches fusionnées dans la fiche principale) ne sont **ni** lues **ni** copiées vers le contact principal, et elles ne pourront pas être récupérées par la suite.
  - Comme ContactMerge+ Cleaner ne peut pas lire le champ Notes, ne déduisez jamais de l'absence de notes dans l'aperçu de fusion qu'une fiche n'en contient pas. Consultez et copiez vos notes importantes directement dans l'app **Contacts** d'Apple avant de fusionner ; si vous y consultez ou modifiez des fiches, revenez dans ContactMerge+ Cleaner et revérifiez les doublons proposés ainsi que l'aperçu avant de confirmer (ne supposez pas que les vues déjà ouvertes s'actualisent automatiquement).
- **Annulation et récupération locale sur l'appareil** :
  - `Undo Last Contact Merge` (annuler la dernière fusion de contacts) porte uniquement sur la toute dernière fusion effectuée (voir [Sauvegarde, annulation et historique de récupération](../fr/recovery.md) pour l'emplacement vérifié à l'écran et les réserves liées aux versions).
  - `Recovery History` (historique de récupération) est un journal local enregistré par l'application sur l'iPhone, qui conserve **au maximum 3 enregistrements de fusion et au maximum 3 enregistrements de suppression** pendant **environ 30 jours sur l'appareil** (son chemin de navigation exact dans l'application n'est pas vérifié dans cette documentation ; voir [Sauvegarde et récupération](../fr/recovery.md)).
  - **Pas une restauration complète du système** : Les notes des fiches secondaires ne peuvent pas être récupérées, et les identifiants système ainsi que les liens d'origine peuvent ne pas être rétablis. Le développeur ne fournit aucun service de sauvegarde cloud (indépendamment de votre synchronisation iCloud/Google ou de vos sauvegardes système iOS ; les fusions peuvent donc se propager vers vos comptes synchronisés). Par précaution, la récupération n'est pas garantie après des modifications ultérieures des contacts, la désinstallation de l'application ou la perte de l'appareil.
- **Sauvegarde indépendante et sécurité des comptes** : L'export d'un fichier `.vcf` est facultatif, mais il est recommandé de conserver une sauvegarde indépendante et datée couvrant les comptes où résident réellement vos contacts avant votre premier nettoyage (la synchronisation de compte ne constitue pas une sauvegarde indépendante). Ne supprimez jamais de contacts sources, ne touchez pas `"Delete from My iPhone"`, ne désactivez/réactivez pas la synchronisation et ne retirez pas vos comptes à titre de dépannage.

## Version gratuite (Free) vs Pro

- **Free** : Analysez vos contacts, consultez tous les groupes de doublons détectés et fusionnez un groupe à la fois (jusqu'à 3 contacts au sein de ce groupe). La fusion par lots de plusieurs groupes n'est pas incluse.
- **Pro** : Déblocage unique sur l'App Store, sans abonnement ; le tarif régional est affiché directement par Apple. Débloque la fusion des groupes de plus de 3 contacts ainsi que la fusion par lots des groupes `Ready to merge` après confirmation (les groupes `Needs review` s'examinent toujours individuellement).
- **Restauration d'achat et facturation** : Pour restaurer un achat Pro existant avec le même compte Apple ou comprendre la procédure de remboursement d'Apple (gérée par Apple sur [reportaproblem.apple.com (en anglais)](https://reportaproblem.apple.com), éligibilité non garantie), consultez la [FAQ](../fr/faq.md#q16) ou contactez l'[assistance officielle (en anglais)](https://contactmerge.app/support).

## Guides d'utilisation

- [Démarrage rapide : analyser et fusionner vos contacts en toute sécurité](../fr/quick-start.md)
- [Sauvegarde, annulation et historique de récupération](../fr/recovery.md)
- [Autorisations et dépannage](../fr/permissions-troubleshooting.md)
- [Foire aux questions (FAQ)](../fr/faq.md)

## Assistance officielle et confidentialité

- **Assistance** : [Assistance officielle (en anglais)](https://contactmerge.app/support)
- **Confidentialité** : [Politique de confidentialité (en anglais)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)
- **Consigne de confidentialité et de masquage** : Ne partagez jamais de listes de contacts privées, de fichiers `.vcf` (vCard), de mots de passe, de coordonnées de paiement ni de reçus d'achat dans des signalements publics. Masquez tous les vrais noms, numéros de téléphone, adresses e-mail, photos, adresses postales, notes et identifiants de compte avant d'envoyer une capture d'écran — utilisez autant que possible des données fictives de démonstration.

## État de la documentation

Vérifié le 8 novembre 2026. Les écrans, intitulés et comportements peuvent varier selon la version installée de l'application et votre version d'iOS.
