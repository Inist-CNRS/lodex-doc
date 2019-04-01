# NUMBER

Transforme la valeur du champ en un nombre. Ceci n'est utile que si la valeur attendue du champ est un nombre.

> **Remarque** : ne perdez pas de vue que par défaut les valeurs des champs sont des chaînes de caractères.

## Exemples

| Valeur de départ | Valeur transformée |
| :--- | :--- |
| "1234" | 1234 |
| "   1234   " | 1234 |
| 1234 | 1234 |
| null | 0 |
| undefined | 0 |
| "45a" | 0 |
| "45 65" | 0 |
| { "a": "hello", "b": "world" } | 0 |

