# Jour 4

## Lien vers la <a href="https://annecemech.github.io/html-css-part-4/" target="_blank">démo</a>

## Lien vers le <a href="https://docs.google.com/presentation/d/e/2PACX-1vRPnC4IrNFnMUKN3GfLkolHloYTLVKHLnJQ4-D2FhVyndyBP8nlTTv-hRLqiOOH_RESiKNtexV9roKi/pub?start=false&loop=false&delayms=3000" target="_blank">cours</a>

Nous présentons ici l'intégration de plusieurs services en ligne dans notre site web. Chacun de ces sites fournis directement le code HTML/CSS/JS d'intégration.

## Google services

Google propose un grand nombre de services en ligne. Nous ne présentons ici que l'intégration de Google Map, d'une vidéo Youtube et d'une police Google Fonts.

Une fois le code d'intégration récupérer, il doit être collé là où l'on souhaite voir apparaitre le service.

### <a href="https://www.google.com/maps/" target="_blank">Google Map</a>

```html
<iframe
  src="https://www.google.com/maps/embed?pb=!1m16!1m12!1m3!1d45250.95061196091!2d-0.608091850603113!3d44.85854041698775!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!2m1!1smuffins!5e0!3m2!1sfr!2sfr!4v1560421401402!5m2!1sfr!2sfr"
  width="600"
  height="450"
  frameborder="0"
  style="border:0"
  allowfullscreen
></iframe>
```

### <a href="https://www.youtube.com/" target="_blank">Vidéo Youtube</a>

```html
<iframe
  width="500"
  height="300"
  src="https://www.youtube.com/embed/fBuSNu2m3XA"
  frameborder="0"
  allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
  allowfullscreen
></iframe>
```

### <a href="https://fonts.google.com/" target="_blank">Google Fonts</a>

Google fonts nous fournit deux lignes de code.

Une ligne permettant de faire le lien vers la feuille de style CSS de Google Fonts (balise "link") à coller dans le head du html (avant le link vers notre propre page de style "style.css) (l.6):

```html
<link
  href="https://fonts.googleapis.com/css?family=Pacifico&display=swap"
  rel="stylesheet"
/>
```

La seconde ligne est une propriété "font-family" qui doit être collé dans le fichier style.css, entre les accolades des élements que l'on souhaite modifier. Dans notre exemple les éléments sont les titres h1, h2, h3 et h4 modifiés aux lignes 10 et 15 :

```css
font-family: "Pacifico", cursive;
```

## <a href="https://fontawesome.com/" target="_blank">Font Awesome</a>

<a href="https://fontawesome.com/" target="_blank">Font Awesome</a> est un services qui permet de récupérer un grand nombre icones (dont les logo des réseaux sociaux) sous forme de police et donc de pouvoir modifier leur taille, leur couleur et leur couleur de fond très falicement (avec les propriétés font-size, color et background).

Il faut d'abord lier notre projet à Font Awesome. Pour cela on copie la ligne de code récupérér dans l'onglet "start" à la ligne 178 juste avant la fermeture de la balise </body> car la ligne inclut du JS :

```html
<script src="https://kit.fontawesome.com/18ee24e4d3.js"></script>
```

En suite, on choisi un icone. une fois l'icone choisi, on récupère le code d'intégration et on le colle là où l'on souhaite voir apparaitre l'icone. Dans notre exemple à la ligne 43, 46 et 49.

```html
<i class="fab fa-facebook-square"></i>
```

## <a href="https://getbootstrap.com/" target="_blank">Bootstrap</a>

<a href="https://getbootstrap.com/" target="_blank">Bootstrap</a> est un service proposé par twitter qui permet de récupérer une feuille CSS et une feuille de JS qui contiennent un grand nombre de classes et de fonctions. Cela nous permet donc de ne pas avoir à réécrir du style et du JS.

Dans l'onglet "Getting Strated" ont trouve deux bout de codes à copier dans notre fichier index.html.

### Le lien CSS

Il faut le copier dans le head avant le lien vers votre propre feuille de style (style.css). Attention si cette ligne est copiée après votre feuille de style, cela peut casser votre mise en page actuelle.

```html
<link
  href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
  rel="stylesheet"
  integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH"
  crossorigin="anonymous"
/>
```

### Les scripts JS

Ils faut copier le scripts à la fin de votre code, juste avant la fermeture de la balise </body>

```html
<script
  src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
  integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
  crossorigin="anonymous"
></script>
```

Une fois ces deux bouts de code collés, on peut commencer à utiliser bootstrap.

### Exemple 1 : La carte

```html
<div class="card">
  <img src="images/muffin1.jpg" class="card-img-top" alt="images/muffin1.jpg" />
  <div class="card-body">
    <h5 class="card-title">Muffin chocolat</h5>
    <p class="card-text">
      Les muffins au chocolat sont super bons.<br />Essayez les!
    </p>
    <a href="#" class="button button-success">Plus d'infos ici</a>
  </div>
</div>
```

### Exemple 2 : Le bouton

```html
<a href="#" class="button button-success">Plus d'infos ici</a>
```

### Exemple 3 : La modale

```html
<!-- Button trigger modal -->
<button
  type="button"
  class="button button-success"
  data-toggle="modal"
  data-target="#exampleModal"
>
  Contact
</button>

<!-- Modal -->
<div
  class="modal fade"
  id="exampleModal"
  tabindex="-1"
  role="dialog"
  aria-labelledby="exampleModalLabel"
  aria-hidden="true"
>
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button
          type="button"
          class="close"
          data-dismiss="modal"
          aria-label="Close"
        >
          <span aria-hidden="true">&times;</span>
        </button>
      </div>
      <div class="modal-body">
        <h3 class="color-green">MihiVai</h3>
        <p>contact@mihivai.com</p>
        <div>
          <a class="socials" href="">
            <i class="fab fa-facebook-square"></i>
          </a>
          <a class="socials" href="">
            <i class="fab fa-instagram"></i>
          </a>
          <a class="socials" href="">
            <i class="fab fa-linkedin"></i>
          </a>
        </div>
      </div>
      <div class="modal-footer"></div>
    </div>
  </div>
</div>
```

### Les grids

CSS Grid permet de créer facilement des mises en page en lignes et colonnes. C’est un outil puissant pour concevoir des designs flexibles et responsives.

Exemple avec une grille de 3 colonnes qui s’adapte aux différentes tailles d’écran :

```css
.cards-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
}
```

### Les media queries

Les media queries permettent d'adapter un site web à différents appareils et tailles d'écran. Elles appliquent des styles spécifiques en fonction de conditions comme la largeur de l'écran, ce qui est essentiel pour créer des designs responsives.

Exemple CSS pour ajuster la largeur d'un conteneur (.container) en fonction de la taille de l'écran :

```css
.container {
  width: 100%;
  max-width: 1140px;
  margin: 0 auto;
}

@media (max-width: 1200px) {
  .container {
    max-width: 960px;
  }
}

@media (max-width: 992px) {
  .container {
    max-width: 720px;
  }
}

@media (max-width: 768px) {
  .container {
    max-width: 540px;
  }
}

@media (max-width: 576px) {
  .container {
    max-width: 100%;
  }
}
```

Dans cet exemple, la largeur maximale du conteneur s'ajuste en fonction des tailles d'écran standards : ordinateurs de bureau, tablettes et mobiles.
