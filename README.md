# Nu — Pure HTML/CSS E-Commerce Site

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![No JavaScript](https://img.shields.io/badge/JavaScript-none-lightgrey?style=flat&logo=javascript)

> **Challenge:** rebuild a complete e-commerce site without a single line of JavaScript.

A personal project to push HTML5 and CSS3 to their limits (mobile navigation, dropdowns, interactive selectors) without any JS.

---

## Pages

| File | Description |
|---|---|
| `index.html` | Home : hero, promotions, collections |
| `costumes_homme.html` | Product catalog (responsive grid) |
| `costume_tanin.html` | Product page : gallery, size selector, add to cart |
| `full_bag.html` | Filled cart |
| `empty_bag.html` | Empty cart |
| `qui_sommes_nous.html` | About |

---

## CSS Techniques Without JavaScript

### Burger menu
The mobile menu works via a hidden checkbox.

```css
#scrolling_menu:checked + .menu { display: flex; }
```

A `<label>` acts as the toggle button : state is managed by `:checked`, no event listener.

### Interactive size selector
Radio buttons are hidden and replaced by styled `<label>` elements. The active state is rendered via `:checked + label`.

```css
input[name="size_"] { display: none; }
input:checked + label { border: 1px solid #1f326d; }
```

### Hover dropdowns
Submenus are hidden by default and revealed on parent `:hover`, absolutely positioned.

### Icon swap on hover
Social icons switch to grayscale on hover via the `content` property.

```css
#img_yt:hover { content: url("images/yt_g.png"); }
```

### Responsive without a framework
Flexbox + native media queries across 6 breakpoints (from 370px to 1250px), no Bootstrap or other dependency.

---

## Stack

- Semantic **HTML5**
- **CSS3** : Flexbox, pseudo-selectors (`:checked`, `:hover`, `:first-of-type`), `@font-face`
- [Quicksand](https://fonts.google.com/specimen/Quicksand) font self-hosted (3 weights)
- No external dependencies

---

## Run the project

```bash
git clone https://github.com/<username>/nu.com.git
cd nu.com
# Open index.html in a browser
```

No build step, no server required.

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
├── style.css               # Global styles, @font-face
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
