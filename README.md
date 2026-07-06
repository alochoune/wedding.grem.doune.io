# Doune & Grem, site de mariage

Site web privé, protégé par code d'accès, pour informer les invités du mariage de Doune & Grem : samedi 28 mai 2028, Provence, France.

Site en ligne : https://alochoune.github.io/wedding.grem.doune.io/

Important : ce README est un simple fichier de documentation. Il ne modifie jamais l'apparence du site. Seul le fichier `index.html` (avec le dossier `photos/`) contrôle ce que voient les invités.

## Structure correcte du dépôt

Le dépôt ne doit contenir que ces fichiers et dossiers :

```
index.html
README.md
photos/
  photobooth-1.png
  gold-texture.jpg
  scroll-left.jpg
  scroll-right.jpg
  gallery/
    gallery-1.jpg
    gallery-2.jpg
    ... jusqu'à gallery-65.jpg
```

Aucun autre fichier ne doit se trouver à la racine (captures d'écran, doublons, etc.) : ça n'empêche pas le site de fonctionner mais ça encombre inutilement le dépôt.

## Contenu actuel du site

- Écran d'accès protégé par un code d'invitation (tulipe dessinée au trait)
- Compte à rebours jusqu'au jour J
- Notre histoire (complète)
- Programme du jour (fond bleu marine, texte blanc, pour marquer son importance)
- Le lieu (adresse, accès, parking)
- Hébergement : cartes par gîte avec la liste des invités qui y logent
- Code vestimentaire (old money vibes)
- Formulaire RSVP (envoi par e-mail)
- Tirelire collective pour le voyage de noces (cagnotte en ligne, plus une urne sur place)
- FAQ
- Galerie photo en fondu aléatoire (65 photos), avec bandes photo défilantes sur les côtés en version bureau uniquement
- Doré texturé (effet feuille d'or) sur le titre du hero, calibré à partir d'une image fournie

## Design

- Palette : ivoire, blanc, bleu de Marseille foncé, doré
- Typographie : Playfair Display et Cormorant Garamond (titres et texte), Cinzel (labels en petites capitales), Great Vibes (script)
- Signature visuelle : tulipe dessinée au trait sur l'écran d'accès, arche florale dans le hero

## Ce qu'il reste à compléter dans index.html

Cherchez `À COMPLÉTER` dans le fichier pour repérer chaque endroit concerné :

- Adresse complète du lieu (section Le lieu)
- Horaires et lieux précis du programme (cérémonie, vin d'honneur, dîner, soirée)
- Parking et accès
- Noms des gîtes, adresses, et listes d'invités assignés (section Hébergement, 4 cartes actuellement en placeholder)
- Précisions sur le code vestimentaire si besoin
- Lien vers la cagnotte en ligne (section Tirelire collective)
- Réponses FAQ restantes (enfants, transport, météo)
- Date limite de réponse au RSVP (actuellement `[date limite]`)

Le formulaire RSVP envoie actuellement un e-mail pré-rempli via `mailto:`. Pour un enregistrement automatique des réponses, il est possible de le relier à un service comme Formspree ou un Google Form à la place.

## Configuration technique

En haut de la balise `<script>` dans `index.html` :

```js
const ACCESS_CODE = "MOUSSE";
const WEDDING_DATE = "2028-05-28T15:00:00";
const MAILTO_ADDRESS = "votre-adresse@example.com";
```

`MAILTO_ADDRESS` doit être remplacé par une vraie adresse e-mail pour recevoir les réponses RSVP.

## Accès au site

Code d'invitation : `MOUSSE` (insensible à la casse : mousse, Mousse, MOUSSE fonctionnent tous).

Cette protection est côté navigateur uniquement : elle filtre les visites accidentelles mais n'est pas une sécurité forte, le code reste visible dans le code source.

## Mettre à jour le site

1. Ouvrir `index.html` sur GitHub
2. Icône crayon (éditer)
3. Cmd+A puis supprimer, coller le nouveau contenu
4. Commit changes

Le déploiement GitHub Pages se relance automatiquement, comptez 1 à 2 minutes.

## Hébergement

Déployé via GitHub Pages depuis la branche `main`, dossier racine.
