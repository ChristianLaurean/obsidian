---
Fecha_creación: 2024-06-14
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - DML
URL:
---
La `INSERT` instrucción SQL se utiliza para agregar nuevas filas de datos a una tabla de la base de datos. Existen tres formas de `INSERT`instrucción: `INSERT INTO` valores, `INSERT INTO` conjunto y `INSERT INTO`selección.

## `INSERT INTO`

La sintaxis básica para `INSERT INTO`los valores:

```SQL
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```

Esta forma de la `INSERT`declaración especifica tanto los nombres de las columnas como los valores que se insertarán.

## `INSERT INTO`[conjunto]

En este sintaxis, puede insertar datos mediante la `SET` palabra clave. Aquí, especifica cada columna en la que desea insertar datos y, a continuación, los datos de esa columna.

```SQL
INSERT INTO table_name SET column1 = value1, column2 = value2, ...;
```

## `INSERT INTO`[[SELECT]]

La `INSERT INTO SELECT`instrucción se utiliza para copiar datos de una tabla e insertarlos en otra tabla, o bien para insertar datos en columnas específicas de otra tabla.

```SQL
INSERT INTO table_name1 (column1, column2, column3, ...)
SELECT column1, column2, column3, ...
FROM table_name2WHERE condition;
```

En todos los casos, si está insertando datos en una tabla donde algunas columnas tienen valores predeterminados, no necesita especificar esas columnas en su `INSERT INTO`declaración.

Nota: tenga cuidado al insertar datos en una base de datos, ya que SQL no tiene un comando de confirmación. Por lo tanto, una vez que ejecute la instrucción de inserción, se insertarán los registros y no podrá deshacer la operación.

