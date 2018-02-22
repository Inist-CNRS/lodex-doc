# Configuration

Cette section de la documentation décrit la face _cachée_ de LODEX: son fichier de configuration. Tout ce qui ne peut pas être fait via l'administration \(aussi appelée _backoffice_\) doit être fait dans le fichier de configuration.

Ces réglages sont mis dans un seul fichier JSON, appelé `config.json`  à la racine du code source de LODEX. Étant donné que LODEX peut être utilisé dans [ezmaster](https://github.com/Inist-CNRS/ezmaster), dans ce cas vous pouvez accéder à ce fichier en utilisant le bouton _Settings_ de l'instance de LODEX que vous voulez modifier \(c'est l'icone en forme de roue dentée\).

Mais que vous modifiiez ce fichier via votre éditeur préféré ou en utilisant l'éditeur JSON d'ezmaster, les principes restent les mêmes.

> **Remarque** : il est conseillé de s'occuper de ce fichier de configuration avant de passer à l'administration, en particulier pour `naan`, `subpublisher`, `routines` et réglages sémantiques. Toutes ces possibilités sont optionnelles.

## Réglages possibles

* [username / password](/Configuration/Authentification/README.md)
* [userAuth](/Configuration/RestrictionAccès/README.md) \(_optionnel_: restriction d'accès à l'application\)
* [naan / subpublisher](/Configuration/ARK/README.md) \(_optionnel:_ usage d'ARK pour les identifiants\)
* [loader](/Configuration/loaders/README.md) \(liste et configuration des loaders utilisables\)
* [routines](/Configuration/routines/README.md) / routinesRepository \(_optionnel:_ utilisé avec les formats graphiques\)
* [exporters](/Configuration/exporters/README.md) \(liste des formats d'export à afficher\)
* [réglages sémantiques](/Configuration/LinkedOpenData/README.md) \(_optionnel:_ exposer ses données suivant les formats du web sémantique\)

![Fichier de configuration](/assets/panneaudedonfiguration.png)

