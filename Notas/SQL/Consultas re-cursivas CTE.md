---
Fecha_creación: 2024-07-10
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - Concepto
URL:
---

# CTE: COMMON TABLE EXPRESION



- Una CTE es una consulta temporal que su resultado de la query lo podemos referencia dentro de otra consulta [[Notas/SQL/SQL|SQL]]

- Las CTE se utilizan para simplificar y hacer mas legibles las consultas SQL complejas.

## Creando el CTE

## CTE BASICA

```SQL
WITH ListaEpisodios AS (
	SELECT serie_id, episodio_id, titulo
	FROM episodios
)
SELECT * FROM ListaEpisodios;

```

## CTE Subconsulta

```sql
WITH nombre_cte AS (
	SELECT
		e.*,
		COUNT(*) AS num
	FROM employees AS e
	INNER JOIN project_employees AS pe
		ON e.id = pe.id_employee
GROUP BY 1
)

SELECT *
FROM nombre_cte;
```

## Podemos usar varias CTE

```sql
WITH ListaEpisodios_cte AS (
	SELECT serie_id, episodio_id, titulo
	FROM episodios
),

lista_series_cte AS (
	SELECT 
		serie_id,
		descripcion 
	FROM series
)

-- query principal
SELECT * FROM ListaEpisodios_cte
LEFT JOIN lista_episodios_cte
	ON ListaEpisodios_cte.serie_id = lista_series_cte.serie_id;
```
