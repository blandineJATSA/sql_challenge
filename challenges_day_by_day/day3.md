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

-**AVG :** qui permet de calculer la moyenne sur un ensemble de ligne

-**SUM :**  qui permet de calculer la somme sur un ensemble de ligne

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
- 
