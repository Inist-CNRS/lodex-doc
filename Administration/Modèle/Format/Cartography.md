# Cartography

Le format `Graphique - Cartographie` \(_Graph - Cartography_\) projette des données numériques sur une carte géographique du monde.  
![Exemple de Cartography](/assets/FormatCartography.png)

## Paramétrage

## ![](/assets/FormatCartographyParameters.png)

Ce format propose 2 paramètres :

1. `jeu de couleurs` \(_colour scheme_\) : permet de choisir les couleurs des pays à partir d'une série de palettes prédéfinies,
2. `jeu de couleurs au survol` \(_hover colour scheme_\) : permet de choisir les couleurs des pays au survol de la souris à partir d'une série de palettes prédéfinies.

## Routines

Si le corpus de données comporte un champ avec les [codes ISO](https://fr.wikipedia.org/wiki/ISO_3166-1) 3 des pays, ce format nécessite l'utilisation de la routine [distinct-by](/Configuration/routines/DistinctBy.md), appliquée à l'identifiant du champ représenté, qui doit être déclarée dans `valeur` \(_value_\) selon:

/api/run/distinct-by/**identifiant**/

où **identifiant** est le code attribué par LODEX au champ contenant les codes ISO 3 des pays.

Si le corpus de données ne comporte pas les codes ISO 3 des pays, ce format nécessite l'utilisation de la route [distinct-ISO3166-1-alpha3-from](//Configuration/routines/DistinctISO31661Alpha3From.md), appliquée à l'identifiant du champ contenant les **pays verbalisés**, \(ou la route distinct-alpha-2-alpha3-from, appliquée à l'identifiant du champ contenant les c**codes ISO 2 des pays**\) qui doit être déclarée dans `valeur` \(_value_\) selon:

/api/run/distinct-ISO3166-1-alpha3-from/**identifiant**/ \(ou /api/run/distinct-alpha-2-alpha3-from/**identifiant**/\)

où **identifiant** est le code attribué par LODEX au champ contenant les **pays verbalisés**.

