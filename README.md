# Simu Moto

Simulateur de moto 3D sur route de col, jouable dans le navigateur.

**▶ Démo en ligne : [https://yoannservices.github.io/moto-rider/](https://yoannservices.github.io/moto-rider/)**

## Fonctionnalités

- Choix de la moto, du décor (montagne ou route ouverte), de la lumière et des aides
- Plusieurs caméras : 3e personne, pilote, roue avant
- Puissances et poids proches des valeurs constructeur (arrondies)

## Commandes

| Touche | Action |
|---|---|
| Z / W / ↑ | Gaz |
| S / ↓ | Freins |
| Q / A / ← | Gauche |
| D / → | Droite |
| C | Caméra |
| Clic gauche + glisser | Tourner la caméra |
| R | Remettre sur la route |
| Échap | Menu |

## Lancer en local

Aucune installation : ouvrez `index.html` dans un navigateur, ou servez le dossier :

```bash
python -m http.server 8000
```

puis allez sur http://localhost:8000 (dans le dossier `web/` de Mes Projets : http://localhost:8000/loisirs/moto-rider/).

## Structure

- `index.html`, `style.css`
- `js/main.js` : le simulateur

## À savoir

Le comportement est une simulation simplifiée, pas un modèle de course.

## Technologies

HTML, CSS et JavaScript ; rendu 3D avec [Three.js](https://threejs.org/) r186 (chargé depuis un CDN par `assets/three-compat.js`). Sans étape de build.

---

Fait partie de [Mes Projets](https://yoannservices.github.io/) · [Portfolio](https://yoannservices.github.io/portfolio/) · par [@yoannservices](https://github.com/yoannservices)

## Fiche technique

Résumé de ce que fait le code, tenu à jour à chaque modification : le lire suffit pour vérifier une information sans relire tout le jeu.

- **Code** : `js/main.js` (script classique).
- **Motos** : Ducati V4R = `ducati-v4r.glb` (yaw 0), les autres = `yamaha-r1.glb` (yaw π) ; pilote procédural.
- **Caméras (C)** : 0 poursuite (distance 4,6 + vitesse × 1,6, orbite à la souris, retour derrière après 1,5 s) ; 1 vue casque (œil (0 ; 1,28 ; 0,1) du repère moto, horizon à moitié incliné) ; 2 vue pilote (position de la tête, vibrations selon la vitesse et le hors-piste).

## Crédits des modèles 3D

Véhicules réels sous licence CC-BY (Sketchfab) : auteurs et licences dans `assets/models/CREDITS.md`.
