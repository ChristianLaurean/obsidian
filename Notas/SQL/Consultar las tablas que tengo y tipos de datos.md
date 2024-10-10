---
Fecha_creación: 2024-06-14
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - Fundamentos
URL:
---

```SQL
-- Query the right table in information_schema

SELECT table_name
FROM information_schema.tables
-- Specify the correct table_schema value
WHERE table_schema = 'public';+
```


## checar las columnas

```SQL
SELECT column_name, data_type
FROM information_schema.columns
WHERE table_name = 'university_professors' AND table_schema = 'public';
```

