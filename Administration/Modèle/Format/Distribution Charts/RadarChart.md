# Radar Chart

![Exemple de Radar](/assets/FormatRadarChart.png)

## Paramétrage

![Paramètres du format Radar Chart](/assets/FormatRadarChartParameters.png)  
En plus des paramètres _Maximum fields number_, _max value_, _min value_, _Order by_, et _Colors set_, similaires à ceux des [diagrammes à barre](/Administration/Modèle/Format/Distribution Charts/BarChart.md) et des [camemberts](/Administration/Modèle/Format/Distribution Charts/PieChart.md), ce diagramme propose de forcer des valeurs entières ou de changer d'échelle.

## Maximum fields number, min value et max value

Les paramètres `Maximum fields number`, `min value` et `max value` permettent de définir, pour le champ représenté, les éléments à afficher.

Le paramètre `Maximum fields number` détermine le nombre maximum d'éléments à afficher \(5 par défaut\).

Les paramètres `min value` et `max value` définissent les éléments à afficher en fonction de leur nombre d'apparitions dans le corpus.

Seuls sont affichés les éléments dont le nombre d'apparitions est:

* supérieur à la valeur de `min value`
* inférieur à la valeur de `max value`

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

### Arrondir les valeurs sur l'axe \(_force rounded-up value in axis_\)

Quand cette case est cochée \(cochée par défaut\), les échelles des axes sont en nombres entiers.

Ce choix a été fait car, en [IST](https://fr.wikipedia.org/wiki/Information_scientifique_et_technique), les valeurs sont souvent des nombres de documents, donc des nombres entiers.

Si d'autres valeurs \(par exemple pourcentage, taux de citation, _etc_.\) sont représentées, il peut être intéressant d'avoir une échelle en nombres décimaux.

### échelle \(_scale_\)

Ce paramètre permet de changer l'échelle d'affichage des valeurs :

* par défaut, échelle linéaire \(_linear_\)  
  pour l'échelle linéaire, deux graduations dont la _différence_ vaut 10 sont à distance constante

* échelle logarithmique  
  lorsqu'un phénomène utilisant une gamme étendue de valeurs est étudié, l'échelle linéaire est mal adaptée. Une échelle logarithmique qui espace les valeurs faibles et rapproche les valeurs fortes est préférable.  
  Pour l'échelle logarithmique, deux graduations dont le _rapport_ vaut 10 sont à distance constante.

## Routine

Ce format nécessite l'utilisation de la routine distinct-by, appliquée à l'identifiant du champ représenté, qui doit être déclarée dans le paramètre `valeur` \(_value_\) selon :

/api/run/distinct-by/**identifiant**/

où **identifiant** est le code attribué par LODEX au champ représenté.

