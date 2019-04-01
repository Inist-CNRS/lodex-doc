# exporters

LODEX a plusieurs formats d'export, et on peut choisir de les proposer ou non à l'utilisateur. Pour être affiché, un exporter doit être présent dans le tableau `exporters`.

Les _exporters_ fournis par LODEX sont les suivants:

* N-Quads : `nquads`
* N-Quads étendus : `extendednquads`
* CSV : `csv`
* TSV : `tsv`
* Turtle : `turtle`
* ATOM : `atom`
* JSON-LD : `jsonld`
* JSONLD \(Compact\) : `jsonldcompacted`
* Sitemap \(pour le référencement\) : `sitemap`
* Widget \(I-Frame\) : `widget`

## Exporters étendus <a id="extended-exporters"></a>

Les _exporters_ étendus ne sont utiles quand un champ est de format ISTEX Query.

### N-Quads extended

L'_exporter_ «N-Quads étendus» renvoie les résultats de la requête dans l'[API ISTEX](https://api.istex.fr). Ils sont formatés en [N-Quads](https://www.w3.org/TR/n-quads/).

Un graphe nommé, utile lors de l'import dans un triple store, est ajouté aux triplets \(TODO: vérifier que c'est encore vrai\).

Le graphe nommé est formé à partir de la valeur de la variable d'environnement `EZMASTER_PUBLIC_URL`.

> **Remarque** : si vous n'utilisez pas [ezMaster](https://github.com/Inist-CNRS/ezmaster/blob/master/README.md), définissez la propriété `graph` dans `config.istexquery`:

```javascript
...
"istexQuery" : {
    "graph" : "http://yoururl.com/graph"
...
```

Dans le fichier de configuration `config.json` vous pouvez configurer l'export:

```javascript
...
    "istexQuery" : {
       "labels": "",
       "linked": "language",
       "context": {
          "language": "dcterms:language",
          "doi": "bibo:doi"
       }
    }
}
```

#### Labels

Si `labels` est vide, tous les champs du format Istex Query seront exportés \(TODO: à expliciter, ce n'est pas clair\). Vous pouvez aussi sélectionner les champs ISTEX de cette manière:

```javascript
"istexQuery" : {
    "labels": "istex_query1,istex_query3,istex_query5",
    ...
```

> Note: This is lodex's columns labels, not output in the istex API. \(TODO: à vérifier\)

#### Context

Dans la propriété `context`, vous pouvez déclarer les champs de l'API ISTEX que vous voulez exporter, comme `doi` ou `language`. Vous pouvez préciser le propriété sémantique à utiliser pour chacun d'eux, en utilisant un préfixe \(`prefix:property`\) ou une URI complète.

```javascript
...
"istexQuery" : {
    "labels": "",
    "context": {
        "language": "dcterms:language",
        "doi": "bibo:doi",
        "rebBibs.host.publicationDate": "http://purl.org/dc/terms/issued"
        }
    }
}
```

La liste des préfixes utilisables dans LODEX est [visible sur Github](https://github.com/Inist-CNRS/lodex/blob/master/src/common/prefixes.js), mais voilà la liste correspondant aux version 8.17+:

* bibo: [http://purl.org/ontology/bibo/](http://purl.org/ontology/bibo/)
* dcdoc: [http://dublincore.org/documents/](http://dublincore.org/documents/)
* dcmitype: [http://purl.org/dc/dcmitype/](http://purl.org/dc/dcmitype/)
* dcterms: [http://purl.org/dc/terms/](http://purl.org/dc/terms/)
* foaf: [http://xmlns.com/foaf/0.1/](http://xmlns.com/foaf/0.1/)
* geo: [http://www.w3.org/2003/01/geo/wgs84\_pos\#](http://www.w3.org/2003/01/geo/wgs84_pos#)
* gn: [http://www.geonames.org/ontology/ontology\_v3.1.rdf/](http://www.geonames.org/ontology/ontology_v3.1.rdf/)
* istex: [https://data.istex.fr/ontology/istex\#](https://data.istex.fr/ontology/istex#)
* owl: [http://www.w3.org/2002/07/owl\#](http://www.w3.org/2002/07/owl#)
* prov: [http://www.w3.org/ns/prov\#](http://www.w3.org/ns/prov#)
* rdf: [http://www.w3.org/1999/02/22-rdf-syntax-ns\#](http://www.w3.org/1999/02/22-rdf-syntax-ns#)
* rdfs: [http://www.w3.org/2000/01/rdf-schema\#](http://www.w3.org/2000/01/rdf-schema#)
* schema: [http://schema.org/](http://schema.org/)
* skos: [http://www.w3.org/2004/02/skos/core\#](http://www.w3.org/2004/02/skos/core#)
* time: [http://www.w3.org/TR/owl-time/](http://www.w3.org/TR/owl-time/)
* xfoaf: [http://www.foafrealm.org/xfoaf/0.1/](http://www.foafrealm.org/xfoaf/0.1/)
* xml: [http://www.w3.org/XML/1998/namespace](http://www.w3.org/XML/1998/namespace)
* xsd: [http://www.w3.org/2001/XMLSchema\#](http://www.w3.org/2001/XMLSchema#)

### Lier les ressources LODEX et les documents ISTEX

Dans la configuration de l'_exporter_ \(nommée `istexQuery`\), il faut ajouter la propriété sémantique liant la ressource LODEX contenant la requête aux documents ISTEX correspondants.

Pour ce faire, on utilise la propriété `linked`, qui pointe le champ \(du `context`\) contenant la propriété à utiliser.

```javascript
"istexQuery" : {
    "labels": "",
    "linked": "LINK",
    "context": {
        "language": "dcterms:language",
        "doi": "bibo:doi",
        "LINK": "dc:example"
    }
}
```

Dans cet exemple, la propriété `LINK` a été déclarée comme étant celle à utiliser pour lier les ressources aux documents.

## Script d'export

L'export peut prendre très longtemps, et il est plus aisé d'utiliser un script bash ou powershell plutôt qu'un navigateur web.

Une bonne solution, sous bash ou powershell 3.0, est d'utiliser la commande `wget`:

```bash
wget -O file -c lodex.url/api/export/nquads
```

> ‘-c’ ‘--continue’ : option wget pour redémarrer le téléchargement et écraser le fichier existant quand l'export LODEX retourne une erreur.

La liste des _exporters_ est disponible [au début de cette section](exporters.md#exporters).

