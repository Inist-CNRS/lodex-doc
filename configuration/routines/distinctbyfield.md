# distinct-by-field

La routine `distinct-by-field` compte, pour chaque élément du champ représenté \(identifiant\), le nombre de fois où cet élément apparaît selon son :

* nombre d'occurrences si le champ n'est pas dédoublonné
* nombre de documents si le champ est dédoublonné ****

Cette routine se comporte comme la routine [distinct-by](distinctby.md), le petit `+`: elle sait interpréter les paramètres associés aux graphiques:

* Nombre max de champs \(`=maxSize`\)
* Valeur maximum à afficher \(`=maxValue`\)
* Valeur minimum à afficher \(`=minValue`\)
* Trier par valeur/label \(`=sortBy`\)

Cette routine peut être utilisée avec les formats graphiques :

* \*\*\*\*[**Bubble Chart**](../../administration/modele/format/bubblechart.md) ****\(Graphe à bulles\)
* \*\*\*\*[**Bar Chart**](../../administration/modele/format/distribution-charts/barchart.md) ****\(Diagramme à barres et histogramme\)
* \*\*\*\*[**Pie Chart**](../../administration/modele/format/distribution-charts/piechart.md) \(Camembert\)
* \*\*\*\*[**Radar Chart**](../../administration/modele/format/distribution-charts/radarchart.md) \(Diagramme Radar\)
* \*\*\*\*[**Cartography**](../../administration/modele/format/cartography.md) \(Cartographie\) \(si code ISO 3 ou code ISO 2 des pays\)

Elle doit alors être déclarée dans `Value` \(Valeur\) selon :

**/api/run/distinct-by-field/identifiant/**

où **`identifiant`** est le code attribué par LODEX au champ représenté.  
****

**Exemple:** [https://lodex9310-changclim.dboard.inist.fr/api/run/distinct-by-field/jpw2?maxSize=100&minValue=2&orderBy=value/desc](https://lodex9310-changclim.dboard.inist.fr/api/run/distinct-by-field/jpw2?maxSize=100&minValue=2&orderBy=value/desc)

![](../../.gitbook/assets/image%20%288%29.png)

