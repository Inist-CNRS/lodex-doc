# Création de l'URI

Avant de paramétrer/styler les colonnes, il est impératif de déclarer l'URI de chacune des ressources constituant votre jeu de données.

Pour cela, il vous suffit de cliquer sur le bouton `URI` précédemment cité.

Le système vous propose trois possibilités :

![Écran de constitution des URI](/assets/creation.png)

Après sélection d'un des choix, cliquez sur le **bouton SAVE.**

L'étape suivante consiste à paramétrer/styler les colonnes de votre tableau.

En sélectionnant `Generate URIs automatically`, LODEX génère un identifiant automatiquement, en fonction de la présence des paramètres `naan` et `subpublisher` dans le [fichier de configuration](/Configuration/README.md).

Si les paramètres sont présents, ils sont utilisés pour générer un ARK valide \(voir l'article [Destination ARK: vos papiers](http://lodex.inist.fr/2016/09/destinationn-ark-papier/)\).

Si les paramètres sont absents, on génère un identifiant préfixé non par `ark://` mais par `uid://`.

> **Remarque :** ces identifiants sont pensés pour être _pérennes_, c'est-à-dire qu'une fois affecté à une ressource, un identifiant doit toujours mener à cette ressource. Il ne s'agit pas de générer plusieurs identifiants différents pour la même ressource _une fois qu'elle est publiée_, car on aurait de grandes chances de perdre tous les identifiants sauf le dernier.
