# Sensible Soccer 2026 — v0.25 / Sélection intelligente

Jeu d'arcade de football autonome, inspiré des sensations des jeux des années 1990. Cette version originale n'utilise pas la ROM de Sensible Soccer.

## Jouer

Ouvrir `Sensible_Soccer_2026_v0.25.html` dans Chrome ou Edge. Aucun serveur ni installation requis.

## Priorité de cette version : choisir le bon joueur

- **Automatique par défaut** : au lieu d'attendre d'avoir perdu le ballon de plusieurs mètres, le moteur classe les joueurs selon leur proximité et leur capacité à atteindre la trajectoire.
- **Anticipation** : calcul d'une position future du ballon (en tenant compte du ralentissement) et priorité à l'interception d'une passe rapide.
- **Sens du jeu** : en défense, préférence mesurée pour un joueur entre l'attaquant et notre but ; sur les passes rapides, préférence pour le joueur placé sur la trajectoire plutôt que derrière elle.
- **Moins de changements incontrôlés** : petite marge d'amélioration requise avant de basculer sur un nouveau joueur ; sélection stabilisée pendant la course et une action engagée.
- **Porteur du ballon** : sélection immédiate de celui qui reçoit ou récupère la possession.
- **Forçage manuel** : touche Q (joueur 1) ou . (joueur 2), bouton FORCER sur mobile, gâchette haute sur manette compatible. Verrou manuel de 1,12 seconde, sauf prise de possession par un coéquipier.
- **Q + direction** : tente de choisir un joueur pertinent dans cette direction.
- **Indicateur** : l'anneau de sélection devient orangé lors d'un choix manuel.

## Commandes, mode Mega Drive

- Joueur 1 : **WASD** / flèches (solo), **Espace (A)** passe / récupération, **X (B)** tir / tacle glissé, **C (C)** tir assisté / interception ou tête, **Maj** sprint, **Q** choix forcé, **Échap** pause.
- Joueur 2 sur le même PC : **flèches**, **N (A)**, **M (B)**, **virgule (C)**, **point** choix forcé, **Maj droite** sprint.
- Tactile : joystick, trois boutons d'action, sprint, FORCER.

## Vérifications

Tests Playwright sur Chromium : 22 joueurs, sélection automatique du plus proche, anticipation d'une passe rapide, forçage manuel, maintien temporaire du choix, retour au mode automatique, sélection automatique du porteur et symétrie du joueur 2. Aucune erreur JavaScript observée sur ces scénarios.

## Points encore ouverts

Cette version corrige la logique de sélection, mais l'intelligence tactique, les animations, les contacts physiques, l'équilibrage des courses et les gardiens restent à affiner par de véritables parties humaines. Les effectifs modernes sont indicatifs. Pas de multijoueur réseau à ce stade.

Dépôt : `architechfr/Sensible-Soccer`, branche de test `prototype/sensible-2026-v025-selection`. La branche principale et le projet `ELIO-anniversaire` ne sont pas modifiés.