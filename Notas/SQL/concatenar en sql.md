---
Fecha_creación: 2024-06-18
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - SQL
URL:
---
Para concatenar una columna con un texto en PostgreSQL, puedes usar el operador de concatenación (`||`). Aquí tienes un ejemplo:

```sql
SELECT nombre || ' - usuario' AS nombre_concatenado
FROM usuarios;
--O

SELECT CONCAT(lpu."Borough",'/',lpu."Zone") AS "pick_up_loc"
FROM table
```

- Si necesitas concatenar múltiples columnas y textos, puedes encadenar el operador de concatenación (`||`). Por ejemplo:
    
```sql 
SELECT nombre || ' ' || apellido || ' - usuario' AS nombre_completo
FROM usuarios;`
```    

- Si la columna contiene valores nulos, puedes usar la función `COALESCE` para evitar problemas con la concatenación. Por ejemplo:
- 
```sql 
SELECT COALESCE(nombre, '') || ' - usuario' AS nombre_concatenado 
FROM usuarios;
```

## concatenar de forma agrupada

STRING_AGG()

```SQL
SELECT 
    INITCAP(e.first_name) || ' ' || INITCAP(e.last_name) AS full_name,
    STRING_AGG(p.title, ', ') AS project_titles,
    COUNT(*) AS num_proyectos
FROM employees AS e
INNER JOIN project_employees AS pe
    ON e.id = pe.id_employee
INNER JOIN projects AS p
    ON pe.id_project = p.id_project
GROUP BY 1
ORDER BY 3 DESC
LIMIT 2;
```
