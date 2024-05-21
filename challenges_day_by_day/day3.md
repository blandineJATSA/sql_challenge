# Mon programme du jour 3 de mon apprentissage de SQL

- [Apprentissage de tous les fonctions les plus utilisés ainsi que la pratique](#apprentissage)




<a name="apprentissage"></a>
## Apprentissage de tous les fonctions les plus utilisés ainsi que la pratique

### Les fonctions d'aggregrations statistiques

Les 5 fonctions les plus utilisés sont: COUNT, SUM, AVG, MAX; MIN

- **COUNT :** permet de compter le nombre de ligne ( non nulle)  d'une colonne ou d'une table
Pour compter le nombre de ligne d'une table tout entière il suffit d'écrire COUNT(*) dans une requète SQL.
Pour compter le nombre de ligne d'une colonne : COUNT(colonne)

**Exemple :**  1. Une requète qui 
               2. Une requète qui 

- **AVG :** qui permet de calculer la moyenne sur un ensemble de ligne

- **SUM :**  qui permet de calculer la somme sur un ensemble de ligne

- **MIN, MAX :** qui recupère le max et le min d'une ensemble de ligne

  
### Les fonctions de chaine de caractères

- **CONCAT :**  permet de concatener les valeurs de plusieurs colonnes en une seule chaine de caractère.

On peut l'utiliser dans la clause SELECT pour concatener par exemple le nom et le prenom.

On peut l'utiliser dans la clause WHERE pour par exemple rechercher les informations d'une persone avec à la fois son nom et prenom ( WHERE  CONCAT(prenom, ' ', nom) LIKE 'Sabine Lemaire')

- **LENGTH/ LEN :**  permet d'extraire le nombre de caractère d'une chaine de caractère
On peut par exemple recuperer les utilisateurs ou client dont le nombre de caractère de leur numero de Tel est inferieur à 10.

- **REPLACE :** permet de remplacer les caractères dans une chaine de caractère : REPLACE ( chaine_caractère, caractères à remplacer, nouveau_caractères)
- **SUBSTRING :** permet d'extraire une partie de caractère d'une chaine de caractère
- **LEFT :**  permet d'extraire le nombre souhaité de caractère à partir du premier caractère d'une chaine. LEFT(chaine, longueur)
- **REVERSE :** permet de retourner une chaine de caractère par ordre inverse de chaine de caractères
- **TRIM :** permet de supprimer un caractère au debut et  la fun d'une chaine de caractère. **LTRIM** permet de supprimer un caractère au debut d'une chaine et **RTRIM :** à la fin d'une chaine de caractère
- **UPPER :** permet de transformer une chaine de caractère en Majuscule et **LOWER** en miniscule
- **UCASE :** permet de transformer toute les lettres d'une chaine de caractère en majuscule
- **LCASE :** permet de transformer toute les lettres d'une chaine de caractère en miniccule
- **LOCATE :** permet de retourner la position d'une chaine de caractère dans une chaine de caractère

### Les fonctions de maths numeriques

- **RAND** : retourne un nombre decimal aleatoire compris entre 0 et 1
- **ROUND :**  permet d'arrondir un nombre pour obtenir exclusivement des nombres entiers

### Les fonctions de dates et d'heures
- **DATE_FORMAT :** permet de formater une donnée date en un format indiqué. DATE_FORMAT(date, format)
- **DATEDIFF :**  permet de determiner la difference ou l'interval entre 2 dates, spécifié : DATEDIFF(type_limite, data1, date2)
- **TIMEDIFF() :** permet de calculer la différence entre 2 heures distinctes
- **DAYOFWEEK :** permet de spécifier le jour de la semaine d'une date spécifié
- **MONTH()** permet d’extraire le numéro de mois à partir d’une date au format AAAA-MM-JJ, **DAY()** pour extraire le jour d’une date, **YEAR()** pour extraire l’année d’une date.
- **NOW()** permet de retourner la date et l’heure du système
- **TIMESTAMP()** est utilisée pour obtenir un DATETIME à partir d’une DATE


### Les fonctions de chiffremments

- **MD5 :**  permet de chiffrer une chaîne de caractère en un entier hexadécimal de 32 caractères; Il permet par exemple de crypter et securiser les infos telq que les mots de passe des utilisateurs 
- **CAST() :** est une fonction de transtypage qui permet de convertir une données d’un type en un autre. Il est par exemple possible de transformer une date au format DATETIME en DATE ou encore le un float en integer
- **ISNULL() :**  permet de vérifier si une données est nulle, peut s’avérer utile pour traiter des résultats qui possèdent des données nulles. ISNULL(colonne) retourne 1 pour les ligne NULL pour cette colonne et 0 sinon.
- **GROUP_CONCAT() :**  permet de regrouper les valeurs non nulles d’un groupe en une chaîne de caractère. Cela est utile pour regrouper des résultats en une seule ligne; par exemple vous avez des categories de produit et pour chaque categorie, vous avez la possibilité de les regroupé sur une seule ligne dans une seule colonne tout juste après chaque categorie, cela regroupe plusieurs information utile en un seul endroit. Par exemple vous avez une table film et pour chaque fim vous avez les nom d'acteur ayant jouer dans ces films, vous pouvez decider, pour chaque acteur,  de regrouper en une seule chaine de caractère le nom des films dans lesquels ils ont joués.
