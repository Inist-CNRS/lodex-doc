# CONCAT

Concatène les valeurs de deux colonnes du fichier tabulé de départ \(dans un tableau\).

## Exemple

Fichier CSV :

| a | b |
| :--- | :--- |
| prem | ière |
| deux | ième |

Paramètres de CONCAT: `a` et `b`

Résultats :

1. `[ "prem", "ière" ]`
2. `[ "deux", "ième" ]`

> `Remarque: pour concaténer des chaînes de caractères, on peut utiliser CONCAT conjointement avec`[`JOIN`](/Administration/Modèle/Transformers/JOIN.md)`.`



