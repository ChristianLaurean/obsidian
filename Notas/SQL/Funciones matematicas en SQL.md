---
Fecha_creación: 2024-07-22
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - intermedio
URL:
---

Son funciones que nos ayudan a redondear números para arriba, para abajo.


# ROUND


```SQL
SELECT 
	titulo,
	duracion/60 AS horas_completas,
	ROUND(duracion/60) AS Horas_completas_redondeadas
FROM Episodios;
```

# CEILING

Redondea un numero hacia arriba del mas cercano

```sql
SELECT 
	titulo,
	duracion AS horas_completas,
	CEILING(duracion/60.0) AS Horas_completas_redondeadas
FROM Episodios;
```

# FLOOR

Se redondea para el numero mas cercano para abajo. 

```SQL
SELECT 
	titulo,
	duracion AS horas_completas,
	FLOOR(duracion/60.0) AS Horas_completas_redondeadas
FROM Episodios;
```