# SUFFIX

Ajoute une chaîne de caractères à la fin de la valeur du champ. Lorsque la valeur est un tableau, la chaîne est ajoutée à la fin du tableau.

> **Remarque** : c'est l'opération inverse de [PREFIX](/Administration/Modèle/Transformers/PREFIX.md).

## Exemples

| Valeur de départ | Paramètre | Valeur transformée |
| :--- | :--- | :--- |
| "hello dear" | " world" | "hello dear world" |
| undefined | "hello" | "hello" |
| \[ "hello", "dear" \] | "world" | \[ "hello", "dear", "world" \] |
