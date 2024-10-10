---
Fecha_creación: 2024-07-23
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - avanzado
URL:
---

Son [[Expresiones Regulares]] en [[Notas/SQL/SQL|SQL]] 

Son una secuencia de caracteres que forman un patrón de búsqueda.

```sql
SELECT
	titulo,
	descripcion
FROM series
WHERE descripcion ~* '(?i)más';
```

`(?i)` Búsqueda entre mayúsculas y minúsculas