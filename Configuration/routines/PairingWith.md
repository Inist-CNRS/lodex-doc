# pairing-with

La routine `pairing-with` \(fournie sur [https://github.com/Inist-CNRS/lodex-extented/](https://github.com/Inist-CNRS/lodex-extented/)\) crée les paires \(`source` et `target`\) entre les éléments de 2 champs \(champs identiques ou différents\) déclarés selon :

/api/run/pairing-with/**identifiant1**/**identifiant1**/

/api/run/pairing-with/**identifiant1**/**identifiant2**/

et compte, pour chaque paire, le nombre de co-occurrences.

Elle peut, en particulier, être utilisée avec les formats [Network](/Administration/Modèle/Format/Network.md) \(Réseau\) et [Heat Map](/Administration/Modèle/Format/HeatMap.md) \(carte de chaleur\).

> **Attention :** dans le cas où cette routine s'applique à un seul champ \(/api/run/pairing-with/identifiant1/identifiant1/\), elle conserve les _auto-paires_ \(source et cible identiques\). Cela peut être intéressant avec le format [Heat Map](/Administration/Modèle/Format/HeatMap.md) pour visualiser la diagonale, mais peut être gênant avec d'autres formats.

**Exemples** :

1. [http://lodex-cop21.dpi.inist.fr/api/run/pairing-with/Xmzn/Xmzn/](http://lodex-cop21.dpi.inist.fr/api/run/pairing-with/Xmzn/Xmzn/) 
   ![](/assets/RoutinePairingWith1.png)
2. [http://lodex-cop21.dpi.inist.fr/api/run/pairing-with/Xmzn/WXcA/](http://lodex-cop21.dpi.inist.fr/api/run/pairing-with/Xmzn/WXcA/)  
   ![](/assets/RoutinePairingWith2.png)



