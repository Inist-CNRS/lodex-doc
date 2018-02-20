# Personnalisation du thème

Votre jeu de données est publié sur le web. Maintenant il vous reste à l'encapsuler dans votre site personnalisé. Pour cela, vous pouvez aller à l'adresse suivante  [https://github.com/Inist-CNRS/lodex-themes](https://github.com/Inist-CNRS/lodex-themes) pour accéder à une bibliothèque de thèmes prédéfinis.

Chaque thème comporte au moins un fichier `index.html` contenant une balise dont l'identifiant est `root`. C'est dans cet élément HTML que s'instanciera l'application.

Le contenu minimum du fichier `index.html` est donc: `<div id="root"></div>`.

C'est de la responsabilité du concepteur du thème d'ajouter les différents liens:

* administration: `/admin`
* connexion: `/login`
* liste des ressources: `/graph`

Si vous avez adopté ezmaster pour installer l'outil, vous devrez utiliser le protocole Webdav pour téléverser les différents fichiers de paramétrage. Sous Linux Sous Windows

Si vous avez adopté docker pour installer l'outil, vous devrez utiliser ........

Si vous avez adopté node  pour installer l'outil, vous devrez utiliser ....

