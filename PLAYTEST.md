# SENSIBLE 2026 — ARCADE FOOTBALL

Version de travail : **v0.2 — Arcade Playtest** (6 novembre 2026)

Jeu de football arcade **original** inspiré des sensations des jeux de foot des années 1990, spécialement de Sensible Soccer. Ce projet n'intègre ni la ROM Mega Drive, ni ses graphismes/sons propriétaires. Le projet `ELIO-anniversaire` n'a pas été modifié.

## Jouer sans installation

Ouvrir `Sensible_Soccer_2026_v0.2.html` dans Chrome ou Edge. Cette version autonome contient tout le code et ne télécharge aucune bibliothèque externe. Pour le développement : `index.html`, `style.css` et `game.js` sont aussi fournis séparément.

## Contenu de v0.2

- Matchs **11 contre 11** sur un terrain complet, contre IA ou à deux joueurs sur le même clavier (PC).
- **20 équipes** : 10 équipes légendaires, 8 équipes modernes/années récentes et 2 clubs des copains. Les effectifs sont des XI indicatifs servant au jeu, pas des compositions officielles à jour.
- Éditeur : nom du club, couleurs, 11 noms de joueurs. Création illimitée dans la limite de 40 clubs personnalisés enregistrés.
- Export et import JSON des équipes personnalisées pour partager les clubs ou sauvegarder ses créations.
- Caméra classique/proche/panoramique, avec changement par `V` pendant le match.
- Déplacement direct, sélection plus stable, accélération et sprint, tirs dirigés, passes orientées, lobs, tacles, tirs avec effet après frappe, têtes plongeantes, animation des plongeons, gardiens réactifs à la trajectoire, rebonds.
- Touches, corners, six mètres, buts, chronomètre et feuille de match de fin avec statistiques simples (tirs, passes, arrêts, têtes, corners).
- Sons synthétiques locaux (pas de fichier audio externe), mode plein écran, interface mobile paysage/portrait.

## Commandes

### Solo au clavier

- WASD ou flèches : déplacer le joueur
- **J ou Z** : bouton rétro — appui court = passe / tacle ; appui prolongé = tir puissant
- **Espace** : passe / tacle direct ; **X** : tir immédiat ; **C** : centre lobé
- Maj : sprint ; **Q** : changement de joueur ; **V** : changement de caméra ; Échap : pause
- Après une frappe, orienter gauche/droite pour courber légèrement le ballon (aftertouch).

### Deux joueurs sur un même PC

- J1 : WASD, Espace / X / C, Q, Maj gauche
- J2 : flèches, **N** passe / tacle, **M** tir, **,** lob, **.** changer de joueur, Maj droite
- Les manettes compatibles sont reconnues si disponibles (J1 première manette, J2 seconde).

### Téléphone

- Joystick tactile gauche. En mode **Old School**, un bouton principal PASSE/TIR à droite : appui bref = passe/tacle ; appui long = tir. Boutons séparés pour sprint et changement de joueur.
- Sélectionner « Moderne — passe, tir, lob » pour afficher trois actions indépendantes.
- Le mode deux joueurs est destiné au clavier/manettes sur un même ordinateur ; il n'est pas encore multijoueur en réseau.

## Vérifications effectuées

- Tests navigateur : démarrage, 22 joueurs, score, tirs rapides, bouton rétro, têtes plongeantes, corners, six mètres, touches, sauvetages, fin de match et revanche.
- Tests d'interface aux formats 1440 × 820, 844 × 390 et 390 × 844.
- Test du mode local à deux joueurs et création de club personnalisé.
- Test de simulation d'une partie longue contre l'IA, sans erreur JavaScript relevée.

## Limites connues / prochaines priorités

C'est un **prototype jouable**, pas encore un jeu commercial fini ni une reproduction de la ROM. La qualité des animations, les différences entre joueurs, l'intelligence collective, les animations de touche/corner, les hors-jeu, les fautes, les pénaltys, le multijoueur en réseau et la jouabilité tactile doivent encore être éprouvés et perfectionnés. Le réglage de la difficulté est encore expérimental. Pour préserver les clubs personnalisés, utiliser **Exporter équipes**, surtout quand le HTML est ouvert depuis le disque local.

## Arborescence

- `Sensible_Soccer_2026_v0.2.html` : version autonome à ouvrir immédiatement
- `index.html`, `style.css`, `game.js` : sources de développement
- `README.md` : notice
- `tests/` : scripts de validation Playwright (environnement Python avec Playwright et Chromium)