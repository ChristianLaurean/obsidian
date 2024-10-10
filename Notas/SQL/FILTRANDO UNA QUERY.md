---
Fecha_creación: 2024-05-31
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - Fundamentos
  - SQL
URL: 
Tipo_recurso: Blog
---

# Seleccionar filas

![[Export (1) 1.png]]

# ¿Que estamos haciendo?

 Reducir las filas que nos devuelven mediante la creación de filtros.

## CÓMO FUNCIONA

La cláusula `WHERE` especifica las filas que queremos devolver. Para hacer eso debemos escribir declaraciones que se evalúen como VERDADERAS o FALSAS y que determinarán si se devuelve una fila o no.

```SQL
SELECT 
   <col_name> {AS <alias>}, 
   <col_name> {AS <alias>}
FROM <table_name>
WHERE <predicate>
	{AND|OR <predicate>}
```

### Combinando filtros

Para combinar filtros, puede utilizar `AND` y `OR`.
```SQL
WHERE 
   date is not null 
   and album_type = 'single'
```

Puede utilizar paréntesis para combinar con una lógica aún más compleja.

```SQL
WHERE
   day >= '2017-12-01'
   and day is not null
   and (
      streams >= 1000000
      or rank between 2 and 5
   )
```

### Filtrar fechas y números

Para variables continuas puede utilizar los siguientes operadores y palabras clave:
 
![[filter_values.png]]
#### Usando `BETWEEN`

Muéstrame Entre este numero y el otro

```sql
SELECT 
	names
FROM table
WHERE 
	year BETWEEN 1992 AND 2000 
	AND names = "MX";

```

### Filtrado de valores discretos

Para columnas discretas (por ejemplo, texto o binarios), puede utilizar las siguientes opciones de filtrado:

![[filter_discrete.png]]
#### Usando `LIKE`

- `LIKE` Lo usamos para encontrar un patrón en un str.
- `%` Coincide con 0, uno o muchos caracteres de texto
- `_` : Solo coincide con un solo valor que sigue

```sql
SELECT 
	names 
FROM table 
WHERE 
	name LIKE 'ADE%' -- Los que empiecen con ade
---
SELECT 
	names 
FROM table 
WHERE 
	name LIKE 'ADE %' -- Tambien podemos buscar con espacios
---
SELECT 
	names 
FROM table 
WHERE 
	name LIKE '_e' -- Solo me trae los que empiecen con un solo caracter

```

- `NOT LIKE` Busca los patrones que no coincidan

```SQL
SELECT 
	names 
FROM table 
WHERE 
	name NOT LIKE '%Ae' -- me trae todos exepto los que terminan con Ae
```

#### USANDO `IN`

```SQL
SELECT 
	names 
FROM table 
WHERE  name IN ('pepe','chris') -- Filtra todos esos nombres
```

### Filtrado de NULL

Cuando desee excluir (o incluir) valores NULL, podemos usar la palabra clave NULL en SQL:

 ![[filter_nulls.png]]
#### `IS NOT NULL`

```SQL
SELECT 
	names 
FROM table 
WHERE  name IS NOT NULL;
-- Filtra los resultados que nos sean nulos
```
## NO OLVIDES

1. Sus declaraciones de filtro deben evaluarse como VERDADERAS o FALSAS.
2. Puede combinar varias declaraciones usando `AND` y `OR`
3. También puede filtrar con la palabra clave `HAVING`; sin embargo, eso solo se aplica a los agregados y, por lo tanto, se analiza en esa sección.
4. También puede utilizar declaraciones lógicas (predicados) en otras partes de una declaración SQL.