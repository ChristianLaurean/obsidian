---
Fecha_creación: 2024-07-14
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - DDL
URL:
---
El lenguaje de definición de datos (DDL) es un subconjunto de [[SQL]]. Su función principal es crear, modificar y eliminar estructuras de bases de datos, pero no datos. Los comandos en DDL son:

1. `CREATE`:Este comando se utiliza para crear la base de datos o sus objetos (como tablas, índices, funciones, vistas, procedimientos de almacenamiento y activadores).
    
```SQL
    CREATE TABLE table_name (
	    column1 data_type(size),
	    column2 data_type(size),
	    ...
	);
```
    
2. `DROP`:Este comando se utiliza para eliminar una base de datos o tabla existente.
    
```SQL
    DROP TABLE table_name;
```
    
3. `ALTER`: Se utiliza para modificar la estructura de la base de datos. Se utiliza para agregar, eliminar, eliminar o modificar columnas en una tabla existente.
    
```SQL
ALTER TABLE table_name 
ADD column_name 
datatype;

ALTER TABLE table_name 
DROP COLUMN column_name;

ALTER TABLE table_name 
MODIFY COLUMN column_name datatype(size);
```
    
4. `TRUNCATE`:Esto se utiliza para eliminar todos los registros de una tabla, incluidos todos los espacios asignados para los registros que se eliminan.
    
```SQL
TRUNCATE TABLE table_name;
```
    
5. `RENAME`:Esto se utiliza para cambiar el nombre de un objeto en la base de datos.
    
```SQL
RENAME TABLE old_table_name 
TO new_table_name;
```
    




