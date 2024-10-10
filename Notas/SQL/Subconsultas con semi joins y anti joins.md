---
Fecha_creación: 2024-05-16
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - Fundamentos
URL: 
Tipo_recurso: DataCamp
---



Una semi joins es usando el Where. con el Where filtramos y encontramos una lista que esa lista la podemos usar para otra clausula del where

```SQL
SELECT *
FROM table
WHERE col IN (
	SELECT col
	FROM table_2
	WHERE year > 1800
);
```