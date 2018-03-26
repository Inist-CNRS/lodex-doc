# distinct-ISO3166-1-alpha2-from

La routine `distinct-ISO3166-1-alpha2-from` \(fournie par [https://github.com/Inist-CNRS/lodex-extented/](https://github.com/Inist-CNRS/lodex-extented/)\) transforme les pays verbalisés du champ représenté en leurs codes ISO 2 et compte, pour chaque code ISO 2 du pays du champ représenté \(identifiant\), le nombre de fois où ce pays apparaît qui correspond à :

* nombre d'occurrences si le champ n'est pas dédoublonné
* nombre de documents si le champ est dédoublonné

Elle est, en particulier, utilisée avec le format [Cartography](/Administration/Modèle/Format/Cartography.md) \(Cartographie\) pour représenter les pays du corpus sur une carte du monde.

> **Attention**: avant d’utiliser cette routine, il peut être utile de vérifier que les formes d’écriture des pays verbalisés du corpus correspondent bien aux formes d’écriture des pays dans la table de correspondance \([https://raw.githubusercontent.com/Inist-CNRS/lodex-use-cases/master/country/data.json](https://raw.githubusercontent.com/Inist-CNRS/lodex-use-cases/master/country/data.json)\).

**Exemple :** [http://lodex-cop21.dpi.inist.fr/api/run/distinct-ISO3166-1-alpha2-from/g61g/](http://lodex-cop21.dpi.inist.fr/api/run/distinct-ISO3166-1-alpha2-from/g61g/) où g61g = PaysENGRSansFrance \(pays verbalisé en anglais: Algeria, Argentina, Australia, etc.\)

![Résultat JSON de la routine distinct-ISO3166-1-alpha2-from](/assets/RoutineDistinctISO31661Alpha2From.png)
