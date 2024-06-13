les CTE (Common Table Expression)


La syntaxe : 

WITH
    my_cte (cte_col_1, cte_col_2) AS (
        SELECT col_1, col_2
            FROM ...
    )
SELECT ... FROM my_cte;

