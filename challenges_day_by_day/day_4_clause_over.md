( à mettre à jour)
PROGRAMME DU JOUR 

Définir une Window function

La syntaxe générale d’une window function

Comment définir le cadre de fenêtrage avec les sous clauses PARTITION BY et ORDER BY

La différence entre PARTITION BY et GROUP BY

Les fonctions de fenêtres : les window functions liées au rang et les fonctions d’agrégations de fenêtrage ou de cadre de fenêtre

⇒      Fonctions liées au rang
RANK
DENSE_RANK
RANK_BETWEEN
ROW_NUMBER
NTILE
LAG
LEAD
FIRST_VALUE
LAST_VALUE
 

⇒   Fonctions d’agrégations de fenêtrage (moyenne mobile, somme cumulative)

SUM
COUNT
AVG
MAX
MIN


La clause OVER est essentielle aux fonctions de fenêtre SQL. 
C’est l’élément principal des fonctions de fenêtrage ou windows functions (j’avoue que c’est plus stylé en anglais, bon bref, c’est pas important ce que je viens de dire ne preter pas attention à ma dernière )
Sans clause OVER(), il nya pas de windows functions 

Mais , c’est quoi une windows functions? pour mieux comprendre ce que c’est: 

je vais faire le parallèle avec les fonctions d’agrégations. 
D’habitude quant on applique une fonction d’agrégation on prend en entrée un groupe ou ensemble de ligne et on retourne en sortie  un résultat avec juste une seule ligne soit la sum, la moyenne, etc 
et donc la fonction d’aggreation reduit les lignes entrée en une seule ligne
et c'est tout le contraire des windows functions qui retourne un résultat avec les mêmes nombre de lignes qu’au départ. les windows fonctions affiche les resultats pour chaque ligne individuels. 
Et donc sur chaque ligne, elle effectue des transformations ou fonctions de fenètre et renvoie le resutat sur chaque ligne en fonction de chaque fonction 

Exemple:
sum(ventes) 
sum(ventes) over()

Comme je disais tant tot, sur chaque ligne, elle effectue des transformations ou fonctions de fenètre et renvoie le resutat sur chaque ligne en fonction de chaque fonction 

Il y a deux choses à savoir sur les fonctions de fenetrage

1er chose, la syntaxe des windows fonctions contient toujours la clause over ()

2ieme chose, à gauche et à droite de la clause over() il ya des choses à savoir autrement dit la syntaxe des functions de fenetrage s’ecrit comme ceci et c’est à maitriser


windows fonctions over( sous clause ) 

A gauche on n’a des windows functions et  à droite dans la clause over on na des sous clause

en terme de windows functions, on a des windows fonctions d’agrégations comme la sum, avg, .. pour les moyennes mobiles(avg), les sum cumul (sum)

Des windows functions de classement comme des row_number, rank, 

Et comme sous clause, on n’a partition by et order by

Et dans une seule requète, on peut avoir plusieurs windows functions

et dans une seule syntaxe, on n’a à la fois des windows functions et les sous clause

Et donc une fenètre ici c’est un ensemble de ligne ou un groupe de ligne et les sous-clause permettent de definir qui sera dans chaque fenètre, quelle ligne sera dans chaque cadre de fenètre quel conditions remplir pour appartenir à tel ou tel fenètre ou encore sous quel condition on doit former les differents cadre de  fenètre

La sous-clause PARTITION BY définit les critères que les enregistrements doivent satisfaire pour faire partie du cadre de fenêtre. En d'autres termes, PARTITION BY définit les groupes dans lesquels les lignes sont divisées ;
la clause ORDER BY définit l'ordre des enregistrements dans le cadre de la fenêtre.
