# Distribution Charts

Les diagrammes de distribution montrent le nombre de fois où chaque élément du champ représenté apparaît dans le corpus:

* nombre d'occurrences si le champ n'est pas dédoublonné
* nombre de documents si le champ est dédoublonné

Les diagrammes de distribution fonctionnent de la même manière \(avec les mêmes données\), mais prennent des formes différentes:

* les [diagrammes à barres](https://github.com/lodex/lodex-user-documentation/tree/7e0012a6c9407d0d35e857ff4e1c93b20d74f66d/Administration/Modèle/Format/Distribution%20Charts/BarChart.md)
* les [camemberts](https://github.com/lodex/lodex-user-documentation/tree/7e0012a6c9407d0d35e857ff4e1c93b20d74f66d/Administration/Modèle/Format/Distribution%20Charts/PieChart.md)
* les [radars](https://github.com/lodex/lodex-user-documentation/tree/7e0012a6c9407d0d35e857ff4e1c93b20d74f66d/Administration/Modèle/Format/Distribution%20Charts/RadarChart.md)

Ces formats nécessitent l'utilisation de la routine [distinct-by](../../../../configuration/routines/distinctby.md), appliquée à l'identifiant du champ représenté, qui doit être déclarée dans `valeur` \(_value_\) selon:

/api/run/distinct-by/**identifiant**/

où **identifiant** est le code attribué par LODEX au champ représenté.

