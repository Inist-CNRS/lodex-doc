# decompose-by

La routine `decompose-by` croise les éléments pour un champ ou plusieurs champs et compte le nombre d’occurrences de chaque croisement.

Elle crée les paires \(`source` et `target`\) entre les valeurs de 1 champ ou plusieurs champs \(champs identiques ou différents\) selon :

* /api/run/decompose-by**/identifiant1/**
* /api/run/decompose-by/**identifiant1/identifiant2/**

et compte, pour chaque paire, le nombre de co-occurrences.

Cette routine se comporte comme la routine [graph-by](graphby.md), le petit `+`: elle sait interpréter les paramètres associés aux graphiques:

* Nombre max de champs \(`=maxSize`\)
* Valeur maximum à afficher \(`=maxValue`\)
* Valeur minimum à afficher \(`=minValue`\)
* Trier par valeur/label \(`=sortBy`\) 

Elle peut, en particulier, être utilisée avec les formats [Network](../../administration/modele/format/network.md) \(Réseau\) et [Heat Map](../../administration/modele/format/heatmap.md) \(carte de chaleur\)

**Attention :** dans le cas où cette routine s'applique à plusieurs champs \(/api/run/decompose-by/identifiant1/identifiant2/\), elle crée les paires **identifiant1/identifiant2** mais aussi **identifiant1/identifiant1 et identifiant2/identifiant2**, ce qui peut ne pas être adapté pour un réseau.  
****

     **Exemple:**[ **https://lodex9310-changclim.dboard.inist.fr/api/run/decompose-by/jpw2/jpw2?maxSize=100&minValue=2&orderBy=value/desc**](https://lodex9310-changclim.dboard.inist.fr/api/run/cross-by/jpw2/jpw2?maxSize=100&minValue=2&orderBy=value/desc)**\)**  
 

