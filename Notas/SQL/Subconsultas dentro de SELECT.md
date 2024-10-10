---
Fecha_creación: 2024-05-16
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - Fundamentos
URL: 
Tipo_recurso: DataCamp
---
- Para incluir un valor agregado en una consulta SQL y con la subquery con SELECT podemos evitar eso
- Son utilez para operaciones matemáticas complejas

## Requisitos

- La subconsulta debe de devolver un único valor
# Es un Groupby pero con subconsulta

```SQL
SELECT countries.name AS country,
-- Subconsulta que proporciona el numero de ciudades
	(SELECT COUNT(*)
	FROM cities
	WHERE countries.code = cities.country_code) AS cities_num
FROM countries
ORDER BY cities_num DESC, country
LIMIT 9;
```