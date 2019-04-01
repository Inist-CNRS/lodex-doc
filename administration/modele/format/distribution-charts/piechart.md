# Pie Chart

![Cammebert](../../../../.gitbook/assets/formatpiechart.png)

Le camembert dispose de plusieurs paramètres : ![Param&#xE8;tres du format Pie Chart](../../../../.gitbook/assets/formatpiechartparameters.png)

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

![Ordres de tri du format Pie Chart](../../../../.gitbook/assets/formatbarchartorderby.png)

## Colour set \(jeu de couleurs\)

Ce paramètre permet de choisir la ou les couleur\(s\) du graphique.

La palette des couleurs se décrit par une liste de valeurs RGB hexadécimales séparées par un espace. Pour trouver facilement une palette lisible et plaisante, on peut utiliser l'outil [ColorBrewer](http://colorbrewer2.org/).

![Champ de saisie des couleurs du format Pie Chart](../../../../.gitbook/assets/formatcolorsset.png)

## Routine

Ce format nécessite l'utilisation de la routine [distinct-by](../../../../configuration/routines/distinctby.md), appliquée à l'identifiant du champ représenté, qui doit être déclarée dans `valeur` \(_value_\) selon :

/api/run/distinct-by/**identifiant**/

où **identifiant** est le code attribué par LODEX au champ représenté.

