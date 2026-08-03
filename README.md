# Aude & Charles — wedding website

This repository contains the wedding website source and the GitHub Pages deployment setup.

## Site content

The main site page is available at [version 1 site/index (4).html](version%201%20site/index%20(4).html).
A redirect entry page is also provided at [index.html](index.html) so GitHub Pages serves the site correctly from the repository root.

## Deployment

The site is published through GitHub Pages using the workflow in [.github/workflows/deploy-pages.yml](.github/workflows/deploy-pages.yml).

Any push to the main branch will trigger an automatic deployment.

## Updating the site

1. Edit the HTML content in [version 1 site/index (4).html](version%201%20site/index%20(4).html).
2. Commit the change.
3. Push to main.
4. GitHub Actions will publish the updated site automatically.
