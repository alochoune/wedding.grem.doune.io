# Doune & Grem, site de mariage

Site web privé, protégé par code d'accès, créé pour informer les invités du mariage de Doune & Grem (samedi 28 mai 2028, Provence, France).

🔗 Site en ligne : https://alochoune.github.io/wedding.grem.doune.io/

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

## Design

- Palette : ivoire parchemin, bleu marine, lavande, olive, doré
- Typographie : Cormorant Garamond (titres), EB Garamond (texte), Jost (labels)
- Signature visuelle : tulipe dessinée au trait, présente sur l'écran d'accès et en en-tête

## À personnaliser avant publication

Le fichier `index.html` contient des espaces réservés entre crochets `[...]` à remplacer :
- Nom et adresse exacts du lieu
- Détails d'accès et de parking
- Texte de "Notre histoire"
- Lieu précis de la cérémonie
- Date limite de réponse au RSVP
- Lien réel de la cagnotte
- Code d'accès (`ACCESS_CODE` dans le `<script>`, actuellement `MOUSSE`)

Le formulaire RSVP est un placeholder : à connecter à un service comme Formspree ou un Google Form pour recevoir réellement les réponses.

## Déploiement

Le site est déployé automatiquement via **GitHub Pages** à chaque `push` sur la branche `main`.
