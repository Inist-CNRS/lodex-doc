# graph-by

La routine `graph-by` \(fournie sur [https://github.com/Inist-CNRS/lodex-extented/](https://github.com/Inist-CNRS/lodex-extented/)\) crée les paires \(`source` et `target`\) entre les éléments de 1 champ ou plusieurs champs \(champs identiques ou différents\) selon :

/api/run/graph-by/**identifiant1**/

/api/run/graph-by/**identifiant1**/**identifiant2**/

et compte, pour chaque paire, le nombre de co-occurrences.

Elle peut, en particulier, être utilisée avec les formats [Network](/Administration/Modèle/Format/Network.md) \(Réseau\) et [Heat Map](/Administration/Modèle/Format/HeatMap.md) \(carte de chaleur\)

> **Attention :** dans le cas où cette routine s'applique à plusieurs champs \(/api/run/graph-by/identifiant1/identifiant2/\), elle crée les paires identifiant1/identifiant2 mais aussi identifiant1/identifiant1 et identifiant2/identifiant2, ce qui peut ne pas être adapté pour un réseau.

**Exemples :**

1. [http://lodex-cop21.dpi.inist.fr/api/run/graph-by/Xmzn/](http://lodex-cop21.dpi.inist.fr/api/run/graph-by/Xmzn/)
   où Xmzn = CodeCNRS2015
   ![](/assets/RoutineGraphBy1.png)

2. [http://lodex-cop21.dpi.inist.fr/api/run/graph-by/Xmzn/WXcA/](http://lodex-cop21.dpi.inist.fr/api/run/graph-by/Xmzn/WXcA/)  
   où Xmzn = CodeCNRS2015 et WXcA = Web of Science Category\(ies\)  
   ![](/assets/RoutineGraphBy2.png)



