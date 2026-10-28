# Dossier photographique

Application web pour photographier un site et situer chaque photo sur les plans (point de prise de vue et direction), puis produire un dossier photographique en PDF A4 pour les administrations : page de garde avec cartouche, plans avec les points numérotés, photos numérotées.

## Utilisation

Ouvrir l'adresse de l'application dans le navigateur (Chrome sur Android, Safari sur iPad et iPhone), puis l'ajouter à l'écran d'accueil (Chrome : menu ⋮ > « Ajouter à l'écran d'accueil » ; Safari : Partager > « Sur l'écran d'accueil »). L'application fonctionne ensuite hors ligne.

## Données

Aucune donnée n'est envoyée sur un serveur et l'app n'utilise aucune intelligence artificielle. Les dossiers, plans et photos restent dans le navigateur de l'appareil. Ils sont perdus si les données du navigateur sont effacées : utiliser la sauvegarde (rubrique « Dossier »).

## Contenu du dépôt

- `index.html` : l'application
- `sw.js`, `manifest.webmanifest`, `icons/` : installation et fonctionnement hors ligne
- `vendor/pdf.min.js`, `vendor/pdf.worker.min.js` : lecture des plans PDF (pdf.js 3.11.174, licence Apache 2.0)
- `vendor/jspdf.umd.min.js` : génération des PDF (jsPDF 2.5.1, licence MIT)
- `fonts/` : polices Barlow (interface) sous licence SIL OFL 1.1 ; la police Carlito (PDF), également sous SIL OFL 1.1, est intégrée dans `index.html`

## Mise à jour

Après avoir remplacé `index.html` ou un autre fichier, augmenter le numéro `VERSION` dans `sw.js` (par exemple `dossier-photo-v2`), sinon les appareils garderont l'ancienne version en cache.
