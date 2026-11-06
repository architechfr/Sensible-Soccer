# SENSIBLE 2026 — Arcade Football v0.24

## Jouer

Ouvrir **Sensible_Soccer_2026_v0.24.html** dans Chrome ou Edge. Le jeu est un fichier HTML autonome (aucune ROM, installation ou connexion requise).

## Nouveautés v0.24 : le jeu sans ballon

- **A = récupération debout** : tente de prendre le ballon à proximité, avec distance et orientation prises en compte.
- **B = tacle glissé** : glissade visible sur plusieurs images, collision avec le porteur du ballon ou un ballon libre, dégagement si contact. Temporisation pour éviter les tacles en continu.
- **C = anticipation / interception** : avance sur la trajectoire du ballon, et tente une **tête** si celui-ci passe en hauteur.
- **Course et sprint** : déplacements plus directs, sprint ajusté et légère différence de vitesse en conduite de balle.
- **Interceptions automatiques** : une passe forte peut être déviée plutôt que capturée instantanément.
- **IA défensive** : placement collectif légèrement renforcé et interventions debout ou glissées selon la distance.
- **Animations** : pied tendu, glissade en mouvement, différence entre une tête debout et une tête plongeante.
- **Boutons tactiles** : libellés adaptés à l'attaque ou à la défense.

Le reste du prototype a été conservé : **22 joueurs (11 contre 11)**, équipes légendaires, modernes et personnalisées, buts, gardiens, corners, touches, six mètres, deux joueurs en local, caméra classique vue du dessus et ballon avec effet.

## Commandes Mega Drive (mode par défaut)

| Bouton | Clavier J1 | Avec ballon | Sans ballon |
| --- | --- | --- | --- |
| A | Espace | Passe | Récupération debout |
| B | X | Frappe dirigée | Tacle glissé |
| C | C | Tir assisté / dégagement | Anticipation, interception ou tête |

- **WASD / flèches** : déplacement, **Maj** : sprint, **Q** : changement de joueur, **V** : caméra, **Échap** : pause.
- **J2 en local** : flèches, **N** (A), **M** (B), **,** (C), **.** (changer), Maj droite (sprint).
- Téléphone : joystick gauche et trois boutons A/B/C à droite ; autres boutons pour sprint et changement de joueur.
- Le mode à un bouton de style Amiga reste disponible dans le menu.

## Tests

Des essais automatiques sur Chromium ont couvert les trois actions en attaque, les actions défensives, la trajectoire du tacle, les têtes, le mode local à deux joueurs, les remises en jeu et l'affichage mobile portrait/paysage. Aucune exception JavaScript relevée dans ces tests. Le rendu et l'équilibrage doivent néanmoins encore être éprouvés par de vrais joueurs et sur appareils réels.

## Limites de la version

Ce jeu est un **prototype original inspiré du football arcade 1990s**, pas une copie de la ROM. L'IA collective, le système de fautes, hors-jeu, les statistiques individuelles, les animations et les contacts doivent encore être approfondis. Le multijoueur en réseau n'est pas intégré. Les effectifs historiques et modernes sont indicatifs.

La branche principale GitHub et le projet Élio sont préservés : cette version est destinée aux tests.