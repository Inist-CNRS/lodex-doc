# JBJ

Applique une feuille de style [JBJ](https://github.com/Inist-CNRS/node-jbj) à la valeur de départ. JBJ \(Json By Json\) est un système de feuille de style entièrement en [JSON](http://json.org/json-fr.html) pour traiter du JSON \(un peu comme XLST pour XML\).

Vous pouvez découvrir JBJ grâce à ce petit dojo : [JSON by JSON par l'exemple](http://inist-cnrs.github.io/jbj-playground/dojo/1.html).

L'utilisation de JBJ offre une grande puissance de transformation, au prix d'une complexité plus grande que les _transformers_ classiques.

## Exemple

Pour verbaliser un code, par exemple, on peut utiliser l'action JBJ `mapping` \(voir [sa documentation](https://github.com/Inist-CNRS/node-jbj-array#mapping)\).

Valeur de départ : `"0"`

Paramètre du _transformer_ JBJ :

```javascript
{
    "mapping": {
        "0": "Première verbalisation",
        "1": "Deuxième verbalisation",
        "2": "Verbalisation improbable"
    }
}
```

Résultat: `"Première verbalisation"`

