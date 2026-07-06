[README.md](https://github.com/user-attachments/files/29719761/README.md)
# Doune & Grem, site de mariage

Site web privé, protégé par code d'accès, créé pour informer les invités du mariage de Doune & Grem (samedi 28 mai 2028, Provence, France).

## Contenu du site

- Écran d'accès protégé par code d'invitation (tulipe dessinée au trait)
- Compte à rebours jusqu'au jour J
- Notre histoire
- Programme du jour (fond bleu marine, texte blanc pour marquer son importance)
- Le lieu (adresse, accès, parking)
- Hébergement : cartes par gîte avec la liste des invités qui y logent
- Code vestimentaire (*old money vibes*)
- Formulaire RSVP
- Tirelire collective pour le voyage de noces (cagnotte en ligne + urne sur place)
- FAQ
- Galerie photo avec fondu enchaîné aléatoire, et bandes photo défilantes sur les côtés (desktop uniquement)

## Structure du dépôt

```
index.html            la page du site (à ouvrir dans un navigateur)
photos/
  photobooth-1.png     photo photomaton affichée en haut de la galerie
  gold-texture.jpg     texture dorée utilisée pour l'effet feuille d'or
  scroll-left.jpg      bande photo défilante, côté gauche
  scroll-right.jpg     bande photo défilante, côté droit
  gallery/             photos de la galerie principale (gallery-1.jpg, gallery-2.jpg, ...)
```

## Accès

Le site est protégé par un code d'invitation saisi sur l'écran d'accueil. Le code n'est pas sensible à la casse (`MOUSSE`, `mousse`, `Mousse`... fonctionnent tous).

Cette protection est uniquement côté navigateur : elle filtre les visites accidentelles mais ne constitue pas une sécurité forte (le code est visible dans le code source de la page).

## Personnalisation

Toutes les informations restant à compléter sont signalées dans le code par `À COMPLÉTER`. La configuration technique (code d'accès, adresse e-mail de RSVP, date du mariage) se trouve en haut de la balise `<script>` dans `index.html` :

```js
const ACCESS_CODE = "MOUSSE";
const WEDDING_DATE = "2028-05-28T15:00:00";
const MAILTO_ADDRESS = "votre-adresse@example.com";
```

Pour ajouter des photos à la galerie, déposez-les dans `photos/gallery/` puis ajoutez leur chemin dans la liste `GALLERY_PHOTOS` du script.

## Hébergement

Le site est déployé via GitHub Pages à partir de la branche `main`.
