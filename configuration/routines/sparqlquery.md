# sparql-query

La routine `sparql-query` sert à faire des graphiques de distribution en prenant ses données dans un tripleStore et non dans Lodex.

Elle est cohérence avec les graphiques pouvant utiliser [distinct-by](distinctby.md) : 

* [Bubble Char](../../administration/modele/format/bubblechart.md) \(Graphe à bulles\)
* [Bar Char](../../administration/modele/format/distribution-charts/barchart.md) \(Diagramme à barres et histogramme\)
* [Pie Char t](../../administration/modele/format/distribution-charts/piechart.md) \(Camembert\) 
* [Radar Chart](../../administration/modele/format/distribution-charts/radarchart.md) \(Diagramme Radar\) 

Ses résultats doivent ressembler à ceux de [distinct-by](distinctby.md).

**`Version minimale de lodex : 9.8.1`**  


Ce type de graphique nécessite la structure suivante : 

* un champ `total` correspondant au nombre d'éléments
* un champ `data` qui est la liste des éléments à afficher dans le graphique. Chaque élément possède 2  champs également. Un champ `_id` qui correspond au nom de l'élément et un champ “value” qui correspond à la valeur numérique qui lui est associée.

![](https://lh6.googleusercontent.com/ExHZSAOegy9h1M8-MOszM8V42k4_zVSCfSm8HabpOxWRJvuZEwm-riHa2Kk9kcIwl1xCDNdRIEvUNTqLcnCKrkowwjLaS6VRzHwnR3Z0Ihzh8W40qUtwIP7e8BFsMv22MlhYkwqo)

`Important:` créer  directement sa requête dans le tripleStore de data.istex.fr via YASGUI 

![](../../.gitbook/assets/image%20%2817%29%20%281%29.png)

Copier le lien de partage --&gt; ce lien sera la valeur à reporter dans un champ LODEX préalablement configuré.

![copie du lien de partage](../../.gitbook/assets/image%20%2812%29.png)

Insérer ce lien dans un nouveau champ **`DATASET`** lodex et récupérer son identifiant \(ici `Kl67` \)

![requ&#xEA;te yasgui &#xE0; reporter dans un champ dataset](../../.gitbook/assets/image%20%2810%29.png)

Créer un autre champ type graphique au niveau du **`DATASET`** pour récupérer les informations de ce champ.

![d&#xE9;claration de la routine sparql-query](../../.gitbook/assets/image%20%282%29.png)

Cette routine doit être déclarée dans `Value` \(Valeur\) selon : /api/run/sparql-query/\*\*identifiant\*\*/ où \*\*identifiant\*\* représente le champ contenant la requête copier depuis le yasgui de data.istex.fr

![configuration graphique](../../.gitbook/assets/image%20%281%29.png)









