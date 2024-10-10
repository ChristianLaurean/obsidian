---
Fecha_creación: 2024-06-14
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - Concepto
URL:
---
# Mayusculas y minusculas
```sql
SELECT UPPER(titulo)FROM table; -- Convierte en mayusculas cualquier texto
SELECT LOWER(titulo)FROM table; -- Convierte en minusculas cualquier texto
```

# LONGITUD

En SQL, `LENGTH`es una función incorporada que le permite encontrar la cantidad de caracteres en una cadena o la longitud de una cadena.

Sintaxis:

```sql
LENGTH ( string )
```

Aquí `string`puede haber cualquier cadena literal, columna o expresión que dé como resultado una cadena.

## Ejemplos

Consideremos una tabla de “empleados”:

|identificación|nombre de pila|apellido|
|---|---|---|
|1|John|Gama|
|2|Jane|Herrero|
|3|Alicia|Murphy|

Para calcular la longitud del campo first_name para todos los registros, utilice la siguiente declaración SQL:

```sql
SELECT first_name, LENGTH(first_name) as length_of_first_name
FROM employees;
```

Producción:

|nombre de pila|longitud del nombre|
|---|---|
|John|4|
|Jane|4|
|Alicia|5|

## Uso con DISTINCT

`LENGTH`También se puede utilizar junto con `DISTINCT`para encontrar el número de longitudes distintas de un campo específico.

```sql
SELECT DISTINCT LENGTH(first_name) as distinct_length_of_first_name
FROM employees;
```

## Uso con cláusula

Puede funcionar en la cláusula WHERE para devolver solo aquellos registros donde la longitud de un campo específico cumple una determinada condición.

```sql
SELECT *FROM employees
WHERE LENGTH(first_name) > 4;
```

# LEFT AND RIGHT

Esta función lo que hace es que toman un texto desde la izquierda o derecha.

```SQL
SELECT LEFT(titulo,3) FROM tabla; -- Extrae los primeros 3 caracteres 
SELECT RIGHT(titulo,3) FROM tabla; -- Extrae los ultimos 3 caracteres
```
# SUBSTRING

La `SUBSTRING`función SQL se utiliza para extraer una parte de una cadena, donde se puede especificar la posición inicial y la longitud del texto. Esta función puede resultar muy útil cuando solo se necesita una parte específica de una cadena.

## Sintaxis

La sintaxis SQL estandarizada `SUBSTRING`es la siguiente:

```sql
SUBSTRING(string, start, length)
```

Dónde:

- `string`es la cadena de origen de la que desea extraer.
- `start`es la posición desde la que se inicia la extracción. La primera posición de la cadena siempre es 1.
- `length`es el número de caracteres a extraer.

## Uso

Por ejemplo, si desea extraer los primeros 5 caracteres de la cadena 'Hola mundo':

```sql
SELECT SUBSTRING('Hello World', 1, 5) as ExtractedString;
```

Resultado:

```
| ExtractedString || --------------- || Hello           |
```

También puedes usarlo `SUBSTRING`en columnas de tabla, de la siguiente manera:

```sql
SELECT SUBSTRING(column_name, start, length)
FROM table_name;
```


Nos sirve para extraer una parte de una cadena de un texto.

```SQL
SELECT SUBSTRING(cadena, inicio, longitud)
FROM tabla;

SELECT SUBSTRING(nombre, 1, 3) AS subcadena FROM clientes;
```
