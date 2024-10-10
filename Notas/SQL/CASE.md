---
Fecha_creación: 2024-07-04
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - Manipulación_datos
URL:
---
`CASE` es una sentencia condicional en SQL que realiza distintas acciones en función de distintas condiciones. Permite ejecutar lógica IF-THEN-ELSE en consultas SQL. Se puede utilizar en cualquier sentencia o cláusula que permita una expresión válida.


EL [[CASE]] es un  condiciónal en programación lo podemos ver con un IF que tiene 3 partes:
- `WHEN`: Comprueba la condición 
`THEN`: Entonces pasara algo si es <font color="#2DC26B">VERDADERO</font>
`ELSE` : Si es <font color="#2DC26B">FALSO</font> que pase otra cosa.

Ejemplo

```SQL
SELECT
	CASE 
		WHEN columns = 1 THEN 'A'
		WHEN colums = 2 THEN 'B'
		ELSE 'c' 
	END AS name_colums
FROM table
```
## Multiples condiciones en una sola

```SQL
SELECT 
	CASE 
		WHEN colum = 'A' AND column > 2 THEN 'HOLA'
		ELSE 'ADIOS'
	END AS f
FROM table;
```

# case EN WHERE 
![[Pasted image 20240704080943.png]]

## case en funciones de agregación

```postgresQL
SELECT 
	columns1,
	COUNT(CASE 
			  WHEN hometeam_id = 2342 
			  AND columns23 > 5 THEN 'HOLA'
		  END) AS count_file
FROM tablesf
GROUP BY columns1;
```
## Calcular el porcentaje de juegos ganados

![[Pasted image 20240704084101.png]]
