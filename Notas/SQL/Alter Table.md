---
Fecha_creación: 2024-06-14
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - DDL
URL:
---
El `ALTER TABLE`comando en SQL se utiliza para agregar, eliminar/eliminar o modificar columnas en una tabla existente. También es útil para agregar y eliminar restricciones como [[primary key]], [[foreign key]], etc.

## Agregar columna

Se puede agregar una sola columna utilizando la siguiente sintaxis:

```SQL
ALTER TABLE tableName
ADD columnName datatype;
```

Para agregar más de una columna:

```SQL
ALTER TABLE tableName
ADD (columnName1 datatype,
	 columnName2 datatype,
	 ...);
```

## Columna de caída

Para eliminar una sola columna:

```SQL
ALTER TABLE tableName
DROP COLUMN columnName;
```

Para eliminar varias columnas:

```SQL
ALTER TABLE tableName
DROP (columnName1,
	  columnName2,
	  ...);
```

## Modificar columna

Para modificar el tipo de datos de una columna:

```SQL
ALTER TABLE tableName
ALTER COLUMN columnName TYPE newDataType;
```

## Agregar o eliminar [[Constraints]]

Para agregar restricciones:

```SQL
ALTER TABLE tableName
ADD CONSTRAINT constraintName 
PRIMARY KEY (column1, column2, ... column_n);
```

Para eliminar restricciones:

```SQL
ALTER TABLE tableName
DROP CONSTRAINT constraintName;
```

En conclusión, `ALTER TABLE`SQL le permite modificar la estructura de una tabla existente. Este es un comando poderoso que le permite agregar, modificar y eliminar dinámicamente columnas, así como las restricciones impuestas sobre ellas. Le garantiza una mayor flexibilidad a la hora de lidiar con los cambios en los requisitos de almacenamiento de datos.

## Cambiar nombre columna

 ```SQL
 ALTER TABLE table_name
 RENAME COLUMN old_name TO new_name;
 ```
## Agregar nuevas columnas

 ```SQL
 ALTER TABLE table_name
 ADD COLUMN cold_name type_date constraint;
 ```
### Eliminar columna


 ```SQL
 ALTER TABLE table_name
 DROP COLUMN cold_name;
 ```

## Cambiar tipo de dato

 ```SQL
 ALTER TABLE table_name
 ALTER COLUMN cold_name
 TYPE varchar(2);
 ```

 ```SQL
 ALTER TABLE table_name
 ALTER COLUMN cold_name
 TYPE integer
 USING ROUND(average_grade)-- especifico que quiero hacer antes de que se modifique
 ```
## Cambiar una restrinción not null

 ```SQL
 ALTER TABLE table_name
 ALTER COLUMN cold_name
 SET NOT NULL;

-- Eliminar restrinccion

 ALTER TABLE table_name
 ALTER COLUMN cold_name
 DROP NOT NULL;
 ```

# combinar dos columnas

 ```SQL
 UPDATE table_name
 SET name_colum = CONCAT(a,b);
 ```