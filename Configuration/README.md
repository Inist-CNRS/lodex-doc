# Configuration

Cette section de la documentation décrit la face _cachée_ de LODEX: son fichier de configuration. Tout ce qui ne peut pas être fait via l'administration \(aussi appelée _backoffice_\) doit être fait dans le fichier de configuration.

Ces réglages sont mis dans un seul fichier JSON, appelé `config.json`  à la racine du code source de LODEX. Étant donné que LODEX peut être utilisé dans [ezmaster](https://github.com/Inist-CNRS/ezmaster), dans ce cas vous pouvez accéder à ce fichier en utilisant le bouton _Settings_ de l'instance de LODEX que vous voulez modifier \(c'est l'icone en forme de roue dentée\).

Mais que vous modifiiez ce fichier via votre éditeur préféré ou en utilisant l'éditeur JSON d'ezmaster, les principes restent les mêmes.

## Réglages possibles

* [username / password](/Configuration/Authentification/README.md)
* [naan / subpublisher](/Configuration/ARK/README.md) \(_optionnel:_ usage d'ARK pour les identifiants\)
* [loader](/Configuration/loaders/README.md) \(liste et configuration des loaders utilisables\)
* [routines](/Configuration/routines/README.md) / routinesRepository \(_optionnel:_ utilisé avec les formats graphiques\)
* [exporters](/Configuration/exporters/README.md) \(liste des formats d'export à afficher\)
* \[languages\]\(/Configuration/Langue de l'interface/README.md\) \(liste des traductions de l'interface utilisateur à rendre disponibles\)
* topFieldsCount \(...\)
* [réglages sémantiques](/Configuration/Linked Open Data/README.md) \(_optionnel:_ exposer ses données suivant les formats du web sémantique\)

![](/assets/panneaudedonfiguration.png)

