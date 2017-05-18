# Exporters

Lodex have many exporters availables :

* N-Quads
* N-Quads extended
* CSV
* TSV
* JSON
* Turtle
* JSON-LD
* JSONLD \(Compacted\)

## Exporters extended {#extended-exporters}

The exporters extended use only the istex query format to the export. A lodex with any istex query columns is useless to these exporters.

### N-Quads extended

The exporter N-Quads extended returns the results of the istex query in istex API. The results is formatted in a [N-Quads format](https://www.w3.org/TR/n-quads/). The exporter add a named graph on the triples. This named graph is useful for the triplestore import.

Lodex allows you to export the istex query fields in format **N-quads **with the `EZMASTER_PUBLIC_URL` to the named graph.

> Note: if you don't use `EZMASTER` , define the named graph with the property `graph` in `config.istexquery`:

```json
...
"istexQuery" : {
    "graph" : "http://yoururl.com/graph"
...
```

In the file `config.json`in lodex root, you can configure the export :

```json
...
    "prefixes":  {
        "bibo": "http://purl.org/ontology/bibo/",
        "dcdoc": "http://dublincore.org/documents/",
        "dcmitype": "http://purl.org/dc/dcmitype/",
        "dcterms": "http://purl.org/dc/terms/",
        "foaf": "http://xmlns.com/foaf/0.1/",
        "geo": "http://www.w3.org/2003/01/geo/wgs84_pos#",
        "gn": "http://www.geonames.org/ontology/ontology_v3.1.rdf/",
        "owl": "http://www.w3.org/2002/07/owl#",
        "prov": "http://www.w3.org/ns/prov#",
        "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
        "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
        "schema": "http://schema.org/",
        "skos": "http://www.w3.org/2004/02/skos/core#",
        "time": "http://www.w3.org/TR/owl-time/",
        "xfoaf": "http://www.foafrealm.org/xfoaf/0.1/",
        "xml": "http://www.w3.org/XML/1998/namespace",
        "xsd": "http://www.w3.org/2001/XMLSchema#"
    },
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

If labels is empty, all fields will export. You can also select your fields like :

```json
"istexQuery" : {
    "labels": "label_name1,label_name3,label_name5",
    ...
```

> Note: This is lodex's columns labels, not output in the istex API.

#### Context

In `context` , you can add any informations from the istex query output, like the `doi` or the `language` . You can join the result with a predicate \( `prefixes:predicate` or an`url` \):

```json
...
"prefixes": {
    "bibo": "http://purl.org/ontology/bibo/",
    "dcterms": "http://purl.org/dc/terms/",
},
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

### Lodex linker

In the exporter, you must add a link between istex data results and your lodex document.

The property `linked` was created for this purpose. 

```json
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

`linked` add in property `LINK` the lodex URI of your document with the rdf predicate `dc:example` .



## Exporter script

An export can take a long time to execute and it's more comfortable to export with a script/commands in bash or powershell.







