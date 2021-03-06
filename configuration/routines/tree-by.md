# tree-by

La routine `tree-by` permet de créer des graphiques en forme d’arbres représentant des données hiérarchisées \(classification, taxonomies ...\) et d’afficher le nombre de documents concernés. 

Format d’entrée obligatoire : JSON

Les valeurs du champ représenté sont listées dans un ordre précis : du plus générique au plus spécifique : 

![Exemple en format Json](../../.gitbook/assets/image%20%289%29%20%281%29.png)

Elle crée des paires 2 à 2 entre les concepts spécifiques et plus génériques, et comptabilise le nombre de documents concernés par les concepts plus spécifiques de chaque segment. 

Cette routine doit être déclarée dans `Value` \(Valeur\) selon : 

                                                                       /api/run/tree-by/**identifiant**/ 

où **`identifiant`** représente les noms des espèces ou les catégories scientifiques \(termes les plus spécifiques d’une classification hiérarchique\) 

Cette routine est destinée à être utilisée avec le format graphique :

**-** HierarchicalGraph

**Exemple:** [**https://xxxxxxxxxxxx/api/run/tree-by/**](https://xxxxxxxxxxxx/api/run/classif-by/)   
 

