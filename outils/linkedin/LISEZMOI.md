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
