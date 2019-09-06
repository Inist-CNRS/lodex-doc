# Moteur de recherche

La recherche s’effectue sur les champs décrivant les ressources, mais pas sur le texte des documents associés, pdf ou autre.

Cliquer sur la loupe « Recherche » dans le menu de gauche.

Un écran s’ouvre avec un masque de requête, le nombre de documents total du corpus, la fonction « recherche filtrée »  et une liste de 10 notices en forme courte.

![](.gitbook/assets/image%20%284%29.png)

Il est possible :

-      soit de chercher indifféremment sur tous les champs indexés des ressources,

-      soit d’utiliser une recherche à facettes sur certains champs prédéterminés lors de la création/modification du modèle de l’instance.

Il est possible également d’associer recherche et représentation graphique dynamique en utilisant le bouton « Graphiques » dans le volet de navigation de gauche.

## 1 - Recherche sur tous les champs indexés

Taper un ou plusieurs termes dans le masque de requête.

![](.gitbook/assets/image002.png)

  
Le moteur de recherche de Lodex est celui de MongoDB.

Il appauvrit les termes de recherche : il supprime les accents, la ponctuation, la casse, les mots vides selon la langue, les marques de pluriel, au moins en ‘s’.

Il recherche les mots dérivés de la racine d’un terme en fonction de la langue, mais il convient de tester l’efficacité de cette méthode avant un usage réel.

Ainsi :

- métadonnées, métadonnée, metadonnees et metadonnee \(ou termes avec majuscules\) rendent les mêmes résultats

- meta-données et meta donnees rendent les mêmes résultats \(booléen « ou » implicite entre les deux termes\)

- « document » et « documents » rendent les mêmes résultats ; « documentation » rend des résultats communs avec le précédent et des résultats spécifiques supplémentaires. 

- "retin" renvoie par exemple "rétinitis", "retina" et "retinal" mais pas "retinoïc", et « retino » renvoie «retinoïc » et quelques autres termes commençant par « retino ».

Il n'existe pas de possibilité d'indiquer une troncature spécifique.

L’opérateur par défaut qui s’applique entre les termes recherchés est le booléen « ou », et il n’existe pas d’opérateurs explicites \(tels OR, AND, NOT\). 

Une recherche sur plusieurs mots propose en résultat un classement des documents du plus pertinent au moins pertinent.

Sur le résultat de la recherche, il est possible de :

-          Sélectionner une ressource en cliquant sur son titre ; pour retourner à la recherche précédente, cliquer à nouveau sur la loupe « Recherche » ;

-          Voir plus de résultats : à chaque clic sur cette proposition présente en bas de la liste de notices, 10 résultats supplémentaires s’ajoutent à l’affichage.

  


### 2 – recherche par facettes

Cliquer sur « recherche filtrée » pour voir la liste des facettes disponibles.

![](.gitbook/assets/image%20%2827%29.png)

  
Le chevron de droite permet de déplier les valeurs associées, avec leur nombre d’occurrences dans le corpus. On sélectionne ensuite les valeurs souhaitées ou à exclure en cochant les cases à leur gauche.

![](.gitbook/assets/image%20%2815%29.png)

Il est possible d'associer plusieurs critères \(opérateur implicite : AND\).

![](.gitbook/assets/image%20%283%29.png)

  


### 3 – graphiques et recherche

Quand on sélectionne un graphique via le menu correspondant « Graphiques », on retrouve sur le côté droit les mêmes facettes dépliables, qui permettent de filtrer des résultats, et de mettre à jour la liste des ressources et le graphique sur ces nouveaux résultats.

Exemple : on souhaite savoir si les mots clé d’auteur sont plus souvent présents dans certains types de publication.

Sélectionner le graphique « Type de publication » puis la facette « Mots clés d’auteur », et le mot-clé le plus fréquent.

Avant sélection d’une facette :

![](.gitbook/assets/image%20%288%29.png)

Après sélection d'une facette, ici les mots-clés d'auteur :

![](.gitbook/assets/image%20%285%29.png)

  


Plus d'info sur le moteur de recherche et son paramétrage : https://docs.mongodb.com/manual/core/index-text/

