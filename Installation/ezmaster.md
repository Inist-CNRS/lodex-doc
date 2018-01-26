# Installer LODEX sur ezmaster

_Pré-requis_: ezmaster 4+

[L'image docker de LODEX](https://hub.docker.com/r/inistcnrs/lodex/) est compatible avec [ezmaster](https://github.com/Inist-CNRS/ezmaster), pour lancer une instance de LODEX, il suffit donc de:

* ajouter l'application `inistcnrs/lodex` dans sa dernière version
* créer une instance utilisant cette application
* éventuellement modifier sa [configuration](//Configuration/README.md) via l'éditeur de configuration

Rien que de très classique dans ezmaster.

> **Note**: dans ezmaster 5+, il faut aussi installer l'application [inistcnrs/ezmaster-mongo](https://hub.docker.com/r/inistcnrs/ezmaster-mongo/), car ezmaster ne fournit plus de serveur mongo.



