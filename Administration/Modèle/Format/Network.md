# Graph - Network

Le format Network représente la valeur du champ sous forme de réseau \([graphe](https://fr.wikipedia.org/wiki/Théorie_des_graphes) non orienté au sens mathématique\).

![](/assets/FormatNetwork.png)

La largeur des liens est calculée automatiquement en fonction du poids de ces liens.

La taille des nœuds est fonction de leur occurrence dans le jeu de données.

On peut cliquer sur un nœud pour griser tous les nœuds qui ne lui sont pas liés \(et leurs liens\).

La position des nœuds est calculée automatiquement, et est dynamique \(cela peut mettre un peu de temps pour se stabiliser\).

## Paramètre

![](/assets/FormatNetworkParameters.png)

Ce format n'a qu'un seul paramètre : la couleur des nœuds.

## Valeur

![](/assets/FormatNetworkValue.png)

La valeur à fournir à ce format est moins triviale que pour les formats textuels. Comme il faut obtenir les données dans le bon format, on passe par le mécanisme des [routines](/Administration/Modèle/Routine/README.md).

En l'occurrence, on utilise la routine `graph-by`, associée à l'identifiant du champ à représenter. Les routines sont appelables via l'API de LODEX, en préfixant le nom de la routine par `/api/run/`.

Le nom du champ se trouve dans l'administration, en cliquant sur `Model` / `View Model`.

![](/assets/AdminModelView.png)

LODEX liste alors les champs du modèle \(ceux du niveau Dataset, et ceux qui s'appliquent à chaque Document\), avec une colonne `Identifier` qui permet de trouver l'identifiant du champ à utiliser.![](/assets/AdminModelViewFields.png)En l'occurrence, on trouve `kMul`.

> **Conseil** : il peut être utile, si le contenu du champ doit être affiché dans les ressources, de créer un deuxième champ dédié au réseau, afin de pouvoir spécifier qu'il ne s'affiche ni la page listant les ressources ni dans la page des ressources. Ce champ aura la même valeur que celui affiché.

![](/assets/FormatNetworkFieldParameters.png)

