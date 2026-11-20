# Journal des versions

Une version est publiée chaque lundi à 7 h. Chaque version est signée « Developer ID » et notarisée par Apple ; l'application
propose elle-même son installation.

## 0.17.0 — 20 novembre 2026

- **Relecture avec Claude** : une PR se relit en deux moitiés. La séparation se fait glisser ; un double-clic revient au 50/50. À gauche, le contexte, qui défile seul : en bref, le ticket, les avis, ce qui a été dit (en entier), la maquette, ce qui se passe autour. À droite, deux onglets : « Écarts » (une liste à trier, aussi longue soit-elle) et « Ma relecture », sur toute la hauteur.
- **Écarts avec la maquette** : Claude relève seulement ce qui se vérifie (une taille, un espacement, un token, une variante, un état). Il précise si l'écart a été vu sur la version de test ou lu dans le code. Chaque écart se garde (il entre dans la relecture, marqué d'un point vert) ou s'écarte. Le relevé se lance à la main, comme la synchro ; la pastille passe à l'orange quand la PR a changé depuis.
- **Réagir** : Claude met en contexte ce qui est écrit ou dicté, en cartes sous les paragraphes. Exemples : une PR déjà en cours sur le même sujet et la personne à qui en parler, ou une remarque qui contredit le ticket ou la maquette, avec ce que changer d'avis impliquerait. « Adapter la maquette dans Figma » lui fait modifier le fichier. La relecture reste écrite par le designer.
- **Idées de Claude** : alternatives et conseils, repliés sous la relecture, à lire une fois les écarts triés. Chaque idée s'ajoute à la relecture d'un clic.
- **Préparer sur GitHub** : un écart gardé lu dans le code devient un commentaire sur sa ligne dans la review en attente. La mise en forme pour GitHub suit la langue de l'équipe sur le dépôt (anglais ou français), quelle que soit celle des notes.
- **Relevé automatique** (facultatif, Réglages › Claude) : à la première ouverture du matin (ou à 10 h si Bridges est déjà ouvert), puis à 14 h 30. Il concerne les PR qui attendent un avis et ont changé depuis le dernier relevé.
- **Maquettes en liens** : plus d'aperçu d'image, qui montrait souvent la couverture du fichier. À la place : le nom de l'écran et « Ouvrir dans Figma ».
- **Claude mieux rangé ailleurs** : sur un ticket, une mention ou une branche, la colonne de gauche sert à comprendre (Contexte, Analyse), celle de droite à agir (notes, Claude). Une seule entrée Claude dans la barre latérale (Discussions, Agents), et un seul libellé dans les menus : « Demander à Claude ».

## 0.16.1 — 20 novembre 2026

- **Nouvelle numérotation** : Bridges passe en 0.x. La version 1.0 viendra quand l'application sera aboutie ; d'ici là, chaque version avance d'un cran (0.17, 0.18…). Les versions précédentes sont renumérotées : la 1.16 devient la 0.16, et ainsi de suite.
- **Une installation en 1.x ne propose pas cette mise à jour** (elle croit avoir une version plus récente) : télécharger Bridges une seule fois depuis bridges.works. Les mises à jour suivantes redeviennent automatiques ; réglages, notes et comptes sont conservés.

## 0.16.0 — 20 novembre 2026

- **Bridges en anglais** : l'application parle français ou anglais (Réglages › Général › Langue, sinon celle de macOS). Claude répond dans la langue choisie, la démo existe dans les deux langues et les liens d'aide mènent au centre d'aide de la langue. Le journal des versions existe aussi en anglais.
- **Bridges agit** : dans une conversation, Claude copie un texte mis en forme dans le presse-papiers, ouvre un fichier ou un écran dans l'app Figma, remplit les notes « Ma relecture » et prépare une review en attente sur GitHub (résumé et commentaires de lignes). Rien n'est publié : la review reste visible du seul designer jusqu'à sa validation sur GitHub.
- **Modifier Figma** : avec le connecteur Figma de Claude Code, Claude modifie les fichiers à la demande dans toutes les conversations, de préférence dans une branche, et demande confirmation avant de toucher un fichier principal.
- **Relecture** : « Préparer sur GitHub » transforme les notes en review en attente ; « Copier et ouvrir la PR » reste dans le menu du bouton. Chaque réponse de Claude se copie d'un clic, et les liens Figma s'ouvrent dans l'app Figma.
- **Maquettes manquantes** (anciennement « Anomalies ») : les groupes disent ce qu'il y a à faire (Construit sans maquette, Maquette attendue, À trancher…). Sur chaque ticket à trancher, « Pas besoin de maquette » ou « Maquette nécessaire » ; la décision se reprend à tout moment. Les tickets sans aucun indice attendent à part.
- **Branches Figma** : plus d'aperçu ; le bouton Merger reste à droite, l'alerte « Mise à jour du principal » à sa gauche, et l'âge de la branche est dit dans sa description.
- **Listes** : la durée affichée sans légende passe dans la ligne de repères, avec ce qu'elle mesure (« mis à jour il y a 51 j », « demandée il y a 5 h »).

## 0.15.1 — 20 novembre 2026

- **Mode démo** : les données fictives suivent la refonte d'une application de supervision de data centers (carte thermique, tableau des alertes, jauges, tokens et composants du design system), comme les visuels de bridges.works.

## 0.15.0 — 20 novembre 2026

- **Ouverture** : l'application s'ouvre sur les demandes de relecture.

## 0.14.1 — 20 novembre 2026

- **Correctif** : ajustements d'affichage.

## 0.14.0 — 20 novembre 2026

- **Agents** : un agent porte l'étoile de Claude, dans la barre latérale, la palette, l'écran Agents et les analyses.
- **Correctif** : deux tickets dont la description avait la même longueur ne partagent plus leurs liens Figma.

## 0.13.0 — 20 novembre 2026

- **Anomalies plus justes** : la maquette d'un ticket est cherchée partout, et plus seulement dans le ticket : ses commentaires anciens, son ticket parent, la description, les commentaires et les avis de sa PR, les branches Figma dont le nom cite le ticket et les liens posés en mode Dev (avec l'autorisation « file_dev_resources:read » du jeton Figma). Les liens Figma écrits sans « https:// » ou sur embed.figma.com sont reconnus.
- **Seule l'interface nouvelle compte** : un ticket est une anomalie quand sa PR crée des écrans ou des composants, ou quand le ticket l'annonce (libellé de design, « nouvel écran », « ajouter un onglet », refonte). Un mot d'interface isolé passe en « À vérifier », une PR qui retouche l'existant en « Retouches de l'existant ». Une barre de recherche filtre l'écran.
- **États en toutes lettres** : dans les listes, les icônes d'état laissent place à un point de couleur suivi du mot (« PR ouverte », « En cours », « À démarrer », « Changements demandés », « Brouillon »). Vert, orange et rouge sont communs à toute l'application.
- **Barre latérale** : le bouton de repli passe à droite de « Bridges », en icône seule. La synchronisation montre une pastille verte, orange ou rouge, et la ligne pulse pendant la mise à jour. Les notifications affichent le nombre seul.
- **Listes plus lisibles** : l'intitulé d'un groupe colle à son contenu, les groupes se détachent nettement, et un filet ne sépare que les lignes d'un même groupe.
- **Correctif** : la bulle « Besoin d'aide ? » s'ouvre au-dessus du bouton ; sa pointe n'est plus tordue.

## 0.12.0 — 20 novembre 2026

- **Aide** : un centre d'aide en ligne, bridges.works/aide, s'ouvre depuis le menu Aide (⌘?), la palette de commandes, Réglages › À propos ou l'icône « ? » à côté des réglages, en bas de la barre latérale. Les retours s'y envoient sans inscription ; « Copier et écrire à l'assistance » joint le diagnostic à un e-mail prêt à compléter.
- **Accessibilité** : « Réduire la transparence » et « Différencier sans couleur » suivent macOS et se règlent dans Réglages › Accessibilité ; les pastilles d'état prennent alors une forme distincte (urgent, à traiter, prêt). Avec VoiceOver, les branches, les conversations et les résultats de la palette se lisent d'un bloc, les en-têtes de groupe sont des titres repliables, la séparation entre le contexte et les notes se règle aux flèches, et les messages de confirmation sont annoncés.
- **Textes** : les demandes d'accès au micro et à la dictée adoptent la formulation impersonnelle du reste de l'application.

## 0.11.0 — 19 novembre 2026

- **Correctif** : ajustements d'affichage.

## 0.10.0 — 19 novembre 2026

- **Textes sans tutoiement** : toute l'application adopte une formulation impersonnelle et professionnelle, sans « tu » ni
  « vous » : l'infinitif pour les actions (« Écrire à Claude… », « Se connecter »), des tournures nominales pour les états
  (« Notes enregistrées sur ce Mac à chaque frappe », « dev-alex attend un avis »). Les libellés à la première personne
  (« Ma relecture », « Assignés à moi ») sont conservés.
- **Claude** : les analyses, les conversations et l'aide sur les notes répondent dans le même registre. Les analyses déjà
  enregistrées gardent leur formulation jusqu'à leur prochaine relance.

## 0.9.0 — 19 novembre 2026

- **Barre latérale** : plus de compteurs à côté des entrées (le nombre reste dans l'infobulle). L'état de la
  synchronisation devient une ligne, entre « Usage » et « Replier la barre latérale », qui actualise d'un clic. La marque est
  alignée sur la barre du panneau.
- **Relectures** : « Règle le ticket » s'affiche au-dessus du nom du ticket, qui garde toute la largeur.
- **Textes** : l'en-tête des relectures passe à une formulation impersonnelle (« dev-alex attend un avis »).

## 0.8.0 — 19 novembre 2026

- **Détail d'un élément — contexte et notes côte à côte, à la largeur voulue** : la colonne des notes est toujours affichée
  (le bouton « Masquer mes notes » disparaît). Le filet qui la sépare du contexte se fait glisser pour donner plus de place à
  l'un ou à l'autre ; la largeur choisie est retenue, un double-clic rend la largeur d'origine.
- **Lisibilité** : le texte du contexte et la zone de notes ne s'étirent plus au-delà d'une longueur de ligne confortable.
- **Finitions** : le bouton « Copier et ouvrir la PR » ne touche plus les bords de la zone de notes ; l'onglet actif n'a plus de
  bordure, sur tous les onglets.

## 0.7.0 — 19 novembre 2026

- **Discussion avec Claude à côté des notes** : sur écran large, la colonne de droite d'un élément propose deux onglets, les
  notes (« Ma relecture », « Ma réponse », « Mes notes ») et « Discussion ». La conversation avec Claude s'ouvre à côté du
  contexte, sans fenêtre par-dessus. Le dernier onglet choisi est conservé d'un élément à l'autre, et « Poser une question à
  Claude… », dans le menu « Claude » des notes, ouvre directement l'onglet. La discussion peut s'agrandir en fenêtre ou se
  poursuivre dans le Terminal.
- **Mode démo** : une nouvelle discussion n'est plus envoyée à Claude.

## 0.6.0 — 19 novembre 2026

- **Relectures — comparaison avec la maquette** : un onglet « Comparaison », à côté de « Contexte », propose sur demande un
  bilan complet des écarts entre la PR et la maquette Figma, écran par écran : écarts, états prévus, ajouts de la PR, éléments
  identiques et points non vérifiables. Chaque écart indique s'il a été constaté sur la version de test ou lu dans le code, et
  s'ajoute aux notes d'un clic. Claude constate sans juger : aucun verdict ni texte prêt à envoyer. La comparaison avec le rendu
  nécessite Claude in Chrome dans les analyses (Réglages › Connecteurs) et une version de test de la PR.
- **Réglages › Claude** : modèle propre à la comparaison (Sonnet par défaut) ; descriptions des analyses mises à jour.

## 0.5.2 — 19 novembre 2026

- **Licence** : Bridges devient un logiciel propriétaire gratuit. Son utilisation reste libre, y compris dans un cadre
  professionnel ; sa copie, sa modification, son adaptation, sa redistribution et sa revente sont interdites
  ([licence d'utilisation](LICENSE)). Les versions jusqu'à la 0.5.1 restent régies par leur licence d'origine (CC BY-ND 4.0).
- **Code source** : il n'est plus public. Le dépôt GitHub de Bridges présente l'application et diffuse ses versions.

## 0.5.1 — 19 novembre 2026

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

  Seuls les deux premiers groupes comptent parmi les anomalies. Trois erreurs de la 0.5.0 sont corrigées : un fichier Python,
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

## 0.5.0 — 19 novembre 2026

Version publiée par anticipation, sans attendre le lundi.

- **Anomalies** : les tickets en développement sans maquette qui ne touchent pas à l'interface sont rangés à part, dans un
  groupe replié « Probablement sans impact sur l'interface », avec la raison : la PR ne modifie aucun fichier d'interface
  (serveur, configuration, tests), ou le titre est technique (« chore: », « refactor », dépendances…). Ils ne comptent plus
  parmi les anomalies et ne déclenchent plus de notification. « C'est bien une anomalie » les y remet ; un libellé de design
  ou un fichier d'interface dans la PR les y maintient toujours.

## 0.4.3 — 19 novembre 2026

- **Correctif — fluidité** : l'application restait figée plusieurs secondes à chaque action dès que les tickets et les branches
  étaient nombreux. Les listes (branches, mentions, anomalies, recoupements) ne sont plus recalculées à chaque affichage ;
  sur un jeu d'essai de 430 tickets et 30 branches, une mise à jour d'écran passe d'environ 4 secondes à moins de 10 ms.
- **Listes longues** : seules les lignes visibles sont construites ; l'ouverture d'un écran ne dépend plus du nombre d'éléments.
- **Notes** : la frappe ne redessine plus l'écran ; l'écriture sur le disque est regroupée.
- **Synchronisation** : l'analyse des fichiers Figma et l'écriture du cache ne bloquent plus l'interface.

## 0.4.2 — 19 novembre 2026

- **Correctif** : ajustements d'affichage.

## 0.4.1 — 19 novembre 2026

- **Correctif — grands écrans** : les vues détaillées gardent une largeur maximale, centrée ; le contexte occupe toute sa
  colonne au lieu de laisser un vide au centre.
- **Barre latérale** : le bouton de repli rejoint les entrées du bas, aligné sur leurs icônes.

## 0.4.0 — 19 novembre 2026

Version publiée par anticipation, sans attendre le lundi.

- **Barre latérale** : le bouton « Accessibilité » est retiré ; les réglages restent dans Réglages › Accessibilité.

## 0.3.0 — 19 novembre 2026

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

## 0.2.1 — 19 novembre 2026

- **Mise en page** : réglages et vues détaillées plus aérés. Les sections sont séparées par l'espace et un filet plutôt que
  par des cadres imbriqués ; chaque titre est rapproché de son contenu.
- **Typographie** : titres allégés d'une graisse.

## 0.2.0 — 19 novembre 2026

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
- **Premier lancement** : l'étape Figma distingue l'accès au compte et le choix des fichiers ; plusieurs fichiers peuvent être ajoutés.
- **Correctif** : les menus « … », « Rappeler plus tard », « Importer » et « Demander à un agent » s'ouvrent de nouveau.

## 0.1.0 — 18 novembre 2026

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

## 0.0.2 — 18 novembre 2026

Version corrective.

- **Choix des modèles** (Réglages › Claude) : les sélecteurs, mal affichés, sont remplacés par un menu déroulant par usage
  (relectures et branches Figma, tickets et mentions, conversations, modification de maquette). Chaque modèle y est décrit,
  avec son niveau de consommation et le choix recommandé.
- **Sélecteurs** : fréquence de synchronisation, contraste et taille du texte utilisent les onglets de 40 px de l'application.

## 0.0.1 — 18 novembre 2026

Version corrective, publiée hors du rythme hebdomadaire.

- **Analyses sur demande** : Claude n'analyse plus aucun élément automatiquement. L'analyse est lancée depuis la vue détaillée
  (« Analyser avec Claude »), puis conservée.
- **Mise à jour proposée** : lorsqu'un élément change après son analyse (commentaire, commit, ticket modifié), un bandeau le
  signale et propose « Mettre à jour l'analyse ». L'analyse précédente reste consultable.
- **Consommation** : aucun appel à Claude n'a lieu sans action de l'utilisateur.

## 0.0.0 — 18 novembre 2026

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
