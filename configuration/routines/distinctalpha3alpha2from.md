# distinct-alpha-3-alpha2-from

La routine `distinct-alpha-3-alpha2-from` \(fournie par [https://github.com/Inist-CNRS/lodex-extented/](https://legacy.gitbook.com/book/lodex/lodex-user-documentation/edit)\) transforme les codes ISO 3 des pays du champ représenté en leurs codes ISO 2 et compte, pour chaque code ISO 2 du pays du champ représenté \(identifiant\), le nombre de fois où ce pays apparaît qui correspond à :

* nombre d'occurrences si le champ n'est pas dédoublonné
* nombre de documents si le champ est dédoublonné

**Attention**: avant d’utiliser cette routine, il peut être utile de vérifier que les codes ISO 3 des pays du corpus correspondent bien aux codes ISO 3 dans la table de correspondance \([https://raw.githubusercontent.com/Inist-CNRS/lodex-use-cases/master/country/data.json](https://legacy.gitbook.com/book/lodex/lodex-user-documentation/edit)\).

