# STRING

Transforme la valeur du champ en une chaîne de caractères. Ceci n'est utile que si elle n'est pas déjà une chaîne \(type par défaut\), ou si vous voulez supprimer les espaces au début et à la fin d'une chaîne.

> **Remarque** : on peut appliquer une séquence de _transformers_ sur une valeur de champ, ce qui implique que la valeur en entrée de STRING peut être autre chose qu'une chaîne de caractères.

## Exemples

| Valeur de départ | Valeur transformée |
| :--- | :--- |
| " hello " | "hello" |
| 0 | "0" |
| null | "" |
| undefined | "" |
| { "a": "hello", "b": "world" } | "" |

