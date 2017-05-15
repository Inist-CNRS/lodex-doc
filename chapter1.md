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

## Exporters extended

Lodex allows you to export the istex query fields in format **N-quads **with the `EZMASTER_PUBLIC_URL` to the named graph.

Note: if you don't use `EZMASTER` , define the named graph with the property `graph` in `config.istexquery`:

```json
...
"istexQuery" : {
    "graph" : "http://yoururl.com/graph"
...
```

In the file config.js, you can configure the export :

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
       "context": {
          "language": "dcterms:language",
          "doi": "bibo:doi"
       }
    }
}
```

#### Labels

If labels is empty, all fields will exports. You can also select your fields like :

```json
"istexQuery" : {
    "labels": "label_name1,label_name3,label_name5",
    ...
```

#### Context

In `context` , you can add any informations from the istexquery output result like the `doi` or the `language` and you can join the result with a predicate \( `prefixes:predicate` or an`url` \):

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



