# distribute-by-interval

La routine ****`distribute-by-interval ` est destinée à des graphiques pour lesquels on souhaite regrouper des valeurs \(nombres entiers ou décimaux\) dans des intervalles de pas “1”. 

Cette routine peut être utilisée avec les formats graphiques :

* \*\*\*\*[**Bar Chart**](../../administration/modele/format/distribution-charts/barchart.md) ****\(Diagramme à barres et histogramme\)
* \*\*\*\*[**Pie Chart**](../../administration/modele/format/distribution-charts/piechart.md) ****\(Camembert\)
* \*\*\*\*[**Radar Chart**](../../administration/modele/format/distribution-charts/radarchart.md) ****\(Diagramme Radar\)

Elle doit alors être déclarée dans `Value` \(Valeur\) selon : 

                 /api/run/distribute-by-interval/**identifiant/**

**Exemple:** [**https://astrophysique-astroconcepts.corpus.istex.fr/api/run/distribute-by-interval/GeKM/**](https://astrophysique-astroconcepts.corpus.istex.fr/api/run/distribute-by-interval/GeKM/%20) ****où **GeKM** représente les scores de qualité, valeurs décimales uniques pour chaque document du corpus.

![](../../.gitbook/assets/image%20%2821%29%20%281%29.png)

