8.20.2+

# Sparql

Le format SPARQL texte dispose de plusieurs paramètres :

![](/assets/FormatSparqlTextAdmin.png)

Les paramètres `SPARQL endpoint`, `SPARQL request` et `max value` permettent de définir, pour la ressource dédiée, les éléments à afficher et la quantité.

## Sparql endpoint

Le paramètre `SPARQL endpoint` permet de sélectionner la base de données SPARQL \(`https://data.istex.fr/sparql/` par défaut\)

Le `SPARQL endpoint` doit être un URL valide.

Les variables présentes dans la requête seront affichées en séparant les mots.  
Exemple :

* `label` → `Label` 
* `LibelleNomBnf` → `Libelle nom bnf` 
* `Lien_Catalogue_Bnf` → `Lien catalogue bnf`

De plus un lien vers un validateur SPARQL a été ajouté \(8.20.4+\)

## Sparql request

Le paramètre `SPARQL request` contient la requête qu va être exécutée sur le _endpoint_.

Pour indiquer la ressource qui va être incluse dans la requête, elle devra être signalée par "`??`".

Si la valeur de la ressource ou le corps de la requête est incorrect, la requête retournera une erreur et affichera `We are not able to display data`.

Les valeurs ne seront prises en compte que lors du chargement de la page.

## Max value

Le paramètre `max value` ignore la clause LIMIT pour la remplacer par la valeur fixée.

Augmenter le nombre de requêtes influe sur le temps de réponse du _enpoint_ interrogé.

Autrement dit, c'est le nombre de lignes \(ou de résultats\) affichées.

## Hide resource field & separator

À partir de la de la version 8.20.4+ il est possible de masquer le champ indiquant la ressource ainsi que le sparql endpoint.

En utilisant dans la requête une concaténation, il est possible d'afficher la valeur en forme de liste en indiquant le séparateur.  
![Hide resource &amp; separator](/assets/FormatSparqlTextUpgrade1.png)

## Exemple

* Valeur du champ : `Physiology`
* Requête SPARQL \(notez les `??`\) :

```sql
PREFIX skos: <http://www.w3.org/2004/02/skos/core#>
SELECT ?genericLabel
WHERE {
  ?wosCat skos:prefLabel "??"@en .
  ?wosCat skos:broader ?generic .
  ?generic skos:prefLabel ?genericLabel .
}
```

Dans ce cas, c'est la requête suivante qui sera exécutée avec le SPARQL EndPoint [https://data.istex.fr/sparql/](https://data.istex.fr/sparql/)

```sql
PREFIX skos: <http://www.w3.org/2004/02/skos/core#>

SELECT ?genericLabel
WHERE {
  ?wosCat skos:prefLabel "Physiology"@en .
  ?wosCat skos:broader ?generic .
  ?generic skos:prefLabel ?genericLabel .
}
LIMIT 1
```

avec le résultat suivant:

![](/assets/ResultExempleSparqlText.png)

