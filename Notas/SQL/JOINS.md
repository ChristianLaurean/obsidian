---
Fecha_creación: 2024-05-31
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - Fundamentos
URL: 
Tipo_recurso: Blog
---



![[Export (2).png]]
# ¿Que estamos haciendo?

Obtener datos de varias tablas en una sola consulta.

¿Cuándo necesito usarlo? Unirse es una acción muy común. La mayoría de las bases de datos almacenan datos en varias tablas, por lo que es común (y eficiente) necesitar consultar varias tablas a la vez para obtener información significativa.

## ¿CÓMO FUNCIONA?

La cláusula `FROM` especifica la tabla de la que queremos obtener datos, pero si necesitamos fusionar tablas podemos usar la cláusula `JOIN`:

```SQL
SELECT 
   <col_name> {AS <alias>}, 
   <col_name> {AS <alias>}
FROM <table_name_1>
JOIN <table_name_2> 
ON <table_name_1>.<column> = <table_name_2>.<column>
```

## Left joins

Esta es la forma más común de unir tablas. Tomará todos los valores de la tabla izqierda y solo los que coincidan de la tabla derecha. si la tabla derecha no tiene valores que se relacionen con la izquierda saldrán valores null

![[Pasted image 20240416112056.png]]

**Soup sales table**        **Customers table**
![[Export (3).png]]

![[left_join.png]]

## Right joins 

Es lo contrario a left joins

![[Pasted image 20240416112313.png]]
## Inner joins 

Lo que hace es buscar solo los registros que tengan ambas tablas con los mismos valores


**Soup sales table**        **Customers table**
![[Export (3).png]]

![[inner_join.png]]
## Uso de `USING`

Se utiliza `USING` cuando el campos que se van a unir tenga el nombre idéntico 

## Multiples joins

```SQL
SELECT *
FROM table_izquierda AS tz
INNER JOIN table_derecha AS td
ON tz.colum = td.column
INNER JOIN otra_table AS ot
ON table_iz_or der.colum = ot.colum;
```

# Joins condicionales

Técnicamente, este no es un tipo diferente de unión: es una idea que se puede aplicar a la mayoría de los tipos de unión. En lugar de equiparar valores entre tablas, puede utilizar declaraciones condicionales para tener mayor flexibilidad a la hora de definir qué filas están unidas y qué no.

Un ejemplo típico de esto es observar la actividad entre ciertas fechas, como toda la actividad de un usuario entre su primera y segunda visita a su sitio web.

```SQL
SELECT *
FROM table_izquierda AS tz
INNER JOIN table_derecha AS td
ON tz.colum = td.column
	AND tz.otra_colum = td.otra_colum 
```



**Soup sales table**        **Customers table**
![[Export (3).png]]

![[conditional_join.png]]
## Full joins

Es la combinación de un Left joins y un Right joins.
Te devolverá todo lo que tenga la tabla izquierda y la tabla derecha no importa si no existe en la otra tabla y si no existe saldrá null.

![[Pasted image 20240416113654.png]]

```SQL
SELECT *
FROM table_izq
FULL JOIN tabla_derecha
USING(id);
```

## CROSS JOIN

Las uniones cruzadas deben usarse con moderación ya que son costosas desde el punto de vista computacional. Básicamente encuentran todas las combinaciones de entradas entre cada tabla.


![[Pasted image 20240416115831.png]]
```SQL
SELECT *
FROM table_izq
CROSS JOIN
```

## Self joins

Los selft joins lo usamos para comparar valores de una tabla con otros valores dentro de la misma tabla

![[Pasted image 20240416121255.png]]
![[Pasted image 20240416121303.png]]