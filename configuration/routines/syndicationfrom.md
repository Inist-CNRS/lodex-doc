# syndication-from

La routine `syndication-from` fait référence à une autre ressource **du même jeu de données** en liant les `valeurs` entre elles et non leurs arks. Il affiche ainsi les informations que l'on souhaite via les identifiants de la ressource.

Elle est, en particulier, utilisée avec le format [Resources Grid](../../administration/modele/format/resourcesgrid.md) pour représenter les champs paramétrés dans [syndication-from](syndicationfrom.md) sur la page de la ressource.

Elle doit alors être déclarée dans `Value` \(Valeur\) selon :

                                                                   /api/run/syndication-from/**nC6e**/...

**nC6e** représente l’**identifiant** du champ de la valeur que nous souhaitons voir liée. 

Par exemple l'instance revue de sommaire \([https://revue-sommaire.data.istex.fr](https://revue-sommaire.data.istex.fr/)\):

![lier un journal &#xE0; une ressource](../../.gitbook/assets/image%20%2820%29.png)

Cette ressource récupére les informations d'une autre ressource via son identifiant ISSN déclaré dans une colonne bien spécifique portant l'identifiant **nC6e**. On reporte donc la valeur à la fin:

                                                             /api/run/syndication-from/**nC6e**/0300-4910

Exemple: [https://revue-sommaire.data.istex.fr/ark:/67375/8Q1-WFCZK0TX-L](https://revue-sommaire.data.istex.fr/ark:/67375/8Q1-WFCZK0TX-L)



