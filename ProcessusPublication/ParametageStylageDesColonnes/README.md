# Le paramétrage/stylage des colonnes

Pour ajouter une colonne, vous devez activez le bouton "**+**" [précédemment décrit](/ProcessusPublication/CreationURI/README.md). Le système se met en mode paramétrage/stylage.

Pour publier les colonnes appartenant initialement à votre jeu de données (et les ajouter au passage à la prévisualisation dans l'écran d'administration), cliquez sur bouton `ADD A COLUMN FROM ORIGINAL DATASET`,  le bouton `ADD TO PUBLICATION` apparaît pour chacune des colonnes à traiter. Il est à noter, qu’il faudra recommencer cette action autant de fois que vous avez de colonnes.

Pour ajouter une nouvelle colonne à votre jeu de données cliquez sur `ADD A NEW COLUMN`, puis renseignez le formulaire de paramétrage composé de six étapes.

> **Note** : Après chaque étape, cliquez sur le bouton `SAVE` pour enregistrer votre choix, sur le bouton `CANCEL` pour annuler votre choix. Les boutons `PREVIOUS` et `NEXT` vous permettent de naviguer d'une étape à l'autre.

Pour chaque intitulé de colonne, le système vous propose cette fenêtre, correspondant aux **six étapes** possibles et à la prévisualisation du résultat du traitement effectué sur cette colonne :
![Les 6 étapes du paramétrage](/assets/parametrage2.png)
> **Note** : dans l'exemple présenté, nous avons sélectionné la colonne `Nom de l'établissement` et "Concept fr". (TODO: expliciter "Concept fr" ou supprimer)

## Descriptif des 6 étapes

### 1 - General informations

Cinq éléments sont à renseigner :
1. Label ;
2. Select a coverage ;
3. scheme ;
4. add new class ;
5. Langue.
![Étape Informations générales](/assets/parametrage3.png)
Le _label_ ainsi que le _coverage_ sont à renseigner obligatoirement, mais à votre convenance.

Les rubriques _scheme_ et _add new class_ sont à renseigner uniquement dans le cas où vous souhaitez publier votre jeu de données selon les normes du web sémantique.

### 2 - How the value is generated

Cette zone permet de définir comment est généré le contenu de la colonne à publier.
![Étape de génération du contenu](/assets/parametrage4.png)
Par défaut, le système propose `A value from an existing column`. À vous de valider ce choix ou de sélectionner une autre option.

### **3 – Transformations applied on the value**

Cette étape, vous permet d’appliquer différentes opérations \(_transformers_\) de traitement de curation sur les données.
![Étape de transformation](/assets/parametre5.png)

Lorsque vous cliquez sur le bouton `ADD AN OPERATION`, action qui est répétable, le système vous propose de sélectionner une action.

La description ainsi que le fonctionnement de chacun des _transformers_ sont développés dans la section des [transformers](/Administration/Modèle/Transformers/README.md).

### **4 - Semantics**

Cette opération vous permet de déclarer en  langage RDF une ressource anonyme ou nœud anonyme \(en anglais _blank node_ ou _bnode_\). C’est une ressource, ou nœud d'un graphe RDF, qui n'est pas identifiée par une URI. Une ressource anonyme peut être sujet ou objet d'un triplet RDF. \(Voir Wikipédia : [https://fr.wikipedia.org/wiki/Ressource\_anonyme](https://fr.wikipedia.org/wiki/Ressource_anonyme)\).

**Deux** possibilités vous sont offertes :
![Étape sémantique](/assets/parametre6.png)
1. _Annotate another field_ : à utiliser lorsque vous voulez préciser la valeur d'une colonne par rapport à une autre. Par exemple pour préciser la source d'une définition; pour cela, on sélectionnera la colonne de définition dans le menu déroulant lors du paramétrage de la colonne source ;
2. _Compose this field_ : à utiliser lorsque vous voulez, au sens du web sémantique, composer un champ à partir d'un ou plusieurs champs. Par exemple, une adresse est composée d'un nom de rue, d'une ville, d'un pays ; pour cela, on sélectionnera les colonnes nom de rue, ville et pays lors du paramétrage de la colonne adresse.

Selon la nature de vos données, à vous de retenir l'option qui convient.

### 5 – How and where it is displayed

Cette opération vous permet de paramétrer l'affichage de la _home page_, l'affichage complet d'une ressource et l'affichage liste des ressources. Pour rappel relire le descriptif de l'[affichage Front office](/AffichagesFrontOffice/README.md).

Lors de l'étape [1-General Informations](#generalinformations), si vous avez indiqué que votre colonne \(en tête et contenu\) avait comme coverage "Different for each resource" alors, vous avez cette fenêtre à remplir :

![](/assets/affichageressource.png)

Lors de l'étape "1-General Informations", si vous avez indiqué que votre colonne \(entête et contenu\) avait comme coverage "Apply to whole dataset" alors, vous avez cette fenêtre à remplir :![](/assets/affichagehomepage.png)

### **6 –Search related**

Lors de cette dernière opération, vous décidez si vos données vont être interrogeable ou non et ou constituer une facette sur sera accessible au niveau de l'affichage "GRAPHLIST".

![](/assets/searchrelated.png)

Les étapes décrites précédemment, ont permis de paramétrer/styler votre jeu de données. Il vous reste, maintenant une étape à réaliser afin de pouvoir afficher les informations qualifiants vos ressources sur la home page.

Pour ce faire, ajouter une nouvelle colonne à votre jeu de données cliquez sur "ADD A NEW COLUMN", puis renseigner le formulaire de paramétrage comme suit :

remplir les champs : 1 "**General informations**" :

```
                                               label : Liste des ressources \(par exemple\)

                                               select a coverage : Apply to whole dataset
```

**                                     2  "How the is generated" :**

```
                                                An arbitary value :  /api/run/syndication 

                                **  5 "How and where it is displayed" :**

                                               Cochez uniquement la case "Display in home page"

                                                Apply a format : Sélectionner : Other - Resources Grid**
```

\*\*

Maintenant, l'ultime étape correspond à la publication de votre jeu de données, en cliquant sur le bouton "PUBLISH" en haut à droite :

![](/assets/publicationjeudedonnées.png)

