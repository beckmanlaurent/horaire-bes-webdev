# Horaire BES Webdeveloper 2026–2027

Site statique qui affiche l'horaire du BES Webdeveloper (1ère et 2ème année) semaine par semaine ou mois par mois.

- Vue **Semaine** et vue **Mois**, navigation avec les flèches du clavier
- Choix **1ère / 2ème** (mémorisé dans le navigateur)
- Horaire perso : l'œil à côté d'un cours le masque partout (semaine, mois, prochain cours), mémorisé dans le navigateur
- Prochain cours, congés et vacances, progression de chaque cours
- Chat public en direct, avec un simple pseudo (messages stockés sur Supabase)
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

## Chat

Les messages sont dans la table `messages` du projet Supabase. L'URL et la clé publique dans `index.html` sont faites pour être visibles : côté base, elles permettent seulement de lire et d'envoyer des messages.

- Supprimer un message : tableau de bord Supabase, **Table Editor**, table `messages`
- Si le chat ne charge plus, vérifier que le projet n'a pas été mis en pause par Supabase pour inactivité
- Ne jamais mettre la clé `secret` ni le mot de passe de la base dans le site (le mot de passe est dans `.env.local`, ignoré par Git)
