# PREFIX

Préfixe une valeur de champ avec une chaîne de caractères. Lorsque la valeur est un tableau, la chaîne de caractères est insérée au début du tableau.

## Exemples

| Valeur de départ | Paramètre | Valeur transformée |
| :--- | :--- | :--- |
| "dear world" | "hello" | "hello dear world" |
| undefined | "hello" | "hello" |
| \[ "dear", "world" \] | "hello" | \[ "hello", "dear", "world" \] |

