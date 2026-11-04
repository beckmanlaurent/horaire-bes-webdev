# Horaire BES Webdeveloper 2026–2027

Site statique qui affiche l'horaire du BES Webdeveloper (1ère et 2ème année) semaine par semaine ou mois par mois.

- Vue **Semaine** et vue **Mois**, navigation avec les flèches du clavier
- Choix **1ère / 2ème** (mémorisé dans le navigateur)
- Prochain cours, congés et vacances, progression de chaque cours
- Données reprises de la grille officielle datée du 25/09/2026

## Structure

```
index.html                  le site (HTML, CSS et JS dans un seul fichier)
data/horaire-2026-2027.json toutes les séances, date par date
```

## Lancer en local

Ouvre `index.html` dans un navigateur, il n'y a rien à installer.

## Déploiement

Site statique sans build : sur Vercel, importer le repo avec le preset **Other**, sans commande de build.
