# 🧱 Better Brick Breaker (Arkanoïd)

Un jeu de casse-briques complet développé en Vanilla JavaScript (ES6) et HTML5 Canvas, basé sur les mécaniques du célèbre jeu Arkanoïd.

## ✨ Fonctionnalités

- **Mode Solo et Mode 2 Joueurs** : Jouez seul ou à tour de rôle ! Dans le mode 2 joueurs, le tour passe à l'autre joueur lorsqu'une vie est perdue.
- **Plusieurs niveaux** : Passage automatique au niveau suivant avec un système d'édition de niveau modulaire.
- **Briques variées** : Briques classiques avec différents niveaux de résistance et briques incassables (obstacles).
- **Power-ups & Malus** : 
  - 🏈 **MultiBall** : Divise la balle pour nettoyer l'écran plus vite.
  - 📏 **Large/Small** : Modifie la taille de la raquette de façon aléatoire.
  - 🔫 **Laser** : Permet de tirer sur les briques depuis la raquette.
  - 🔥 **Perforing Ball** : La balle traverse les briques sans rebondir.
  - 🧲 **Sticky Ball** : La balle reste collée à la raquette jusqu'au prochain tir.
- **Interfaces Modernes** : Menu de démarrage et écran de fin avec affichage du résultat final des deux joueurs.

## 🎮 Contrôles

- **Flèches Gauche / Droite** : Déplacer la raquette.
- **Barre Espace** : Relâcher la balle collée (début de manche ou bonus) et Tirer (avec le bonus Laser).

## 🚀 Installation & Utilisation

### Via Docker (Recommandé)
1. Exécutez le script d'initialisation : 
   ```bash
   ./init.sh
   # S'il n'est pas exécutable : chmod +x ./init.sh
   ```
2. Démarrez l'environnement : 
   ```bash
   docker-compose up
   ```
3. Ouvrez votre navigateur sur l'adresse locale indiquée par votre terminal (souvent `http://localhost:8080` ou similaire).

### Via NodeJS (Local)
1. Rendez-vous dans le dossier de l'application :
   ```bash
   cd app
   ```
2. Installez les paquets :
   ```bash
   npm install
   ```
3. Lancez le serveur de développement :
   ```bash
   npm run start
   ```

## 🛠️ Créer ses propres niveaux

Vous pouvez facilement dessiner vos niveaux dans le fichier `app/src/levels.json` sous forme de matrice.
Les valeurs correspondent à l'état de la brique :
- `0` : Espace vide
- `1` à `X` : Brique basique (le nombre correspond à ses points de vie/sa résistance)
- `-1` : Brique incassable

Amusez-vous bien ! 👾