# Other - ISTEX  Query

Ce format affiche la liste paginée des documents correspondant à une requête dans l'API ISTEX.

Les documents sont cliquables, et directement affichables \(le PDF\) dès lors que l'utilisateur en a le droit \(fait partie de l'Enseignement Supérieur et de la Recherche français\).

## Valeur

La valeur à donner à ce format n'est pas une URL, mais la partie _requête_, que l'on peut mettre au point dans le [démonstrateur ISTEX](http://demo.istex.fr/).

Elle suit la syntaxe d'interrogation de l'[API ISTEX](https://api.istex.fr/documentation/).

## Exemple

Valeur : `categories.inist.raw:("4 - vertebres: systeme cardiovasculaire")`

![](/assets/FormatIstexValue.png)

> **Remarque** : la propriété sémantique \(scheme\) utilisée pour une requête ISTEX est [istex:query](https://data.istex.fr/ontology/istex#query)



