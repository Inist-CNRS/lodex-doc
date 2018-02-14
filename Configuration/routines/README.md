# Routines

Les routines de LODEX sont des scripts, stockable n'importe où sur le web, ou fournies par LODEX, qui peuvent effectuer des agrégations, des calculs, des reformatages et renvoient des données utilisables \(souvent par un format de type graphique\).

Les routines sont appelées via l'API web de LODEX, et s'appliquent à un champ. Quand on connaît le nom de la routine à utiliser \(disons `routine-exemple`\), il suffit de l'ajouter derrière /api/run/ pour obtenir la _route_ à utiliser \(comme valeur de champ pour un format graphique\).

## Format des routines

Les routines sont stockées dans des fichiers dont l'extension est `.ini`.

Un commentaire est une ligne commençant par `#`.

Le fichier est séparé en sections dont le nom est donnée entre crochets.

### Entête

Chaque fichier de routine commence par un entête comprenant les champs suivant:

* extension \(valeurs possibles: `js`, ?\)
* mimeType \(valeurs possibles: `application/json`, ?\)
* type \(valeurs possibles: `file`, ?\)
* label \(optionnel, explication sur l'objet de la routine\)

### Section \[use\]

Dans cette section, on déclare les plugins qu'on va utiliser dans la routine.

Pour trouver une liste des plugins disponibles, voir la page [https://www.npmjs.com/browse/keyword/ezs](https://www.npmjs.com/browse/keyword/ezs).

Chaque plugin commence par `ezs-`, par exemple `ezs-basics` est le plugin `basics`, qui fournit une série d'instructions:

* BUFObject
* CSVObject
* CSVParse
* CSVString
* JSONParse
* JSONString
* OBJCount
* OBJFlatten
* OBJStandardize
* SKOSObject
* TXTConcat
* TXTObject
* TXTParse
* URLFetch
* XMLParse

### Instructions disponibles

D'ailleurs, LODEX fournit sa propre série d'instructions:

* filterVersions
* filterContributions
* useFieldNames
* linkDataset
* JSONLDCompacter
* JSONLDString
* JSONLDObject
* extractIstexQuery
* scroll
* convertJsonLdToNquads
* convertToExtendedJsonLd
* convertToAtom
* convertToSitemap
* LodexContext
* LodexConfig
* LodexParseQuery
* LodexRunQuery
* LodexReduceQuery
* LodexSetField
* LodexOutput

### Section \[assign\]

On peut ajouter des sections \[assign\] n'importe où dans le fichier de routine, elles servent à affecter une valeur à une variable.

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

