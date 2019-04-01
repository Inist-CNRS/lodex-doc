# DEFAULT

Renvoie une valeur par défaut si la valeur par défaut n'existe pas \(vaut `null`, `undefined`, `0`, `""`, c'est-à-dire une des valeurs _falsy_ de Javascript\).

| Valeur de départ | Paramètre | Valeur d'arrivée |
| :--- | :--- | :--- |
| null | "Yo" | "Yo" |
| "Ya" | "Yo" | "Ya" |
| 0 | "Oh!" | "Oh!" |
| "" | "Ah." | "Ah." |
| "0" | "Oh." | "0" |

> **Remarque** : faites attention au type de la valeur de départ \(en particulier si vous manipulez des nombres\), car `"0"` est différent de `0`, et sa valeur de vérité différente. C'est pourquoi vous pouvez vouloir utiliser un opérateur de transtypage, comme [BOOLEAN](boolean.md), [STRING](string.md), ou [NUMBER](number.md).

