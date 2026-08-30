# SleepArc

App de recommandation de sommeil basée sur l'âge (saisi manuellement) et l'activité du jour, importée depuis l'app Santé via un Raccourci iOS.

Fichier unique (`index.html`), sans étape de build — React, Babel et Tailwind sont chargés depuis un CDN directement dans la page.

## Mettre en ligne avec GitHub Pages

1. Crée un nouveau dépôt sur GitHub (public, sans README/`.gitignore` ajoutés automatiquement).
2. Dans ce dossier :
   ```bash
   git remote add origin https://github.com/<ton-compte>/<nom-du-depot>.git
   git push -u origin main
   ```
3. Sur GitHub : **Settings → Pages → Source → Deploy from a branch → main → / (root)**.
4. L'app sera accessible sur `https://<ton-compte>.github.io/<nom-du-depot>/` après une à deux minutes.

## Sur l'iPhone

- Ouvre le lien dans Safari → bouton Partager → **Sur l'écran d'accueil**. L'app s'ouvre alors en plein écran, comme une vraie app.
- Le guide intégré (onglet **Guide** dans l'app) explique comment créer le Raccourci iOS qui exporte les données Santé, et comment le rendre automatique chaque matin.

## À savoir

- **Les données restent sur l'appareil** : elles sont stockées dans le navigateur (`localStorage`), pas envoyées à un serveur. Si tu changes de navigateur ou d'appareil, l'historique ne suit pas. Si tu effaces les données de site de Safari, l'historique est perdu.
- Le calcul du temps de sommeil recommandé est basé sur les repères de fourchettes d'âge des organismes de santé du sommeil ; il reste toujours dans une plage saine, quelle que soit l'activité du jour.
