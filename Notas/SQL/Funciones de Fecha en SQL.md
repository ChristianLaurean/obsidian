---
Fecha_creación: 2024-07-21
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - intermedio
URL:
---


# Extract
```SQL
SELECT 
	fecha_estreno,
	EXTRACT(YEAR FROM fecha_estreno) AS Year,
	EXTRACT(MONTH FROM fecha_estreno) AS MES,
	EXTRACT(DAY FROM fecha_estreno) AS DIA
FROM episodios

```
# DATEPART

