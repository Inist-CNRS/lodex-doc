# TRUNCATE

Supprime les derniers élément de la valeur du champ, en fonction du nombre passé en paramètre.

Le nombre indique la position du caractère \(ou de l'élément dans le cas d'un tableau\) à partir duquel couper la valeur. La position la plus à gauche a la valeur zéro \(0\).

> **Remarque** : c'est la transformation inverse de [SHIFT](shift.md).

## Exemples

| Valeur de départ | Paramètre | Valeur transformée |
| :--- | :--- | :--- |
| "hello world" | 5 | "hello" |
| \[ 1, 2, 3, 4, 5 \] | 3 | \[ 1, 2, 3 \] |
| \[ 0, 1, 2, 3, 4 \] | 1 | \[ 0 \] |

