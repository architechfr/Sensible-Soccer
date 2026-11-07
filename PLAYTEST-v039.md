# Sensible Soccer 2026 — v0.39 : ralentis, célébrations et arbitrage

Version HTML autonome construite sur la v0.38. Prototype original ; ne modifie pas la ROM du jeu de référence.

## Jouer

Ouvrir `index.html` dans un navigateur. Sur mobile, tourner le téléphone en paysage, puis activer le plein écran proposé. Les réglages d'équipe et de durée sont sur le menu initial.

## Ajouts principaux

- **Après un but :** marquage du score, clameur, célébration du buteur les bras levés et rapprochement des partenaires, puis ralenti de la dernière action réellement enregistrée, avant un nouvel engagement.
- **Grosse occasion ratée :** si une frappe récente et suffisamment rapide passe juste à côté d'un poteau ou juste au-dessus du cadre, une courte reprise au ralenti affiche la trajectoire enregistrée. Les six mètres et corners continuent ensuite normalement.
- **Buts plus visibles :** ouverture agrandie (216 unités contre 180), profondeur du filet et montant supérieur accentués.
- **Sons :** effets de foule originaux générés dans le navigateur : clameur sur un but, « ooh » synthétique sur les tirs frôlant le cadre, réaction sur faute ; sifflet arbitral distinct.
- **Sanctions :** affichage des cartons jaunes et rouges ; exclusion et match à dix après un tacle glissé par derrière sanctionné.

## Contrôles

- Déplacement : joystick mobile / WASD au clavier.
- A : passe ou interception.
- B : tir ou tacle glissé.
- C : centre/passe en profondeur, action contextuelle sans ballon.
- Maintien des boutons : puissance ; joystick après frappe : effet.
- Q : sélection manuelle temporaire.

## Validation

Tests automatisés Chromium à 1280×720 et 844×390 : coup d'envoi, séquence de but et célébration, ralenti puis reprise, frappe manquée proche du cadre, carton rouge et passage à dix, absence d'erreur JavaScript. Le rendu et les sons restent à apprécier en match réel sur chaque appareil.

## Limites

- Les réactions du public sont des sons de synthèse, pas des enregistrements de voix.
- Le ralentissement utilise des positions des joueurs et de la balle mémorisées sur les dernières secondes, non une vidéo capturée.
- Les règles disciplinaires sont simplifiées par rapport au football officiel. Les cas contestables de faute doivent être vérifiés pendant les tests.
- La finesse des animations et le rendu des gradins ne reproduisent pas encore l'original à l'identique.