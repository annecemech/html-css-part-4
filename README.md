# Jour 4

### <a href="https://github.com/Joz84/ten-hours-of-html-css" target="_blank">Retour au menu principal</a>

## Lien vers la <a href="https://joz84.github.io/day-d.github.io/" target="_blanck">démo</a>

Nous présentons ici l'intégration de plusieurs services en ligne dans notre site web. Chacun de ces sites fournis directement le code HTML/CSS/JS d'intégration.

## Google services
Google propose un grand nombre de services en ligne. Nous ne présentons ici que l'intégration de Google Map, d'une vidéo Youtube et d'une police Google Fonts.

Vous trouverez ici les imprim-écrans des différentes étapes à suivre pour intégrer ces différents services :

<a href="https://docs.google.com/presentation/d/e/2PACX-1vTLmGtfz9n-WrBU_SiyQgcKNcaaRmbqAAmJ5BQuWSUupa2B9sqL04YmkLfjyHc_cxZwL3o_t6Im3c-g/pub?start=false&loop=false&delayms=60000" target="_blanck">Google services demo</a>

Une fois le code d'intégration récupérer, il doit être collé là où l'on souhaite voir apparaitre le service. 

### <a href="https://www.google.com/maps/" target="_blanck">Google Map</a>(l.132)
```html
<iframe src="https://www.google.com/maps/embed?pb=!1m16!1m12!1m3!1d45250.95061196091!2d-0.608091850603113!3d44.85854041698775!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!2m1!1smuffins!5e0!3m2!1sfr!2sfr!4v1560421401402!5m2!1sfr!2sfr" width="600" height="450" frameborder="0" style="border:0" allowfullscreen></iframe>
```
### <a href="https://www.youtube.com/" target="_blanck">Vidéo Youtube</a>(l.82)
```html
<iframe width="500" height="300" src="https://www.youtube.com/embed/fBuSNu2m3XA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

### <a href="https://fonts.google.com/" target="_blanck">Google Fonts</a>
Google fonts nous fournit deux lignes de code. 

Une ligne permettant de faire le lien vers la feuille de style CSS de Google Fonts (balise "link") à coller dans le head du html (avant le link vers notre propre page de style "style.css) (l.6):
```html
<link href="https://fonts.googleapis.com/css?family=Pacifico&display=swap" rel="stylesheet">
```

La seconde ligne est une propriété "font-family" qui doit être collé dans le fichier style.css, entre les accolades des élements que l'on souhaite modifier. Dans notre exemple les éléments sont les titres h1, h2, h3 et h4 modifiés aux lignes 10 et 15 :
```css
font-family: 'Pacifico', cursive;
```

## <a href="https://fontawesome.com/" target="_blanck">Font Awesome</a>

<a href="https://fontawesome.com/" target="_blanck">Font Awesome</a> est un services qui permet de récupérer un grand nombre icones (dont les logo des réseaux sociaux) sous forme de police et donc de pouvoir modifier leur taille, leur couleur et leur couleur de fond très falicement (avec les propriétés font-size, color et background). 

Vous trouverez ici les imprim-écrans des différentes étapes à suivre pour intégrer ce service :

<a href="https://docs.google.com/presentation/d/e/2PACX-1vR_nPGm05oNGHC-bbJDOYtubMDld9FiunNOBVQR0h_i4oE8uU_vCAXtOrcuxze172Mc9e7l3xeTnjUm/pub?start=false&loop=false&delayms=60000" target="_blanck">Font Awesome demo</a>

Il faut d'abord lier notre projet à Font Awesome. Pour cela on copie la ligne de code récupérér dans l'onglet "start" à la ligne 178 juste avant la fermeture de la balise </body> car la ligne inclut du JS :
```html
<script src="https://kit.fontawesome.com/18ee24e4d3.js"></script>
```
En suite, on choisi un icone. une fois l'icone choisi, on récupère le code d'intégration et on le colle là où l'on souhaite voir apparaitre l'icone. Dans notre exemple à la ligne 43, 46 et 49.
```html
<i class="fab fa-facebook-square"></i>
```

## <a href="https://getbootstrap.com/" target="_blanck">Bootstrap</a>

<a href="https://getbootstrap.com/" target="_blanck">Bootstrap</a> est un service proposé par twitter qui permet de récupérer une feuille CSS et une feuille de JS qui contiennent un grand nombre de classes et de fonctions. Cela nous permet donc de ne pas avoir à réécrir du style et du JS.

Vous trouverez ici les imprim-écrans des différentes étapes à suivre pour intégrer ce service :

<a href="https://docs.google.com/presentation/d/e/2PACX-1vRN32BRSc27tVZ5qZtwkxMuMkMY6ynF-PUHDHsRyFiaIMvy0yDlmSpYYOakTcNr_-7pTBX5acufW6ly/pub?start=false&loop=false&delayms=60000" target="_blanck">Bootstrap demo</a>

Dans l'onglet "Getting Strated" ont trouve deux bout de codes à copier dans notre fichier index.html.
### Le lien CSS (l.7)
Il faut le copier dans le head avant le lien vers votre propre feuille de style (style.css). Attention si cette ligne est copiée après votre feuille de style, cela peut casser votre mise en page actuelle.
```html
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
```

### Les scripts JS (l.180-182)
Ils faut copier les scripts à la fin de votre code, juste avant la fermeture de la balise </body>
```html
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>
```

Une fois ces deux bouts de code collés, on peut commencer à utiliser bootstrap.
### Exemple 1 : La carte (l.142-149, 151-158, 160-167)
```html
      <div class="card" style="width: 18rem;">
        <img src="images/muffin1.jpg" class="card-img-top" alt="images/muffin1.jpg">
        <div class="card-body">
          <h5 class="card-title">Muffin chocolat</h5>
          <p class="card-text">Les muffins au chocolat sont super bons.<br>Essayez les!</p>
          <a href="#" class="btn btn-success">Plus d'infos ici</a>
        </div>
      </div>
```

Nous avons créer 3 cartes produits que nous avons aligné horizontalement grace à des classes flexbox également fournies par bootstrap, lignes 141-168.
```html
<div class="d-flex justify-content-between">
...
</div>
```   
      
### Exemple 2 : Le bouton (l.147, 156, 165)
```html
<a href="#" class="btn btn-success">Plus d'infos ici</a>
```

### Exemple 3 : La modale (l.29-57)

```html
      <!-- Button trigger modal -->
      <button type="button" class="btn btn-success" data-toggle="modal" data-target="#exampleModal">
        Contact
      </button>

      <!-- Modal -->
      <div class="modal fade" id="exampleModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
        <div class="modal-dialog" role="document">
          <div class="modal-content">
            <div class="modal-header">
              <button type="button" class="close" data-dismiss="modal" aria-label="Close">
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
            <div class="modal-footer">
            </div>
          </div>
        </div>
      </div>
```

