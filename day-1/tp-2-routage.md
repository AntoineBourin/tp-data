# TP Routage & navigation

- Récupérer les produits et les afficher dans une **page d’accueil** (`mocked.ts`).

- Ajouter un **layout** avec un **menu de navigation** vers différentes pages (par exemple **Contact**, **Accueil**…).

- Permettre la **navigation** vers une **page produit** avec un lien vers `/product/{id}`.  
  La page produit **redirige vers une page 404** si l’ID du produit n’est pas trouvé.

- **Bonus** : la page d’accueil peut prendre un paramètre `?query` qui, si précisé, **filtre les produits** par titre.

- **Bonus** : le paramètre `query` peut être **modifié via un champ de recherche** dédié.

---

### Ressources

- [Fichiers de routage](https://nextjs.org/docs/app/getting-started/project-structure#routing-files)
- [notFound](https://nextjs.org/docs/app/api-reference/functions/not-found)
