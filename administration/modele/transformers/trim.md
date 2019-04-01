# TRIM

Supprime les espaces au début et à la fin de la valeur du champ quand c'est une chaîne de caractères. Sinon, renvoie la valeur sans la toucher.

> **Remarque** : sur une chaîne de caractères, [STRING](string.md) fait la même chose.

## Exemples

| Valeur de départ | Valeur transformée |
| :--- | :--- |
| " hello " | "hello" |
| null | null |
| 5 | 5 |
| { "a": 1, "b": 2 } | { "a": 1, "b": 2 } |
| \[ 1, 2, 3 \] | \[ 1, 2, 3 \] |

