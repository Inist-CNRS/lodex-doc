DIPONIBLE EN 8.18.7+

# Sparql

Le format texte dispose de plusieurs paramètres :

![](/assets/FormatSparqlTextAdmin.png)

Les paramètres `SPARQL endpoint`, `SPARQL request` et `max value` permettent de définir, pour le champ représenté, les éléments à afficher et la quantité.

## Sparql endpoint

Le paramètre `SPARQL endpoint` permet de sélectionner la base de données sparql \(//data.istex.fr/sparql/ par défaut\)

Le `SPARQL endpoint` doit être un URL valide.


## Sparql request

le paramètre `SPARQL request` contient la requête qu va être exécuté sur le endpoint.

Pour indiquer la ressource qui va être incluse dans la requête, il devra être signalé par `??`.

## Max value

le paramètre `max value` ignore la clause LIMIT pour la remplacer par la valeur fixée.

Augmenter le nombre de requête influ sur le temps de réponse du enpoint interrogé.



