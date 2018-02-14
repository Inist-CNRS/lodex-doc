# Routines

Les routines de LODEX sont des scripts, stockable n'importe où sur le web, ou fournies par LODEX, qui peuvent effectuer des agrégations, des calculs, des reformatages et renvoient des données utilisables \(souvent par un format de type graphique\).

Les routines sont appelées via l'API web de LODEX, et s'appliquent à un champ. Quand on connaît le nom de la routine à utiliser \(disons `routine-exemple`\), il suffit de l'ajouter derrière /api/run/ pour obtenir la _route_ à utiliser \(comme valeur de champ pour un format graphique\).

## Format des routines

Les routines sont stockées dans des fichiers dont l'extension est `.ini`.

Un commentaire est une ligne commençant par `#`.

### Entête

Chaque fichier de routine commence par un entête comprenant les champs suivant:

* extension \(valeurs possibles: `js`, ?\)
* mimeType \(valeurs possibles: `application/json`, ?\)
* type \(valeurs possibles: `file`, ?\)
* label \(optionnel, explication sur l'objet de la routine\)

## Routines fournies par LODEX

* all-documents
* all-fields
* all-resources
* count-all
* count-by-fields
* distinct-by
* syndication

## Routines externes

Il est possible d'écrire ses propres routines, et de les rendre accessibles à LODEX sans avoir le droit de modifier LODEX. Il suffit pour cela de mettre les fichiers sur le web, et de renseigner LODEX sur leur emplacement, en utilisant le champ `pluginsURL` du fichier de configuration.

Exemple: `"pluginsURL": "https://raw.githubusercontent.com/Inist-CNRS/lodex-extented/master/routines/"`



