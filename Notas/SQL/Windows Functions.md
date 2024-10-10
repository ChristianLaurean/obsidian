---
Fecha_creación: 2024-07-22
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - avanzado
URL:
---


Las funciones de ventana nos ayudan a hacer cálculos en un conjunto de [[filas]] relacionadas y devuelve un valor para cada fila de esa relacion. 

Las funciones de ventana en verde juntar todas las filas en una, las [[Windows Functions]] lo que hacen es conservar las filas originales muentras agregas información adicional. 

## consideraciones al usar [[Windows Functions]] 

1. Se procesan después de la consulta completa excepto la instrucción ORDER BY
2. Usa el conjunto de resultados y hace las operaciones
3. No están en SQL Lite
#### Nos ayuda a utilizar funciones agregadas sin group by

```SQL
SELECT 
	colums,
	(colum1 + columns2) OVER() AS windosw
FROM table
WHERE date = "2022";
```

resultado: 

![[Pasted image 20240801105031.png]]

# ROW_NUMBER

La función lo que hace es agregar un numero_unico a cada fila del resultado de nuestra consulta basándonos en el orden que especifiquemos.

`OVER()` Sobre que queremos correr la función row_number

```SQL
SELECT 
	titulo,
	año_lanzamiento,
	ROW_NUMBER() OVER(ORDER BY año_lanzamiento DESC) AS order_lanzamiento  
FROM series
```

# PARTITION BY

Nos ayuda a dividir los resultados de una consulta en particiones en las que luego le podemos agregar una [[Windows Functions]]

```sql
SELECT 
	titulo,
	genero,
	año_lanzamiento,
	AVG(Colums) 
		OVER(PARTITION BY column2 ORDER BY año_lanzamiento) AS ranking  
FROM series;


SELECT 
	titulo,
	genero,
	año_lanzamiento,
	ROW_NUMBER() OVER(PARTITION BY genero ORDER BY año_lanzamiento) AS ranking_por_genero  
FROM series;
```
Agrega un valor único por cada partición de genero y se vuelve a reiniciar por cada nuevo genero. 
![[Pasted image 20240723111937.png]]

# RANK()

- Es el hermano mayor de ROW_NUMBER
rank no ayuda a darle rangos a las filas de nuestra consulta basándonos en un criterio de ordenamiento .
si dos o mas filas tienen el mismo valor de la columna que estamos ordenando, todas van a recibir el mismo rango. 

```SQL
SELECT
	titulo,
	rating_imdb,
	RANK() OVER(ORDER BY rating_imdb) AS ranking_imdb
FROM episodios;
```

Lo que hace es que repite el rango si son iguales y por dentro cuenta el rango y por eso sigue de 2 a 6
![[Pasted image 20240723120025.png]]
# DENSE_RANK()

Es muy similar a RANK() pero con un enfoque distinto de como maneja los emparejamientos.

No deja espacios en los valores de clasificación con los rangos, Osea que hace una secuencia continua a diferencia de rank que es separada la secuencia
```SQL
SELECT 
    titulo,
    rating_imdb,
    DENSE_RANK() OVER(ORDER BY rating_imdb) AS ranking_imdb
FROM episodios;
```

![[Pasted image 20240723120337.png]]

# Sliding windows

Hace cálculos relativos a las filas actual del conjunto se puede usar con funciones agregadas.

Dividir cada registro

```SQL
ROWS <funciones_especiales> <start> AND <end>

-- funciones especiales disponibles
PRECEDING -- Especifica el numero de filas antes o despues de la fial actual 
FOLLOWING -- Igual que proceding 
UNBOUNDED PRECEDING -- le dice a SQL que desea incluir cada fila desde el principio o el final del conjunto
UNBOUNDED FOLLOWING
CURRENT ROW -- LE dice que desea detener su calculo en la fila actual 
BETWEEN
```

```sql
SELECT
	date,
	SUM(colum)
		OVER(ORDER BY date ROWS BETWEEN
			UNBOUNDED PRECEDING AND CURRENT ROW) AS 
FROM table;
```

## RANGE

# LAG

Nos permite acceder a una fila anterior a la fila actual en el conjunto del resultado de una consulta.
```sql
SELECT
    id,
    fecha,
    monto,
    LAG(monto, 1) OVER (ORDER BY fecha) AS monto_anterior
FROM
    ventas;
```
![[Pasted image 20240803090836.png]]

# LEAD
Es similar a LAG, pero nos permite acceder a una fila posterior.
```sql
SELECT
    id,
    fecha,
    monto,
    LEAD(monto, 1) OVER (ORDER BY fecha) AS monto_siguiente
FROM
    ventas;
```

![[Pasted image 20240803093408.png]]
# FIRST_VALUE and LAST_VALUE

FIRST_VALUE(column):Retorna el primer valor de la tabla dentro de una partición definida
LAST_VALUE(column): Retorna el ultimo valor de la tabla dentro de una partición definida

```sql
SELECT
    id,
    fecha,
    monto,
    FIRST_VALUE(monto) OVER (ORDER BY fecha) AS primer_monto
FROM
    ventas;
```
![[Pasted image 20240803093742.png]]

Ejemplo de Uso de LAST_VALUE

```sql
SELECT
    id,
    fecha,
    monto,
    LAST_VALUE(monto) OVER (ORDER BY fecha ROWS BETWEEN UNBOUNDED PRECEDING AND UNBOUNDED FOLLOWING) AS ultimo_monto
FROM
    ventas;
```
![[Pasted image 20240803093808.png]]