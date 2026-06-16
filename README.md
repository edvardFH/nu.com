# Nu : Site marchand HTML/CSS pur

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![No JavaScript](https://img.shields.io/badge/JavaScript-aucun-lightgrey?style=flat&logo=javascript)

> **Défi :** recréer un site e-commerce complet sans une seule ligne de JavaScript.

Projet personnel pour approfondir HTML5 et CSS3 en repoussant leurs limites : navigation mobile, menus déroulants, sélecteurs interactifs : entièrement sans JS.

---

## Pages

| Fichier | Description |
|---|---|
| `index.html` | Accueil : hero, promotions, collections |
| `costumes_homme.html` | Catalogue produits (grille responsive) |
| `costume_tanin.html` | Fiche produit : galerie, sélecteur de taille, ajout au panier |
| `full_bag.html` | Panier rempli |
| `empty_bag.html` | Panier vide |
| `qui_sommes_nous.html` | À propos |

---

## Techniques CSS sans JavaScript

### Menu burger
Le menu mobile fonctionne via une checkbox cachée.

```css
#scrolling_menu:checked + .menu { display: flex; }
```

Une `<label>` agit comme bouton : l'état est géré par `:checked`, aucun event listener.

### Sélecteur de taille interactif
Les radio buttons sont masqués et remplacés par des `<label>` stylisées. L'état actif est rendu via `:checked + label`.

```css
input[name="size_"] { display: none; }
input:checked + label { border: 1px solid #1f326d; }
```

### Sous-menus au survol
Les sous-menus sont cachés par défaut et révélés au `:hover` du parent, positionnés en absolu.

### Swap d'icônes au hover
Les icônes sociales passent en niveaux de gris au survol via la propriété `content`.

```css
#img_yt:hover { content: url("images/yt_g.png"); }
```

### Responsive sans framework
Flexbox + media queries natives sur 6 breakpoints (de 370 px à 1250 px), sans Bootstrap ni autre dépendance.

---

## Stack

- **HTML5** sémantique
- **CSS3** : Flexbox, pseudo-sélecteurs (`:checked`, `:hover`, `:first-of-type`), `@font-face`
- Police [Quicksand](https://fonts.google.com/specimen/Quicksand) auto-hébergée (3 niveaux de gras)
- Aucune dépendance externe

---

## Lancer le projet

```bash
git clone https://github.com/<username>/nu.com.git
cd nu.com
# Ouvrir index.html dans un navigateur
```

Aucun build, aucun serveur requis.

---

## Structure

```
nu.com/
├── index.html
├── costumes_homme.html
├── costume_tanin.html
├── full_bag.html
├── empty_bag.html
├── qui_sommes_nous.html
├── style.css               # Styles globaux, @font-face
├── header.css
├── footer.css
├── main_index.css
├── main_costumes_hommes.css
├── main_costume_tanin.css
├── main_empty_bag.css
├── main_full_bag.css
├── images/
└── font/
```
