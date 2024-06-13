
Les fonctions de classement en SQL sont un sous-ensemble de fonctions de fenêtre qui attribuent un classement unique à chaque ligne d'une partition ou fenètre. Ces valeurs de classement correspondent à un ordre spécifique, déterminé par la clause ORDER BY au sein de la fonction.



Il existe trois fonctions de classement principales dans SQL, à savoir :
- RANK(),
- ROW_NUMBER(),
- DENSE_RANK() 

Chacune de ces fonctions fonctionne légèrement différemment, mais elles ont toutes pour objectif commun de classer les données en fonction de conditions spécifiées. 

RANK() et DENSE_RANK() les fonctions ont un comportement similaire dans la mesure où elles attribuent le même rang aux lignes avec des valeurs identiques. La différence cruciale réside dans la manière dont ils gèrent le classement suivant. RANK() saute le rang qui suit les lignes identiques, alors que DENSE_RANK() ce n'est pas le cas. Par exemple, si deux lignes sont classées 1, la suivante sera classée 3.

D'un autre côté, ROW_NUMBER attribue un numéro de ligne unique à chaque ligne, que les valeurs de tri par colonne soient identiques ou non. 

Le choix entre ces fonctions peut avoir un impact significatif sur vos résultats et les informations dérivées de vos données.


* RESUME

- **ROW_NUMBER :** Attribue un numéro unique à chaque ligne au sein de la partition. Même si les valeurs sont les mêmes, les numéros seront différents.

- **RANK :** Attribue le même numéro de rang aux lignes avec des valeurs identiques, mais laisse des "trous" dans le classement. Par exemple, si deux lignes sont classées 1, la suivante sera classée 3.

- **DENSE_RANK :** Attribue le même numéro de rang aux lignes avec des valeurs identiques, mais sans laisser de "trous" dans le classement. La ligne suivante après des valeurs identiques aura le rang suivant immédiat, es valeurs retournées par la fonction DENSE_RANK ne comportent pas de vides et définissent toujours des valeurs de rang consécutives.



**EXEMPLES PRATIQUES QUI UTILISENT CES FONCTIONS DE CLASSEMENTS**

* Une requête qui classe les vendeurs en fonction de leurs ventes annuelles,

* Une requête qui classe les commerciaux de chaque secteur de vente en fonction de leurs ventes totales

* Une requête qui classe les produits de l’inventaire par les emplacements d’inventaire spécifiés, en fonction de leurs quantités. 

* Une requête qui retourne les dix principaux employés classés en fonction de leur salaire. 

*  Une requète qui classe les produits au sein de chaque catégorie basé sur leurs prix de détail 

