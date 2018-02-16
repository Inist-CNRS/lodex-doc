# Le paramétrage/stylage des colonnes

Pour ce faire, vous devez activez le bouton "**+**" [précédemment décrit](https://www.gitbook.com/book/lodex/lodex-user-documentation/edit#/edit/master/assets/écranchargementdonnées6.png?_k=5jwyv7). Le système se met en mode paramétrage/stylage.

Pour paramétrer/styler les colonnes appartenant initialement à votre jeu de données, cliquez sur bouton "ADD A COLUMN FROM ORIGINAL DATASET",  le bouton "**ADD TO PUBLICATION**" apparaît pour chacune des colonnes à traiter. Il est à noter, qu’il faudra recommencer cette action autant de fois que vous avez de colonnes.

Pour ajouter une nouvelle colonne à votre jeu de données cliquez sur "ADD A NEW COLUMN", puis renseigner le formulaire de paramétrage correspondant à six opérations à effectuer.

NB : Après chaque opération, cliquez sur le bouton "SAVE" pour enregistrer votre choix, sur le bouton "CANCEL" pour annuler votre choix. Les bouton "PREVIOUS" et "NEXT" vous permette de naviguer d'une opération à l'autre.

Pour chaque intitulé de colonne, le système vous propose cette fenêtre, correspondant aux **six opérations** possibles et à la visualisation du résultat du traitement effectué sur cette colonne  :![](/assets/parametrage2.png)NB : dans l'exemple présenté, nous avons sélection la colonne "Nom de l'établissement" et "Concept fr".

## Descriptif des 6 étapes :

### 1 - General informations

Six éléments sont à renseigner : Label ; Select a coverage ; scheme ; add new class ; Langue.![](/assets/parametrage3.png)Le label ainsi que le coverage sont à renseigner obligatoirement, mais à votre convenance.

Les rubriques "scheme" et "add a new class" sont à renseigner uniquement dans le cas où vous souhaitez publier votre jeu de données selon les normes du web sémantiques.

### 2 - How the value is generated

Cette zone permet de définir comment est générer le contenu de la colonne à publier.![](/assets/parametrage4.png)Par défaut, le système propose "A value from an existing column". A vous de valider ce choix ou de sélectionner une autre option.

### **3 – Transformations applied on the value**

Cette étape, vous permet d’appliquer différentes opérations \(transformers\) de traitement de curation sur les données.![](/assets/parametre5.png)

Lorsque vous cliquez sur le bouton "**ADD AN OPERATION**", action qui est répétable, le système vous propose de sélectionner une action.

La description ainsi que le fonctionnement de chacun des transformers est développée dans [cette section](/Administration/Modèle/Transformers/README.md).

### **4 - Semantics**

Cette opération vous permet de déclarer en  langage RDF, une ressource anonyme ou nœud anonyme \(en anglais blank node ou bnode\). C’est une ressource, ou nœud d'un graphe RDF, qui n'est pas identifiée par une URI. Une ressource anonyme peut être sujet ou objet d'un triplet RDF. \(Voir Wikipédia : [https://fr.wikipedia.org/wiki/Ressource\_anonyme](https://fr.wikipedia.org/wiki/Ressource_anonyme)\).

**Deux** possibilités vous sont offertes : ![](/assets/parametre6.png)

### 5 – How and where it is display

Cette opération vous permet de paramétrer l'affichage de la home page, l'affichage complet d'une  ressource et l'aafichage GraphLIST. Pour rappel relire le descriptif de l'[affichages Front office](/Affichages front office/README.md).

Lors de l'étape "1-General Informations", si vous avez indiqué que votre colonne \(en tête et contenu\) avait comme coverage "Different for each resource" alors, vous avez cette fenêtre à remplir :

![](/assets/affichageressource.png)

Lors de l'étape "1-General Informations", si vous avez indiqué que votre colonne \(entête et contenu\) avait comme coverage "Apply to whole dataset" alors, vous avez cette fenêtre à remplir :![](/assets/affichagehomepage.png)

### **6 –Search related**

Lors de cette dernière opération, vous décidez si vos données vont être interrogeable et ou constituer une facette à partir de l'affichage "GRAPHLIST".

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

