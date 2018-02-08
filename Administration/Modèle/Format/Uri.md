# URL - Internal URI

Le format _Internal URI_ ajoute un lien sur la valeur du champ.

## Valeur

Ce champ est censé contenir l'URI d'une autre ressource du même jeu de données.

Si la valeur commence par `http://`, TODO

Si la valeur est un ARK \(commençant par `ark:/`\) ou un UID \(commençant par `uid:/`\), lien pointera sur la même instance LODEX, et pointer vers la ressource dont l'identifiant a été fourni.

Si la valeur ne commence ni par `ark:/`, ni par `uid:/`, ni par `http://`, elle est considérée comme un identifiant UID.

