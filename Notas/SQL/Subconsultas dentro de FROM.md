---
Fecha_creación: 2024-05-16
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - Fundamentos
URL: 
Tipo_recurso: DataCamp
---
```sql
-- Selecciona local_name y lang_num de las tablas apropiadas
SELECT local_name, lang_num
FROM countries,
	(SELECT code, COUNT(*) AS lang_num
	FROM languages
	GROUP BY code) AS sub
-- Donde coincida code
WHERE countries.code = sub.code
ORDER BY lang_num DESC;
```


