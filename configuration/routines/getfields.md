# get-fields

Pour utiliser des nombres affectés à des champs des ressources \(pas un comptage mais  la valeur numérique du champ\), il faut pouvoir générer des paires `_id` / `value` contenant les valeurs de deux champs \(en général, un libellé et un nombre, par exemple pour un camembert\).

Pour sélectionner le libellé, on donne l'identifiant du champ contenant le libellé comme `identifiant1`, puis on ajoute l'identifiant du champ contenant la valeur numérique comme `identifiant2`.

                                                 /api/run/get-fields**/identifiant1/identifiant2/**

**Exemples de ressources:**

en tsv 

* nom de fichier Unitex-anglais Unitex-français
* wiley 4460007 12832
* elsevier 5879095 82652
* springer-journals 1424762 20131

\*\*\*\*

**résultat de la routine:**  


![](../../.gitbook/assets/image%20%2828%29.png)

\*\*\*\*

