# UNIQ

Dédoublonne les valeurs de la valeur du champ quand c'est un tableau. Retourne la valeur quand c'est une chaîne, un nombre ou un booléen. Renvoie `null` sinon.

## Exemples

| Valeur de départ | Valeur transformée |
| :--- | :--- |
| \[ "hello", "hello" \] | \[ "hello" \] |
| \[ "hello", "world", "hello", "world" \] | \[ "hello", "world" \] |
| 0 | 0 |
| "hello" | "hello" |
| { "a": "hello", "b": "world" } | null |



