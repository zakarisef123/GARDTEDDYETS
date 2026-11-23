# Teddy-ets — Gard (30)

Site statique (HTML/CSS/JS, sans build) de Teddy-ets (SOS RENOV), entreprise de plomberie à Nîmes et dans tout le Gard (30).

## Structure

- `index.html` : accueil
- `urgence-plombier/`, `prestations/` et une page par prestation (fuite, débouchage, chauffe-eau, sanitaire, dégât des eaux, salle de bain, assainissement)
- `zones-intervention/` : secteurs et liste de toutes les communes
- `plombier/<commune>/` : une page par commune du Gard (350 communes, liste officielle geo.api.gouv.fr).
  Chaque page est **une copie exacte de l'accueil** (mêmes rubriques, même menu, même zone, même pied de page),
  avec le nom de la commune à la place de « Nîmes et tout le Gard » et **aucune mention du Gard**
  (pratique pour les annonces Google Ads ciblées par ville). La liste complète est sur `/zones-intervention/`.
- Les anciennes pages secteurs (`/plombier-nimes/`, `/plombier-ales/`…) sont redirigées (301, fichier `_redirects`)
  vers la page de la ville principale (`/plombier/nimes/`, `/plombier/ales/`…).
- `notre-entreprise/`, `realisations/`, `faq/`, `contact/`, `merci/`, mentions légales et confidentialité
- `assets/app.css` et `assets/app.js` : styles et scripts communs

## À compléter avant la mise en ligne

- **Nom de domaine** : les URL canoniques, le `sitemap.xml` et `robots.txt` utilisent l'adresse provisoire
  `https://gardteddyets.netlify.app`. À remplacer par le vrai domaine.
- **Mentions légales** (`mentions-legales/index.html`) : éditeur SOS RENOV renseigné ; restent `[À COMPLÉTER]` : TVA intracommunautaire, assureur, médiateur.
- **Suivi Google** : Google Tag Manager, Google Ads et la validation Search Console ne sont pas installés
  (identifiants propres à ce site à ajouter).
- **Formulaires** : envoyés via FormSubmit vers sos.renov10@gmail.com ; un e-mail d'activation FormSubmit sera envoyé
  au premier envoi depuis ce site. Pour utiliser une autre boîte, remplacer cette adresse dans les `action="https://formsubmit.co/..."`.
- **Téléphone** : 07 54 86 49 39 (constantes `PHONE`/`TEL`).
