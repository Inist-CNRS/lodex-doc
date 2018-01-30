# BOOLEAN

Transforme la valeur du champ en un booléen \(dont la valeur ne peut être que `true `ou `false`, vrai ou faux\). Ceci n'est utile que si la valeur attendue est un booléen \(par défaut, la valeur d'un champ est une chaîne de caractères\).

Toute chaîne de caractères valant `true`, `1`, `on`, `ok`, `oui`, `yes` ou `true` sera vraie, et toute autre chaîne sera fausse \(excepté si on encadre les valeurs de vérité par des espaces\).

Tableau de conversion :

| Valeur de départ | Valeur transformée par BOOLEAN |
| :--- | :--- |
| "true" | true |
| "1" | true |
| "on" | true |
| "ok" | true |
| "oui" | true |
| "yes" | true |
| " true " | true |
| " 1 " | true |
| " ok " | true |
| " on " | true |
| " oui " | true |
| " yes " | true |
| "yes 1 ok on oui" | false |
| "whatever" | false |
| true | true |
| 1 | true |
| 0 | false |
| 2 | false |
| false | false |
| \[ \] | false |
| { } | false |
| undefined | false |
| null | false |



