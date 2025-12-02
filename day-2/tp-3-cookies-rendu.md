# TP : rendu et cookies

- Ajouter une page admin dans l’application

- Au clic sur un bouton « Se connecter » dans le layout, un cookie est défini `isAdmin`

- Lors de l’accès à la page admin, la présence du cookie est vérifiée avant l’accès à la page

- Si le cookie n’est pas présent, renvoyer vers une page d’erreur

- **Bonus** : Remplacer le bouton « Se connecter » par une page /login dédiée qui permet d’entrer un nom d’utilisateur et un mot de passe. Si lors de l’accès à la page `/login`, un cookie existe, renvoyer vers la page `/admin`.
