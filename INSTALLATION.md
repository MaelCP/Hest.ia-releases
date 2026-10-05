# Installer Hest.ia — guide pour le praticien

Comptez **20 minutes** la première fois. Vous aurez besoin du mot de passe de votre Mac et d'une feuille de papier
(pour la clé de secours).

---

## 1. Vérifier votre Mac

Menu  (en haut à gauche) → **À propos de ce Mac** :

- **Puce** : Apple M1, M2, M3 ou M4 (pas « Intel »).
- **macOS** : version **26** ou plus récente. Sinon : Réglages Système → Général → Mise à jour de logiciels.

Avant de mettre de vrais dossiers dans l'app, vérifiez aussi :

- **FileVault activé** (chiffrement du disque) : Réglages Système → Confidentialité et sécurité → FileVault.
- **Time Machine activé** (sauvegarde) : Réglages Système → Général → Time Machine.

## 2. Télécharger

Sur **https://github.com/MaelCP/Hest.ia-releases/releases/latest**, téléchargez le fichier `Hest.ia_…_aarch64.dmg`
(environ 530 Mo, il contient le moteur de transcription). Pas besoin de compte GitHub.

## 3. Installer

1. Double-cliquez le fichier `.dmg` téléchargé : une fenêtre s'ouvre.
2. **Glissez l'icône Hest.ia sur le dossier Applications** (pas le fichier `.dmg` lui-même).
3. Éjectez le disque « Hest.ia » (icône dans la barre latérale du Finder).

## 4. Premier lancement (autoriser l'app)

L'app n'est pas encore signée par Apple : macOS la bloque la première fois. C'est normal.

1. Ouvrez **Applications** et double-cliquez **Hest.ia**. Un message dit qu'Apple ne peut pas vérifier l'app :
   cliquez **Terminé** (ou OK).
2. Ouvrez **Réglages Système → Confidentialité et sécurité**, descendez jusqu'à la section **Sécurité** :
   à côté de « Hest.ia a été bloqué », cliquez **Ouvrir quand même**, puis saisissez le mot de passe du Mac.
3. Relancez Hest.ia. Les fois suivantes, elle s'ouvre normalement.

## 5. Les autorisations demandées

macOS pose quelques questions au fil de l'utilisation. Répondez ainsi :

| Question | Réponse | Pourquoi |
|---|---|---|
| Trousseau : « Hest.ia veut utiliser … » | **Toujours autoriser** (mot de passe du Mac) | La clé qui chiffre vos dossiers y est rangée |
| Micro | **Autoriser** | Dictée et test de la voix ; le son reste sur le Mac |
| Reconnaissance vocale | **Autoriser** | Dictée en direct |
| « Hest.ia souhaite contrôler Mail » | **Autoriser** | Lire vos mails (sans rien modifier) et envoyer ceux que vous rédigez |
| Calendriers | **Autoriser** | Agenda sur l'accueil, rendez-vous |
| Contacts | **Autoriser** | Suggestions de destinataires |

Une autorisation refusée par erreur : Réglages Système → Confidentialité et sécurité → (Micro, Calendriers,
Contacts, Automatisation…) → activer Hest.ia.

> À chaque **nouvelle version** de l'app, macOS peut reposer ces questions : répondez de la même façon.

## 6. Premiers pas (dans l'app)

Au premier lancement, Hest.ia vous guide en 5 étapes ; chacune peut être passée et refaite plus tard
(Réglages → **Revoir les premiers pas**).

1. **Votre identité** : nom (tel qu'après « Docteur »), spécialité, qualités, liste d'inscription, titre sous la
   signature. Ils remplissent l'en-tête et la signature de vos expertises.
2. **Votre signature** : dessinez-la au trackpad (ou importez une image PNG).
3. **Votre messagerie** : voir le point 7.
4. **Votre clé de secours** : **recopiez-la sur papier**, rangez-la en lieu sûr, cochez « Je l'ai notée ».
   Sans elle, vos dossiers sont perdus si vous changez de Mac ou si le trousseau est réinitialisé.
5. **Votre voix** : un essai de 30 secondes vérifie le micro.

L'assistant (bulle en bas à droite, ⌘K) marche sans rien installer ; l'IA locale se télécharge depuis
Réglages → **Assistant et IA locale** (5,2 Go, une fois). Son micro n'est pas disponible dans l'éditeur Word.

## 7. Connecter votre messagerie

**Le plus simple : ajouter votre compte à l'app Mail du Mac.**
Réglages Système → **Comptes internet** → ajoutez votre messagerie :

- **Exchange** (messagerie de l'établissement) : adresse mail professionnelle et mot de passe du webmail.
  Si le serveur est demandé, votre service informatique vous l'indiquera.
- **Outlook / Microsoft 365**, **Google** : suivez les écrans de connexion.

Ouvrez une fois l'app **Mail** pour qu'elle télécharge vos messages. Hest.ia relève ensuite ces comptes
toutes les 30 secondes (en lecture seule) et peut envoyer depuis eux.

**Autre possibilité : connexion Exchange directe** (Premiers pas → étape 3, ou Réglages → Messagerie Exchange) :
adresse, identifiant et mot de passe du webmail. Le mot de passe est rangé dans le trousseau du Mac, jamais dans
l'app. **Prévenez votre service informatique** de cet usage.

## 8. Reprendre vos dossiers existants

Vous avez déjà des patients dans le Finder ? **Patients → Importer des dossiers** → choisissez le dossier.

- Rangement accepté : **un sous-dossier par patient** (« DUPONT Jean ») ou **des documents en vrac**
  (« CR_DUPONT_Jean.pdf ») ; à défaut de nom, Hest.ia le cherche au début du document (« Monsieur DUPONT Jean, né le… »).
- Un **tableau** montre chaque patient trouvé : corrigez un nom, décochez ce que vous ne voulez pas, « existe déjà »
  indique un patient présent (les documents s'y ajoutent). Rien n'est importé avant votre clic.
- PDF, Word, images et textes sont copiés, chiffrés, dans Hest.ia ; **le dossier d'origine n'est jamais modifié**.
  Les mémos audio sont laissés de côté : importez-les depuis le dossier du patient pour les transcrire.
- Relancer l'import du même dossier ne crée pas de doublons.

## 9. Premier essai conseillé (avec des données fictives)

1. Créez un patient fictif (Patients → Nouveau patient).
2. Dans son dossier : **Nouveau document** → « Expertise — protection juridique (trame) » ; cliquez dans le texte
   et **dictez** (bouton rouge ou ⌘⇧D) ; « à la ligne » crée un paragraphe ; Échap arrête.
3. **→ PDF pour signer** → apposez votre signature → **Envoyer par mail…** à votre propre adresse.
4. Envoyez-vous un mail avec un PDF en pièce jointe : il apparaît dans **Réception** en moins d'une minute.

## 10. Bon à savoir

- **Vos données** sont dans un seul fichier chiffré :
  `~/Library/Application Support/io.medicassist.desktop/base.sqlite` (sauvegardé par Time Machine).
- **Nouvelle version** : quand une version sort, « Mise à jour … » apparaît en bas du menu de gauche.
  Réglages → **Mises à jour** → **Mettre à jour** : l'app se télécharge, s'installe et redémarre ;
  vos dossiers, votre signature et vos réglages sont conservés. Après une mise à jour, macOS peut redemander
  l'accès au trousseau ou au micro : répondez comme au point 5.
- **Apparence** : Réglages → Apparence (clair, sombre ou comme le Mac).
- **Désinstaller** : glissez Hest.ia à la corbeille. Les dossiers restent dans le fichier ci-dessus
  (à supprimer seulement si vous êtes sûr de ne plus en avoir besoin).

## 11. En cas de problème

| Problème | Solution |
|---|---|
| « Hest.ia est endommagé ou ne peut pas être ouvert » | Refaire le point 4 (Confidentialité et sécurité → Ouvrir quand même) |
| La Réception reste vide | Vérifier que le compte est dans l'app **Mail** et que Mail a téléchargé les messages ; Réglages Système → Confidentialité et sécurité → Automatisation → Hest.ia → **Mail** coché |
| La dictée ne démarre pas | Réglages Système → Confidentialité et sécurité → **Micro** et **Reconnaissance vocale** → Hest.ia activé |
| L'app demande une « clé de secours » au lancement | Le trousseau ne contient plus la clé (nouveau Mac, trousseau réinitialisé) : saisissez la clé notée sur papier, rien n'est effacé |
| L'agenda est vide | Confidentialité et sécurité → **Calendriers** → Hest.ia |

Pour signaler un problème : une capture d'écran et une phrase (« j'ai fait…, je m'attendais à… ») suffisent.
