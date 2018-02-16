# Installer LODEX avec docker

_Pré-requis_: docker, docker-compose

Pour installer puis lancer LODEX dans un conteneur docker:

```bash
make install
make run-dev
```

Si vous n'avez pas encore de MongoDB écoutant sur le port 27017, vous pouvez utiliser:

```bash
make mongo
```
