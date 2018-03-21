# Bubble Chart

Le format `Graphique - Graphe à bulles` \(_Graph - Bubble_\) montre les corrélations \(regroupement de bulles\) et les poids \(taille des bulles\) des différents éléments du champ représenté, montrant ainsi les proportions des différentes valeurs.

![Exemple de Bubble Chart](/assets/FormatBubbleChart.png)

## Paramétrage

![](/assets/FormatBubbleChartParameters.png)

Ce format propose 2 paramètres :

1. `jeu de couleurs` \(_colour scheme_\) : permet de choisir les couleurs du graphique à partir d'une série de palettes prédéfinies
2. `Diamètre des bulles` \(_Chart Diameter_\) : diamètre du graphique en pixels

## Routine

Ce format nécessite l'utilisation de la routine [distinct-by](/Configuration/routines/DistinctBy.md), appliquée à l'identifiant du champ représenté, qui doit être déclarée dans  `valeur` \(_value_\) selon:

/api/run/distinct-by/**identifiant**/

où **identifiant** est le code attribué par LODEX au champ représenté.

> **Voir aussi** : la section [Configuration/Routines](/Configuration/routines/README.md) et la routine [distinct-by](/Configuration/routines/DistinctBy.md).



