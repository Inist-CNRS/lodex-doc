# Distribution Charts

Les diagrammes de distribution montrent le nombre de fois où chaque élément du champ représenté apparaît dans le corpus:

* nombre d'occurrences si le champ n'est pas dédoublonné
* nombre de documents si le champ est dédoublonné

Les diagrammes de distribution fonctionnent de la même manière \(avec les mêmes données\), mais prennent des formes différentes:

* les [diagrammes à barres](/Administration/Modèle/Format/Distribution Charts/BarChart.md)
* les [camemberts](/Administration/Modèle/Format/Distribution Charts/PieChart.md)
* les [radars](/Administration/Modèle/Format/Distribution Charts/RadarChart.md)

Ces formats nécessitent l'utilisation de la routine [distinct-by](/Configuration/routines/DistinctBy.md), appliquée à l'identifiant du champ représenté, qui doit être déclarée dans `valeur` \(_value_\) selon:

/api/run/distinct-by/**identifiant**/

où **identifiant** est le code attribué par LODEX au champ représenté.

