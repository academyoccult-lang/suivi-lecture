# Suivi de lecture

Le Google Sheets reste la base de données. Cette app en est une seconde porte
d'entrée : elle lit et écrit **directement** via l'API Google Sheets, sans
intermédiaire. Plus de Apps Script.

- App en ligne : https://academyoccult-lang.github.io/suivi-lecture/
- Source : ce dossier (`~/Desktop/lecture-app`), relié au dépôt
  `academyoccult-lang/suivi-lecture`

## Publier une modification

    cd ~/Desktop/lecture-app
    git add -A && git commit -m "…" && git push

GitHub Pages se met à jour en une minute environ.

## Réglages

Dans l'app, bouton `Réglages` :

- **ID client OAuth** — obligatoire, obtenu une fois dans la console Google Cloud.
  L'origine à autoriser est `https://academyoccult-lang.github.io`.
- **Clé Google Books** — facultative mais recommandée : sans elle, seules les
  couvertures d'Open Library sont trouvées, et sa couverture du catalogue
  français est partielle.

L'objectif annuel reste piloté par la cellule **B4** du tableau de bord du
tableur. Les formules du Sheets continuent de tourner.

## Ce qui est public, ce qui ne l'est pas

Le dépôt est public, mais il ne contient **aucune donnée** : ni tes lectures,
ni tes clés. L'ID client OAuth et la clé Books vivent dans le stockage local de
ton navigateur. L'identifiant du tableur figure dans la page, mais il ne donne
aucun accès : sans connexion Google autorisée, l'API refuse tout.

## Hors ligne

L'app affiche la dernière version synchronisée, en lecture seule.
`Réglages` → `Exporter en JSON` pour une sauvegarde.
