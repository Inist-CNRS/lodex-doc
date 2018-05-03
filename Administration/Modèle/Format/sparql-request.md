# Sparql Pie Chart

![Cammebert](/assets/FormatPieChart.png)

Le camembert dispose de plusieurs paramètres : 

![](/assets/Sparql_Pie_Chart_Admin.png)

Les paramètres `Maximum fields number`, `min value` et `max value` permettent de définir, pour le champ représenté, les éléments à afficher. 

## Sparql_hostname

Le paramètre `Sparql_hostname` permet de selectionner la base de données sparql \(data.istex.fr/sparql/ par défaut\)


## Max value

Le paramètre `Max_value` détermine le nombre maximum d'éléments à afficher \(5 par défaut\). 

Le protocole (http/https) est facultatif mais utilisera par défaut https

Le `?query=` après l'uri est falculatif 

## Order by

L'ordre de tri peut prendre quatre valeurs en fonction:

* des éléments `Label` du champ représenté \(ordre alphabétique\)
  * Label ascendant
  * Label descendant
* des nombres d'apparitions \(`Valeur` \(_Value_\)\) des éléments du champ représenté
  * valeur croissante \(par défaut\)
  * valeur décroissante

![Ordres de tri du format Pie Chart](/assets/FormatBarChartOrderBy.png)

## Colour set \(jeu de couleurs\)

Ce paramètre permet de choisir la ou les couleur\(s\) du graphique.

La palette des couleurs se décrit par une liste de valeurs RGB hexadécimales séparées par un espace. Pour trouver facilement une palette lisible et plaisante, on peut utiliser l'outil [ColorBrewer](http://colorbrewer2.org/).

![Champ de saisie des couleurs du format Pie Chart](/assets/FormatColorsSet.png)

## Obligation

Ce format nécessite l'utilisation de requête avec un format prédifini.

Les données qui seront affichés dans le graphe devront être dans le SELECT et devront utilisé un alias : 
 * `?label` pour la légende
 * `?value` pour les valeurs du graphe

exemple: `(count(*) as ?value)` 




