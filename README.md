# Suivi de lecture

Interface web sur un Google Sheets privé : le tableur reste la base de données,
cette page en est une seconde porte d'entrée.

- Aucune donnée n'est stockée dans ce dépôt ni dans la page.
- La lecture et l'écriture passent par l'API Google Sheets, après connexion
  OAuth de la personne propriétaire du tableur.
- Sans cette connexion, la page n'affiche rien : l'identifiant du tableur seul
  ne donne aucun accès.
