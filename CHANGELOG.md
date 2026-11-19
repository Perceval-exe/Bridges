# Journal des versions

Une version est publiée chaque lundi à 7 h. Chaque version est signée « Developer ID » et notarisée par Apple ; l'application
propose elle-même son installation.

## 1.9.0 — 19 novembre 2026

- **Accueil plus lisible** : la page occupe toute la largeur de la fenêtre ; les chiffres clés sont nettement plus grands ; le
  forfait Claude s'affiche en deux anneaux (session et semaine) ; « Demandes reçues » montre chaque jour sur un rail, les
  relectures et les mentions empilées ; les tickets créés et les branches Figma ont un anneau de répartition avec le chiffre clé
  au centre. Les cartes d'une même rangée ont la même hauteur.
- **Barre latérale** : plus de compteurs à côté des entrées (le nombre reste dans l'infobulle et sur l'accueil). L'état de la
  synchronisation devient une ligne, entre « Usage » et « Replier la barre latérale », qui actualise d'un clic. La marque est
  alignée sur la barre du panneau.
- **Relectures** : « Règle le ticket » s'affiche au-dessus du nom du ticket, qui garde toute la largeur.
- **Textes** : l'accueil et l'en-tête des relectures passent à une formulation impersonnelle (« 16 actions en attente »,
  « dev-alex attend un avis »).

## 1.8.0 — 19 novembre 2026

- **Détail d'un élément — contexte et notes côte à côte, à la largeur voulue** : la colonne des notes est toujours affichée
  (le bouton « Masquer mes notes » disparaît). Le filet qui la sépare du contexte se fait glisser pour donner plus de place à
  l'un ou à l'autre ; la largeur choisie est retenue, un double-clic rend la largeur d'origine.
- **Lisibilité** : le texte du contexte et la zone de notes ne s'étirent plus au-delà d'une longueur de ligne confortable.
- **Finitions** : le bouton « Copier et ouvrir la PR » ne touche plus les bords de la zone de notes ; l'onglet actif n'a plus de
  bordure, sur tous les onglets.

## 1.7.0 — 19 novembre 2026

- **Discussion avec Claude à côté des notes** : sur écran large, la colonne de droite d'un élément propose deux onglets, les
  notes (« Ma relecture », « Ma réponse », « Mes notes ») et « Discussion ». La conversation avec Claude s'ouvre à côté du
  contexte, sans fenêtre par-dessus. Le dernier onglet choisi est conservé d'un élément à l'autre, et « Poser une question à
  Claude… », dans le menu « Claude » des notes, ouvre directement l'onglet. La discussion peut s'agrandir en fenêtre ou se
  poursuivre dans le Terminal.
- **Mode démo** : une nouvelle discussion n'est plus envoyée à Claude.

## 1.6.0 — 19 novembre 2026

- **Relectures — comparaison avec la maquette** : un onglet « Comparaison », à côté de « Contexte », propose sur demande un
  bilan complet des écarts entre la PR et la maquette Figma, écran par écran : écarts, états prévus, ajouts de la PR, éléments
  identiques et points non vérifiables. Chaque écart indique s'il a été constaté sur la version de test ou lu dans le code, et
  s'ajoute aux notes d'un clic. Claude constate sans juger : aucun verdict ni texte prêt à envoyer. La comparaison avec le rendu
  nécessite Claude in Chrome dans les analyses (Réglages › Connecteurs) et une version de test de la PR.
- **Réglages › Claude** : modèle propre à la comparaison (Sonnet par défaut) ; descriptions des analyses mises à jour.

## 1.5.2 — 19 novembre 2026

- **Licence** : Bridges devient un logiciel propriétaire gratuit. Son utilisation reste libre, y compris dans un cadre
  professionnel ; sa copie, sa modification, son adaptation, sa redistribution et sa revente sont interdites
  ([licence d'utilisation](LICENSE)). Les versions jusqu'à la 1.5.1 restent régies par leur licence d'origine (CC BY-ND 4.0).
- **Code source** : il n'est plus public. Le dépôt GitHub de Bridges présente l'application et diffuse ses versions.

## 1.5.1 — 19 novembre 2026

- **Correctif — Anomalies** : l'écran ne faisait pas remonter les tickets qui ont réellement besoin d'une maquette. Il se
  contentait d'écarter ce qui paraissait technique, puis triait par date. Il cherche maintenant des preuves et range les tickets
  par besoin de maquette :
  - « Interface développée sans maquette » : la PR crée ou retouche des fichiers d'interface. La ligne dit combien, et lesquels
    sont nouveaux ; les plus gros chantiers passent en tête.
  - « Probablement à maquetter » : un libellé de design, le titre ou la description du ticket parlent d'interface.
  - « À vérifier » : aucun indice dans un sens ou dans l'autre.
  - « Corrections de bugs » (replié) : type « Bug », libellé ou titre de correction. Une correction qui crée un écran remonte
    en tête.
  - « Probablement sans impact sur l'interface » (replié).

  Seuls les deux premiers groupes comptent parmi les anomalies. Trois erreurs de la 1.5.0 sont corrigées : un fichier Python,
  Ruby, Go ou Elixir n'est plus tenu pour technique d'office ; un ticket dont le titre annonce un écran n'est plus écarté parce
  que sa PR n'a encore touché que le serveur ; des mots du métier (« pipeline », « worker », « logs ») ne suffisent plus à
  classer un titre comme technique.
- **Anomalies — tickets examinés** : la recherche remonte jusqu'à 300 tickets par critère au lieu de 100, pour ne plus perdre
  ceux qui sont en développement depuis des mois. En bas de l'écran, une ligne dit combien de tickets ont été examinés et
  combien ont été laissés de côté (lien Figma déjà présent, corbeille, libellé ignoré, toi seul·e dessus).
- **Correctif — zone de rédaction** : taper du texte ouvrait parfois le ticket dans le navigateur. Les listes avaient des
  raccourcis à une seule touche (O ou Entrée pour ouvrir, J et K pour changer de ligne) qui se déclenchaient dès que le curseur
  n'était plus dans la zone. Ils sont retirés : restent les flèches, Échap, et ⌘O pour ouvrir dans le navigateur.
- **Avatars retirés** des listes, du détail des tickets, des discussions, de l'historique et des notifications. Chaque ligne
  porte à la place l'état du ticket ; le nom de la personne reste écrit.
- **« Ce qu'ajoutent les agents »** : nouveau rendu. Le nom de l'agent est écrit en clair (« Fidélité à la maquette »), une
  rangée par agent séparée d'un filet, le constat en premier et sa question en gris. La consigne donnée aux agents demande des
  points plus courts.

## 1.5.0 — 19 novembre 2026

Version publiée par anticipation, sans attendre le lundi.

- **Anomalies** : les tickets en développement sans maquette qui ne touchent pas à l'interface sont rangés à part, dans un
  groupe replié « Probablement sans impact sur l'interface », avec la raison : la PR ne modifie aucun fichier d'interface
  (serveur, configuration, tests), ou le titre est technique (« chore: », « refactor », dépendances…). Ils ne comptent plus
  parmi les anomalies et ne déclenchent plus de notification. « C'est bien une anomalie » les y remet ; un libellé de design
  ou un fichier d'interface dans la PR les y maintient toujours.

## 1.4.3 — 19 novembre 2026

- **Correctif — fluidité** : l'application restait figée plusieurs secondes à chaque action dès que les tickets et les branches
  étaient nombreux. Les listes (branches, mentions, anomalies, recoupements) ne sont plus recalculées à chaque affichage ;
  sur un jeu d'essai de 430 tickets et 30 branches, une mise à jour d'écran passe d'environ 4 secondes à moins de 10 ms.
- **Listes longues** : seules les lignes visibles sont construites ; l'ouverture d'un écran ne dépend plus du nombre d'éléments.
- **Notes** : la frappe ne redessine plus l'écran ; l'écriture sur le disque est regroupée.
- **Synchronisation** : l'analyse des fichiers Figma et l'écriture du cache ne bloquent plus l'interface.

## 1.4.2 — 19 novembre 2026

- **Accueil** : graphiques en nuances de gris bleuté (une seule teinte, quatre clartés contrastées) ; les couleurs franches
  restent réservées aux signaux d'état.

## 1.4.1 — 19 novembre 2026

- **Correctif — grands écrans** : les vues détaillées gardent une largeur maximale, centrée ; le contexte occupe toute sa
  colonne au lieu de laisser un vide au centre.
- **Accueil** : graphiques redessinés (cartes à filet fin, barres fines, chiffres clés en tête de chaque graphique, détail au
  survol) et chiffres clés regroupés en une seule bande.
- **Barre latérale** : le bouton de repli rejoint les entrées du bas, aligné sur leurs icônes.

## 1.4.0 — 19 novembre 2026

Version publiée par anticipation, sans attendre le lundi.

- **Accueil** : nouvel écran d'ouverture. Chiffres clés (relectures, mentions, tickets assignés, anomalies, branches à
  merger), actions du jour classées par urgence avec accès direct à l'élément, graphiques (demandes reçues sur 14 jours,
  attente des relectures, avancement des tickets créés, état des branches Figma) et usage du forfait Claude.
- **Barre latérale** : le bouton « Accessibilité » est retiré ; les réglages restent dans Réglages › Accessibilité.

## 1.3.0 — 19 novembre 2026

Version publiée par anticipation, sans attendre le lundi.

- **Vues détaillées** : sur un écran large, le contexte à gauche et les notes à droite ; le titre reprend le numéro et le titre
  exacts du ticket ou de la PR. Le contexte de Claude est rédigé en texte suivi.
- **Notes du designer** : une zone de notes par élément, enregistrée à chaque frappe, avec annulation conservée d'un écran à
  l'autre et dictée vocale qui se poursuit pendant la navigation.
- **Aide de Claude sur les notes** : formaliser, mettre en forme pour GitHub, vérifier les remarques, identifier les points non
  couverts, traduire. Les retours s'affichent dans un onglet dédié.
- **Agents par section** : sept agents intégrés, rattachés aux sections où ils servent et consultés à chaque analyse ; leur
  apport est présenté à part. Le rattachement se règle dans l'écran Agents.
- **Mise à jour de l'application** : fenêtre d'installation (téléchargement, vérification, redémarrage) et confirmation après
  le redémarrage.
- **Écran Claude** : les demandes de Claude s'affichent en bandeau au-dessus de la conversation ; les analyses à lire sont
  nommées par type.
- **Interface** : barre latérale repliable (⌃⌘S), réglages regroupés, espacements et alignements harmonisés.

## 1.2.1 — 19 novembre 2026

- **Mise en page** : réglages et vues détaillées plus aérés. Les sections sont séparées par l'espace et un filet plutôt que
  par des cadres imbriqués ; chaque titre est rapproché de son contenu.
- **Typographie** : titres allégés d'une graisse.

## 1.2.0 — 19 novembre 2026

Version publiée par anticipation, sans attendre le lundi.

- **Analyses plus courtes** : chaque analyse de Claude se limite à quelques points d'attention, lisibles en moins d'une minute,
  sans analyse complète ni texte prêt à envoyer.
- **Branches Figma** : une branche est prête à fusionner dès que son design est validé (marquage dans Bridges, PR ouverte ou
  développeur assigné), sans attendre la livraison. Le signal « Mise à jour du principal » indique les écrans du fichier
  principal que la branche n'a pas encore récupérés, avec la marche à suivre.
- **Autres tickets sur les mêmes écrans** : les tickets non livrés qui visent le même écran ou la même section Figma sont
  signalés sur les tickets, les branches et les relectures, avec l'indication d'une dépendance déjà notée ou non.
- **Liens Figma cassés** : les liens de tickets qui ne mènent plus à aucun écran sont signalés.
- **Délai de relecture** : le réglage est retiré.
- **Accueil** : l'étape Figma distingue l'accès au compte et le choix des fichiers ; plusieurs fichiers peuvent être ajoutés.
- **Correctif** : les menus « … », « Rappeler plus tard », « Importer » et « Demander à un agent » s'ouvrent de nouveau.

## 1.1.0 — 18 novembre 2026

Version publiée par anticipation, sans attendre le lundi.

- **Relectures** : Claude prépare la relecture sans la faire. L'analyse présente ce que change la PR, l'intention du ticket,
  les écrans à comparer, les pistes à vérifier (à cocher) et la version de test. Elle ne contient plus de verdict ni de
  commentaire GitHub rédigé : l'avis reste celui du designer. Les avis d'agents suivent le même principe.
- **Délai de relecture** (Réglages › Suivi) : facultatif, désactivé par défaut, réglable de deux heures à deux jours.
- **Rappeler plus tard** : un élément peut être retiré de sa liste pour une heure, trois heures, jusqu'au lendemain 9 h ou au
  lundi suivant ; il revient avec une notification macOS.
- **Analyses coûteuses** : un avertissement discret, avec une estimation fondée sur les analyses précédentes, s'affiche sous le
  bouton d'analyse lorsque la consommation attendue est élevée.
- **Apparence** : thème sombre par défaut ; « Automatique » suit le réglage de macOS.
- **Licence** : mentions alignées sur la licence CC BY-ND 4.0 dans l'application.

## 1.0.2 — 18 novembre 2026

Version corrective.

- **Choix des modèles** (Réglages › Claude) : les sélecteurs, mal affichés, sont remplacés par un menu déroulant par usage
  (relectures et branches Figma, tickets et mentions, conversations, modification de maquette). Chaque modèle y est décrit,
  avec son niveau de consommation et le choix recommandé.
- **Sélecteurs** : fréquence de synchronisation, contraste et taille du texte utilisent les onglets de 40 px de l'application.

## 1.0.1 — 18 novembre 2026

Version corrective, publiée hors du rythme hebdomadaire.

- **Analyses sur demande** : Claude n'analyse plus aucun élément automatiquement. L'analyse est lancée depuis la vue détaillée
  (« Analyser avec Claude »), puis conservée.
- **Mise à jour proposée** : lorsqu'un élément change après son analyse (commentaire, commit, ticket modifié), un bandeau le
  signale et propose « Mettre à jour l'analyse ». L'analyse précédente reste consultable.
- **Consommation** : aucun appel à Claude n'a lieu sans action de l'utilisateur.

## 1.0.0 — 18 novembre 2026

Première version officielle.

- **Relectures** : comparaison de chaque PR avec la maquette Figma, écarts rédigés écran par écran avec les valeurs attendues,
  commentaire de relecture en anglais conforme aux conventions du dépôt. Délai de six heures signalé en orange à trois heures,
  en rouge à quatre heures, en retard au-delà de six heures.
- **Assignés, mentions, tickets créés, anomalies, branches Figma** : vue détaillée propre à chaque tâche, analyse préparée par
  Claude en arrière-plan.
- **Agents spécialisés** : accessibilité, design system, rédaction ou agents personnalisés (créés dans l'application, importés
  de fichiers ou d'un dépôt GitHub, synchronisés manuellement avec explication des changements). Suggérés selon le contexte,
  exécutés uniquement sur demande.
- **Design system de référence** : bibliothèque Figma, Storybook, fichier de tokens ; vérification de chaque nom cité par Claude.
- **Suivi et priorités** : actions requises par Claude, analyses disponibles, notifications réservées à l'activité de l'équipe.
- **Accessibilité** : contraste AA ou AAA, réduction des animations, liens soulignés, focus renforcé, texte espacé, taille du texte.
- **Corbeille par écran**, avec annulation immédiate de chaque action.
- **Installation** : assistant de configuration, installation de GitHub CLI sans Homebrew, diagnostic, page « Données ».
- **Mises à jour** : vérification quotidienne des nouvelles versions et installation proposée en un clic.
- **Claude** : utilisation de Claude Code et de l'abonnement Claude, sans clé API.
