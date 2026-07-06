[README.md](https://github.com/user-attachments/files/29711798/README.md)
# Doune & Grem — Site de mariage

Site web privé, protégé par code d'accès, créé pour informer les invités du mariage de Doune & Grem (mai 2028, Provence, France).

## Contenu du site

- Écran d'accès protégé par code d'invitation
- Compte à rebours jusqu'au jour J
- Notre histoire
- Programme du jour (cérémonie, vin d'honneur, dîner, soirée)
- Le lieu (adresse, accès, parking)
- Hébergement
- Code vestimentaire (*old money vibes*)
- Formulaire RSVP
- Liste de mariage
- FAQ
- Galerie photo

## Structure du dépôt

```
index.html       → la page du site (à ouvrir dans un navigateur)
photos/           → images utilisées sur le site (galerie, photomaton...)
```

## Accès

Le site est protégé par un code d'invitation saisi sur l'écran d'accueil. Le code n'est pas sensible à la casse (`MOUSSE`, `mousse`, `Mousse`... fonctionnent tous).

⚠️ Cette protection est uniquement côté navigateur : elle filtre les visites accidentelles mais ne constitue pas une sécurité forte (le code est visible dans le code source de la page).

## Personnalisation

Toutes les informations restant à compléter sont signalées dans le code par `À COMPLÉTER`. La configuration technique (code d'accès, adresse e-mail de RSVP, date du mariage) se trouve en haut de la balise `<script>` dans `index.html` :

```js
const ACCESS_CODE = "MOUSSE";
const WEDDING_DATE = "2028-05-20T15:00:00"; // à remplacer par la date exacte
const MAILTO_ADDRESS = "votre-adresse@example.com";
```

## Hébergement

Le site est déployé via **GitHub Pages** à partir de la branche `main`.
