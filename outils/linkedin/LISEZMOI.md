# Visuels LinkedIn RH Facility

Cartes et carrousels 1080×1350 (format portrait LinkedIn), faits sans outil externe.

- `base.css` : charte (bordeaux #5C1522 / #7B1E2E, filet doré #c9a96e, Playfair Display + DM Sans, polices dans `fonts/`).
- Une page HTML par post dans `semaines/AAAA-MM-JJ/` ; chaque `<section class="slide">` devient une image.
- Rendu : `node outils/linkedin/render.mjs <page.html> linkedin <AAAA-MM-JJ-sujet>`
- Les images sont servies par GitHub Pages sur `https://celine06800.github.io/rh-facility-media/linkedin/…` pour que Metricool les récupère.
  Ce dépôt ne contient que des visuels publics : il est séparé de l'application RH Facility, qui n'est jamais modifiée.
  Les posts restent en brouillon dans Metricool jusqu'à la validation de Céline.

Règles : vouvoiement, faits RH Facility vérifiés dans le code (prix HT), règles juridiques vérifiées sur une source officielle,
aucun témoignage ni chiffre client inventé (voir le skill contenu-rh-facility).

## Vidéos (ajout du 02/11/2026)

Une petite vidéo animée toutes les 2 semaines, à la place d'un visuel fixe, sur le post qui s'y prête le mieux.

- Format : 1080 × 1350 (portrait 4:5), 15 à 30 s, 30 images/s, **sans son** (LinkedIn lance les vidéos en muet) : tout le message est écrit à l'écran, sans visage, sans image générée par IA.
- `anim.css` : animations à poser sur les éléments avec un délai `--d` (en secondes) : `.fondu`, `.monte`, `.gauche`, `.zoom`, `.trace` (filet qui se dessine), `.compteur`, `.sort` ; `.scene` = un écran plein qui entre à `--d` et sort à `--f` (contenu centré).
- Accroche lisible dès la 1re image : première scène et titre avec `--d:-1s`.
- Rendu : `node outils/linkedin/render-video.mjs <page.html> <durée_s> linkedin/<AAAA-MM-JJ-sujet>.mp4`, puis contrôle de 5 à 6 images avec ffmpeg avant mise en ligne.
- Une page par vidéo dans `semaines/AAAA-MM-JJ/` (avec `<link rel="stylesheet" href="../../anim.css">`).
- Exemple validé : voir la page `exemple-video-*.html` de ce dossier.
- Dans Metricool : `media` = l'adresse publique du MP4 (`https://celine06800.github.io/<dépôt>/linkedin/<fichier>.mp4`), `linkedinData {"type":"post"}`.
